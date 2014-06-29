# CSS Tips

Writing CSS is an exercise in vocabulary. You just have to know the right words. Things like `font-size` and `background-color` are self explanatory. In my opinion, there are basically just two tricky things about CSS: `display` and `position`. (I'll add some Codepen examples soon.)



## Display
The `display` property controls how an element is... displayed. There are a huge number of different values you can assign to `display` but you really only need to know three: `block`, `inline`, and `inline-block`. There's one other interesting value, `flex`, which I'll touch on later.

### `block`
Most HTML elements default to `display: block`. This means they take up the full width of their parent container, and any following elements are displayed below them. You can set the width of a `block` element, but it'll still push everything below it.

### `inline`
Tags like `<span>`, `<em>`, and `<code>` default to `display: inline`. They're just a part of the normal flow of their parent's content with some extra presentational features. Setting the `height` or `margin` of elements with `display: inline` has no effect.

### `inline-block`
`display: inline-block` is used when you want elements to sit beside each other horizontally, but also want to control properties like `height` and `margin`. A common use case is the horizontal navigation bar. Typically, you'd put the links in `<li>` elements, which exist within a parent `<ul>`, and set `display: inline-block` on the `<li>`s. 



## Position
Positioning in CSS is finicky. All elements default to `position: static`, so it's unlikely you'd ever assign that value directly. The `top`, `right`, `bottom`, and `left` properties only have an effect on elements which have a `position` value other than `static`. (I'm going to refer to these four as "positional properties" from here on out.)

### `relative`
For elements with `position: relative`, the positional properties move the element from where it would have been had it been `static` instead. So, basically, you're moving an element _relative_ to it's default position. This element is still part of the "flow" of the document, so it affects how other elements are displayed.

### `absolute`
When `position` is set to `absolute`, positional properties refer to distance from the element's _closest positioned ancestor_. This means the nearest element up the tree which has `position` set to something besides `static`. Often you'll just set `position: relative` on the parent container of `absolute`ly positioned elements. If there is no non-`static` ancestor element, it'll be positioned relative to the `<body>`. When you set `position: absolute`, the element is removed from the normal flow of the document, so it doesn't affect where other elements are displayed. 

### `fixed`
`fixed` positioning is relative to the actual viewport (window). For example, you'd use `position: fixed` on a  navbar that sticks to the top of the window. Like `absolute`, `fixed` also removes an element from the content flow.



## Flexbox
Flexbox is an awesome new CSS feature that allows you to do all sorts of neat layout stuff. Exploring it in detail is beyond this post's scope, but if you're developing for modern browsers only, it can save you like a million headaches. Checkout this [awesome showcase](http://philipwalton.github.io/solved-by-flexbox/) of things flexbox can do. 