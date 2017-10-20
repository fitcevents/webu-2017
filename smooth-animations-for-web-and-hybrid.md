**Smooth Animations for Web & Hybrid**
-----------------------------------------------------------
*with [Alexander Blom](https://twitter.com/alexblom?lang=en)*

[Slides](https://www.slideshare.net/secret/aIov6z5953NHz8)

*  ##### What makes a good animation?
    * FPS Target
        * 60fps is considered best
        * 1000ms/60fps = 16.6ms per frame
        * 60fps is not always achievable
            * It's better to deliver a consistent frame rate, consider targeting 30fps
    * Animation Options
        * Declarative: CSS;
            * Generally the most performant
            * Browser knows what's happening up front, can save you from yourself
            * Can become quite complex to write (keyframe animations)
        * Imperative: JS;
            * Tell the browser _how_
            * Run on the main thread (not super performant)
            * `requestAnimationFrame` can help with this
    * How our content is rendered
        1. DOM Tree Constructed
        2. Layout (recursively from top left)
            * Highly interdependent
            * Expensive
    * Reflow
        * Recomputes the layout over and over again
        * _Changing_ `width`, `position`, `height`, `padding`, `font` _properties, resizing the browser window, adding or removing elements from the DOM, changing an element's classes, and many others_ causes Reflow.
        * Paint styles, however, are isolated in the individual node and _do not cause Reflow_.
        * Opacity is a special case
    * Layers
        * Default is a single layer
        * Composed layer is most efficient to animate - GPU
        * Pushing every node to its own layer is the _worst possible case_
    * Promoting a Layer
        * `will-change` in CSS gives the browser a heads up that `will-change: scroll`, `will-change: transform`, etc. is coming down the pipeline and will be easier and less costly to animate
    * Layout Thrashing
        * Part of the key here is keeping the JS thread as free as possible
            * Think about things like:
            ```javascript
            $('.boxes').css(blah, blah);

            // VS.

            var boxes = $('.boxes');

            // ACTION HERE so that the DOM isn't getting queried every time
            ```

            * Test -> have a look at the frame reader in devtools
* ##### Case Studies
    * Survivor Green Square Animation
        * __Takeaways:__
            * `setInterval()` should be considered a minimum amount of time, not precise as they will get pushed off if the thread is busy
            * `setInterval()` will fire at (or near) the stated interval indefinitely, _even if the tab is inactive_
        * Animation Frames
            * `animationFrame` is supported for all major browsers
            * Will only draw when:
                * the animation will be visible
                * the browser is ready
                * there are no other frames waiting to be drawn
        * Passive Event Listeners
            * allows you to indicate `preventDefault` will not be used, e.g. eliminates block on scroll
* ##### Best Practices
    * Avoiding JS animation API until better Safari support
    * Pages with smaller animations
        * CSS/Hardware accelerated animations are fine
        * Will generally promote frequent/transitional animations to their own layers
