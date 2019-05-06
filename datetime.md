* Parsing non-zero padded timestamps in Python
``` 
datetime.strptime(datestr, "%m/%d/%Y %H:%M") 
```

* Find closest row of DataFrame to given time in Pandas
``` 
dist = abs(up_on_to.start_ts - ts_i)
closest = np.argmin(dist)
print(closest,dist[closest])
```
