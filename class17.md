# Web Scrape

Def :

Web scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort.



## Important notes about web scraping:
1. Read through the website’s Terms and Conditions to understand how you can **legally** use the data. Most sites prohibit you from using the data for commercial purposes.
2. Make sure you are not downloading data at too rapid a rate because this may break the website. You may potentially be **blocked** from the site as well.

## Inspecting the Website

On the website, right click and click on “Inspect”. This allows you to see the raw code behind the site.Once you’ve clicked on “Inspect”, you should see this console pop up.

## Python Code  
```
import requests
import urllib.request
import time
from bs4 import BeautifulSoup


url = 'http://web.mta.info/developers/turnstile.html'
response = requests.get(url)
```
Next we parse the html with BeautifulSoup so that we can work with a nicer, nested BeautifulSoup data structure.

```
soup = BeautifulSoup(response.text, “html.parser”)

soup.findAll('a')
```

```
one_a_tag = soup.findAll(‘a’)[38]
link = one_a_tag[‘href’]

```

```
download_url = 'http://web.mta.info/developers/'+ link
urllib.request.urlretrieve(download_url,'./'+link[link.find('/turnstile_')+1:])
```

```
time.sleep(1)
```
