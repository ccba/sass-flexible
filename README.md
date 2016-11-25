
# sass-flexible
Provide sass mixins for lib-flexible sulution, and support multiple properties and multiple values for perperty.
Introduction of lib-flexible refres to [lib-flexible](https://github.com/amfe/lib-flexible)

## How to use
  at first, you shoud refer the js on the html page, download from [lib-flexible](https://github.com/amfe/lib-flexible)

### propertiesToRem mixin

  Convert the px to rem for multiple properties and multiple values for perperty.
```css
@include propertiesToRem(".audience-count-info",  (width: 120px, height: 200px, margin:20px 30px 40px 12px)，75)
```
  result:
```css
.audience-count-info{
   width:" 1.6rem";
   height:" 2.66667rem";
   margin:" .26667rem .4rem .53333rem .16rem"
}
```

### pxToRem function

  Convert the px to rem by this function.
```css
.audience-count-info
{
  width:pxToRem(120px);
}
```
  result:
```css
.audience-count-info
{
  width:1.6rem;
}
```

### fontSize mixin

  Generate the font size values base on the dpr.

```css
@include fontSize(36px, "p")
```
  result:
```css
html[data-dpr="1"] p
{
   font-size:18px;
}

html[data-dpr="2"] p{
   font-size:36px;
}

html[data-dpr="3"] p{
  font-size:54px;
}
@media all and (min-d
