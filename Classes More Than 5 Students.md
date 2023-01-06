**Classes More Than 5 Students**

```mysql
select class 
from Courses
group by class
having count(class)>=5;
```

