# Sicredi Inclusion Project

This repository contains the codes used to conduct research on the inclusion of Black people and women in credit cooperatives, which will be presented at the **ICA CCR** (_International Cooperative Alliance - Committee on Co-operative Research_) in Dundee, Scotland.

## About the Project

The project uses data available from the Central Bank of Brazil (BACEN) from October 2023 regarding all credit cooperatives operating in Brazil in that month. From the file `202310COOPERATIVAS.CSV`, information about cooperatives linked to the Sicredi System was extracted, totaling 101 cooperatives.

Next, using the names of the cooperatives, a scraping process was carried out on the Sicredi institutional website to discover the URL where documents such as assembly minutes and annual reports are saved. This process was automated using a Python script, utilizing the `Selenium` and `BeautifulSoup` libraries.

## Code Execution

The file `Webscraping.ipynb` contains the complete data scraping process and is available in this repository.
To execute the codes, follow the instructions contained in the comments of each code snippet.

## Notes

- Make sure you have installed all necessary Python libraries.
- Make sure you have Chromedriver installed to use `Selenium` with [Google Chrome](https://chromedriver.chromium.org/downloads).
- The file `202310COOPERATIVAS.CSV` must be present in the working directory.
- The codes were developed and tested in a Python 3.x environment.

## To-Do

- [ x ] Organize downloaded files in the data `raw\` folder.
- [ x ] Separate downloaded files from text files in the `data\npl\` folder.
- [ x ] Develop a script to extract information from .txt files using OCR function.
- [ ] Develop a script to normalize data (delete duplicates, punctuations, filters, stopwords, stemming, lemmatization, etc.).
- [ ] Create corpus categories for statistical analysis, develop the analysis model, and data visualization.
- [ ] Write the methodology, introduction, theoretical framework, results, and discussions of the work.

## Authors

This project was developed by [Matheus Zago](https://github.com/mjzago), [Ricardo Theodoro](https://github.com/rtheodoro), and Flávia Zancan, under the guidance of Davi Rogério de Moura Costa.

---

_Last updated: Febuary 2024_
