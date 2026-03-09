# Conventional


```
visitors_per_month = {}

import datetime as dt 

for row in potus:
    appt_start_date = row[2]
    month_year = appt_start_date.strftime("%B, %Y")
    if month_year not in visitors_per_month:
        visitors_per_month[month_year] = 1
    else:
        visitors_per_month[month_year] += 1
```

## convert string to datetime
```
date_string = '12/18/15 16:30'
date, time = date_string.split()
hr, mn = time.split(':')
mnth, day, yr = date.split('/')

hr = int(hr)
mn = int(mn)
mnth = int(mnth)
day = int(day)
yr = int(yr)

import datetime as dt
date_dt = dt.datetime(yr,mnth,day,hr,mn)

```


```
datetime.strptime(value,format)
datetime.strptime("24/12/1985","%d/%m/%Y")

date_1_str = "24/12/1984"
date_1_dt = dt.datetime.strptime(date_1_str, "%d/%m/%Y")
print(type(date_1_dt))
print(date_1_dt)

date_2_str = "12-24-1984"
date_2_dt = dt.datetime.strptime(date_2_str, "%m-%d-%Y")
print(date_2_dt)
```


```
The calendar module
The time module
The datetime module

The datetime module contains a number of classes, including the following:

import datetime
datetime.datetime: for working with date and time data
datetime.time: for working with time data only
datetime.timedelta: for representing time periods

```

```
datetime.datetime(year, month, day, hour=0, minute=0, second=0)

import datetime as dt
eg_1 = dt.datetime(2000, 1, 1)
print(eg_1)


eg_2 = dt.datetime(1985, 3, 13, 21, 26, 2)
print(eg_2)

eg_3 = dt.datetime(1998, 7, 7, 8, 39)
print(eg_3)


```


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
