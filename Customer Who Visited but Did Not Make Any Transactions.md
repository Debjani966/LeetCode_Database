**Customer Who Visited but Did Not Make Any Transactions**

```mysql
select customer_id, count(customer_id) as count_no_trans
from Visits
where visit_id not in (select visit_id from Transactions)
Group by(customer_id)
order by count(customer_id) desc;
```

