
# Mysql Bulk Insert

Bulk-inserts django objects by generating the sql as text and using cursor.execute()


## Example usage:

```python
from mysql_bulk_insert import bulk_insert
objects = [o1,o2,o3,...]
bulk_insert(objects)
```

If you want to inspect the generated sql instead:

```python
bulk_insert(objects, show_sql=True)
```

## limitations

bulk_insert doesn't follow references to other models.
It just outputs the foreign key.
If you have a hierarchy of objects, you need to save each group of objects in the correct order.
(Or submit a patch :) )

bulk_insert only knows about mysql.



Cheers!

