# Universal Adversarial Perturbations

> 2023/10/23 - 2023/10/29

## High Order Tracking Accuracy (HOTA)

|                         | KITTI |                         CARLA      |
| :---------------------- | :---: | :---------------------------------------------------: |
|Dataset (Ground Truth)  |   [x](https://www.cvlibs.net/datasets/kitti/eval_tracking.php)   |           [x](https://github.com/wuhanstudio/carla-tracking-dataset)  |
|Tracking (Model Output) |   [x](https://github.com/wuhanstudio/2d-kitti-tracking)    | [x](https://github.com/wuhanstudio/2d-carla-tracking) |
|Evaluation              |   x   |                           x       |
|Attack                  |       |                                                       |

<br />

|         HOTA                | KITTI |                         CARLA      |
| :---------------------- | :---: | :---------------------------------------------------: |
|Ground Truth  |   100.00   |    100.00         |
|Ground Truth (Strong SORT)  |  93.72    |     89.32           |
|Ground Truth (Deep SORT)  |   85.55  |     82.70      |
|Ground Truth (SORT) |  84.62     |  84.07  |
| **CWIT** |  **66.31**     |  -   |
|YOLO (Strong SORT)  |  55.17  |     42.59          |
|YOLO (Deep SORT)  |   51.99   |    41.48       |
|YOLO (SORT) |    50.63   |    40.50    |
