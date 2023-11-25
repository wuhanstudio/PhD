# Week 7

> 2023/11/06 - 2023/11/12

## High Order Tracking Accuracy (HOTA)

|                         | KITTI |                         CARLA      |
| :---------------------- | :---: | :---------------------------------------------------: |
|Dataset (Ground Truth)  |   [x](https://www.cvlibs.net/datasets/kitti/eval_tracking.php)   |           [x](https://github.com/wuhanstudio/carla-tracking-dataset)  |
|Tracking (Model Output) |   [x](https://github.com/wuhanstudio/2d-kitti-tracking)    | [x](https://github.com/wuhanstudio/2d-carla-tracking) |
|Evaluation              |   x   |                           x       |
|Attack                  |       |                                                       |

<br />

|         HOTA               |    KITTI   |     CARLA      |
| :------------------------- | :--------: | :------------: |
|Ground Truth                |   100.00   |    100.00      |
|Ground Truth (OC SORT)      |   93.84    |     92.93      |
|Ground Truth (Strong SORT)  |   93.72    |     91.19      |
|Ground Truth (Deep SORT)    |   85.55    |     82.49      |
|Ground Truth (SORT)         |   84.62    |     82.11      |
|     **3D Lidar**           |            |                |
|PermaTrack (OC-SORT)        |   76.50    |      -         |
|   **Stereo Camera**        |            |                |
|  CWIT                      |   66.31    |      -         |
|   **Single Camera**        |            |                |
|YOLOX (OC SORT)             |   53.78    |     60.40      |
|YOLOX (Strong SORT)         |   54.30    |     59.60      |
|YOLOX (Deep SORT)           |   52.82    |     56.97      |
|YOLOX (SORT)                |   51.32    |     57.01      |
|         &nbsp;             |            |                |
|YOLO (OC SORT)              |   53.38    |     57.99      |
|YOLO (Strong SORT)          |   55.17    |     59.49      |
|YOLO (Deep SORT)            |   51.99    |     56.65      |
|YOLO (SORT)                 |   50.63    |     56.31      |
