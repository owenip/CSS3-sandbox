## Link
[CSS HSL](#CSS-HSL)     
[CSS ::before Selector](#CSS-::before-Selector)     
[CSS radial-gradient()](#CSS-radial-gradient())     
[CSS data type: `<position>`](#CSS-data-type:`<position>`)        


## CSS HSL
HSL stands for hue, saturation and lightness.       
`hsl(hue, saturation, lightness)`       
**Hue**     
Hue is a degree on the color wheel from 0 to 360. 0 is red, 120 is green, 240 is blue

**Saturation**      
Saturation is a percentage value; 0% means a shade of gray and 100% is the full of color/

**Lightness**       
Lightness is also a percentage; 0% is black, 100% is white.

## CSS ::before Selector
The `::before` selector inserts something before the content of each selected element(s).

## CSS radial-gradient()
The `radial-gradient()` CSS function creates an image consisting of a progressive transition between two or more colors that radiate from an origin. The shape maybe a circle or an ellipse.        

```
radial-gradient(
  [ [ circle || <length> ]                         [ at <position> ]? , |
    [ ellipse || [ <length> | <percentage> ]{2} ]  [ at <position> ]? , |
    [ [ circle | ellipse ] || <extent-keyword> ]   [ at <position> ]? , |
    at <position> ,
  ]?
  <color-stop> [ , <color-stop> ]+
)
where <extent-keyword> = closest-corner | closest-side | farthest-corner | farthest-side
  and <color-stop>     = <color> [ <percentage> | <length> ]? 
```     
*Keyword*       
[`<position>`](#CSS-data-type:`<position>`)        



[More detail](https://developer.mozilla.org/en-US/docs/Web/CSS/radial-gradient)

## CSS data type:`<position>`
The `<position>` CSS data type denotes a two-dimensional coordinate used to set a location relative to an element box. It is used in the `background-position` property.        
**Syntax**      
The `<position>` data type is specified with one or two keywords, with optional offsets.        
The keywords values are `center`, `top`, `right`, `bottom` and `left`. Each keyword represents either an edge of the element's box or the center line between two edges. Depending on the context, `center` represents either the center between the left and right edges, or the center between the top and bottom edges.      
If specified, an offset can be either a relative `<percentage>`, or an absolute `<length>` value.       

If only a single offset value is specified, it defines the xcoordinate, with the value for the other axis defaulting to `center`.

```
/* 1-value syntax */
keyword                  /* Either the horizontal or vertical position; the other axis defaults to center */
value                    /* The position on the x-axis; the y-axis defaults to 50% */

/* 2-value syntax */
keyword keyword          /* A keyword for each direction (the order is irrelevant) */
keyword value            /* A keyword for horizontal position, value for vertical position */
value keyword            /* A value for horizontal position, keyword for vertical position */
value value              /* A value for each direction (horizontal then vertical) */

/* 4-value syntax */
keyword value keyword value /* Each value is an offset from the keyword that preceeds it */
```