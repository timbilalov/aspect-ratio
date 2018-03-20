# Aspect ratio block (updated)

Original aspect-ratio block: https://www.w3schools.com/howto/howto_css_aspect_ratio.asp

It works well unless you have "one-string" content inside it. But sometimes you can't predict your inner content, or you know that will be more than one-two strings of text.

A little update in CSS solve this issue.

## Code

Raw CSS:
```
.g-aspect--upd {
    padding-top: 33.33%; // Need to be the same abs values
    box-sizing: border-box;
}

.g-aspect--upd .g-aspect-inner {
    margin-top: -33.33%; // Need to be the same abs values
}
```

Stylus mixin:
```
aspect-ratio--upd(w, h = w)
    pt = (round((h / w) * 100, 2))%
    padding-top pt

    .g-aspect-inner
        margin-top (- pt)
```


## Demo

https://codepen.io/unfriend/pen/JLKzvg

![Demo screencast](demo.gif?raw=true)


## Warnings

Test carefully in all browsers before use in production.
