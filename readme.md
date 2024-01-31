# Projeto Sicredi

Este repositório contém os códigos utilizados para conduzir uma pesquisa sobre a inclusão de negros e mulheres em cooperativas de crédito, que será apresentada no **ICA CCR** (_International Cooperative Alliance - Committee on Co-operative Research_) em Dundee, Escócia.

## Sobre o Projeto

O projeto usa de dados disponíveis no Banco Central do Brasil (BACEN) de outubro de 2023 referentes a todas as cooperativas de crédito operantes no Brasil naquele mês. A partir do arquivo `202310COOPERATIVAS.CSV`, foram extraídas informações sobre as cooperativas vinculadas ao Sistema Sicredi, totalizando 101 cooperativas.

Em seguida, utilizando os nomes das cooperativas, foi realizada uma raspagem no site institucional do Sicredi para descobrir a URL onde são salvos documentos como atas de assembleias e relatórios anuais. Esse processo foi automatizado com o uso de um script em Python, utilizando as bibliotecas Selenium e BeautifulSoup.

## Códigos Utilizados

### Pré-processamento dos Dados

```python
import pandas as pd

# Lê o arquivo CSV pulando as linhas iniciais
df = pd.read_csv('202310COOPERATIVAS.CSV', delimiter=';', skiprows=3, encoding='ISO-8859-1')

# Filtra as cooperativas do Sicredi e remove duplicatas
cooperativas_sicredi = df[df['NOME_INSTITUICAO'].str.contains('Sicredi', case=False)].drop_duplicates(subset=['NOME_INSTITUICAO'])
```

### Raspagem de Dados

```python
from selenium import webdriver
from selenium.webdriver.chrome.options import Options
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from bs4 import BeautifulSoup
import pandas as pd
import time

# Configurações do perfil do Chrome e inicialização do driver
chrome_options = Options()
# Configurações do Chrome...

# Inicializar o driver do Chrome com as configurações do perfil
driver = webdriver.Chrome(options=chrome_options)

# Loop para cada cooperativa Sicredi
for index, row in cooperativas_sicredi.iterrows():
    # Raspagem dos URLs dos documentos...
```

## Execução do Código

Para executar os códigos, siga as instruções contidas nos comentários de cada trecho de código.

## Observações

- Certifique-se de ter instalado todas as bibliotecas Python necessárias.
- O arquivo `202310COOPERATIVAS.CSV` deve estar presente no diretório de trabalho.
- Os códigos foram desenvolvidos e testados em ambiente Python 3.x.

## Autores

Este projeto foi desenvolvido por Matheus Zago, Ricardo Theodoro e Flávia Zancan, sob a orientação de Davi Moura.

---

_Última atualização: Janeiro de 2024_
