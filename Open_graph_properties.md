# Open graph properties

In addition to the Schema.org metadata it can be helpful to add support for Facebook’s Open Graph protocol. This metadata format improves the user experience when your content is shared on their corresponding social network.

## Code example

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta property="og:title" content="The Rock" />
  <meta property="og:type" content="video.movie" />
  <meta property="og:url" content="https://example.com/" />
  <meta property="og:image" content="https://example.com/image.png" />
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>...</title>
</head>
<body>
  ...
</body>
</html>
```

### Best practice

* Best practice is to use these 5 properties: og:url, og:title, og:description, og:images and og:type.
* [How to use open graph properties](http://ogp.me/).
* Test your Open Graph markup with the [Facebook Object Debugger Tool](https://developers.facebook.com/tools/debug/).
