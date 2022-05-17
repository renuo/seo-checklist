# Inline CSS

## HTML Style-Attributes
Avoid inline CSS like `<p style="font-size: 16px">`: Inline CSS attributes unnecessarily increase page size, and can be moved to an external CSS stylesheet. Removing inline CSS properties can improve page loading time and make site maintenance easier.

## Prefer external files over <style>-Tags
Prefer external files over style-Tags in the HTML:

```html
<style>
  body {
    font-size: 14px;
  }
</style>
```

## (optional) Critical CSS
Since CSS-Files can become large and downloading them can get slow especially on slow connections, this makes CSS a render-blocking resource. If performance is bad, this can be improved with a technique called `Critical CSS`. The idea is to move CSS which is relevant for everything above-the-fold (all content a viewer sees on page load, before scrolling), so that no additional request is needed to fetch these styles. The remainder of the CSS can be loaded asynchronously.

**Note:** Aim to keep above-the-fold content under 14 KB (compressed).

Further reading: https://web.dev/extract-critical-css/