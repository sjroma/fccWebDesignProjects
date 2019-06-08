# Notes  

* Don’t be afraid to be descriptive with class names. It’ll be more semantic for yourself, and others who read your code. For example, if you have several two letter IDs that make sense to you now, they may not a year later and probably won’t mean anything to other people.  
* Take an in-depth look at Flexbox and Grid. Learn one first, then the other. You can combine them both to make powerful, responsive layouts. [CSS-Tricks](https://css-tricks.com) has an amazing write-up on [Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) and [Grid](https://css-tricks.com/snippets/css/complete-guide-grid/) that I reference often. I usually use grid for my entire page-layout and flex for formatting rows and columns.
  * [Wes Bos has free courses](https://wesbos.com/courses/) for both Flexbox and Grid that are well written and quick and easy to go through.
* Get familiar with the [box methodology](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model). Once you realize everything you see on a webpage is just a box you need to move around and resize, things will start to click. Often times, I’ll use a bit of the following bit of JS in the console to outline every element so I can see what’s going on if I’m having trouble with something.  
  ```javascript
  (function(){
    var all=document.getElementsByTagName("*");
    for(var i=0,max=all.length;i<max;i++) {
      all[i].style.outline="1px solid #"+((1<<24)*Math.random()|0).toString(16)
    };
  })();
  ```
* Codepen creates large and small screen shots of pens that can be used in your portfolio.  
  * Access them from; https&#58;//codepen.io/userName/pen/penName/image/large.png and https&#58;//codepen.io/userName/pen/penName/image/small.png
* Including Google fonts, should I use the **link** or **import**?
  * For 90%+ of the cases you likely want the **&lt;link&gt;** tag. As a rule of thumb, you want to avoid **@import** rules because they defer the loading of the included resource until the file is fetched.
