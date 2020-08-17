---
name: ReelLife
tools: [Python, Machine-Learning, Hackathon]
image: https://i5.walmartimages.com/asr/bc1390d5-52e9-4359-acdd-7c38962a67c5_1.8776c90ead6e778008c1152d962cb806.jpeg
description: 2019 SFSU Hackathon Project
---

# ReelLife
![Project Preview](http://ashazar.me/assets/reellife-gif.gif)

## What Is It?
ReelLife was a hackathon project developed for the SFSU 2019 Hacks competition. It provides any content creator an easy way to find thumbnails, highlights, or even the perfect shot for your promotional material. By giving a curated list of top quality images, it cuts down on time spent digging through footage looking for only the best shots.

## How Does It Work?
All the end user has to do is input the video of their choice and it will give the user a set of the best shots to choose from. In the python backend, it leverages a Convolutional Neural Network (CNN) that was trained on a highly curated dataset that featured "action shots". With this machine learning classifier, it would help identify the best shots within the user's video.

## Biggest Challenges
The biggest challenge working on this project was building the dataset. It was difficult defining what constituted an "action shot" or a scene of importance that the content creator would want to showcase due to how subjective it is. So we took a very simple approach where we defined it as a scene where a character's face was clearly visible and in the forefront of a scene. To speed data collection, we also employed facial recognition to cut down on the number of images that did not contain a proper image of a face. From there we curated the data further to emphasize scenes where the character was front and center and in focus of the image.

## Future Improvements
The main improvement we would work on next time around would be the dataset we've built. Our current dataset consists only of frontal shots of people within movie scenes. This proved to work great in the identification of a majority of highlight scenes within videos. However, a great highlight scene can still lack this frontal shot criteria and still convey a significant message to the video as a whole. We would like to expand this dataset to identify the various different highlight scenes that can exist.


#### Check out the full project here: https://github.com/AashinShazar/reellife

