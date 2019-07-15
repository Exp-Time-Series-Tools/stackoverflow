# Time Series Normalization with Pandas Numpy Python

* Series from DataFrame
```
  power_sr = power_df.power_w.loc[start_loc:end_loc]
```

* Percentage Change (not useful everytime)
```
  power_sr = power_sr.pct_change()
```

* Log Change
```
power_sr = np.log(power_sr) - np.log(power_sr.shift(1))
```

* StandardScaler, MinMaxScaler (best known)
```
  from sklearn.preprocessing import StandardScaler, MinMaxScaler
  ss = StandardScaler()
  mm = MinMaxScaler()

  power_sr_nm = pd.Series(np.log2(power_sr.values.reshape(-1, 1))[:,0])
  power_sr_nm = pd.Series(ss.fit_transform(power_sr_nm.values.reshape(-1, 1))[:,0])
  power_sr_nm = pd.Series(mm.fit_transform(power_sr_nm.values.reshape(-1, 1))[:,0])
```

# Time Series Matching
```
  from dtw import dtw
```
