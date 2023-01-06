**Capital Gain/Loss**

```mysql
select stock_name, Sum(case
                            when operation='Buy' then -price
                            when operation='Sell' then price
                            else 0
                   end) As capital_gain_loss  
from Stocks
group by stock_name;
```

