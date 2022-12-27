---
layout: post
title: Chrome Extension to change playback speed of videos on OneDrive
---


<div class="message">
  Howdy! This is an example blog post that shows several types of HTML content supported in this theme.
</div>

During the Fall Finals prep I had to revise a bunch of lecture videos, and I wanted to watch them at 2x speed. The only problem was that I had these lecture recordings on One Drive, which until now does not support the 2x speed button. So, I looked around online and somewhere on reddit I found a solution for my problem. By running `document.querySelector("video").playbackRate = 2`, I could increase the playback speed of the one drive video. However, I had to open the console and write paste and run this piece of code for each video, and it was getting a bit annoying considering I had something like 30 videos and I had to re-execute this piece everytime video page reloaded. 

I decided to use an extension for running this code, and wrote the [twox_onedrive](https://github.com/martianbilal/twox_onedrive) extension for chrome, that allows you to change the playback speed of a video on One Drive and a bunch of other sites. 

I made some slight changes to it and it now has a nice UI for increasing and decreasing the playback speed in chunks of 0.25. 

[Nouman](https://github.com/MNoumanAbbasi) also helped with some bug fixes and UI updates. 

