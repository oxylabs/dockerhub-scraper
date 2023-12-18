# Dockerhub Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Dockerhub Scraper](https://oxylabs.io/products/scraper-api/web/dockerhub?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Dockerhub website effortlessly. This brief guide explains how an Dockerhub Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Dockerhub results by providing your own URLs to our service. We can return the HTML for any Dockerhub page you like.

#### Python code example

The example below illustrates how you can get HTML of Dockerhub page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://hub.docker.com/search?q='
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/dockerhub-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html>\n<html lang=\"en\">\n<head>\n<title>Docker</title>\n<meta name=\"viewport\" content=\"width=d ... </html>",
      "created_at": "2023-12-18 10:43:00",
      "updated_at": "2023-12-18 10:43:01",
      "page": 1,
      "url": "https://hub.docker.com/search?q=",
      "job_id": "7142464261950802945",
      "status_code": 200
    }
  ]
}
```
With our Dockerhub Scraper, you can seamlessly extract public data from any Dockerhub web page. Gather the necessary repository information, such as image tags, pull counts, stars, or descriptions, to analyze the market trends around container software and stay ahead of your competitors. If you have any questions, contact our support team via live chat or email us at hello@oxylabs.io.