Social Drop Bar
======

As Featured on http://www.hackmyhealth.com (After you share to Facebook)

Social Drop Bars are perfect to engage your website users with your social profiles. Here, I'll show you how to make one!

So, let's get started.
======
*Step 1:* For this tutorial, we'll be using the .slideUp() and .slideDown() JQuery features. So, we'll need to include the library. You can use the Google hosted library, if you want.

```javascript
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js" type="text/javascript"></script> 
```

*Step 2:* The next step is the markup for the share div. I've named it fbshare, since I only used it to engage with users after sharing to Facebook.

```html
<div class="fbshare">
Become Social with TeraTech Mobile CEO Zac Brown
<br><br>
<font style="font-size: 16px;">Make sure you check me out on these networks! I always follow back, and engage with my fans.</font>
<br><br>
<img src="http://www.hackmyhealth.com/twit.png" style="cursor: pointer; height: 150px; width: 150px; margin-right: 50px;" onclick="window.open('http://www.twitter.com/YupItsZac', '_blank');">
<img src="http://grassrootschange.net/wp-content/uploads/2013/11/FacebookLogo.png" style="cursor: pointer; height: 150px; width: 150px; margin-right: 50px;" onclick="window.open('https://www.facebook.com/YupItsZac', '_blank');">
<img src="http://www.agilart.com/Media/Default/BlogPost/blog/github.png" style="cursor: pointer; height: 150px; width: 150px; margin-right: 50px;" onclick="window.open('http://www.github.com/YupItsZac', '_blank');">

<a href="#" onclick="$('.fbshare').slideUp('slow');" style="position: absolute; right: 50px; bottom: 10px; color: #fff; font-size: 12px;">Close Dialog</a>

</div>
```

*Step 3:* Now we need to style the markup to make it look pretty. We'll do that with some basic CSS. nothing too fancy, but make sure you have display set to *none*. This is very important.

```css
.fbshare {
  position: fixed;
  height: 350px;
  background-color: #4c66a4 ;
  color: #fff;
  font-size: 32px;
  width: 100%;
  text-align: center;
  z-index: 102;
  top: 0px;
  left: 0px;
  padding: 10px;
  display: none;
  
}
```

*Step 4:* Now, we add the JQuery. This is what will actually slide the bar up and down. On the close link in the bar div, we added this to onclick="". (This can also be done by adding a "click" listener to the link, but we'll do it this way for now.

```javascript
$('.fbshare').slideDown('slow');

//This goes on your open link. It will slide the social bar down when clicked.

$('.fbshare').slideUp('slow');

//This goes on the close link inside the social bar. That way when your user gets tired of seeing the social bar or wants to go back to your site content, they can just close it gracefully.
```

Conclusion & Live Demo
======

It's as easy as that, guys! I've included a fully functional example that you are more than welcome to play around with. Don't forget to Tweet me (@YupItsZac) and let me know what your thoughts are. Also, feel free to visit my website at www.yupitszac.com

If you would like to see a working demo before you try it, visit: http://www.yupitszac.com/demo/social-drop-bar.html