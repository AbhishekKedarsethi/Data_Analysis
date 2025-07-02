import pandas as pd
import os
from sqlalchemy import create_engine
import time
import logging

engine = create_engine("postgresql://postgres:Rajani%1234@localhost:5432/Exercise")

logging.basicConfig(
    filename="logs/ingestion_db.log",
    level=logging.DEBUG,
    format="%(asctime)s - %(levelname)s - %(message)s",
    filemode="a"
)

def ingest_db (df, table, engine):
    ''' This function will ingest dataframe into database table'''
    df.to_sql(table, con = engine, if_exists = 'replace', index = False) #We use append for automation

def load_raw_data():
    ''' This function will load the csv data as dataframes and ingests into DB'''
    start = time.time()
    for file in os.listdir('Data'):
        if '.csv' in file:
            df = pd.read_csv('Data/'+file)
            logging.info(f'Ingesting {file} in DB')
            ingest_db (df, file[:-4], engine)

    end = time.time()
    Total_time = (end-start)/60
    logging.info(f'Ingestion Completed')
    logging.info(f'Total time taken = {Total_time} minutes')

if __name__ == '__main__':
    load_raw_data()
