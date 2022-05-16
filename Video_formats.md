# Video formats
Large GIFs are inefficient for delivering animated content. Consider using MPEG4/WebM videos for animations and PNG/WebP for static images instead of GIF to save network bytes.

### Best practice
Check [the following link](https://web.dev/replace-gifs-with-videos/) for the best practices for this topic.

### Code example
* Use MPEG4 as a legacy option

```
ffmpeg -i my-animation.gif -b:v 0 -crf 25 -f mp4 -vcodec libx264 -pix_fmt yuv420p my-animation.mp4
```

* Use WebM for browsers that support it. WebM videos are much smaller than MP4 videos, but not all browsers support WebM so it makes sense to generate both.

```
ffmpeg -i my-animation.gif -c vp9 -b:v 0 -crf 41 my-animation.webm
```

* Compare the difference to see if it's useful

* Use the video on the webpage:

```
<video autoplay loop muted playsinline>
  <source src="my-animation.webm" type="video/webm">
  <source src="my-animation.mp4" type="video/mp4">
</video>
```

### Check
* Google lighthouse can identify issues with large GIF files.