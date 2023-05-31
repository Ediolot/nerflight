# NerfLight [CVPR 2023]: Fast and Light Neural Radiance Fields using a Shared Feature Grid

## Abstract
![pipeline](https://github.com/Ediolot/nerflight/blob/gh-pages/assets/pipeline.png?raw=true)

While original Neural Radiance Fields (NeRF) have shown impressive results in modeling the appearance of a scene with compact MLP architectures, they are not able to achieve real-time rendering. This has been recently addressed by either baking the outputs of NeRF into a data structure or arranging trainable parameters in an explicit feature grid. These strategies, however, significantly increase the memory footprint of the model which prevents their deployment on bandwidth-constrained applications. In this paper, we extend the grid-based approach to achieve real-time view synthesis at more than 150 FPS using a lightweight model. Our main contribution is a novel architecture in which the density field of NeRF-based representations is split into N regions and the density is modeled using N different decoders which reuse the same feature grid. This results in a smaller grid where each feature is located in more than one spatial position, forcing them to learn a compact representation that is valid for different parts of the scene. We further reduce the size of the final model by disposing of the features symmetrically on each region, which favors feature pruning after training while also allowing smooth gradient transitions between neighboring voxels. An exhaustive evaluation demonstrates that our method achieves real-time performance and quality metrics on a pair with state-of-the-art with an improvement of more than 2× in the FPS/MB ratio.

## Citation
```
@InProceedings{
    Rivas-Manzaneque_2023_CVPR,
    author = {Rivas-Manzaneque, Fernando and Sierra-Acosta, Jorge and Penate-Sanchez, Adrian and Moreno-Noguer, Francesc and Ribeiro, Angela},
    title = {NeRFLight: Fast and Light Neural Radiance Fields Using a Shared Feature Grid},
    booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
    month = {June},
    year = {2023},
    pages = {12417-12427}
}
```
