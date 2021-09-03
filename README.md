# Hazard Detector
The hazard detector analyzes an input distance image, compares it to a calibration matrix and outputs whether it detected a hazard.
This can be used to let a rover stop in case there is an obstacle just in front.

**This is research code, expect that it changes often and any fitness for a particular purpose is disclaimed.**

## Visualizations
The following picture presents the hazard detector's visualization:
![roi_visualization](media/roi_visualization.png?s=50)
Green: Area under consideration, Red: Hazard.

From this, we compute a local traversability map in the rover frame. White pixels depict the detected hazard:
![local_traversability](media/local_traversability.png)

## Library and configuration
This ROCK component makes use of this library: https://github.com/esa-prl/perception-orogen-hazard_detector
This config file lists all available configuration options: https://github.com/esa-prl/bundles-rover/blob/master/config/orogen/hazard_detector::Task.yml

## Publications
If you use this work in an academic context, please cite our publication
["Efficient Autonomous Navigation for Planetary Rovers with Limited Resources"](https://doi.org/10.1002/rob.21981)
since it explains the library, the motivation, and its greater context while also showing field test results.

```
Gerdes, L, Azkarate, M, Sánchez-Ibáñez, JR, Joudrier, L, Perez-del-Pulgar, CJ. Efficient autonomous navigation for planetary rovers with limited resources. J Field Robotics. 2020; 37: 1153: 1153– 1170. https://doi.org/10.1002/rob.21981
```

```
@article{https://doi.org/10.1002/rob.21981,
author = {Gerdes, Levin and Azkarate, Martin and Sánchez-Ibáñez, José Ricardo and Joudrier, Luc and Perez-del-Pulgar, Carlos Jesús},
title = {Efficient autonomous navigation for planetary rovers with limited resources},
journal = {Journal of Field Robotics},
volume = {37},
number = {7},
pages = {1153-1170},
keywords = {autonomy, exploration, perception, planetary robotics, planning},
doi = {https://doi.org/10.1002/rob.21981},
url = {https://onlinelibrary.wiley.com/doi/abs/10.1002/rob.21981},
eprint = {https://onlinelibrary.wiley.com/doi/pdf/10.1002/rob.21981},
abstract = {Abstract Rovers operating on Mars require more and more autonomous features to fulfill their challenging mission requirements. However, the inherent constraints of space systems render the implementation of complex algorithms an expensive and difficult task. In this paper, we propose an architecture for autonomous navigation. Efficient implementations of autonomous features are built on top of the ExoMars path following navigation approach to enhance the safety and traversing capabilities of the rover. These features allow the rover to detect and avoid hazards and perform significantly longer traverses planned by operators on the ground. The efficient navigation approach has been implemented and tested during field test campaigns on a planetary analogue terrain. The experiments evaluated the proposed architecture by autonomously completing several traverses of variable lengths while avoiding hazards. The approach relies only on the optical Localization Cameras stereo bench, a sensor that is found in all current rovers, and potentially allows for computationally inexpensive long-range autonomous navigation in terrains of medium difficulty.},
year = {2020}
}
```
