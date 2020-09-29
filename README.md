# Introduction about Project:

 `I set up face recognition in real time with my webcam using artificial intelligence. This AI is so fast that we can draw the different faces and expressions of each person in the video in real time without enduring a lot of power. We will use the Face API JS library based on Tensor Flow to set up face recognition.`

# IMPORTANT: Bug Fixes

## `navigator.getUserMedia`

`navigator.getUserMedia` is now deprecated and is replaced by `navigator.mediaDevices.getUserMedia`. To fix this bug replace all versions of `navigator.getUserMedia` with `navigator.mediaDevices.getUserMedia`

## Low-end Devices Bug

The video eventListener for `play` fires up too early on low-end machines, before the video is fully loaded, which causes errors to pop up from the Face API and terminates the script (tested on Debian [Firefox] and Windows [Chrome, Firefox]). Replaced by `playing` event, which fires up when the media has enough data to start playing.
