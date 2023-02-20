
## Data Modeling with Postgres 

### Sparkify Project Purpose: 

Sparkify is a startup company for an online music streaming app. They are interested in gathering data regarding music streaming and user preferences to enhance customer experience and increase app functionality. Specifically, Sparkify is interested in determining which songs and genres are most popular among Sparkify users.

### Sparkify Project Description: 

Song and user data is currently stored within json files which is not easily queried to perform analyses. This project centered on creating a database and ETL pipeline to extract data from these json files for analytic ease and efficiency.

### Database Schema: 

In order to efficiently query desired data, a star database schema was created. This database centered on a Fact table (Songplay) which contains data related to song start time, user id, user level, song id, artist id, session id, location, and user agent. This songplay table holds measured factual data relating to four Dimension tables (users, songs, artists, and time), each holding additional information regarding to user data, song data, artist data, and time data related to song and user activity. All tables contain unique primary keys that relate back to the Songplay fact table, allowing for multiple queries to be performed. 

### Database Files: 

The database includes files containing code allowing for access and manipulation of the data. Within these files, The json files song_data and log_data are loaded into the database sparkifydb, which then extracts, transforms, and loads the data into the database tables. Files utilized to create the sparkifydb and the ETL pipeline include:
>
> - **test.ipynb** - displays the first few rows of each table to allow us to check on the database.
> - **etl.ipynb** - notebook that reads and processes single file from song_data and log_data json files and loads the data into tables.
> - **etl.py** - reads and processes files from song_data and log_data json files and loads the data into tables using functions.
> - **sql_queries.py** - contains all SQL queries to run the database, it is imported into create_tables.py, etl.py, and etl.ipynb 
> - **create_tables.py** - Contains the code to Drop/Create tables and Drop/Create database. Running this file is necessary to reset the tables/database each time the ETL scripts are run.

### How To Run The Database:

1. Run **create_tables.py** to create the database and tables
2. Run **etl.py** to extract, transform, and load the data into tables.
3. Run **test.ipynb** to ensure data is loaded properly, ensure database is created and works efficently, and test queries.


    
