# attribute selector 

`syntax`
```css
h1[attr = value]{
    color:red;
}
```

### advanced 
```css
/* get all h1 elements that have "attr" attribute */
h1[attr]{
    color:red;
}

/* get all h1 elements that attr attribute equals value*/
h1[attr = "value"]{
    color:red;
}

/* ^= means the value of attr must start with "value"(not required the whole word),
"value234" "value-dfs" "value ds" all is ok */
h1[attr ^= "value"]{
    color:red;
}

/* $= means the value of attr must end with "value"(not required the whole word),
"fsdvalue" "sda-value"all is ok */
h1[attr $= "value"]{
    color:red;
}

/* *= means the value of attr must contain "value"(not required the whole word),
"sdvaluedfs" is ok */
h1[attr *= "value"]{
    color:red;
}

/* ~= means attr contains the value (the whole word),
"value XXX" "ss value" is ok,
"sdfvalue" "dfs-value" is not ok*/
h1[attr ~= "value"]{
    color:red;
}

/* |= means the value of attr must start with "value"(the whole word,or follow with -),
"value XXX" "value-xxx" is ok,
"valuexxx" "value " is not ok */
h1[attr |= "value"]{
    color:red;
}
```