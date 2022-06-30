## Liersch 506 Lower Thread Rotation

### Description
This repository contains data generated with a Liersch 506 automatic sewing machine equipped with a lower thread sensor system.

The data is split into two numpy arrays, one for normal sewing operations and one for anomalous sewing operations. Each row represents a completed stitching and each column a single stitch.

With the data folder being the active directory, the data files can be loaded using numpy as follows.

```
import numpy as np

normal = np.load('normal-3436x86.npy')
anomalous = np.load('anomalous-206x86.npy')
```

### Link to GitHub repository with data
[Liersch 506 lower thread data set](https://github.com/TuLAUT/ds_sewing_machine_lt)

### Published Papers

| Title    | Authors       | Year |
|:-|:-|:-|
|[Anomaly detection based on time series data from industrial automatic sewing machines](https://ieeexplore.ieee.org/Xplore/home.jsp) | Daniel Vranješ, Oliver Niggemann | 2022 |


### Contact
daniel.vranjes{at}hsu-hh.de
