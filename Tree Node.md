**Tree Node**

```mysql
select id, case
                when p_id is null then 'Root'
                when id in (Select p_id from Tree group by P_id) then 'Inner'
                else 'Leaf'
                end as type
from Tree;
```

