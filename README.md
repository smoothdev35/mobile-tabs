# mobile-tabs

  - Stand-alone: https://vue-mobile-tabs.netlify.app/
  
  - Codepen: https://codepen.io/smoothdev35/pen/yLYEabN
  
  
  
This is a simple Vue demo to explore an idea of sliding tab navigation. 
I used svg to create the curved shape and gsap to do the animation.

The trick is simple: with a white bottom navbar and a grey background (replace with your colors), 
I just need to place a svg path with the curved shape right on top (width equal to 1/4 or 1/ as many items as your navbar holds), 
filled with the color of the background behind the navbar. This way, you have a nice curved "hole" you just need to translate between 
the nav items to give a smooth sliding effect. 

I just added the ball as another svg element, and used a gsap timeline to make it go down then up during tab change. 
The enter-leave animation for the slides/pages are a basic vue transition with v-if and the tab data coupled with a css 
transition declaration on relevant classes.

Feel free to use the code as you please!
