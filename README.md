# ceo-reporting
The voice assistant that your CEO will love

![Screenshot](alex1.png)
![Screenshot](alex2.png)
![Screenshot](alex3.png)
![Screenshot](flowww.png)

### Generate Dummy dataset

```python
import pandas as pd
from datetime import datetime
import numpy as np

# create DatetimeIndex
date_rng = pd.date_range(start='1/1/2018', end='9/5/2019', freq='D') # m/d/yyyy

# create dataframe
df = pd.DataFrame(date_rng, columns=['date'])

# create column 'revenue' with random values
df['revenue'] = np.random.randint(3000000,6000000,size=(len(date_rng)))

# create column 'bookings' with random values
df['bookings'] = np.random.randint(10000,20000,size=(len(date_rng)))

# export csv file (you can create the table in BigQuery from pandas dataframe as well)
df.to_csv(<path>)
```
