# wait
versatile class for pausing a program until some time in the future

### usage
```
from wait import wait
waiter = Wait()
waiter.wait_til(30)                   # sleep for 30 seconds
waiter.wait_til('23:59:00')           # sleep til 11:59PM
waiter.wait_til('01:15:20:23:59:00')  # sleep til 12AM on Jan 15, 2020

from datetime import datetime, timedelta
today = datetime.today()
tomorrow = today + timedelta(days=1)
tomorrow = tomorrow.replace(hour=12, minute=0, second=0, microsecond=0)
waiter.wait_til(tomorrow)             # sleep til 12PM tomorrow
```

all times passed to wait_til() must be in the future
