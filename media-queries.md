# Media queries

For public websites, your page should implement responsive design functionalities using the media query technique.
Media query techniques allow different presentation and content to be served depending on the output device, helping ensure that your website renders optimally on all devices and platforms. The '@media' rule allows different style rules for different screen sizes. Use a mobile-first approach.

## Example
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

## Best practices
* Always use `min-width`, never `max-width` and never ever both.
* Refactor old code which is not yet mobile first.
