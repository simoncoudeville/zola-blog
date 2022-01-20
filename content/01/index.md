+++
title = "A long overdue hello world"
description = "Why and how I finally made this place"
date = 2019-11-27
slug = "a-long-overdue-hello-world"
+++

I've been designing and making websites since 2004. That's a long time in internet terms. When I started studying the web was only just starting to get mainstream attention. CSS didn't exist. Back then everything was done with tables and HTML properties. By now you should have a guess how old I really am.
So it took me allmost over 20 years to finally start a blog. But here we are. This is my first personal blog post ever. It's about how and why I finally made this place.

## Tech stack 

Nulla facilisi. Aenean urna metus, egestas quis mauris non, dignissim vestibulum risus. Mauris posuere nisl a massa commodo rhoncus. Fusce sed euismod dui, eget aliquet sem. Aenean quam est, iaculis quis aliquet at, semper id tellus. Suspendisse fringilla ipsum diam, suscipit commodo neque varius ac. Maecenas commodo orci vitae massa dapibus, interdum ultricies ex scelerisque. Nullam volutpat mollis aliquam. Donec fringilla interdum urna, nec posuere est tincidunt a.

Morbi molestie aliquam congue. Sed pulvinar id lectus eget luctus. Fusce non augue efficitur, posuere dolor et, gravida enim. In ullamcorper lorem turpis, in finibus eros posuere id. Maecenas vulputate dapibus risus vel tempor. In pulvinar commodo dui eu mattis. Duis fringilla dictum elit, et dictum nisi sollicitudin non. Vestibulum fermentum ligula id augue ullamcorper, a bibendum neque ultrices.

## Design

Vivamus at volutpat dolor, vitae interdum nulla. Morbi vitae sagittis mi, a pulvinar ex. Fusce convallis diam quis turpis tristique, sodales euismod nunc ullamcorper. Aenean id nulla et leo sodales aliquam. Donec a felis vel ipsum fringilla volutpat. Praesent luctus nisl sit amet est interdum elementum. Etiam tincidunt malesuada sapien, quis tincidunt urna faucibus sed. Aliquam iaculis ex at felis sodales iaculis. Sed quis mauris finibus, consequat risus rutrum, ornare libero. Maecenas ultrices mollis nibh in interdum. Cras molestie quis velit quis dictum. Cras vehicula neque id turpis facilisis fringilla. Quisque sit amet tincidunt lectus, vel feugiat diam. Nullam euismod lacinia mi non facilisis.

```css
/* comment */

:root {
    --color: #BADA55;
}

.test {
    color: var(--color);
}

@media (min-width: 40rem) {
  :root {
    --global-baseline: 0.315789473684211rem;
    --global-root-fontSize: 118.75%;
  }
}

::selection {
  background-color: var(--global-selection-backgroundColor);
  color: var(--global-selection-color);
  text-shadow: none;
}

a:hover {
  color: var(--link-hover-color, var(--global-link-hover-color));
  text-decoration-color: var(--link-hover-color, var(--global-link-hover-color));
}
```

```javascript
async function getStoredPoem(url) {
    url = apiUrl + storedTitle;

    // Storing response
    const response = await fetch(
        url
    );

    // Storing data in form of JSON
    var data = await response.json();

    if (response) {
        show(data);
    } else {
        console.log('something bad happened');
    }
}
```

<style>
  :root {
  --global-color-primary-hue: 250;
  --global-color-primary-saturation: 50%;
  --global-color-primary-lightness: 60%;
  --html-before-backgroundColor: var(--global-color-primary);
  --html-before-background-gradient-color1-hsl: calc(var(--global-color-primary-hue) - 20) var(--global-color-primary-saturation) var(--global-color-primary-lightness);
  --html-before-background-gradient-color2-hsl: calc(var(--global-color-primary-hue) + 20) var(--global-color-primary-saturation) var(--global-color-primary-lightness);
  --header__logo-color: white;
  --header__meta-color: rgba(255 255 255 / .65);
  --header__logo-decoration-color: var(--header__meta-color);  
  --intro__title-color: white;
}

@media (prefers-color-scheme: dark) {
  :root {
    --html-before-opacity: .25;
  }
}
</style>
