# grouping selector

```css
    p{
        color:red;
    }

    h1{
        color:red;
    }

    h2{
        color:red;
    }
```

For the preceding example,all the p,h1,h2 elements have the same style definitions.It's better to group selectors for minimizing the code.

```css
    p,h1,h2{
        color:red;
    }
```