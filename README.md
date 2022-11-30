# GitHub Action Workflows

Moving to data-pipeline/experiments.

There are 3 workflow samples here in [.github/workflows](tree/main/.github/workflows).  

1. flat-data.yml workflow uses githubocto/flat@v3 to get batmanflat.json (Batman API became unavailable fall 2022, so disabled Action by clicking Flat's 3-dot menu)
2. get_file.yml workflow pulls using curl to get cameraready.json for the [CameraReady map](https://map.georgia.org/localsite/map/#show=cameraready&state=GA).  
3. fetch-api-data.yml workflow uses fetch-api-data-action to get batman.json (BUG! saves [object Object])


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
Use this sample of including a Python script in GitHub Actions:  

https://github.com/abrie/atl-council-scraper

We can run our comtrade script to populate folders for each country:
https://github.com/modelearth/data-pipeline/tree/main/international/comtrade