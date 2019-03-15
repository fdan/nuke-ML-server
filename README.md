# Deep Learning Plug-in for Nuke

This repository contains the Client-Server system enabling Deep Learning (DL) inference in Nuke.
The following models are provided as examples:
- blur: a simple gaussian blur operation
- [Mask-RCNN] (https://github.com/facebookresearch/Detectron)
- [DensePose] (https://github.com/facebookresearch/DensePose)

<!-- <div align="center">
  <img src="~/Pictures/DLClient_0.png" width="700px" />
  <p>Example of Nuke doing DensePose inference.</p>
</div> -->

## Introduction

The Deep Learning (DL) plug-in connects Nuke to a Python server to apply DL models to images.
The plug-in works as follows:
- The Nuke node can connect to a server given an ip address and port
- The Python server responds with the list of available Deep Learning (DL) models and options
- The Nuke node displays the models in an enumeration node, from which the user can choose
- On every engine call, the current image and model options are sent from the Nuke node to the server
- The server does an inference on the image using the chosen model/options
This inference can be an actual inference operation of a deep learning model, or just other image processing code
- The resulting image is sent back to the Nuke node

## Installation

Please find installation instruction in [INSTALL.md](INSTALL.md)

## License

The source code is licensed under the license found in the [LICENSE](LICENSE) file in the root directory of this source tree.

## Contact

- Johanna Barbier (Johanna.Barbier@foundry.com)
This plug-in was initially created by Sebastian Lutz (XXX mail?)

## References

- [Mask R-CNN](https://arxiv.org/abs/1703.06870).
  Kaiming He, Georgia Gkioxari, Piotr Dollár, and Ross Girshick.
  IEEE International Conference on Computer Vision (ICCV), 2017.
- [DensePose: Dense Human Pose Estimation In The Wild](https://arxiv.org/abs/1802.00434)
  Riza Alp Güler, Natalia Neverova, Iasonas Kokkinos
  IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2018