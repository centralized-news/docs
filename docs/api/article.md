---
layout: default
title: Article Posting Endpoint
parent: API
nav_order: 2
---

# Article Posting Endpoint

You can post an article by making a POST request to [www.centralizednews.org/api/writers/article/new](https://www.centralizednews.org/api/writers/article/new). It is important to include the `www.` in the URL.
It will return an error if you don't have writer access tied to your account.

```json
{
    "title": "some title",
    "body": "some body",
    "image": "some image url",
    "apikey": "your api key", // you can get one buy emailing: alec@centralizednews.org
    "tags": "tags for seo"
}
```

JS Example of This Endpoint:
{: .fs-6 .fw-100 }
First you have to import jQuery
```
https://code.jquery.com/jquery-3.5.1.min.js
```
Next is the script to make the post request using jQuery:
```js
$.post('https://www.centralizednews.org/api/writers/article/new', {
    "title": 'Examples are taking over documentation',
    "body": 'This is an example body',
    "image": 'http://example.com/image.png',
    "apikey": '1234567890',
    "tags": 'nodejs, docs'
}, function (result) {
    console.log(result);
    window.location.replace(`https://www.centralizednews.org/article?id=${result._id}`)
})

```