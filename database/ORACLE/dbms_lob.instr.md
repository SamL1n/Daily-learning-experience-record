# dbms_lob.instr

This function is used to blob search.

`syntax`
```sql
select *
from table1
where dbms_lob.instr (t1, -- the blob 
                   utl_raw.cast_to_raw ('foo'), -- the search string cast to raw 
                   1, -- where to start. i.e. offset 
                   1 -- Which occurrance i.e. 1=first 
                    ) > 0 -- location of occurrence. Here I don't care.  Just find any 
;
```