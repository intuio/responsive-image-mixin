# Responsive Image Mixin

> This SASS mixin lets you easily create responsive images as via the background-image css-property. It's part of the [awesomeness-framework](awesomeness.intuio.at) developed at [intuio](http://intuio.at/).

## Why

Using this mixin allows you to easily create responsive images via CSS. This technique works in all current browsers and no additional javascript is needed.
The big advantage of this approach is that you can maintain your breakpoints as variables in SASS, while the [picture element](http://scottjehl.github.io/picturefill/) forces you to maintain it in your CSS as well as your HTML. The downside to this approach is, that image URLs have to be part of the SASS/CSS-code and a ``div`` is used to do the job of an ``img`` which can affect SEO-performance. We use ``aria-label`` and ``role`` to lessen the impact on accessibility and SEO.

### Requirements

You need [compass](http://compass-style.org/) and [breakpoint SASS](http://breakpoint-sass.com/) to use this mixin.

### HTML

```html
<div id="my-oreo-cake" class="responsive-image" aria-label="this is a yummy oreo cake" role="img">
        <div class="responsive-image__inner"></div>
</div>
```

### SASS

```scss
// Load the partials
@import "breakpoint";
@import "responsive-images";

#my-oreo-cake
{
    // @include responsive-image(url, width(px), height(px), <breakpoint>);
    @include responsive-image("oreocake.jpg", 400, 249);
    @include responsive-image("oreocake--medium.jpg", 750, 467, 35rem);
    @include responsive-image("oreocake--large.jpg", 1024, 638, 46.8rem);
}
```

### Examples

[Visit the awesomeness-framework to see the mixin in action](http://awesomeness.intuio.at/images/) or download this mixin and check out the example folder.

## License

MIT
