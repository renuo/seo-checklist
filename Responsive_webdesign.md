# Responsive Webdesign

## Best practice

* For public websites, your page should implement responsive design functionalities using the media query technique.
Media query techniques allow different presentation and content to be served depending on the output device, helping ensure that your website renders optimally on all devices and platforms. The '@media' rule allows different style rules for different screen sizes.
* Develop mobile first: [Google Developer Help](https://developers.google.com/search/mobile-sites/mobile-seo/responsive-design).
* Consider limited network bandwith.
* Test your mobile friendliness: [Search Console Test](https://search.google.com/test/mobile-friendly) and [Lighthouse](https://developers.google.com/web/tools/lighthouse/).

## Code example

```css
// This applies from 0px to 600px
body {
  background: red;
}

// This applies from 600px onwards
@media (min-width: 600px) {
  body {
    background: green;
  }
}

```

## Best practice

* Always use `min-width`, never `max-width` and never ever both.
* Refactor old code which is not yet mobile first.
