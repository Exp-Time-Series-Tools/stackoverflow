# find the “elbow point” on an optimization curve with Python

```python
y = [7342.1301373073857, 6881.7109460930769, 6531.1657905495022,  
6356.2255554679778, 6209.8382535595829, 6094.9052166741121, 
5980.0191582610196, 5880.1869867848218, 5779.8957906367368, 
5691.1879324562778, 5617.5153566271356, 5532.2613232619951, 
5467.352265375117, 5395.4493783888756, 5345.3459908298091, 
5290.6769823693812, 5243.5271656371888, 5207.2501206569532, 
5164.9617535255456]

x = range(1, len(y)+1)

from kneed import KneeLocator
kn = KneeLocator(x, y, curve='convex', direction='decreasing')
print(kn.knee)
5

import matplotlib.pyplot as plt
plt.xlabel('number of clusters k')
plt.ylabel('Sum of squared distances')
plt.plot(x, y, 'bx-')
plt.vlines(kn.knee, plt.ylim()[0], plt.ylim()[1], linestyles='dashed')
```

![alt text](https://github.com/timeseries-at-ytg/stackoverflow/raw/master/images/XhP1x.png)

[scr.](https://stackoverflow.com/questions/51762514/find-the-elbow-point-on-an-optimization-curve-with-python)
