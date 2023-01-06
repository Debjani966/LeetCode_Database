**Combine Two Tables**

```mysql
select P.firstName as firstName, P.lastName as lastName, A.city as city, A.state as state
from Person P 
left join Address A
on P.personId=A.personId;
```

