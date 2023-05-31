<video width="100%" autoplay controls>
  <source src="https://github.com/Ediolot/nerflight/blob/gh-pages/assets/NeRFLight.mp4?raw=true" type="video/mp4">
Your browser does not support the video tag.
</video>

&nbsp;
## Abstract
![pipeline](https://github.com/Ediolot/nerflight/blob/gh-pages/assets/pipeline.png?raw=true)

<div style="align:justify">
While original Neural Radiance Fields (NeRF) have shown impressive results in modeling the appearance of a scene with compact MLP architectures, they are not able to achieve real-time rendering. This has been recently addressed by either baking the outputs of NeRF into a data structure or arranging trainable parameters in an explicit feature grid. These strategies, however, significantly increase the memory footprint of the model which prevents their deployment on bandwidth-constrained applications. In this paper, we extend the grid-based approach to achieve real-time view synthesis at more than 150 FPS using a lightweight model. Our main contribution is a novel architecture in which the density field of NeRF-based representations is split into N regions and the density is modeled using N different decoders which reuse the same feature grid. This results in a smaller grid where each feature is located in more than one spatial position, forcing them to learn a compact representation that is valid for different parts of the scene. We further reduce the size of the final model by disposing of the features symmetrically on each region, which favors feature pruning after training while also allowing smooth gradient transitions between neighboring voxels. An exhaustive evaluation demonstrates that our method achieves real-time performance and quality metrics on a pair with state-of-the-art with an improvement of more than 2× in the FPS/MB ratio.
</div>


## Results

### FPS/MB Ratio improvement
![ratio-improvement](https://github.com/Ediolot/nerflight/blob/gh-pages/assets/results1.png?raw=true)


*NeRFLight is able to double the FPS/MB ratio of the second best method while obtaining similar quality metrics to state-of-the-art*

### Qualitative results

<video width="100%" poster="https://github.com/Ediolot/nerflight/blob/gh-pages/assets/results3.png?raw=true" autoplay controls>
  <source src="https://github.com/Ediolot/nerflight/blob/gh-pages/assets/NERFCOMPS.mp4?raw=true" type="video/mp4">
Your browser does not support the video tag.
</video>

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
