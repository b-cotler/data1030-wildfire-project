
The data for this project comes from a SQLite database. The file is too large to upload to github, but it can be accessed using the following python commands.


import pandas as pd
import sqlite3

connection = sqlite3.connect('../final-project/FPA_FOD_20170508.sqlite')
DATAFRAME_NAME = pd.read_sql_query("SELECT FIRE_YEAR,STAT_CAUSE_DESCR,LATITUDE,LONGITUDE,STATE,DISCOVERY_DATE,FIRE_SIZE FROM 'Fires'", connection)
