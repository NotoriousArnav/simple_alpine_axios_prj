# CrawlX: Demo Project

This is a demo project showcasing how to use the CrawlX API to scrape data from a website. In this example, we demonstrate how to fetch an article's headline and body using the CrawlX API.

We will be using Articles from The Guardian

Hosted ["Here"](https://notoriousarnav.github.io/simple_alpine_axios_prj/)

## Overview

The project consists of an HTML file that uses Axios for making HTTP requests and Alpine.js for data binding. When the user enters the URL of an article and clicks "Fetch Article", the HTML file sends a POST request to the CrawlX API, specifying the URL of the article and the CSS selectors for extracting the headline and body. Upon receiving the response from the API, the headline and body of the article are displayed on the webpage.

## Usage

To run the demo project:

1. Open the `index.html` file in a web browser.
2. Enter the URL of an article in the text input field.
3. Click the "Fetch Article" button.

## Code Explanation

The HTML file contains JavaScript code that uses Axios to make a POST request to the CrawlX API. The request payload includes the URL of the article and CSS selectors for extracting the headline and body. Upon receiving the response from the API, the headline and body are displayed on the webpage.

```html
<!-- Add this code to the HTML file to explain how it works -->

<div>
    <h4 class="font-bold text-lg">News Scraper Website</h4>
    <p>In this example, we are using the CrawlX API to scrape data from a given URL.</p>

    <div style="height:25px;" class="mt-6">
        <p x-show.transition="ok" style="display: none;" class="bg-blue-500 text-white rounded inline py-1 px-2">Data updated!</p>
    </div>

    <div class="mt-4">
        <label>Enter article URL: <input x-model="articleUrl" type="text" class="border border-1"></label>
        <button @click="fetchArticle()" class="bg-blue-500 text-white px-4 py-2 rounded">Fetch Article</button>
    </div>

    <div x-show.transition="axiosResponse" class="mt-4">
        <h2 x-text="axiosResponse.headline" class="text-xl font-bold"></h2>
        <p x-text="axiosResponse.body" class="mt-2"></p>
    </div>
</div>
```

---

This README.md provides an overview of the demo project and explains how to use it. Additionally, it includes code snippets to illustrate how the HTML file interacts with the CrawlX API.