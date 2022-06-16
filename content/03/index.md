+++
title = "Fix margin collapsing with flow-root"
date = 2021-11-28
slug = "fix-margin-collapsing-with-flow-root"
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
    const y1 = random(50, 450);
    const y2 = random(50, 450);
    const x1 = random(50, 950);
    const x2 = random(50, 950);
        
    svg.line(x1, y1, x2, y2).stroke({ width: 1 });
  }
  
}

generate();
</script>