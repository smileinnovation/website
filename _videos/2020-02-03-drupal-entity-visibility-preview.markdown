---
layout: post
title: "Drupal Entity Visibility Preview"
date: "2020-02-03 17:07:26 +0100"
description: At the end of 2019, we developed a Drupal 8 module called Entity visibility preview. Let's dive together on what you can do with this module.
author: fltor
lang: en_US
youtube_url: https://youtu.be/hF-Lzroc7NU
---
At the end of 2019, we developed a Drupal 8 module called [Entity visibility preview](https://www.drupal.org/project/entity_visibility_preview).

Its goal is to allow site owners to add visibility conditions (date interval, categorization, other) on content entities to be able to display different contents to visitors depending on their categorization, the current date or other conditions.

It also allows previewing the website in the combination of conditions you want to test what your expected visitors will see.

To do so, the module provides a new plugin type, and two plugins of this new type (One for the date and one for categorization) and a new field type to add to your content entities.

You can see the presentation and a demo in the video. Here is the transcript of the video:

### Transcript:

Welcome to this presentation and demonstration of the Entity visibility preview module!

This module had been developed and maintained by the research and development department at Smile called Smile innovation.

Its goal is to allow site owners to add visibility conditions (date interval, categorization, other) on content entities to be able to display different contents to visitors depending on their categorization, the current date or other conditions.

It also allows previewing the website with combinations of conditions so you can to test what you expect your visitors to see.

To do so, the module provides a new plugin type, and two plugins of this type (One for the date and one for categorization) and a new field type to add to your content entities.

Now, let’s see the module in action. To shorten the length of this demo, here is the setup I have done in preparation:
- Create a new taxonomy vocabulary named “public type”
- Add two terms, “Children” and “Teenagers” (let’s say we are on a website about toys, you want to show different toys depending on your public age
- Add a taxonomy term reference field on user profile named “public type” which allows referencing taxonomy terms from the previously created vocabulary
- Create a paragraph type named “text” with a unique text field for the purpose of the demo and a new entity visibility condition field, with the date range and the taxonomy condition plugins enabled and set to use the public type vocabulary and the public type field on users for the taxonomy condition plugin. You can select different vocabularies and fields on the user profiles for each field instance giving you a wide range of usage.
- On the basic page content type, the default body field had been removed and a paragraph field had been added.
- Also, an entity visibility preview field had been added with only the date range condition plugin to show that in the case of nodes the widget is placed in the “advanced” column. We will not use this field during the demo.
- Create two users, “child” and “teen” with respectively the associated taxonomy terms “children” and “teenagers”
- Create a basic page “Landing page” with a menu link in the main menu for easier access. On this node, the following paragraphs had been created:
    - one available for everybody anytime
    - one available for everybody in January
    - one available for everybody in February
    - one for children anytime
    - one for teenagers anytime
    - one for children in January
    - one for teenagers in January
    - one for children in February
    - one for teenagers in February
So we will be able to demonstrate date and categorization conditions combined.
- For anonymous users, the module provides a dedicated page to configure which taxonomy terms for which entity visibility preview field instance and field on user profile an anonymous user is considered to have. So as an administrator you will have great flexibility.

Now let’s see the node as an administrator: we only see paragraphs 1 and 2 because the administrator user account does not have categorization and we are in January.

Using the preview form to go to a date in February we now see paragraphs 1 and 3.

Using the preview form to go to the current date and been categorized in “children” we now see paragraphs 1, 2, 4 and 6.

Using the preview form to go to the current date and been categorized in “teenagers” we now see paragraphs 1, 2, 5 and 7.

Using the preview form to go to a date in February and been categorized in “children” we now see paragraphs 1, 3, 4, and 8.

Using the preview form to go to a date in February and been categorized in “teenagers” we now see paragraphs 1, 3, 5, and 9.

Let’s reset the preview and log out so we will see what the anonymous user sees. Currently paragraphs 1 and 2.

Let’s go to the configuration form and add the “children” categorization to anonymous users. Now we see paragraphs 1, 2, 4 and 6.

Let’s go to the configuration form and change the “children” categorization to “teenagers” to anonymous users. Now we see paragraphs 1, 2, 5 and 7.

Let’s go to the configuration form and get both categorizations to anonymous users. Now we see paragraphs 1, 2, 4, 5, 6 and 7.

The demo is now finished. As you have seen, with the Entity visibility preview module you can change parts of your page if based on paragraphs, depending on date and categorization and other conditions depending on your needs and be able to preview the combinations. All of that with great flexibility in terms of configuration.

Although this demo has been done on paragraphs, you can add entity visibility condition fields to any fieldable content entity so you can cover a lot of other use cases.

Please note the following warning, the implementation of Entity visibility preview lies on the hook_entity_access which in the case of nodes is only triggered when viewing the node’s page. So a node with visibility conditions will still be accessible if it is in view results for example.

I hope you enjoyed the demo and the video. Do not hesitate to reach us using the module’s issue queue if you have questions or want to add new features.

Note: The browser datepicker has not been captured during the recording.
