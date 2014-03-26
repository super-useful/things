# things

a collection of "stuff" that's `super-useful` to remember

## css

### pseudo-elements

- trying to access the `content` of a pseudo-element using `getComputedStyle( element:HTMLElement, pseudo:String )` when the pseudo-element is `display : none;` will return empty string `""`, regardless of what content is actually inside the pseudo element in your stylesheet.

### stacking contexts

- remember using css transforms creates a new stacking context.
  unless you know what you are doing, then do not — **DO NOT** — apply that shizzle to the `<body />`

### animations/transitions

- don't add a `transition` to an element using an `animation` or you may get unexpected results in certain browsers, e.g. firefox 26.
- fix flickering — or f**ked — animations/transitions — that utilise `translateZ` or `translate3d` — in webkit by adding:
  
  ``` css

     backspace-visibility : hidden;
     perspective          : 1000;
  ```
  
  to the same selector rule.
