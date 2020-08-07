# Animation with css

## Transition

```css
.heading {
  color: red;
  font-size: 16px;
  transition: font-size 0.5s ease-in 1s;
}

.heading:hover {
  color: green;
  font-size: 24px;
}
```

parameter order of transition
* transition property: all / css-selector
* transition-duration: time in seconde
* transition-timing-function: ...
* transition-delay: time in seconde


## Animation

```css
.box {
    width: 100px;
    height: 100px;
    background: blue;
    border: 1px solid black;
    animation: grow 1s ease-in 1s 4 alternate both;
}

@keyframes grow {
    from {width: 100px; height: 100px; background: blue;}
    to {width: 10px; height: 10px; background: red;}
}



/*
@keyframes: --name {
  0% { width: 100px; height: 100px;}
  50% { width: 200px; height: 100px;}
  100% { width: 200px; height: 200px;}
}
*/
```



parameter order of animtion
* animation-name: grow;
* animation-duration: 1s;
* animation-timing-function: ease-in;
* animation-delay: 1s;
* animation-iteration-count: 4;
* animation-direction: alternate;
* animation-fill-mode: both;


