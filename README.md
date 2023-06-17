# Gutenberg API

This is a stable and reliable unofficial API for [Project Gutenberg API](https://rapidapi.com/rabahdjebbes6-VpFXFzqdF1R/api/project-gutenberg-api/).

## Features

- Get download links for books in many formats.
- Get information about the book (title, author, language, copyright, publish date).
- Search for a book and get its corresponding ID.

## Installing (Python)

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install requests.

```bash
pip install requests
```

## Usage (Python)

Get your free credentials at [RapidAPI](https://rapidapi.com/rabahdjebbes6-VpFXFzqdF1R/api/project-gutenberg-api/pricing).

```python
import requests

url = "https://project-gutenberg-api.p.rapidapi.com/get_data"

querystring = {"id": "24"}

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
  "id": 15,
  "title": "Moby-Dick; or, The Whale",
  "authors": [
    {
      "name": "Melville, Herman",
      "birth_year": 1819,
      "death_year": 1891
    }
  ],
  "translators": [],
  "subjects": [
    "Adventure stories",
    "Ahab, Captain (Fictitious character) -- Fiction",
    "Mentally ill -- Fiction",
    "Psychological fiction",
    "Sea stories",
    "Ship captains -- Fiction",
    "Whales -- Fiction",
    "Whaling -- Fiction",
    "Whaling ships -- Fiction"
  ],
  "bookshelves": [
    "Adventure",
    "Best Books Ever Listings"
  ],
  "languages": [
    "en"
  ],
  "copyright": false,
  "media_type": "Text",
  "formats": {
    "text/html; charset=utf-8": "https://www.gutenberg.org/files/15/15-h/15-h.htm",
    "application/epub+zip": "https://www.gutenberg.org/ebooks/15.epub.images",
    "application/rdf+xml": "https://www.gutenberg.org/ebooks/15.rdf",
    "application/x-mobipocket-ebook": "https://www.gutenberg.org/ebooks/15.kindle.images",
    "image/jpeg": "https://www.gutenberg.org/cache/epub/15/pg15.cover.medium.jpg",
    "text/plain; charset=utf-8": "https://www.gutenberg.org/files/15/15-0.txt",
    "text/html": "https://www.gutenberg.org/ebooks/15.html.images"
  },
  "download_count": 872
}
```
