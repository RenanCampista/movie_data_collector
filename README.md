# movie_data_collector

Collects data from movies using the OMDb API and TMDB API.


## Installation

To use this script, it is necessary to configure the environment variables in the `.env` . To do this, follow the steps below:

1. Copy the `.env.example` file to a new file called `.env`:

   ```shell
   cp .env.example .env
   ```

2. Open the `.env` file and fill in the environment variables with their values:

   ```shell
    OMDb_API_KEY="your_api_key"
    TMDB_API_KEY="your_api_key"
    ```

### Usage
To use this script just use the command:

```sh
python requester.py
``` 
Data is saved in a [csv](https://en.wikipedia.org/wiki/Comma-separated_values) file.

## Search settings
### Number of films returned
The script is configured to collect data from approximately 100 movies, but you can change this value by changing the `MAX_PAGES` constant in the `requester.py` file. One page contains approximately 19 movies.

### List Type
The script is configured to collect data from the most popular movies, but you can change this value by changing the `list_type` parameter in the `get_tmdb_movies` function in the `requester.py` file. Possible values ​​are:
- `POPULAR` - Popular movies
- `TOP_RATED` - Top rated movies
- `UPCOMING` - Upcoming movies

