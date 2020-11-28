# swissvotes-importer
A tool to import all historic and actual votes in Switzerland from swissvotes.ch into a postgres database

## About
swissvotes.ch contains a database with all present and historic votes (initiatives, referendums) that where ever held in Switzerland since 1848. This tool will help you download the latest version from the site and import the data into a postgres database.

## Run
You can the tool by passing the connection arguments for you postgres database as needed

```bash
python swissvotes-importer -u <DBUSER> -p <DBPASS> -h <DBHOST> -d <DBNAME>
```

which will generate:
```
1) Connecting to database swissvotes
2) Downloading and parsing latest swissvotes_dataset.csv
3) Parsed 661 lines
4) (Re-)created table and wrote data
```

## Documentation
The data format is documented in a (german) cookbook [here on swissvotes.ch](https://swissvotes.ch/page/dataset/codebook-de.pdf)

