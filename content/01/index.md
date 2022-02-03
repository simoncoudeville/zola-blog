+++
title = "A long overdue hello world"
description = "Why and how I finally made this place"
date = 2022-01-27
slug = "a-long-overdue-hello-world"
+++

<!-- <figure class="terminal mb-double">
    <div class="terminal__top">
        <div class="terminal__button"></div>
        <div class="terminal__button"></div>
        <div class="terminal__button"></div>
    </div>
    <div class="terminal__body">
        <p class="cursor-text">Hello world</p>
    </div>
</figure> -->

I've been designing and making websites since 2004.* That's a long time in* internet terms. When I started studying the web was only just starting to get mainstream attention. CSS didn't exist. Back then everything was done with tables and HTML properties. By now you should have a guess how old I really am.
So it took me allmost over 20 years to finally start a blog. But here we are. This is my first personal blog post ever. It's about how and why I finally made this place.

## Tech stack 

Nulla facilisi. Aenean urna metus, egestas quis mauris non, dignissim vestibulum risus. Mauris posuere nisl a massa commodo rhoncus. Fusce sed euismod dui, eget aliquet sem. Aenean quam est, iaculis quis aliquet at, semper id tellus. Suspendisse fringilla ipsum diam, suscipit commodo neque varius ac. Maecenas commodo orci vitae massa dapibus, interdum ultricies ex scelerisque. Nullam volutpat mollis aliquam. Donec fringilla interdum urna, nec posuere est tincidunt a.

### Zola

Morbi molestie aliquam congue. Sed pulvinar id lectus eget luctus. Fusce non augue efficitur, posuere dolor et, gravida enim. In ullamcorper lorem turpis, in finibus eros posuere id. Maecenas vulputate dapibus risus vel tempor. In pulvinar commodo dui eu mattis. Duis fringilla dictum elit, et dictum nisi sollicitudin non. Vestibulum fermentum ligula id augue ullamcorper, a bibendum neque ultrices.

## Design

Vivamus at volutpat dolor, vitae interdum nulla. Morbi vitae sagittis mi, a pulvinar ex. Fusce convallis diam quis turpis tristique, sodales euismod nunc ullamcorper. Aenean id nulla et leo sodales aliquam. Donec a felis vel ipsum fringilla volutpat. Praesent luctus nisl sit amet est interdum elementum. Etiam tincidunt malesuada sapien, quis tincidunt urna faucibus sed. Aliquam iaculis ex at felis sodales iaculis. Sed quis mauris finibus, consequat risus rutrum, ornare libero. Maecenas ultrices mollis nibh in interdum. Cras molestie quis velit quis dictum. Cras vehicula neque id turpis facilisis fringilla. Quisque sit amet tincidunt lectus, vel feugiat diam. Nullam euismod lacinia mi non facilisis.

### Typography

Nulla facilisi. Aenean urna metus, egestas quis mauris non, dignissim vestibulum risus. Mauris posuere nisl a massa commodo rhoncus. Fusce sed euismod dui, eget aliquet sem. Aenean quam est, iaculis quis aliquet at, semper id tellus. Suspendisse fringilla ipsum diam, suscipit commodo neque varius ac. Maecenas commodo orci vitae massa dapibus, interdum ultricies ex scelerisque. Nullam volutpat mollis aliquam. Donec fringilla interdum urna, nec posuere est tincidunt a.

```css
/* comment */

:root {
    --color: #BADA55;
}

@media (min-width: 40rem) {
  :root {
    --color: Hotpink;
  }
}

a:hover {
  color: var(--link-hover-color, var(--global-link-hover-color));
  text-decoration-color: var(--link-hover-color, var(--global-link-hover-color));
}
```

Vivamus at volutpat dolor, vitae interdum nulla. Morbi vitae sagittis mi, a pulvinar ex. Fusce convallis diam quis turpis tristique, sodales euismod nunc ullamcorper. Aenean id nulla et leo sodales aliquam. Donec a felis vel ipsum fringilla volutpat. Praesent luctus nisl sit amet est interdum elementum. Etiam tincidunt malesuada sapien, quis tincidunt urna faucibus sed. Aliquam iaculis ex at felis sodales iaculis. Sed quis mauris finibus, consequat risus rutrum, ornare libero. Maecenas ultrices mollis nibh in interdum. Cras molestie quis velit quis dictum. Cras vehicula neque id turpis facilisis fringilla. Quisque sit amet tincidunt lectus, vel feugiat diam. Nullam euismod lacinia mi non facilisis.

<style>
.terminal {
    --terminal-backgroundColor: var(--global-color-neutral-900);
    --terminal__buttonSize: .75rem;
    border: 1px solid var(--terminal-borderColor, var(--terminal-backgroundColor));
    border-radius: var(--global-border-radius-1);
    background-color: var(--terminal-backgroundColor);
    overflow: hidden;
    width: 100%;
    height: auto;
    aspect-ratio: 3 / 2;
    color: var(--global-color-neutral-100);
    font-family: var(--global-code-fontFamily);
    font-size: var(--global-fontSize-s);
}

.terminal__top {
    display: flex;
    gap: .5rem;
    padding: 1rem 1rem 0;
}

.terminal__button {
    display: inline-block;
    height: var(--terminal__buttonSize);
    width: var(--terminal__buttonSize);
    border-radius: 100%;    
    background-color: hsla(var(--global-neutral-hue), var(--global-neutral-saturation), 100%, .15);
}

/* .terminal__button + .terminal__button {
    margin-left: calc(var(--terminal__buttonMargin) / -2);
} */

.terminal__body {
    padding: var(--page-inner-whitespace);
}

.cursor-text:after {
    content: "_";        
    animation: 1s blink step-end infinite;
}


@media (prefers-color-scheme: dark) {
    .terminal {
        --terminal-backgroundColor: transparent;
        --terminal-borderColor: var(--global-border-color);
    }    
}

@keyframes blink {
  from, to {
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
}
</style>

<!-- more -->
