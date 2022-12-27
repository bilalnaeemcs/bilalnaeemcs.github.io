---
layout: post
title: Chrome Extension to change playback speed of videos on OneDrive
---


As a student preparing for fall finals, I found myself needing to review a large number of lecture videos. I wanted to watch them at a faster pace, but unfortunately, One Drive – where my recordings were stored – did not offer a 2x speed option.

While searching online for a solution, I came across a piece of code on Reddit that allowed me to increase the playback speed of One Drive videos by running `document.querySelector("video").playbackRate = 2` in the console. While this worked, the process of opening the console and pasting the code every time I switched to a new video became tedious, especially since I had around 30 videos to get through.

To make the process more efficient, I decided to create a Chrome extension called [twox_onedrive](https://github.com/martianbilal/twox_onedrive/) that would allow me to easily adjust the playback speed of One Drive videos (and videos on other sites as well). I made some modifications to the original code, including the addition of a user interface that allows users to increase or decrease the playback speed in increments of 0.25.

I received helpful bug fixes and UI updates from [Nouman](https://github.com/MNoumanAbbasi) as well. 

Details on installation and usage are available in the github repo for [twox_onedrive](https://github.com/martianbilal/twox_onedrive/).

I hope it helps you!

