---
layout: post
title: "Computer Vision Car Speed Challenge"
author: "Omar Husain"
date: 2021-02-04
comments: true
youtubeId: 
cover-photo: "/assets/images/car.jpg"
photo: "/assets/images/car.jpg"
photo-alt: "/assets/images/car.jpg"
---

After listening to a podcast featuring the CEO of the self-driving car company comma.ai, and loving his vision and attitude, I decided to look at their website and learn more. On their careers page I found an old programming challenge that they created for potential hires. The goal was to create a computer vision model that would take dash-cam video footage from a car and predict the speed of the car in each frame.

I wrote a post on <a href="https://www.linkedin.com/pulse/computer-vision-speed-challenge-omar-husain/?trackingId=R9XWgUxrwAUH9Ov6fqyMEg%3D%3D">LinkedIn</a> with more details about this project for the nerds.

<!-- Animation Goes Here -->
![Animation](/assets/images/car.gif){:class="image fit"}

The basic concept is that the algorithm taks in two successive frames at a time from the camera and then processes them. The algorithm then does a lot of math on the pixels and then tries to guess what the speed of the car is at that moment. For every guess during training, the model is graded and then tries to self-correct.

I was really surprised at how accurate the model was given that it only took a few minutes to train. But the thing I learned the most from this project is just to keep going even if you're lost and full of doubt. Just take baby steps and try to solve small problems and eventually you will get closer to where you want to be.
