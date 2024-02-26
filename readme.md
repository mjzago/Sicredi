# Projeto Inclusão na Sicredi

Este repositório contém os códigos utilizados para conduzir uma pesquisa sobre a inclusão de negros e mulheres em cooperativas de crédito, que será apresentada no **ICA CCR** (_International Cooperative Alliance - Committee on Co-operative Research_) em Dundee, Escócia.

## Sobre o Projeto

O projeto usa de dados disponíveis no Banco Central do Brasil (BACEN) de outubro de 2023 referentes a todas as cooperativas de crédito operantes no Brasil naquele mês. A partir do arquivo `202310COOPERATIVAS.CSV`, foram extraídas informações sobre as cooperativas vinculadas ao Sistema Sicredi, totalizando 101 cooperativas.

Em seguida, utilizando os nomes das cooperativas, foi realizada uma raspagem no site institucional do Sicredi para descobrir a URL onde são salvos documentos como atas de assembleias e relatórios anuais. Esse processo foi automatizado com o uso de um script em Python, utilizando as bibliotecas `Selenium` e `BeautifulSoup`.

## Execução do Código

O arquivo `Webscraping.ipynb` contém o processo completo de raspagem de dados e está disponível neste repositório.
Para executar os códigos, siga as instruções contidas nos comentários de cada trecho de código.

## Observações

- Certifique-se de ter instalado todas as bibliotecas Python necessárias.
- Certifique-se de ter o Chromedriver instalado para utilizar o `Selenium` com o [Google Chrome](https://chromedriver.chromium.org/downloads)
- O arquivo `202310COOPERATIVAS.CSV` deve estar presente no diretório de trabalho.
- Os códigos foram desenvolvidos e testados em ambiente Python 3.x.

## To-Do

- [ x ] Organizar os arquivos baixados na raspagem de dados em uma pasta `data\raw\`
- [ x ] Separar os arquivos baixos dos arquivos de texto na pasta `data\npl\`
- [ x ] Desenvolver script para extrair informações dos arquivos .txt com funcao OCR.
- [ ] Desenvolver script para normalizar os dados (deletar duplicatas, ponctuations, filtros, stopwords, stammer, lemmatizer etc).
- [ ] Criar as categorias de corporas para analise estatísitca, desenvolver o modelo de análise e a visualizacao dos dados.
- [ ] Escrever a metodologia, introducao, referencial teório, resultados e discussoes do trabalho.

## Autores

Este projeto foi desenvolvido por [Matheus Zago](https://github.com/mjzago), [Ricardo Theodoro](https://github.com/rtheodoro) e Flávia Zancan, sob a orientação de Davi Rogério de Moura Costa.

---

_Última atualização: Janeiro de 2024_
