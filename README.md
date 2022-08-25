# cameraready_locations_curl

There are 3 workflow samples here.  
get_file.yml pulls the live data for the [CameraReady map](https://map.georgia.org/localsite/map/#show=cameraready&state=GA).  

## Build from source

Create a virtual environment (OSX / Linux / Windows):
`python3 -m venv .venv`

OSX / Linux:
`source .venv/bin/activate`

Windows:
`\.venv\Scripts\activate.bat`

Running `make dependencies` will install BeautifulSoup4

1. `make dependencies`
2. `make test`
3. `python3 -m app scrape > scraped/atl-citycouncil.json`

Change line 3 above.
Came from: 