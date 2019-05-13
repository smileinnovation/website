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

## config

The configuration of the website is in the `_config.yml` file. You'll have the following variables.

- `title` The website title, which will be use in the homepage and in the `<title>` tag in the head of each page
- `email` the contact email that will be display on the site
- `author` the default author for the content
- `description` the description that will be used for SEO/SMO
- `footer_legal_note` the legal note displayed in the footer of each page
- `baseurl` subpath of the site@
- `url` the base hostname & protocol for your site
- `date_format` date format following strftime function
- `twitter:username` the twitter usernamee
- `twitter:card` the type of twitter card (reads: embed on twitter) that will be use for sharing
- `facebook:app_id` your facebook app ID for your page
- `facebook:publisher` your facebook publisher ID
- `facebook:admins` your facebook admins ID (in an array)
- `logo` the URL of your logo
- `social:medium` the URL of your medium publication
- `social:youtube` the URL of your youtube channel
- `social:newsletter` the URL of your newsletter signin page
- `webmaster_verifications:google` your google webmaster verification code
- `webmaster_verifications:bing` your bing webmaster verification code
- `webmaster_verifications:alexa` your alexa webmaster verification code
- `webmaster_verifications:yandex` your yandex webmaster verification code
- `webmaster_verifications:baidu` your baidu webmaster verification code
- `lang` the default language of your content
-
