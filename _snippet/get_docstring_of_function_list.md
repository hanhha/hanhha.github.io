---
title: "Get docstring of list of functions"
excerpt: "Function list docstring"
tags: ["docstring","code snippet","python","candle sticks pattern"]
use_math: true
---
I need to do quick review the usage of a group of functions. Here is what I've done for list of candle stick pattern regconition of TA-Lib python wrapper.
```python
import talib

pattern_list = talib.get_function_groups()['Pattern Recognition']

with open('pattern_usage.txt', 'w+') as cf:
	for pt in pattern_list:
		func = 'talib. ' + pt
		cf.write ('\n' + eval(func).__doc__)
```
