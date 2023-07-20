# Medical Instrument Segmentation
Segmentation of surgical devices on Synthetic MICCAI dataset. The goal is to segment surgical instruments defined by input images and masks ("ground_truth"). To solve my task I used U-Net convolutional neural network architecture.

Synthetic MICCAI example images:
| ![Picture4](https://github.com/BenceBiricz/Medical_Instrument_Segmentation/assets/71565433/8d2d592d-9d1b-4638-9fc7-111adfdf4ec9) | ![Picture3](https://github.com/BenceBiricz/Medical_Instrument_Segmentation/assets/71565433/c4c3dfa2-b84f-4354-982a-50a1cad7ce9d) | ![Picture2](https://github.com/BenceBiricz/Medical_Instrument_Segmentation/assets/71565433/cb437cd6-0cc3-4dd7-81f3-3b65d5376b2f) |
| --- | ---| --- |

Masks in the data series:
| ![Picture7](https://github.com/BenceBiricz/Medical_Instrument_Segmentation/assets/71565433/49e37c1a-3675-4b2d-83cd-073f28c032fe) | ![Picture6](https://github.com/BenceBiricz/Medical_Instrument_Segmentation/assets/71565433/bf252112-2076-471e-9845-3b1015673ae2) | ![Picture5](https://github.com/BenceBiricz/Medical_Instrument_Segmentation/assets/71565433/279e5aa3-70d5-43a1-9222-2c9a88999225) |
| --- | ---| --- |

# Theoretical background
U-NET is a convolutional network architecture for fast and accurate image segmentation. It implements a semantic segmentation technique and is often used in medical imaging.

![Picture8](https://github.com/BenceBiricz/Medical_Instrument_Segmentation/assets/71565433/f4df9fdb-c7dc-4dd2-904f-c7d8267bdc45)

# Input data processing
The dataset contains 14 different videos, each divided into 300 frames. So, 4200 input frames and 4200 masks were used in the training.
These were saved in a numpy array after normalization.

![Picture9](https://github.com/BenceBiricz/Medical_Instrument_Segmentation/assets/71565433/40212a5d-e1e6-4a7c-ba5a-64d6326c1102)

# Teaching
During the teaching I tried different optimizers and loss functions to get the best result.
Optimizer:
- RMSprop 
- SGD
- Adam - chosen
- Adadelta
- Adagrad
- RMSpropNadam
- Ftrl
Loss function:
- binary_crossentropy - arbitration
- categorical_crossentropy
- sparse_categorical_crossentropy
- mean_squared_error

![Picture10](https://github.com/BenceBiricz/Medical_Instrument_Segmentation/assets/71565433/c6a3778f-f72e-437c-9300-bb19f2d8ce07)

# The results of teaching

 ![Picture11](https://github.com/BenceBiricz/Medical_Instrument_Segmentation/assets/71565433/638f4d6f-72b4-47d6-aefc-dfa6e0929448)

| ![Picture12](https://github.com/BenceBiricz/Medical_Instrument_Segmentation/assets/71565433/01e8730d-58ce-4989-a896-714e2e695e5f) | ![Picture13](https://github.com/BenceBiricz/Medical_Instrument_Segmentation/assets/71565433/2be9f2fc-1cf8-4bdb-b7a6-d641fe0ec028) |
| --- | --- |






