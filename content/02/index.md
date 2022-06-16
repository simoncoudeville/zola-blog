+++
title = "Vertical rhytm on the web"
date = 2022-01-26
slug = "vertical-rhytm-on-the-web"
draft = false
+++

This is my second blog post.

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

  const pathData = spline(points, 0, true);
  // render an svg <path> using the spline path data
  svg.path(pathData).fill("none").cy(250).cx(500);
  // svg.ellipse(1000, 1000).fill('#f06');
}

generate();
</script>

<!-- more -->