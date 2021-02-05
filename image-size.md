# Image size
Images often represent the largest part of downloaded bytes on a webpage and occupy a considerable part of the visible area. Therefore, image optimization can often save the largest amount of bytes and achieve significant performance improvements for a website.

## Best practice

* Use small images (< 200 KB) that load quickly. Dive deep in the [Google Developers Fundamentals](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization).
* Use lossy formats where possible. Have a quick bite in the older [Google Developers Insights v4](https://developers.google.com/speed/docs/insights/OptimizeImages).
* Use PNG and JPEG compression tools such as https://tinypng.com/.

## Check

* Google lighthouse can identify issues with image sizes

## Code

Convert PNG to JPEG (settings from Google PageSpeed insights v4)

```
convert $IMG.png -sampling-factor 4:2:0 -strip -quality 85 -interlace JPEG -colorspace sRGB $IMG.jpg
```

As a special trick you can add `-gaussian-blur 0.05` to the above command to get much smaller (but blurry) images.
This can work very well for backgrounds.
