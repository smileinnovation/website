---
layout: post
title: "KODA, giving a voice to vocally impaired people"
date: "2019-08-27 18:19:32 +0200"
author: thmil
tags: [koda, LSF, ML, IA]
image: /uploads/2019/08/27/jens-johnsson-OFpzBycm3u0-unsplash.jpg
---

Nearly one year ago, we ran our annual hackathon at Smile. A good real hackathon, one you would want to attend, tech for good, people for people hackathon. Offering 48h to teams at our company and paying for travel and accommodation in the nice [Mama works](https://www.mamaworks.com/fr/bordeaux/) of Bordeaux. Lovely spaces, well decorated and with a fantastic tech support team to give the best frame for groundbreaking ideas to sprout.

During this hackathon, emerged, along with other brilliant ideas, what would become KODA a couple of weeks later. The idea is pretty neat. Using computer vision to "read" sign language and translate it to text, then speak it out loud using speech synthesis.

## Some stats

There are around 370 millions deaf or hearing-impaired people in the world, according to numbers. Unfortunately, there are only 15 fully LSF (Langue des Signes Française, French Sign Language) scholar establishments for the 7 millions deaf or hearing-impaired people in France. With 1/1000 new born with hearing-impairment, it’s not enough. Nowadays, 200 000 people are signing in France and, for half of them, it’s their primary language used on a daily basis.

## Current solutions

What are the options when it comes to interacting with the hearing world ? For instance, when you have administrative tasks to do and people to contact.

Obviously, several solutions already exist, and there is a trend for more accessibility from devices, especially from Apple / Google. [Google Live Transcribe](https://www.android.com/accessibility/live-transcribe/), for instance, is an Android App that can differentiate several people talking around the smartphone and convert speech to text, in big characters, on the user screen. With also identifying contextual sounds like someone coughing.

Sign Aloud are wearable gloves which will read your hands movements and translate each letters from the American signed alphabet into their spoken equivalent but ... [that’s not enough](https://www.theatlantic.com/technology/archive/2017/11/why-sign-language-gloves-dont-help-deaf-people/545441/).

## Challenges

When it comes to translating an entire language to another, you can’t do a to word to word translation (remember why you are using Google translate instead of reverso ?). You have to get the context of each sentence, of the entire conversation, in order to be more relevant. Actually, that’s one of our biggest challenge. Sometimes, a few sign are needed to translate into a full sentence in French. Understanding the temporality and the context are then, essential. Because the past, present or future are expressed differently than in French, we have to  « unlearn » what we are used to with French to open our mind (and unbias our model) for LSF.

Testing which kind of artificial neuronal architecture to work with and how to train it properly is a major aspect for us. It’s an ongoing process we are doing while we are refining our solution. This is never fixed, it is constantly evolving. Sometimes, one of our team member wants to try out something because he thought about it last evening while watching Netflix. It could be a big improvement as well as something that just doesn’t add much to the actual state of the model.

Last but not least, the control of the execution environment also needs to be taken into account. For our experiments, we want to run a web-based client app, with a complete training and prediction stack in the cloud. Although, locally running model into embedded is definitely an evolution we are looking at. So far, we executed limited version of the model straight to the web browser or on a raspberry pi with a fairly good success rate.

## What we have today

We did a lot of exploration today and we are looking for funds to extend the prototyping phase. With the technical solution under control (although, we are always looking for improvements) we need to run our medium / large scale training data capture.

### Data collection

To collect data, we created a web platform where people can record pre-determinate words and expression. It’s light, performant, and lets the user record him/her self with just their camera (you can even give it a go with your tablet).

### In-browser model training

As we wanted to go to edge computing, we worked on a lightweight version of our model, which can run in-browser (and even on a small edge device like a raspberry pi) data collection and training. In this version of our web app, we let user input whatever phrase or word they want to train.

### Live-stream interpretation

At the very early stage of the project, the team went for something they know to be working well: training on frames. But as real people are not signing each letter to make a word, the hands motion is essential for the interpretation of the language. And in a near future, we even want to work with emotion recognition to enhance our prediction on what people are talking about. That’s why we worked on a server solution that will be able to handle live stream and pass it to the prediction engine, make the prediction, return it, and doing this « live », continuously.

Then finally, we would have improved our first solution of video capture + inference to plug a livestream capture and send it to this new architecture. And the results will be great.

<div class="ui horizontal divider">
<i class="envelope icon"></i> Get more infos
</div>

Wants to know more about this project? You can get in touch with [Fabien Gasser](mailto:fabien.gasser@smile.eu).
