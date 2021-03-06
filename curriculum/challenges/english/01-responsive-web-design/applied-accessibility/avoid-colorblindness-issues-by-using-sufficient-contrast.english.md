---
id: 587d778f367417b2b2512aac
title: Avoid Colorblindness Issues by Using Sufficient Contrast
challengeType: 0
videoUrl: 'https://scrimba.com/c/cmzMEUw'
---

## Description
<section id='description'>
Color is a large part of visual design, but its use introduces two accessibility issues. First, color alone should not be used as the only way to convey important information because screen reader users won't see it. Second, foreground and background colors need sufficient contrast so colorblind users can distinguish them.
Previous challenges covered having text alternatives to address the first issue. The last challenge introduced contrast checking tools to help with the second. The WCAG-recommended contrast ratio of 4.5:1 applies for color use as well as gray-scale combinations.
Colorblind users have trouble distinguishing some colors from others - usually in hue but sometimes lightness as well. You may recall the contrast ratio is calculated using the relative luminance (or lightness) values of the foreground and background colors.
In practice, the 4.5:1 ratio can be reached by darkening the darker color and lightening the lighter one with the aid of a color contrast checker. Darker colors on the color wheel are considered to be blues, violets, magentas, and reds, whereas lighter colors are oranges, yellows, greens, and blue-greens.
</section>

## Instructions
<section id='instructions'>
Camper Cat is experimenting with using color for his blog text and background, but his current combination of a greenish <code>background-color</code> with maroon text <code>color</code> has a 2.5:1 contrast ratio. You can easily adjust the lightness of the colors since he declared them using the CSS <code>hsl()</code> property (which stands for hue, saturation, lightness) by changing the third argument. Increase the <code>background-color</code> lightness value from 35% to 55%, and decrease the <code>color</code> lightness value from 20% to 15%. This improves the contrast to 5.9:1.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should only change the lightness value for the text <code>color</code> property to a value of 15%.
    testString: assert(code.match(/color:\s*?hsl\(0,\s*?55%,\s*?15%\)/gi), 'Your code should only change the lightness value for the text <code>color</code> property to a value of 15%.');
  - text: Your code should only change the lightness value for the <code>background-color</code> property to a value of 55%.
    testString: assert(code.match(/background-color:\s*?hsl\(120,\s*?25%,\s*?55%\)/gi), 'Your code should only change the lightness value for the <code>background-color</code> property to a value of 55%.');

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<head>
  <style>
  body {
    color: hsl(0, 55%, 20%);
    background-color: hsl(120, 25%, 35%);
  }
  </style>
</head>
<body>
  <header>
    <h1>Deep Thoughts with Master Camper Cat</h1>
  </header>
  <article>
    <h2>A Word on the Recent Catnip Doping Scandal</h2>
    <p>The influence that catnip has on feline behavior is well-documented, and its use as an herbal supplement in competitive ninja circles remains controversial. Once again, the debate to ban the substance is brought to the public's attention after the high-profile win of Kittytron, a long-time proponent and user of the green stuff, at the Claw of Fury tournament.</p>
    <p>As I've stated in the past, I firmly believe a true ninja's skills must come from within, with no external influences. My own catnip use shall continue as purely recreational.</p>
  </article>
</body>
```

</div>



</section>

## Solution
<section id='solution'>


```js
var code = "body {color: hsl(0, 55%, 15%); background-color: hsl(120, 25%, 55%);}"
```

</section>
