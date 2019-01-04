# webScrapping
A python script to scrape the data of the website http://www.fallingrain.com/world/IN/ into a CSV file containing State, City, Latitude, Longitude, Elevation, Estimated Population.

<img src="https://img.shields.io/badge/language-python3-brightgreen.svg"/>

## Getting Started

Follow these instructions to get a copy of the project up and to run on your local machine for development and testing purposes.

### Prerequisites

Following are the prerequisites for executing the project:

Libraries used:

BeautifulSoup
```
sudo apt-get install python3-bs4

```
numpy
```
sudo apt-get install python3-numpy
```

### Installing

Clone the repository

```
git clone https://github.com/jaiswalkautish/webScrapping.git
```

Change the directory

```
cd webScrapping
```

Run the python script
```
python3 webScrape.py
```

Upon the successful execution a file named output.csv will be created in which the entire data of the website will be scraped in the required format i.e.

City, State, Latitude, Longitude, Elevation, EstmdPopulation.

### A brief about Implementation

The script webScrape is wrritten in python3 which uses the concept of multithreading for the efficient and parallel scraping of the website. The data that is the required output is dumped into a csv file by each thread simultaneously. To enable this a csv lock is used. Thus as soon as a thread reaches the required data it is dumped there only into the csv file.

The project is tested on the local machine with following specification:

Operating System: ubuntu 18.04

Number of cores: 4

Because of the limited number of cores and system specifications around 2L cities were computed into the csv while the script was still running without any error.

Thus the entire scraping would take some time in systems with normal specifications but as the number of cores will be increased more threads can be executed parallely and hence would produce the required result in less time.
