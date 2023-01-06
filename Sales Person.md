**Sales Person**

```mysql
select name
from SalesPerson
where sales_id not in (select S.sales_id from ((SalesPerson S Join Orders O on S.sales_id=O.sales_id) Join Company C on C.com_id=O.com_id)
where C.name = 'RED');
```

