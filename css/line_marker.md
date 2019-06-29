参考 : https://gurio.work/marker-animation01/

```css
.sc_marker-animation {
    background-image: -webkit-linear-gradient(left,transparent 50%,rgb(255,247,2) 50%);
    background-image: -moz-linear-gradient(left,transparent 50%,rgb(255,247,2) 50%);
    background-image: -ms-linear-gradient(left,transparent 50%,rgb(255,247,2) 50%);
    background-image: -o-linear-gradient(left,transparent 50%,rgb(255,247,2) 50%);
    background-image: linear-gradient(left,transparent 50%,rgb(255,247,2) 50%);
    background-repeat: repeat-x;
    background-size: 200% .8em;
    background-position: 0 .5em;
    font-weight: bold
}

.sc_marker-animation.active {
    background-position: -100% .4em;
    transition: 2.5s
}
```