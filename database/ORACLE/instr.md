# instr 

`syntax`
```sql
INSTR( string, substring [, start_position [, th_appearance ] ] )
```

### Parameter

string: the source string to search
substring: the substring to search for in string.
start_position: the position in string where the search will start.If omitted,the position is 1.
                if the position is negative,the INSTR function counts back `start_position` number of 
                characters from the end of the string and then search toward to the beginning.
th_appearance: the nth appearence of the substring.




### Return

If substring  is not found in the string ,it returns 0;