**Department Highest Salary**

```mysql
select D.name as Department, E.name as Employee, E.salary as Salary
from Employee E Join Department D
on E.departmentId=D.id
where E.salary In 
(select max(salary)
from Employee ee
 where E.departmentId=ee.departmentId
group by departmentId);
```

