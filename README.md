# Analysis Favorit Youtube Video using Selenium and Beautiful Soup Python


Okay, this project was started on Saturday, 19 October 2019. At first, the reason why I want to build this project is I want to know what the topics that I like on Youtube and what is my favorite channel. 

## Introduction 

### 1. Selenium

So, what is Selenium? 

```
"Selenium automates browsers. "
```

In modern web application, it's common that they use infinite scroll to load data instead of pagination. We know that is hard to scrapping the javascript web page than the PHP web page (server-side rendering). Most of the javascript web uses client-side rendering to render a web page.  

Youtube uses client-side rendering and infinite scroll, to avoid the limitation I use Selenium which commonly used for automation testing. With this library, you can control a web browser and interact with the website. I used it to load all Youtube data on the page using the Chrome browser and then scrapping it.

### 2. Beautiful Soup

Beautiful Soup is a Python library that use for data extraction of HTML and XML files. That is my favorite library to scrape and parse the HTML web page because it's easy to use and save a lot of time compare to manual parsing. 

### 3. Youtube API

Youtube is a video streaming services platform owned by Google where you can watch a lot of videos. Nowadays, Google opens API services for Youtube. So, it helps developers and everyone who wants to use Youtube as a 3rd party library services and to gather information.


## The Goal 
The goal of this project is to give me information about: 
* The topics that mostly I like based on the category.
* My favorite channels.
* What the words that commonly appear on the video that I like based on the title and tagging. 

## Steps of Process

### 1. Let's get started
First, install Anaconda and use Jyupter Notebook to run your python code. Here is the download link: 
```
https://www.anaconda.com/distribution/
```

After you finished install Anaconda, then install Selenium by running command below :
```
pip install selenium
```

Create your first project in Jupiter Notebook.  

After that, we need to import the web driver to control Chrome with our code. Here is the download link and chose the one that compatible with your browser: 
```
https://sites.google.com/a/chromium.org/chromedriver/downloads
```

more information about chrome web driver: 
```
https://github.com/SeleniumHQ/selenium/wiki/ChromeDriver
```

Note: If you using macOS, at first you must enable permission at security settings. 

### 2. Getting Youtube API Key 
At this session, I need Youtube API to get information about video detail. The fields that I use are the title, description, category, channel id, channel name, and tags.

Before you can use Youtube API, you must register your application to get permission and access key.
Here is the link: 
```
https://developers.google.com/youtube/v3/getting-started
```

### 3. Save the data to CSV File

Youtube has limitation quota access per day. So, I decided to save the data into local storage. Instead of save it into the MySQL database, I prefer to save it into CSV file because it easy to save and load data without querying first.

### 4. Stop words

I use stop words to filter and erase common words like the, a, that, and etc.

### 5. Present data into Chart and Wordcloud

