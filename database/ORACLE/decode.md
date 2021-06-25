# decode

```sql
select decode(USERSNAME,'sam','山姆',
                        'tom','汤姆',
                        'jane','简',
                        'anonymous') as NAME
from USERS 
where 
```

the `decode` functionality is equivalent to `switch case ` in c# 
```c#
    switch(userName)
    {
        case "sam":
            //todo
        break;

        case "tom":
            //todo
        break;

        case "jane":
            //todo
        break;

        default:
            //todo
        break;
    }
```