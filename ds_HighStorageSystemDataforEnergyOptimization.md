## High Storage System Data for Energy Optimization

### Description
The high storage system consists of 4 short conveyor belts (BLO, BHL, BHR, BRU) and 2 rails (HR, HL). The two conveyor belts in the middle (BHL, BHR) can be moved in the vertical by the rails, the other ones are fixed and they all have a size of 64cm x 8.5cm x 29.7cm. Each conveyor belt has three induction sensors. The first one is 3.6cm from the left edge, the second one 26.6 cm from the left edge and the last sensor is 3.6cm from the right edge.

It uses a SPS with Codesys V3, which corresponds to IEC61131-Standard.

The high storage system transports one package between two spots, as you can see in this Video. The first run is the non-optimized run. The two conveyor belts in the middle are only moving vertical when they do not move the package horizontal. The second run is the optimized run. While the two conveyor belts in the middle are moving the package horizontal, they move vertical as well.

The generated data is split in four files. HRSS_normal_standard.csv contains normal runs without failures and not optimized.

HRSS_normal_optimized.csv containes optimized runs without failures.

HRSS_anomalous_standard.csv contains runs with failures and not optimized.

And HRSS_anomalous_optimized.csv contains optimized runs with failures.

The Label column in each file marks the rows with anomalies. With these files you can test energy based optimization processes by using the normal non-optimized and normal optimized files.
Furthermore you can test anomaly detection with the normal and anomaly files.

### Link to repository with data
[Kaggle](https://www.kaggle.com/datasets/inIT-OWL/high-storage-system-data-for-energy-optimization)

### Published Papers

| Title    | Authors       | Year |
|:-|:-|:-|
|[Using Self-Organizing Maps to Learn Hybrid Timed Automata in Absence of Discrete Events](https://www.hs-owl.de/init/veroeffentlichungen/publikationen/a/filteroff/3054/single.html) | Birgelen et al. | 2017 |
|[Enable learning of Hybrid Timed Automata in Absence of Discrete Events through Self-Organizing Maps](https://www.hs-owl.de/init/veroeffentlichungen/publikationen/a/filteroff/3369/single.html) | Birgelen et al. | 2018 |
|[A Novel Anomaly Detection Algorithm for Hybrid Production Systems based on Deep Learning and Timed Automata](https://www.hs-owl.de/init/veroeffentlichungen/publikationen/a/filteroff/2881/single.html) | Hranisavljevic et al. | 2016 |

### Contact
-
