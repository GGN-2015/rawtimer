# rawtimer
a simple timer manager.

GitHub repo: [https://github.com/GGN-2015/rawtimer](https://github.com/GGN-2015/rawtimer)

## Installation
```bash
pip install rawtimer
```

## Usage
```python
import rawtimer
import time

rawtimer.begin_timer("timer_name_1")
time.sleep(2.0)                    # Do something that you want to time
rawtimer.end_timer("timer_name_1") # this will output a line into stdout

# means do not output to show time cost
with rawtimer.timer_silent(): 
    rawtimer.begin_timer("timer_name_1")
    time.sleep(2.0)
    time_cost = rawtimer.end_timer("timer_name_1") # silent
    print(f"time_cost: {time_cost:13.3f}s")        # you can output yourself
```
