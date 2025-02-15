# engeto-project-3
Code for the third Engeto project – Election scraper

# Election scraper #
## Project description ##
The goal of this project is to obtain [the results of the elections to the Chamber of Deputies of the Parliament of the Czech Republic in 2017](https://www.volby.cz/pls/ps2017nss/ps3?xjazyk=CZ) using scraping.
After entering the selected URL address, the script will download the data of the relevant cities along with the election results and save them to the selected CSV file.

### Library installation ###
List of required libraries and their versions: `requirements.txt`

**Procedure in IDE**
1. Create a virtual environment (recommended)
2. Activate the virtual environment
3. Install libraries using the `requirements.txt` file

| Command                              | Description                            |
|--------------------------------------|----------------------------------------|
| `.venv\Scripts\activate`             | Activating the virtual environment |
| `pip install -r requirements.txt`    | Installing libraries from `requirements.txt` |

### File execution ###
Running the project is via terminal/command line and require 2 arguments:
1. District URL
2. Output file name (in CSV format)

### Project example ###
Voting results for Svitavy district:
1. argument `https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=9&xnumnuts=5303`
2. argument `vysledky_svitavy.csv`

**Running the script**:  
`python engeto-project-3 'https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=9&xnumnuts=5303' 'vysledky_svitavy.csv'`

**Download progress**:  
Connecting to URL: 'https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=9&xnumnuts=5303'  
Downloading data from URL: 'https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=9&xnumnuts=5303'  
Saving data to file: '<pathdescription>/vysledky_svitavy.csv'  
Successfully written data to file: vysledky_svitavy.csv

**Partial output**:
| City code | City name          | Registered voters | Envelopes | Valid votes | Občanská demokratická strana | Řád národa - Vlastenecká unie | ... |
|-----------|--------------------|-------------------|-----------|-------------|------------------------------|-------------------------------|-----|
| 572560    | Banín              | 264               | 157       | 157         | 7                            | 0                             | ... |
| 572586    | Bělá nad Svitavou  | 413               | 238       | 237         | 16                           | 0                             | ... |
| 505391    | Bělá u Jevíčka     | 310               | 203       | 203         | 8                            | 7                             | ... |
| 577774    | Benátky            | 286               | 204       | 200         | 28                           | 0                             | ... |
| ...       | ...                | ...               | ...       | ...         | ...                          | ...                           | ... |