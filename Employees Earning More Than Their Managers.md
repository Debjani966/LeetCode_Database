**Employees Earning More Than Their Managers**

```mysql
select E.name as Employee
from Employee E
where E.salary>(select salary from Employee e2 where E.managerId=e2.id);
```

