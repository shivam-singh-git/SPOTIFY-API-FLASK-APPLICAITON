# Spotify Artist API

This is a Flask-based API that provides access to various Spotify artist data, including information about artists' popularity, tracks, releases, genres, and more. The data is sourced from a CSV file containing detailed information about Spotify artists such as their number of followers, tracks, and releases.

## Features

- **Fetch list of all artists**: Get a list of all unique artists from the dataset.
- **Artist popularity**: Retrieve an artist's popularity score, monthly listeners, and followers.
- **Artist tracks**: Get the number of tracks and releases by an artist.
- **First and last release information**: Get the first and last release year of an artist.
- **Top 5 artists by followers**: List the top 5 artists based on follower count.
- **Top 5 genres by followers**: List the top 5 genres based on the followers of the artists.
- **API documentation**: Get a list of all available API endpoints with detailed descriptions.

## Setup Instructions

To set up and run this Flask-based API locally, follow these steps:

### Prerequisites

- Python 3.x
- `pip` (Python package installer)

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/spotify-artist-api.git
    cd spotify-artist-api
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Place the `CLEANED_Spotify_artist_info.csv` file in the root directory of the project.

4. Run the Flask app:

    ```bash
    python app.py
    ```

The app will be accessible at `http://127.0.0.1:5000/`.

## API Endpoints

Below is a list of available endpoints:

### `GET /`
Returns a basic "Hello World" message.

### `GET /names`
Returns a list of all unique artist names in the dataset.

### `GET /artistPopularity?artist=<artist_name>`
Returns the popularity, monthly listeners, followers, and genre of the specified artist.

### `GET /artistTracks?artist=<artist_name>`
Returns the number of tracks and releases for the specified artist.

### `GET /artistFirstLastRelease?artist=<artist_name>`
Returns the first and last release year for the specified artist.

### `GET /top5artists`
Returns the top 5 artists by their follower count.

### `GET /top5Genres`
Returns the top 5 genres based on the follower count of the artists.

### `GET /allApis`
Lists all available API endpoints along with their descriptions.

## Error Handling

If the artist is not found or any error occurs, the API will return a JSON object with an error message, for example:

```json
{
    "error": "Artist not found"
}

License
This project is open-source and available under the MIT License.





