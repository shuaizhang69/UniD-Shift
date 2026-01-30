# Visualization of UniD-Shift on the SemanticKITTI Test Set

This repository contains visualizations of the UniD-Shift model predictions on the SemanticKITTI test set (sequences 11-21). The visualizations demonstrate the semantic segmentation performance across different driving scenarios captured in various urban and highway environments.

## Test Set Visualizations

The following animations showcase the model's predictions on all test sequences. Each GIF displays the point cloud semantic segmentation results in a bird's-eye view, with colors representing different semantic classes according to the SemanticKITTI standard color scheme.

<div align="center">

| Sequence 11 | Sequence 12 | Sequence 13 | Sequence 14 |
|:-----------:|:-----------:|:-----------:|:-----------:|
| <img src="./vis_gifs/seq_11.gif" width="240" height="180" alt="Sequence 11"/> | <img src="./vis_gifs/seq_12.gif" width="240" height="180" alt="Sequence 12"/> | <img src="./vis_gifs/seq_13.gif" width="240" height="180" alt="Sequence 13"/> | <img src="./vis_gifs/seq_14.gif" width="240" height="180" alt="Sequence 14"/> |
| **Sequence 15** | **Sequence 16** | **Sequence 17** | **Sequence 18** |
| <img src="./vis_gifs/seq_15.gif" width="240" height="180" alt="Sequence 15"/> | <img src="./vis_gifs/seq_16.gif" width="240" height="180" alt="Sequence 16"/> | <img src="./vis_gifs/seq_17.gif" width="240" height="180" alt="Sequence 17"/> | <img src="./vis_gifs/seq_18.gif" width="240" height="180" alt="Sequence 18"/> |
| **Sequence 19 (Part 1)** | **Sequence 19 (Part 2)** | **Sequence 20** | **Sequence 21** |
| <img src="./vis_gifs/seq_19_part1.gif" width="240" height="180" alt="Sequence 19 Part 1"/> | <img src="./vis_gifs/seq_19_part2.gif" width="240" height="180" alt="Sequence 19 Part 2"/> | <img src="./vis_gifs/seq_20.gif" width="240" height="180" alt="Sequence 20"/> | <img src="./vis_gifs/seq_21.gif" width="240" height="180" alt="Sequence 21"/> |

</div>

## Dataset Information

- **Dataset**: [SemanticKITTI](http://www.semantic-kitti.org/)
- **Test Sequences**: 11-21 (11 sequences, 20,351 frames total)
- **Visualization Format**: Bird's-eye view point cloud with semantic labels
- **Color Scheme**: Standard SemanticKITTI color mapping
- **Frame Rate**: 15 FPS

## Semantic Classes

The visualizations use the standard SemanticKITTI 19-class semantic segmentation labels:

- **Dynamic Objects**: car, bicycle, motorcycle, truck, other-vehicle, person, bicyclist, motorcyclist
- **Static Structures**: road, parking, sidewalk, other-ground, building, fence, vegetation, trunk, terrain, pole, traffic-sign

## Notes

- Sequence 19 is split into two parts due to its large number of frames (4,981 frames)
- All visualizations are rendered at 50% resolution for optimal file size and loading speed
- The bird's-eye view perspective provides a comprehensive overview of the semantic segmentation results


## License

This visualization follows the SemanticKITTI dataset license. Please refer to the original [dataset license](http://www.semantic-kitti.org/) for usage terms.
