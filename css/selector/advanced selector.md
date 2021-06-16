# advanced selector 

```css
/*select all the child li element under the ul element*/
ul li{
    color: red;
}

/*select all the direct child li element under the ul element*/
ul > li{
    color: red;
}

/*select the li element which follow the ul element*/
ul + li{
    color: red;
}

/*select the sibling li element which follow the ul element*/
ul ~ li{
    color: red;
}
```