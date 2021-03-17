# CSS code snippets to solve practical problems

I hand-picked some of the most useful code snippets I use in my developer routine. Hope you like.

## Align elements in the middle of a div:

```
div {
  display: flex;
  align-items: center;
  justify-content: center;
}
```

## Reset elements:

```
html, body, div, span, applet, object, iframe, h1, h2, h3, h4, h5, h6, p, blockquote, pre, a, abbr, acronym, address, big, cite, code, del, dfn, em, img, ins, kbd, q, s, samp, small, strike, strong, sub, sup, tt, var, b, u, i, center, dl, dt, dd, ol, ul, li, fieldset, form, label, legend, table, caption, tbody, tfoot, thead, tr, th, td, article, aside, canvas, details, embed, figure, figcaption, footer, header, hgroup, menu, nav, output, ruby, section, summary, time, mark, audio, video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
  outline: none;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}

body { font-size: 62.5%; line-height: 1; font-family: Arial, Tahoma, sans-serif; }
 
article, aside, details, figcaption, figure, footer, header, hgroup, menu, nav, section { display: block; }

ol, ul { list-style: none; }
 
blockquote, q { quotes: none; }

blockquote:before, blockquote:after, q:before, q:after { content: ''; content: none; }

strong { font-weight: bold; } 
 
table { border-collapse: collapse; border-spacing: 0; }

img { border: 0; max-width: 100%; }
 
p { font-size: 1.2em; line-height: 1.0em; color: #333; }
```

## Cross-Browser transparency:

```
.transparent {
  filter: alpha(opacity=50); /* internet explorer */
  -khtml-opacity: 0.5; /* khtml, old safari */
  -moz-opacity: 0.5; /* mozilla, netscape */
  opacity: 0.5; /* fx, safari, opera */
}
```

## Custom text selection:
```
::selection { background: red; }
::-moz-selection { background: red; }
::-webkit-selection { background: red; }
```

## Anchor link pseudo classes:
```
a:link { color: blue; }
a:visited { color: purple; }
a:hover { color: red; }
a:active { color: yellow; }
```

## Background:
```
div { 
  background: url('image.jpg') no-repeat center center fixed;
  background-color: red;
  background-size: cover;
}
```

## Fontface:
```
@font-face {
  font-family: 'my-font';
  src: url('my-font.otf');
  font-display: swap;
}
```

## Root variables:
```
:root {
  --color-primary: #F36B22;
  --color-secondary: #47CDC6;
}

p {
  color: var(--color-primary);
}
```

## Table zebra stripes:
```
tbody tr:nth-child(odd) {
  background-color: #ccc;
}
```

## Inner box shadow:
```
div { 
  -moz-box-shadow: inset 2px 0 4px #000;
  -webkit-box-shadow: inset 2px 0 4px #000;
  box-shadow: inset 2px 0 4px #000;
}
```

## Outer box shadow:
```
div { 
  -webkit-box-shadow: 0 2px 2px -2px rgba(0, 0, 0, 0.52);
  -moz-box-shadow: 0 2px 2px -2px rgba(0, 0, 0, 0.52);
  box-shadow: 0 2px 2px -2px rgba(0, 0, 0, 0.52);
}
```

## Force hand cursor over clickable items:
```
a[href], input[type='submit'], input[type='image'], label[for], select, button, .pointer {
  cursor: pointer;
}
```

## Display URLS in a printed webpage:
```
@media print {  
  a:after { content: " [" attr(href) "] "; }  
}
```

## Truncate string with ellipsis:
```
p {
  width: 250px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
```

## Animation:
```
div {
  animation-name: example;
  animation-duration: 5s;
  animation-timing-function: linear;
  animation-delay: 2s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}

div {
  animation: example 5s linear 2s infinite alternate;
}
```

## Keyframes:
```
@keyframes myKeyFrame {
  0% {
    width: 100px;
  }
  30% {
    width: 120px;
  }
  100% {
    width: 130px;
  }
}

div {
   animation: myKeyFrame 2s ease-out;
}
```

## Placeholder styling:
```
::placeholder { /* Chrome, Firefox, Opera, Safari 10.1+ */
  color: rgba(255, 255, 255, .5);
  opacity: 1; /* Firefox */
}

:-ms-input-placeholder { /* Internet Explorer 10-11 */
  color: rgba(255, 255, 255, .5);
}

::-ms-input-placeholder { /* Microsoft Edge */
  color: rgba(255, 255, 255, .5);
}
```

## Scrollbar:
```
div {
  scrollbar-color: #63799B rgb(207,214,225) !important; // Firefox
  scrollbar-width: thin !important; // Firefox
}

div::-webkit-scrollbar {
  width: 9px;
}

div::-webkit-scrollbar-track { 
  background: rgb(207,214,225);
  background: linear-gradient(90deg, rgba(207,214,225,0) 20%, rgba(207,214,225,1) 20%, rgba(207,214,225,1) 80%, rgba(207,214,225,0) 80%);
  border-radius: 5px;
}
  
div::-webkit-scrollbar-thumb {
  background: #63799B;
  border-radius: 5px;
}

div::-webkit-scrollbar-thumb:hover {
  background: #63799B; 
}
```
