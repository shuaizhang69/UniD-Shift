# Visualization of UniD-Shift on SemanticKITTI and nuScenes

This repository presents qualitative results of the **UniD-Shift** model on the **SemanticKITTI** test set (Sequences 11-21) and **nuScenes** dataset. These visualizations demonstrate the model's performance in 3D semantic segmentation across diverse urban and highway driving scenarios.

## 磁 SemanticKITTI Test Set Visualizations

The animations below showcase the segmentation inference results. 
**Viewpoint:** Ego-centric 3D point cloud view (First-person perspective from the vehicle).
**Color Legend:** Standard SemanticKITTI color palette.

<div align="center">

| Sequence 11 | Sequence 12 | Sequence 13 |
| :---: | :---: | :---: |
| <img src="./vis_gifs/seq_11.gif" width="100%" alt="Seq 11"> | <img src="./vis_gifs/seq_12.gif" width="100%" alt="Seq 12"> | <img src="./vis_gifs/seq_13.gif" width="100%" alt="Seq 13"> |

| Sequence 14 | Sequence 15 | Sequence 16 |
| :---: | :---: | :---: |
| <img src="./vis_gifs/seq_14.gif" width="100%" alt="Seq 14"> | <img src="./vis_gifs/seq_15.gif" width="100%" alt="Seq 15"> | <img src="./vis_gifs/seq_16.gif" width="100%" alt="Seq 16"> |

| Sequence 17 | Sequence 18 | Sequence 19 (Part 1) |
| :---: | :---: | :---: |
| <img src="./vis_gifs/seq_17.gif" width="100%" alt="Seq 17"> | <img src="./vis_gifs/seq_18.gif" width="100%" alt="Seq 18"> | <img src="./vis_gifs/seq_19_part1.gif" width="100%" alt="Seq 19 p1"> |

| Sequence 19 (Part 2) | Sequence 20 | Sequence 21 |
| :---: | :---: | :---: |
| <img src="./vis_gifs/seq_19_part2.gif" width="100%" alt="Seq 19 p2"> | <img src="./vis_gifs/seq_20.gif" width="100%" alt="Seq 20"> | <img src="./vis_gifs/seq_21.gif" width="100%" alt="Seq 21"> |

</div>

<br>

## 磁 nuScenes Visualizations

The animations below showcase the segmentation inference results on the nuScenes dataset. 
Unlike standard evaluation which typically focuses on annotated keyframes (2Hz), these visualizations are generated from **12 selected scenes** comprising both **Test Set keyframes and their corresponding intermediate "dropped" frames (sweeps)**. This dense inference (20Hz) demonstrates the model's stability and temporal consistency.

**Viewpoint:** Ego-centric 3D point cloud view.
**Color Legend:** Standard nuScenes color palette.

<div align="center">

| Scene 0088 | Scene 0485 | Scene 0487 |
| :---: | :---: | :---: |
| <img src="./vis_gifs/scene-0088.gif" width="100%" alt="Scene 0088"> | <img src="./vis_gifs/scene-0485.gif" width="100%" alt="Scene 0485"> | <img src="./vis_gifs/scene-0487.gif" width="100%" alt="Scene 0487"> |

| Scene 0489 | Scene 0496 | Scene 0549 |
| :---: | :---: | :---: |
| <img src="./vis_gifs/scene-0489.gif" width="100%" alt="Scene 0489"> | <img src="./vis_gifs/scene-0496.gif" width="100%" alt="Scene 0496"> | <img src="./vis_gifs/scene-0549.gif" width="100%" alt="Scene 0549"> |

| Scene 0551 | Scene 0601 | Scene 0612 |
| :---: | :---: | :---: |
| <img src="./vis_gifs/scene-0551.gif" width="100%" alt="Scene 0551"> | <img src="./vis_gifs/scene-0601.gif" width="100%" alt="Scene 0601"> | <img src="./vis_gifs/scene-0612.gif" width="100%" alt="Scene 0612"> |

| Scene 0621 | Scene 0829 | Scene 0830 |
| :---: | :---: | :---: |
| <img src="./vis_gifs/scene-0621.gif" width="100%" alt="Scene 0621"> | <img src="./vis_gifs/scene-0829.gif" width="100%" alt="Scene 0829"> | <img src="./vis_gifs/scene-0830.gif" width="100%" alt="Scene 0830"> |

</div>

<br>

## 投 Dataset & Method Details

- **Method**: UniD-Shift
- **Datasets**: 
  - [SemanticKITTI](http://www.semantic-kitti.org/) (Test Sequences 11-21)
  - [nuScenes](https://www.nuscenes.org/) (12 selected scenes, full sweep reconstruction)
- **Data Modality**: 
  - SemanticKITTI: 64-beam LiDAR
  - nuScenes: 32-beam LiDAR
- **Inference Scope**:
  - **SemanticKITTI**: Standard test set sequences.
  - **nuScenes**: Dense inference including non-annotated sweeps (approx. 20Hz) to visualize continuous motion, derived from the Test Set split.
- **Visualization FPS**: 15 FPS

## 耳 Semantic Classes

### SemanticKITTI (19 Classes)

| Category | Classes |
| :--- | :--- |
| **Dynamic Objects** | Car, Bicycle, Motorcycle, Truck, Other-vehicle, Person, Bicyclist, Motorcyclist |
| **Static Structures** | Road, Parking, Sidewalk, Other-ground, Building, Fence, Vegetation, Trunk, Terrain, Pole, Traffic-sign |

### nuScenes (16 Classes)

The nuScenes visualizations follow the official **LiDARSeg** 16-class definition:

| Category | Classes |
| :--- | :--- |
| **Dynamic Objects** | Car, Truck, Bus, Trailer, Construction-vehicle, Pedestrian, Motorcycle, Bicycle, Barrier, Traffic-cone |
| **Static Structures** | Driveable-surface, Sidewalk, Terrain, Manmade, Vegetation, Other-flat |

## 統 Notes

1.  **Sequence 19 Split**: Due to the sequence length (4,981 frames), Sequence 19 is visualized in two parts for better loading performance.
2.  **nuScenes Density**: Visualizations use image dilation techniques to enhance the visibility of the sparse 32-beam LiDAR points for better qualitative analysis.
3.  **Resolution**: Visualizations are rendered at optimized resolution to balance visual fidelity and file size for web viewing.

## 塘 License

These visualizations are based on the SemanticKITTI and nuScenes datasets. Please refer to the original dataset licenses for usage terms:
- [SemanticKITTI License](http://www.semantic-kitti.org/)
- [nuScenes License](https://www.nuscenes.org/terms-of-use)
