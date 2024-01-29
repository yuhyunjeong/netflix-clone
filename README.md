## CSS practice

### Fixed Top Nav

```
position: fixed;<br>
top: 0;<br>
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

.play{
  position: absolute; // positioned relative to the nearest positioned ancestor
  z-index: 1;
}
```

the stack order of an element (which element should be placed in front of, or behind, the others).

z-index only works on positioned elements (position: absolute, position: relative, position: fixed, or position: sticky) and flex items (elements that are direct children of display: flex elements).
