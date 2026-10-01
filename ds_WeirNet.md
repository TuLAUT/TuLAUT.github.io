## WeirNet: A Large-Scale 3D CFD Benchmark for Geometric Surrogate Modeling of Piano Key Weirs

### Description
Reliable prediction of hydraulic performance is challenging for Piano Key Weir (PKW) design because discharge capacity depends on three-dimensional geometry and operating conditions. Surrogate models can accelerate hydraulic-structure design, but progress is limited by scarce large, well-documented datasets that jointly capture geometric variation, operating conditions, and functional performance. WeirNet is a large 3D CFD benchmark dataset for geometric surrogate modeling of PKWs.

WeirNet contains 3,794 parametric, feasibility-constrained rectangular and trapezoidal PKW geometries, each scheduled at 19 discharge conditions using a consistent free-surface OpenFOAM workflow, resulting in 71,387 completed simulations that form the benchmark and with complete discharge coefficient labels. The dataset is released in multiple modalities (compact parametric descriptors, watertight surface meshes and high-resolution point clouds) together with standardized tasks and in-distribution and out-of-distribution splits.

Representative surrogate families are benchmarked for discharge coefficient prediction. Tree-based regressors on parametric descriptors achieve the best overall accuracy, while point- and mesh-based models remain competitive and offer parameterization-agnostic inference. All surrogates evaluate in milliseconds per sample, providing orders-of-magnitude speedups over CFD runtimes. Out-of-distribution results identify geometry shift as the dominant failure mode compared to unseen discharge values, and data-efficiency experiments show diminishing returns beyond roughly 60% of the training data. By publicly releasing the dataset together with simulation setups and evaluation pipelines, WeirNet establishes a reproducible framework for data-driven hydraulic modeling and enables faster exploration of PKW designs during the early stages of hydraulic planning.

### Link to Zenodo record
[WeirNet dataset on Zenodo](https://zenodo.org/records/22707711)

### Published Papers

| Title    | Authors       | Year |
|:-|:-|:-|
|[WeirNet: A Large-Scale 3D CFD Benchmark for Geometric Surrogate Modeling of Piano Key Weirs (arXiv preprint)](https://arxiv.org/abs/2602.20714) | Lüddecke, L., Hohmann, M., Eilermann, S., Tillmann-Mumm, J., Pourabdollah, P., Oertel, M., Niggemann, O. | 2026 |
