# Notes  
* Don’t be afraid to be descriptive with class names. It’ll be more semantic for yourself, and others who read your code. For example, if you have several two letter `id`'s that make sense to you now, they may not a year later and probably will never mean anything to other people. 
* In general, an `id` is typically used when you want to target HTML elements with JavaScript. A `class` is used to style the page. You can use an `id` to style the page if you want but know that they have more weight than a `class` does and the `id` will override a `class` targeting the same element. In your own personal projects that you create outside of freeCodeCamp some people recommend only using a `class` to style the page and an `id` if using JavaScript in your project. However, JavaScript can target a `class` too, so you may not need `id`'s that much in your personal projects.
* Get familiar with the [box methodology](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model). Once you realize everything you see on a webpage is just a box you need to move around and resize, things will start to click. Often times, use the following bit of JS in the console to outline every element to see what’s going on if having trouble with something.  
  ```javascript
  (function(){
    var all=document.getElementsByTagName("*");
    for(var i=0,max=all.length;i<max;i++) {
      all[i].style.outline="1px solid #"+((1<<24)*Math.random()|0).toString(16)
    };
  })();
  ```
* Take an in-depth look at Flexbox and Grid. Learn one first, then the other. You can combine them both to make powerful, responsive layouts. [CSS-Tricks](https://css-tricks.com) has an amazing write-up on [Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) and [Grid](https://css-tricks.com/snippets/css/complete-guide-grid/) that anyone can (and should) reference often. Some people usually use grid for the entire page-layout and flex for formatting rows and columns.
  * [Wes Bos has free courses](https://wesbos.com/courses/) for both Flexbox and Grid that are well written and quick and easy to go through.
* Elements in CSS layout are normally either block-level or inline (with exceptions for elements within flex, table and grid elements). So it’s the basis for all of CSS layout: it treats all elements like boxes or text. `display:block` makes them act like a block element regardless of what they were before (images are inline for example). `display:inline` makes them act like an inline element. `display:inline-block` makes it act like a block that is laid out inline. See [CSS display properties: block, inline, and inline-block — & how to tell the difference](https://medium.com/@DaphneWatson/css-display-properties-block-inline-and-inline-block-how-to-tell-the-difference-7d3a1e6e3051)
* Including Google fonts, should I use the **link** or **import**?
  * For 90%+ of the cases you likely want the **&lt;link&gt;** tag. As a rule of thumb, you want to avoid **@import** rules because they defer the loading of the included resource until the file is fetched.
* 12 Easy Read Fonts
  - Georgia (serif) 
  - Rooney (serif)
  - Futura (sans-serif)
  - Helvetica (sans-serif)
  - Karla (sans-serif)
  - Lato (sans-serif)
  - PT Sans & PT Serif
  - Open Sans (sans-serif)
  - Quicksand (sans-serif)
  - Roboto (sans-serif)
  - Ubuntu (sans-serif)
  - Verdana (sans-serif) 
* Codepen creates large and small screen shots of your pens that can be used in your portfolio.
Access them from;  
  https://codepen.io/userName/pen/penName/image/large.png (for the large screenshot)  
  and  
  https://codepen.io/userName/pen/penName/image/small.png (for the small screenshot)
  * where you replace _userName_ with your codepen userId and _penName_ with the id of one of your codepen pens
  
## HTML tags vs. elements vs. attributes
### HTML tags
Tags are used to mark up the start and end of an HTML element. The following are paragraph tags.  
`<p></p>`  

### HTML elements
An element in HTML represents some kind of structure or semantics and generally consists of a start tag, content, and an end tag. The following is a paragraph element:  
`<p>This is the content of the paragraph element.</p>`

### HTML attributes
An attribute defines a property for an element, consists of an attribute/value pair, and appears within the element’s start tag. An element’s start tag may contain any number of space separated attribute/value pairs.
The most popular misuse of the term “tag” is referring to `alt` attributes as “alt tags”. There is no such thing in HTML. **Alt is an attribute, not a tag.**   
`<img src="foobar.gif" alt="A foo can be balanced on a bar by placing its fubar on the bar's foobar.">`  
