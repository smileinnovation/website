# website
Our Jekyll-website

## Writing

We have several type of content, called _Collections_ in Jekyll world:
- demos
- projects
- videos

When you want to contribute, simply create a new `[year]-[month]-[day]-[title].markdown` file into the folder of the content type.
Then pay attention to include the front-matter in the begining of the file. By default it look like this, but can have more data into it:

```
---
layout: post
title: "[your title]"
date: "2019-04-19 14:08:20 +0200"
description: [please fill that it will be use for social media preview]
image: [gonna be use for social media preview]
author: [put here a key from _data/authors.yml like alrou]
lang: en_US
---
```

### Demos

### Projects

### Video
Video are content we are published online on Youtube (so far only Youtube).
Here's the front matter data you need to add :

```
youtube_url: url_without_quotes_or_doublequotes_around

```

You don't need to enter a content, if you do, it will be taken as description for the content's page.
