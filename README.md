# Visualization of UniD-Shift on the SemanticKITTI Test Set

This repository presents qualitative results of the **UniD-Shift** model on the **SemanticKITTI** test set (Sequences 11-21). These visualizations demonstrate the model's performance in 3D semantic segmentation across diverse urban and highway driving scenarios.

## 🎥 Test Set Visualizations

The animations below showcase the segmentation inference results. 
**Viewpoint:** Ego-centric 3D point cloud view (First-person perspective from the vehicle).
**Color Legend:** Standard SemanticKITTI color palette.

<div align="center">

| Sequence 11 | Sequence 12 |
| :---: | :---: |
| <img src="./vis_gifs/seq_11.gif" width="100%" alt="Seq 11"> | <img src="./vis_gifs/seq_12.gif" width="100%" alt="Seq 12"> |

| Sequence 13 | Sequence 14 |
| :---: | :---: |
| <img src="./vis_gifs/seq_13.gif" width="100%" alt="Seq 13"> | <img src="./vis_gifs/seq_14.gif" width="100%" alt="Seq 14"> |

| Sequence 15 | Sequence 16 |
| :---: | :---: |
| <img src="./vis_gifs/seq_15.gif" width="100%" alt="Seq 15"> | <img src="./vis_gifs/seq_16.gif" width="100%" alt="Seq 16"> |

| Sequence 17 | Sequence 18 |
| :---: | :---: |
| <img src="./vis_gifs/seq_17.gif" width="100%" alt="Seq 17"> | <img src="./vis_gifs/seq_18.gif" width="100%" alt="Seq 18"> |

| Sequence 19 (Part 1) | Sequence 19 (Part 2) |
| :---: | :---: |
| <img src="./vis_gifs/seq_19_part1.gif" width="100%" alt="Seq 19 p1"> | <img src="./vis_gifs/seq_19_part2.gif" width="100%" alt="Seq 19 p2"> |

| Sequence 20 | Sequence 21 |
| :---: | :---: |
| <img src="./vis_gifs/seq_20.gif" width="100%" alt="Seq 20"> | <img src="./vis_gifs/seq_21.gif" width="100%" alt="Seq 21"> |

</div>

<br>

## 📊 Dataset & Method Details

- **Method**: UniD-Shift
- **Dataset**: [SemanticKITTI](http://www.semantic-kitti.org/) (Test Sequences 11-21)
- **Data Modality**: LiDAR Point Cloud
- **Total Frames**: 20,351 frames
- **Visualization FPS**: 15 FPS

## 🎨 Semantic Classes

The visualizations strictly follow the SemanticKITTI 19-class definition:

| Category | Classes |
| :--- | :--- |
| **Dynamic Objects** | Car, Bicycle, Motorcycle, Truck, Other-vehicle, Person, Bicyclist, Motorcyclist |
| **Static Structures** | Road, Parking, Sidewalk, Other-ground, Building, Fence, Vegetation, Trunk, Terrain, Pole, Traffic-sign |

## 📝 Notes

1.  **Sequence 19 Split**: Due to the sequence length (4,981 frames), Sequence 19 is visualized in two parts for better loading performance.
2.  **Resolution**: Visualizations are rendered at optimized resolution to balance visual fidelity and file size for web viewing.

## 📄 License

These visualizations are based on the SemanticKITTI dataset. Please refer to the [original dataset license](http://www.semantic-kitti.org/) for usage terms.