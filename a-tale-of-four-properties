A Tale of Four Properties
-------------------------------------
*With [Chris Coyier](https://twitter.com/chriscoyier?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor)*

Note: Speakers have been paraphrased

Using some lesser known CSS features to create interesting layouts. As an example creating a hilarious fan page for They Might Be Giants.  

Using [shape-outside](https://developer.mozilla.org/en-US/docs/Web/CSS/shape-outside) to flow text around polygons, 
ellipses and more. Try polygon() and elipse() to create a shape to flow around. Available in all major browsers except Edge/IE. ie. float a triangle 
to the left and the text will flow/slant along the edge of the triangle. This does not have a path property.  

Using [offset-path](https://developer.mozilla.org/en-US/docs/Web/CSS/offset-path) to create an animation path. 
This was formerly known as motion-path. offset-path does note support the shape properties like polygon or ellipse. Only has .path 
as an option for setting the shape.  

[clip-path](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/clip-path) can be used to mask an image and animate a reveal of the image. ie. sliding in a part of an image, or revealing a 
full image from a slice of it. Use it with polygon to chop up things - ie. create a slanted edge on a div clipping the background.
clip-path doesn't support .path so to create a curved clip path you need to either point the clip path to an svg with a curved path 
or use a mask with a black and white image with the curve.  

SVG can be used for all sorts of things like clipping and masking, or animating on a path. SMIL will likely be deprecated eventually 
and this is driving much of most recent additions to css in an attept to give developers the same abilities natively in CSS. 

The current inconsistencies in the availability of path and some other implementations around this stuff can make using them 
problematic. The standards bodies have indicated that they intended to reign all this in.

