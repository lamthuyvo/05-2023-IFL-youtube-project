# YouTube Archive Analysis 

This repository contains scrapers and analytic code for people interested in scraping API information about YouTube channels and  YouTube Archives. This code was used to analyze information from a Vietnamese community member to better understand the information needs of the Vietnamese community in Oakland and is part of a project done as part of a fellowship with [the Brown University Information Futures Lab](https://sites.brown.edu/informationfutures/). 

Note that to use this repository, you will need to create a `data` folder and an `ouput` folder within your project folder, on top of copying over the `notebooks` folder from this project.

## Data

There are two data sets used in this analysis. Both are not included in this repository to protect the identity of the people who shared the data with us. 

First commnunity members shared YouTube channels with us that they frequently watch. If you wish to replicate our analysis you will need a list of channel ids for which you would like to compile the information, such as number of subscribers and number of videos. A channel ID can usually be found at the end of the URL:  https://www.youtube.com/channel/UCjnWysJh9-r9wo82zlbMT3A 

When a user changed the end of their URL to something other than their ID, you can also find ids via free tools online, such as [this one](https://commentpicker.com/youtube-channel-id.php).

The second analysis this repository contains is one of a personal YouTube archive, which contains information such as the complete viewing and search history associated with one Google account. As with the other data, this information is not included in this repository but you can request a YouTube archive of an account's view and watch history [on Google's Takeout page](https://takeout.google.com/settings/takeout) by selecting the archive you would like to download while logged into the account for which you want the data. This same account will be emailed a download link once the archive is ready. 


##  Data extraction/scraping
The data extraction was performed in the following Jupyter notebooks, using the Python programming language. There are two notebooks:

The [`01-youtube-api-scraper.ipynb` notebook](notebooks/01-youtube-api-scraper.ipynb) gathers information from the YouTube API for a list of channels and exports them as `.csv` files in the output folder. Information gathered inclues the title of the channel, its description and the number of subscribers.  

The [`01-youtube-archive-scraper.ipynb` notebook](notebooks/01-youtube-archive-scraper.ipynb)  extracts data from the `search-history.html`, `watch-history.html` and `my-comments.html` files of a YouTube Archive and exports them into an `output` folder. 

As with the input data, any output data is also excluded from this repository to protect the identity of the people who shared the data with us. 

## Data analysis

The data analysis was performed in the following Jupyter notebook, using the Python programming language. 

The Python code for BuzzFeed News analysis, implementing the methodology above, can be found in the [`02-analyze-gentrification-and-demographic-changes.ipynb` notebook](notebooks/02-analyze-gentrification-and-demographic-changes.ipynb). The notebook additionally calculates percentage-point changes for six non-overlapping race/ethnicity groups.

Among the analyses it performs are:

#### Overall findings 
- Totals
- Ads vs watched things
- searched terms vs watched vs other
- searched terms (list)
    
#### Specific to Google Ads
- repeat videos
- NLP, such as words most often used
- Time-related trends

#### Specific to non-ad views
- repeat videos
- NLP, such as words most often used
- Time-related trends

As previously mentioned, any output data is also excluded from this repository to protect the identity of the people who shared the data with us. 

## Licensing

All code in this repository is available under the [MIT License](https://opensource.org/licenses/MIT). All data files in the output/ directory are available under the [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0) license. All data files in the data/ directory are available, under their own terms, from the sources described above.

## Feedback / Questions?

Contact [Lam Thuy Vo](https://twitter.com/lamthuyvo) at lam.vo@journalism.cuny.edu.
