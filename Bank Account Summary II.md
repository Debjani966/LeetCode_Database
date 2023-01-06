**Bank Account Summary II**

```mysql
select U.name, sum(T.amount)as balance
from Users U
Join Transactions T
on U.account=T.account
group by T.account
Having sum(T.amount)>10000
order by balance desc;
```

