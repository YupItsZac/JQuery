Sliding Page Background with JQuery
======

One of the many cool things you can do with JQuery is slide between backgrounds of a website. If you'll notice on mine ( www.yupitszac.com ) I use this technique to change the background when the site content is chosen by the user.

So, let's get started.
======
Step 1): For this tutorial, we'll be using the .animate() feature included in JQueryUI. So, we'll need to include the JQuery and JQueryUI Javascript files. You can use the hosted content from Google, if you'd like.

<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script> 
<script src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.10.3/jquery-ui.min.js"></script> 


Step 2): You will need to store the background images youwish to use in DIVs. This gives us the ability to actually make the bg slide across the page.

<div id="bg" class="bg"></div>
<div id="bgg" class="bgg"></div>


Step 3): Now let's add some CSS to make sure the background divs stay in the back.

.bg {
  position: fixed;
  height: 100%;
    background: url(URL TO BACKGROUND 1) no-repeat center center fixed;
    -webkit-background-size: cover; /* For WebKit*/
    -moz-background-size: cover;    /* Mozilla*/
    -o-background-size: cover;      /* Opera*/
    background-size: cover;         /* Generic*/
  z-index: 90;
  margin: 0;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
}

.bgg {
  position: fixed;
  height: 100%;
    background: url(URL TO BACKGROUND 2) no-repeat center center fixed;
    -webkit-background-size: cover; /* For WebKit*/
    -moz-background-size: cover;    /* Mozilla*/
    -o-background-size: cover;      /* Opera*/
    background-size: cover;         /* Generic*/
  z-index: 90;
  margin: 0;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  display: none;
}

Step 4): Finally, we need to add some Javascript, so the backgrounds will slide. You can do it automatically like a slideshow, but for this tutorial we will slide the BGs when the user clicks a button.

$('#bg').delay(5000).hide('slide', {direction: 'left'}, 1000);

//.delay(5000) waits 5 seconds before sliding the first bg off the page with .hide()

$('#bgg').delay(5000).show('slide', {direction: 'right'}, 1000);

//In this second line, we wait 5 seconds from page load to show the second bg, since our first will be sliding out at that time.


Conclusion
======

It's as easy as that, guys! I've included a fully functional example that you are more than welcome to play around with. Don't forget to Tweet me (@YupItsZac) and let me know what your thoughts are. Also, feel free to visit my website at www.yupitszac.com

If you would like to see a working demo before you try it, visit: http://www.yupitszac.com/demo/sliding-background.html