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



<!--# Typography
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Font stack

By default, Just the Docs uses a native system font stack for sans-serif fonts:

```scss
-apple-system, BlinkMacSystemFont, "helvetica neue", helvetica, roboto, noto, "segoe ui", arial, sans-serif
```

ABCDEFGHIJKLMNOPQRSTUVWXYZ
abcdefghijklmnopqrstuvwxyz
{: .fs-5 .ls-10 .code-example }

For monospace type, like code snippets or the `<pre>` element, Just the Docs uses a native system font stack for monospace fonts:

```scss
"SFMono-Regular", Menlo, Consolas, Monospace
```

ABCDEFGHIJKLMNOPQRSTUVWXYZ
abcdefghijklmnopqrstuvwxyz
{: .fs-5 .ls-10 .text-mono .code-example }

---

## Responsive type scale

Just the Docs uses a responsive type scale that shifts depending on the viewport size.

| Selector              | Small screen size `font-size`    | Large screen size `font-size` |
|:----------------------|:---------------------------------|:------------------------------|
| `h1`, `.text-alpha`   | 32px                             | 36px                          |
| `h2`, `.text-beta`    | 18px                             | 24px                          |
| `h3`, `.text-gamma`   | 16px                             | 18px                          |
| `h4`, `.text-delta`   | 14px                             | 16px                          |
| `h5`, `.text-epsilon` | 16px                             | 18px                          |
| `h6`, `.text-zeta`    | 18px                             | 24px                          |
| `body`                | 14px                             | 16px                          |

---

## Headings

Headings are rendered like this:

<div class="code-example">
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
</div>
```markdown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

---

## Body text

Default body text is rendered like this:

<div class="code-example" markdown="1">
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
</div>
```markdown
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
```

---

## Inline elements

<div class="code-example" markdown="1">
Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](another-page).
</div>
```markdown
Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](another-page).
```

---

## Typographic Utilities

There are a number of specific typographic CSS classes that allow you to override default styling for font size, font weight, line height, and capitalization.

[View typography utilities]({{ site.baseurl }}{% link docs/utilities/utilities.md %}#typography){: .btn .btn-outline }
-->