# Image optimization

Images often represent the largest part of downloaded bytes on a webpage and occupy a considerable part of the visible area. Therefore, image optimization can often save the largest amount of bytes and achieve significant performance improvements for a website.

## Best practice

* Use small images (< 200 KB) that load quickly
* Choose the right image format: 
  * Instead of gifs use `<video>`: e.g. [Video formats](https://github.com/renuo/seo-checklist/blob/performance-1/video-formats.md) and https://web.dev/replace-gifs-with-videos/
  * Fine detail with highest resolution: `png` or `SVG`
  * Optimizing a photo, screenshot, or a similar image asset: `jpeg`
  * If you use a WebView to render content in your platform-specific application: `WebP`
* Choose the correct level of compression: Use PNG and JPEG compression tools such as https://tinypng.com/, Imagemin (suggested by Google) or [ImageOptim](https://imageoptim.com)
* Serve responsive images with the `srcset` tag
* Use image CDNs to optimize images

Source: [web.dev Fast load times - Optimize your images](https://web.dev/fast/#i18n.paths.fast.topics.optimize_your_images)

## Check

* Google lighthouse can identify issues with image sizes

## Code

Convert PNG to JPEG (settings from Google PageSpeed insights v4)

```
convert $IMG.png -sampling-factor 4:2:0 -strip -quality 85 -interlace JPEG -colorspace sRGB $IMG.jpg
```

As a special trick you can add `-gaussian-blur 0.05` to the above command to get much smaller (but blurry) images.
This can work very well for backgrounds.
