# Import-IMDB-Data-to-PostgreSQL-through-Python

In this notebook, I prepared a pipeline to dump IMDB data to Postgres DB through Python. But as a requirement it is needed to install Postgres to your local machine and create a DB as well as a user to upload all datasets as tables. This notebook does not cover this part. 

Of course, the datasets can be imported directly to Postgres by using ***CREATE TABLE*** and ***COPY*** commands or just clicking from available menus through pgAdmin IDE. But the main idea in here is to split them into chunks and manupilate datasets before dumping them. 

After creation of DB and extracting downloaded files from IMDB data page, you can use this notebook to create tables and load data into that tables separately. The main drawback of IMDB dataset is its volume. So I used pandas in chunks for reading some of the tables and used Dask for some others to show both options. 

I downloaded publicly published IMDB dataset from this [link](https://datasets.imdbws.com/), in which includes 7 different datasets as tsv files. Explanalations of the data can be investigated through this [page](https://www.imdb.com/interfaces/). 
