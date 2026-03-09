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

```
datetime.time(hour=0, minute=0, second=0, microsecond=0)

two_thirty = dt.time(14, 30)
print(two_thirty)

five_sec_after_8am = dt.time(8,0,5)
print(five_sec_after_8am)


jfk_shot_dt = dt.datetime(1963, 11, 22, 12, 30)
print(jfk_shot_dt)


jfk_shot_t = jfk_shot_dt.time()
print(jfk_shot_t)

time_str = "8:00"
time_dt = dt.datetime.strptime(time_str,"%H:%M")
print(time_dt)

time_t = time_dt.time()
print(time_t)


```

### Comparing times

```
t1 = dt.time(15, 30)
t2 = dt.time(10, 45)

comparison = t1 > t2
print(comparison) // true

times = [
           dt.time(23, 30),
           dt.time(14, 45),
           dt.time(8, 0)
        ]

print(min(times))
print(max(times))
```

### comparing dates
```
dt1 = dt.datetime(2022, 4, 14)
dt2 = dt.datetime(2022, 3, 29)

 timedelta type represents a period of time, compared to the other classes we've seen which represent a specific moment in time.

print(dt1 - dt2)
diff = dt1 - dt2
print(type(diff))

datetime.timedelta(days=0, seconds=0, microseconds=0,
                   milliseconds=0, minutes=0, hours=0, weeks=0)


```

```
two_days = dt.timedelta(2)
print(two_days)

three_weeks = dt.timedelta(weeks=3)
print(three_weeks)

one_hr_ten_mins = dt.timedelta(hours=1, minutes=10)
print(one_hr_ten_mins)

```

add to static times
```
d1 = dt.date(1963, 2, 21)
d1_plus_1wk = d1 + dt.timedelta(weeks=1)
print(d1_plus_1wk) // 1963-02-28
```

```
dt_1 = dt.datetime(1981, 1, 31)
dt_2 = dt.datetime(1984, 6, 28)
dt_3 = dt.datetime(2016, 5, 24)
dt_4 = dt.datetime(2001, 1, 1, 8, 24, 13)

answer_1 = dt_2 - dt_1
answer_2 = dt_3 + dt.timedelta(days=56)
answer_3 = dt_4 - dt.timedelta(seconds=3600)
```

```
length_counts = {
                  dt.timedelta(minutes=15): 21,
                  dt.timedelta(hours=3): 1,
                  dt.timedelta(seconds=45): 15
                }
min_length = min(length_counts)
print(min_length)
```
