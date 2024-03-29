## CSS exercise

![Alt text](netflix-clone.gif)

### Fixed Top Nav

```
position: fixed;
top: 0;
width: 100%;
```

### Right-Align Links

```
float: right;
```

### z-index property

```
nav {
  position: fixed;
  z-index: 2;
}

.background-image {
  position: relative; // positioned relative to its normal position.
}

.representation{
  position: absolute; // positioned relative to the nearest positioned ancestor
  z-index: 1;
}
```

the stack order of an element (which element should be placed in front of, or behind, the others).

z-index only works on positioned elements (position: absolute, position: relative, position: fixed, or position: sticky) and flex items (elements that are direct children of display: flex elements).

### Scale up the box on hover

- transition: transform 0.3s ease;

  - a transition effect for transformations of an element.
  - It specifies that changes to the 'transform' property should occur smoothly over a duration of 0.3 seconds, with an easing function called ease.
  - commonly used for smoothly animating changes in the size or position of an element.

- transition: opacity 0.3s ease;

  - a transition effect for the opacity of an element.
  - It specifies that changes to the opacity should occur smoothly over a duration of 0.3 seconds, using the ease easing function.
  - often used to create a fading in or out effect when elements appear or disappear.

- transform: scale(1.05);
  - a scaling transformation to an element, making it larger or smaller.
  - It specifies that the element should be scaled to 1.05 times its original size.
  - commonly used to create a subtle zoom-in effect when hovering over an element.

```
<div class="box">
    <img />
    <div class="additional-content">

    </div>
</div>

.box {
  position: relative;
  transition: transform 0.5s ease; /* Set transition effect for transform */
  width: 250px;
  height: 150px;

  margin: 6px;
  overflow: hidden; /* Hide content if overflow */
  border-radius: 3px; /* Set transition effect for transform */
}

.additional-content {
  position: absolute;

  left: 0; /* Position at the left */
  width: 100%;
  height: 100px;

  transition: opacity 0.5s ease; /* Set transition effect for opacity */
  opacity: 0; /* Initially hidden */
}

.box:hover {
  transform: scale(1.5); /* Slightly scale up the box on hover */
  z-index: 1;
  height: 250px;
}

.box:hover .additional-content {
  opacity: 1; /* Show on hover */
}
```

### box shadow

- Horizontal offset
  - how far the shadow should be offset horizontally from the element.
  - Positive values move the shadow to the right, while negative values move it to the left.
- Vertical offset
  - how far the shadow should be offset vertically from the element.
  - Positive values move the shadow downwards, while negative values move it upwards.
- Blur radius
  - the blurriness of the shadow.
  - A higher value creates a more blurred shadow effect.
- Spread radius
  - controls the size of the shadow.
  - Positive values increase the size of the shadow, while negative values decrease it.
- Color
  - This sets the color of the shadow.

```
  box-shadow: 0px 0px 10px black; /* Horizontal, Vertical, blur */
```

The shadow is set to be 0 pixels to the right, 0 pixels down, with a blur radius of 10 pixels, no spread radius and it has a black color.

### -webkit-text-stroke

specifies the width and color of strokes for text characters

```
.number {
  -webkit-text-stroke: 2px grey; /* text border */
}

```

### decrease the gap between number and img and have img positioned above number

- translateX()

  perform the horizontal translation <br>
  Positive values move the element to the right, while negative values move it to the left

- display: inline-block;

  can sit inline with text and other elements, but it also behaves like a block element in that you can set its width, height, margins, and paddings

```
.rank {
  position: relative;
  display: inline-block; /* allows the element to have both inline and block-level properties */

}
.rank .box {
  position: absolute;
  top: 0;
  left: 50%; /* Move the image to the horizontal center */

  transform: translateX(-20%); /* the element is moved 20% to the left relative to the size of the element's parent from its current position */

  margin: 6px; /* adjust the spacing between the number and the image */
}
```

<hr>

### Google Material Icon

https://fonts.google.com/icons

### Image source

[TMDB](https://www.themoviedb.org/)

<hr>

## 🛠️ Troubleshooting

```
remote: error: File netflix-clone-1.gif is 288.89 MB; this exceeds GitHub's file size limit of 100.00 MB
remote: error: GH001: Large files detected. You may want to try Git Large File Storage - https://git-lfs.github.com.
```

Solution: Reduce file size
