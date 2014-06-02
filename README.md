# List Carousel
_Also called Hero Carousel or Hero Slider_

This adds a jQuery plugin I wrote called listCarousel.

Pass it a list, it will turn it into a carousel. Should work for any kind of list with any content, but it was written with certain assumptions in mind.

## Assumptions:

1. **jQuery is installed** - this module requires jQuery to work. It includes xml to link `js/jquery/jquery-1.10.0.min.js`, but does not include that particular file. That file should be included in 1.13 Magento. If it isn't, download jQuery and place it at that location.
2. **Intended for Images** - This module assumes the carousel will contain images, so it sets some CSS on the `<li>` elements to force images to a certain ratio. For example, the `<li>`s height is forced to be it's `width * .565`, with `overflow: hidden`, meaning anything outside of that height will be hidden.
3. **Intentionally left out some CSS** - This module only adds minimal CSS to get the carousel generally looking okay. It's assumed that the style of the carousel/controls will have to be changed per Magento theme, or to make the page responsive.

This module also installs a test CMS page at `[URL]/hero-carousel` to use as an example.

## Usage


Take any `<ul>` and make a jQuery object out of it, then call the .listCarousel() jQuery plugin on that object:

```
    <ul id="cms-slider">
        <li><img src="http://www.getours.com/blog/wp-content/uploads/2013/05/dana-italy9.jpg" alt="" class="first"></li>
        <li><img src="http://ppcdn.500px.org/18349925/391c74c94517b36efb18a5d5b8c75b1922ccb3a9/5.jpg" alt="" class=""></li>
        <li><img src="http://1.bp.blogspot.com/-ajKP1dsO4XE/UAx0hpKLPFI/AAAAAAAAEtI/yktlGRtTWrw/s1600/IMG_1216.JPG" alt="" class=""></li>
        <li><img src="http://1.bp.blogspot.com/-vdx75oQX0pE/UBFyDNmBCXI/AAAAAAAAE3s/gT5u4DT-ugI/s1600/IMG_2545.JPG" alt="" class=""></li>
        <li><img src="http://www.getours.com/blog/wp-content/uploads/2013/05/dana-italy5.jpg" alt="" class=""></li>
        <li><img src="http://www.getours.com/blog/wp-content/uploads/2013/05/dana-italy10.jpg" alt="" class="last"></li>
    </ul>

```

```
jQuery(function() {
    jQuery('#cms-slider').listCarousel();
})
```

