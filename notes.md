## Link
[CSS HSL](#css-hsl)     
[CSS ::before Selector](#css-before-selector)     
[CSS radial-gradient()](#css-radial-gradient)     
[CSS data type: `<position>`](#css-data-typeposition)        
[CSS z-index](#z-index)     
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

## z-index
The `z-index` CSS property specifies the z-order of a positioned element and its descendants or flex items. When elemts overlap, z-order determines whic hone covers the other.     
An element with a **larger** z-index generally **covers** an element with a lower one. [More detail](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index)      

## box-shadow
The `box-shadow` CSS property s used to add shadow effects around an element's frame. Multiple effects can be specified by using comma in between. A box shadow is described by X and Y offsets relative to the element, blur and spread radii, and color.
### Syntax
```CSS
/* offset-x | offset-y | color */
box-shadow: 60px -16px teal;

/* offset-x | offset-y | blur-radius | color */
box-shadow: 10px 5px 5px black;

/* offset-x | offset-y | blur-radius | spread-radius | color */
box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2);

/* inset | offset-x | offset-y | color */
box-shadow: inset 5em 1em gold;

/* Any number of shadows, separated by commas */
box-shadow: 3px 3px red, -1em 0 0.4em olive;

/* Global keywords */
box-shadow: inherit;
box-shadow: initial;
box-shadow: unset;
```      
Specify a single box-shadow using:
- Two, three, or four `<length>` values.    
  - If only two values are given, they are interpreted as [`<offset-x><offset-y>`](#offset-x-offset-y) values.
  -If a third value is given, it is interpreted as a [`<blur-radius>`](#blur-radius).
  -If a fourth value is given, it is interpreted as a [`<spread-radius>`](#spread-radius).
- Optionally, the [`inset`](#inset) keyword.
- Optionally, a `<color>` value.

### Values
#### `inset`
If not specified (default), the shadow is assumed to be a drop shadow (as if the box were raised above the content).
The presence of the inset keyword changes the shadow to one inside the frame (as if the content was depressed inside the box). Inset shadows are drawn inside the border (even transparent ones), above the background, but below content.
#### `<offset-x> <offset-y>`
`<offset-x>` specifies the **horizontal** distance. Negative values place the shadow to the left of the element.    
`<offset-y>` specifies the **vertical** distance. Negative values place the shadow above the element.   
If both values are `0`, the shadow is placed behind the element (and may generate a blue effect if [`<blur-radius>`](#blur-radius) and/or  [`<spread-radius>`](#spread-radius) is set).
#### `<blur-radius>`
This is a third `<length>`. The larger this value, the bigger the blur, so the shadow becomes bigger and lighter. Negative values are not allowed. If not specified, it will be `0` (the shadow's edge is sharp). 
#### `<spread-radius>`
This is a forth `<length>` value. Positive will cause the shadow to expand and grow bigger, negative values will cause the shadow to shrink. If not specified, it will be `0`(the shadow will be the same size as the element).
