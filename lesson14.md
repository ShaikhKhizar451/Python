[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/zsw-dHRk)
# Scrape and catalog URLs

**Write a function `scrape_site` that...**

1. Download the contents of url `https://httpbin.org`
2. Extract and store all the urls from the downloaded content
3. Randomly select from the list of urls the greater of (a) 50% of the number of downloaded urls, or (b) 100 urls
4. Return the randomly selected list

``` python
>>> urls = scrape_site()
>>> urls
['foo', 'bar', 'baz', 'http://dev.null/']
```

**Write a function `catalog_urls` that catalogs the status_code of a given list of urls**

1. Use `request` to fetch every url in list provided to the function
2. Create a dictionary with keys set to the status code of the response to the requests in [4] and the values set to the list of urls that returned the status code in the key.
3. Return the dictionary

``` python
>>> catalog_urls(urls)
{
    200: ["foo", "bar"],
    300: ["baz", "https://dev.null/"]
}
```