* Parsing non-zero padded timestamps in Python [solved]
```py
datetime.strptime(datestr, "%m/%d/%Y %H:%M") 
# OR
arrow.get(datestr,"YYYY-MM-DD H:mm:ss")
```

* Find closest row of DataFrame to given time in Pandas [solved]
```py
dist = abs(up_on_to.start_ts - ts_i)
closest = np.argmin(dist)
print(closest,dist[closest])
```
