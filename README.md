# Plus Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Plus Scraper](https://oxylabs.io/products/scraper-api/ecommerce/plus?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Plus website effortlessly. This brief guide showcases how Plus Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Plus results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Plus page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.plus.nl/producten/pasta-rijst-internationale-keuken/pasta/spaghetti-linguine-tagliatelle'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/plus-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\r\n<!DOCTYPE html>\r\n<html>\r\n    <head><script src=\"/vse-need-How-Goes-Hear-and-purride-To-shou-the-W\" ... </html>",
      "created_at": "2024-02-20 12:56:37",
      "updated_at": "2024-02-20 12:56:40",
      "page": 1,
      "url": "https://www.plus.nl/producten/pasta-rijst-internationale-keuken/pasta/spaghetti-linguine-tagliatelle",
      "job_id": "7165690711700971521",
      "status_code": 200
    }
  ]
}
```
With our Plus Scraper, you can seamlessly gather public data from any Plus web page. Procure crucial book information, like author details, publication date, or book reviews, to perform comprehensive market analysis and stay a step ahead in the literary world. If you need any assistance, our support team is available to help you via live chat or you can email us at hello@oxylabs.io.