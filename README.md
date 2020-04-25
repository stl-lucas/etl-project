<h1>Project 2: ETL Challenge</h1>
<h3>Authors: John Jostes and Tim Lucas</h3>
<p>This project was designed to follow the extract, transform and load steps for ETL. 
We chose to focus on movie data from the 1970's wihtin the Action genre for our target data set.</p>

<h3>Extract</h3>
<p>During the extraction phase we focused on collecting our data in two different ways. The first step was to download two seperate .tsv files from
the IMDB (Internet Movie Database) website. These files were extremely large (at about 500MB each) so we knew there was going to be a lot of 
transformation required. The resources we used for downloading these files can be found here.</p>
<h6>IMDB Datasets</h6>
<ul>
<li>Documentation: <a href="https://www.imdb.com/interfaces/" target="_blank">https://www.imdb.com/interfaces/</a></li>
<li>Downloads: <a href="https://datasets.imdbws.com/" target="_blank">https://datasets.imdbws.com/</a></li>
</ul>

<p>This data contained a lot of great information but was also missing a lot of valuable information. We found the OMDB API (Open Movie Database) contained
some of the missing information we were interested in such as awards, box office numbers, country, etc. Our second step in extraction was setting up an API key
and making a pledge to the OMDB Patreon so that we could make more than 1,000 API calls and collect the missing data we needed. We did this utilizeing the movie 
ids provided by the IMDB files and creating a for loop that would make individual API calls for each movie and extracting the information we needed from each response.
<h6>OMDB API - The Open Movie Database</h6>
<ul>
<li>Documentation: <a href="http://www.omdbapi.com/" target="_blank">http://www.omdbapi.com/</a></li>
<li>Endpoint: http://www.omdbapi.com/?i={movie_id}&apikey={api_key}</li>
</ul>

<p>The data extraction went very smooth and we started with over XXXX records and made just over 2,000 api calls to complete the extraction portion of this project.</p>

<h3>Transform</h3>
<p>Transforming this data took place throughout and after the extraction process. We first transformed the original IMDB data sets and narrowed our list of movies down to just 2.400.
This enabled us to make fewer API calls and create a curated dataset of 1970s action movies from all around the world.</p>

<h3>Load</h3>
<p>For loading our data we decided to use a could based mongo server. We utilized the free db options offered by Mongo Atlas and created our movie_db database with a single collection
of movies. We used Mongo Compass to import the csv file and the command line to connect to the remote db and verify that our records loaded properly and could be queried.</p>