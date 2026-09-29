## Avionic Main Fuel Pump Simulation and Fault-Diagnosis Benchmark

### Description
In many cyber-physical systems, especially in critical applications such as aeroplanes, data to train anomaly detection and diagnosis algorithms is lacking due to data protection issues and partial observability. This benchmark addresses that lack of data with a high-fidelity, physics-informed co-simulation of a common aircraft main fuel pump system, modelled in MATLAB/Simulink with Simscape Fluids. The model comprises the tank, main pump, bypass, Fuel Metering Unit (FMU), pressure relief valve and injectors, and is driven by a throttle command profile (0–1) representing a typical flight power profile.

The benchmark provides synthetic multivariate time-series data (CSV) of healthy and faulty operation, generated with explicit fault injection of predefined fault scenarios and annotated with health and fault modes at component level. The repository contains the Simulink model (developed in MATLAB R2025a; requires Simulink, Simscape and Simscape Fluids) and the scripts to generate the throttle profile and to run the simulations and write the labelled time series (approx. 12 GB of CSV files). To show the feasibility of the benchmark, the accompanying paper applies an unsupervised Recurrent Variational Autoencoder (RNN-VAE) for anomaly detection and a SOM-VAE for operating mode discretization, trained to separate healthy and faulty conditions.

### Link to GitHub repository with data and simulation model
[Avionic Main Fuel Pump Simulation and Fault-Diagnosis Benchmark](https://github.com/Elix96J/Avionic_Main_Fuel_Pump_Simulation_and_Fault-Diagnosis_Benchmark)

### Published Papers

| Title    | Authors       | Year |
|:-|:-|:-|
|[Avionic Main Fuel Pump Simulation and Fault-Diagnosis Benchmark (IFAC World Congress 2026)](https://arxiv.org/pdf/2604.22869) | Janzen, F. L., Moddemann, L., Diedrich, A., Niggemann, O. | 2026 |
