## LayerWatch – A Benchmark for Layer-wise Multi-Class Visual Defect Detection in Fused Filament Fabrication

### Description
LayerWatch is a benchmark for visual defect detection and classification in Fused Filament Fabrication (FFF). Automating this task is challenging because defects can emerge gradually during printing and often only become visible several layers after their physical occurrence, and because their appearance varies substantially with part geometry, material and recording conditions. The benchmark is designed to capture the temporal, multi-class and distribution-shifted nature of real FFF processes. State-of-the-art object detection models are evaluated on it and reported as baselines.

The images are annotated in YOLO format (one label file with bounding boxes per image); file names include a timestamp and the layer index. There are six classes: clogged nozzle, delamination, OK (no defect), layer shift, off platform and warping.

The training dataset consists exclusively of the Benchy geometry (72 print jobs, 288 objects, 22,856 images including offline-generated augmentations). For evaluation, there is one in-distribution validation dataset with previously unseen Benchy objects (1,478 images) and three out-of-distribution validation datasets:

- Pyramid: geometry shift (1,814 images)
- Clamp part, orange: unseen geometry with similar appearance (575 images)
- Clamp part, silver: geometry and appearance shift (209 images)

Training and validation data are strictly separated at the object level. The data are compatible with Ultralytics YOLO and RT-DETR pipelines; the code for training and evaluating the baseline models is available on GitHub.

### Link to Harvard Dataverse record and GitHub repository
- [LayerWatch dataset on Harvard Dataverse](https://doi.org/10.7910/DVN/AWWBAZ)
- [LayerWatch on GitHub (benchmark code, baselines, evaluation)](https://github.com/SEilermann/LayerWatch)

### Published Papers

| Title    | Authors       | Year |
|:-|:-|:-|
|LayerWatch – A Benchmark for Layer-wise Multi-Class Visual Defect Detection in Fused Filament Fabrication | Rieckmann, A., Eilermann, S., Ehrhardt, J., Mayer, M., Meyer, T., Streekmann, N., Niggemann, O. | 2026 |
