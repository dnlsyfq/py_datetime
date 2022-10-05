### Calender

```
import calendar

calendar.month(2019,7)

random.randint(int_min,int_max)
random.choice(list_var) // pick value randomly
random.shuffle(list_var) // rearrange list randomly
```

```
from datetime import datetime

current_time = datetime.now()

print(current_time)
```

### datetime

* .strptime()
convert string to a datetime
```
from datetime import datetime
datetime.strptime("06/11/2016","%m/%d/%Y")
```

* .strftime()
convert datetime to string
```
"2014-02-11".strftime('%m/%d/%Y')
```

* .isoformat()
output datetime as iso standard
```
"06/11/2016".isoformat()
```

### time format

```
%d i.e 01,02..31
%m i.e 01,02...12
%Y i.e 0001,2014...2022
```
