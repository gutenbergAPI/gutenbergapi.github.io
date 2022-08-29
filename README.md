# Gutenberg API

This is an unofficial [Project Gutenberg API](https://rapidapi.com/rabahdjebbes6-VpFXFzqdF1R/api/project-gutenberg-api/).

## Features

- Download books in an epub format (more coming soon...).
- Get information about the book (title, author, language, copyright, publish date).

## Installing

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install requests.

```bash
pip install requests
```

## Usage

Get your free credentials at [RapidAPI](https://rapidapi.com/rabahdjebbes6-VpFXFzqdF1R/api/project-gutenberg-api/pricing).

```python
import requests

url = "https://project-gutenberg-api.p.rapidapi.com/get_data"

querystring = {"id":"24"}

headers = {
	"X-RapidAPI-Key": "<your credentials>",
	"X-RapidAPI-Host": "<your credentials>"
}

response = requests.request("GET", url, headers=headers, params=querystring)

print(response.text)
```

## Response

```json
{
    "status": 200,
    "title": "O Pioneers!",
    "author": "Cather, Willa, 1873-1947",
    "language": "English",
    "copyrights": "Public domain in the USA.",
    "publish date": "Jun 27, 2008"
}
```
