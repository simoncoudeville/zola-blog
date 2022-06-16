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
        <p class="cursor-text">
        Building site... <br>
        Checking all internal links with anchors. <br>
        > Successfully checked 0 internal link(s) with anchors. <br>
        -> Creating 5 pages (1 orphan) and 0 sections <br>
        Done in 109ms. <br>
        </p>
    </div>
</figure> -->

I've been designing and making websites since 2004. That's a long time on the internet. When I started studying the web was only just starting to get mainstream attention. CSS didn't exist. Back then everything was done with tables and HTML properties. Maybe By now you should have a good guess how old I am. So it took me almost 20 years to finally start a blog. I always wanted one but never really got around finishing. I've made tons of designs over the years all of which I felt where not good enough. I'm the kind of designer that overthinks everything too much, always pushing pixels, changing typefaces, layouts and so on. To the point I'm fed up with it and start over. Meanwhile procrastinating actually writing something. Even when writing this I kept changing stuff. Somehow this time it sticked. So here we are. This is my first personal blog post ever. It's about why and how I finally made this place.

## Why now?

Before I started teaching 5 years ago I was a senior designer at what is now [Duke & Grace](https://www.dukeandgrace.com/en/). So I was always busy designing and developing websites for clients, big and small. At that moment I wasn't enjoying it as much as I used to so when the opportunity to start teaching presented itself I didn't hesitate. Without really knowing it it was time for something new. I haven't regretted it for one second. As it turns out I actually know a lot about certain topics. And I enjoy explaining it. But after 5 years of teaching and a lot of . This blog is supposed to become my digital playground where I can write, experiment with new typefaces and so on&hellip;

Sharing what I know and get better at writing qmsdlfj taeching

I was inspired by Leticia Portella's blogpost [Why you should have a blog (and write in it)](https://leportella.com/why-have-a-blog.html/) to finally start writing and sharing my knowledge.

Finally The Oatmeal convinced me to [stop petting my painting](https://theoatmeal.com/comics/creativity_petting). In his comic

## Tech stack

So yeah, no more Sass. Since the time I last used Sass for a professional project and when I started developing this site so much has changed in the CSS landscape. When I tried using it with the CSS I had written so far I got lots of errors. One of them being I couldn't use

I still use Sass but mainly for declaring breakpoint variables to use in media queries. Until we have custom media queries this is the way I get around that. I know there's something like a post CSS plugin but I haven't figured out how to use this yet.

### Zola

## Design

At the time of writing the homepage features the one and only "latest" article. Since I have only one article this seems like the most logic way to present it. Also, I find it hard to write about myself so I don't want a "hello, I'm this guy and I do this and that" kind of homepage.

### Typography

## Content

```css
/* comment */

:root {
  --color: #bada55;
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

<script type="module">
import { SVG } from "https://cdn.skypack.dev/@svgdotjs/svg.js";
import {
  spline,
  random
} from "https://cdn.skypack.dev/@georgedoescode/generative-utils@1.0.0";

const svg = SVG(".svg-canvas");

function generate() {
  // clear the contents of the SVG
  svg.clear();

  const iterationCount = random(5, 10);
  const points = [];

  for (let i = 0; i <= iterationCount; i++) {
    const y = random(50, 450);
    const x = random(50, 950);

    points.push({
      x,
      y
    });
  }

  const pathData = spline(points, 1, true);
  // render an svg <path> using the spline path data
  svg.path(pathData).fill("none").cy(250).cx(500).attr("vector-effect","none-scaling-stroke");
  // svg.ellipse(1000, 1000).fill('#f06');
}

generate();
</script>

<!-- more -->
