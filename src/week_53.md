# Week 4

> 2023/10/16 - 2023/10/22

## High Order Tracking Accuracy (HOTA)

|                         | KITTI |                         CARLA      |
| :---------------------- | :---: | :---------------------------------------------------: |
|Dataset (Ground Truth)  |   [x](https://www.cvlibs.net/datasets/kitti/eval_tracking.php)   |           [-](https://npm3d.fr/kitti-carla)  |
|Tracking (Model Output) |   [x](https://github.com/wuhanstudio/2d-kitti-tracking)    | [x](https://github.com/wuhanstudio/2d-carla-tracking) |
|Evaluation              |   x   |                           -       |
|Attack                  |       |                                                       |

<br />

|         HOTA                | KITTI |                         CARLA      |
| :---------------------- | :---: | :---------------------------------------------------: |
|Ground Truth  |   100.00   |             |
|Ground Truth (Strong SORT)  |  93.72    |                |
|Ground Truth (Deep SORT)  |   85.55  |           |
|Ground Truth (SORT) |  84.62     |   |
| **CWIT** |  **66.31**     |   |
|YOLO (Strong SORT)  |  55.17  |               |
|YOLO (Deep SORT)  |   51.99   |           |
|YOLO (SORT) |    50.63   |   |

## Siamese Tracking (SOT)

![](imgs/sot.gif)

[![](imgs/siamese.jpg)](https://ieeexplore.ieee.org/document/9503425)

[![](imgs/ml-siam-mot2.gif)](https://tech.fusic.co.jp/posts/2021-06-01-ml-siam-mot/)

## Physical Patch

[![](imgs/patch.gif)](https://medium.com/element-ai-research-lab/physical-adversarial-textures-that-fool-visual-object-tracking-3b5413eb8bbe)
