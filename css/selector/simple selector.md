# CSS SELECTOR

### element selector
``` css
        p{
            color:red;
        }  
```

### class selector
``` css
    .className{
        color: red;
    }
```

### id selector
``` css
    #name{
        color:red;
    }
```

### combinator selector
``` css
    /* select <p> elements which have the "name" id */
    p#name{
        color:red;
    }
    
    /* select <p> elements which have the "className" class */
    p.className{
        color:red;
    }
```

## Which selector is more powerful?

inline style(not recommended) > id selector > class selector > element selector
