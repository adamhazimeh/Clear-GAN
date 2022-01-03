# Clear-GAN

A PyTorch implementation of Clear-GAN, a deep learning approach for cloud removal in satellite imagery. Clear-GAN relies on a CycleGAN architecture (as proposed in [[1]](#1)) and is a variation of the model used in Cloud-GAN [[2]](#2). 

A CycleGAN architecture was implemented as it eliminates the constraint of training on a paired dataset (cloudy/cloudless images of the same geographical location on the same day).

In addition to RGB input channels, Clear-GAN uses a Near-Infrared (NIR) input channel as NIR displays partial cloud penetration abilities. The addition of an NIR input channel may help Clear-GAN reveal more low-level landscape features and ultimately enhance the quality of the output image.

The included Jupyter Notebook contains the detailed implementation of Clear-GAN and automatically downloads a custom-collected dataset. The model was trained for 70 epochs (at least 100-200 epochs are required for satisfactory results; could not train for longer due to time and computational constraints).

For more details regarding the project, refer to the PDF report and comments written in the Jupyter Notebook included in this repo.

## References
<a id="1">[1]</a>
Zhu, Jun-Yan & Park, Taesung & Isola, Phillip & Efros, Alexei. (2017). Unpaired Image-to-Image Translation Using Cycle-Consistent Adversarial Networks. 2242-2251. 10.1109/ICCV.2017.244.

<a id="2">[2]</a>
Singh, Praveer & Komodakis, Nikos. (2018). Cloud-Gan: Cloud Re- moval for Sentinel-2 Imagery Using a Cyclic Consistent Generative Adversarial Networks. 1772-1775. 10.1109/IGARSS.2018.8519033.

Note: This project's CycleGAN implementation relied heavily on that contributed by GitHub user Lornatang (https://github.com/Lornatang/CycleGAN-PyTorch).
