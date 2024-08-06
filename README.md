# ResNet-50 Visualization and Transfer Learning

## Sections

- [About](#about)
- [Resnet-50](#resnet)
- [Transfer Learning on ResNet-50](#learn)
- [Finetuned Model](#finetune)
- [Feature Extraction Model](#extraction)

## About <a id="about"></a>

The ResNet-50 Visualization and Transfer Learning project leverages the [CIFAR-10 dataset](https://www.cs.toronto.edu/~kriz/cifar.html) to demonstrate advanced techniques in convolutional neural networks (CNNs). 
This project focuses on visualizing the inner workings of the ResNet-50 model and applying transfer learning for image classification.

- **CIFAR-10 Dataset:** The project utilizes the CIFAR-10 dataset, which consists of 60,000 32x32 color images in 10 different classes. The labels are one-hot encoded to facilitate multi-class classification.

- **Class Filtering:** Initially, the class "ship" is filtered out from the dataset and is later reintroduced through transfer learning.

- **Visualizations:** The project includes two sets of plots for each model:

  - Intermediate Activations: Visualizing intermediate convolutional network outputs, or “intermediate activations” helps in understanding how successive convnet layers transform their input at different stages of the model.
 
  - Covnet Filters: Visualizing filters of the convolutional network reveals the specific visual patterns or concepts each filter is receptive to, offering deeper insights into the model’s internal representations.


## Resnet-50 <a id="resnet"></a>

A ResNet-50 model is employed as the core CNN architecture. This model is renowned for its depth and ability to handle image classification tasks effectively.

| Original Image | Preprocessed Image |
| -------- | ------- |
| <img src="https://github.com/user-attachments/assets/ca52ebd6-86a9-4098-b9f0-eb146f9b5869" /> | <img src="https://github.com/user-attachments/assets/d247756d-6024-49be-890d-aced8bc8741b" /> |

### Intermediate Activations

<img src="https://github.com/user-attachments/assets/1fb97c01-6483-4811-a091-1afe2f55debf" />

<img src="https://github.com/user-attachments/assets/6c0cbf75-735f-462b-913e-c8caf44c3579" />

<img src="https://github.com/user-attachments/assets/6a8da8a5-cd25-477d-b52c-ef2025ec6e3c" />

### Covnet Filters

<img src="https://github.com/user-attachments/assets/9739138e-7832-4282-89d8-0fd905c45f0b" />

<img src="https://github.com/user-attachments/assets/25fb9a0f-f422-40f4-9182-fe3ef47fb5f1" />

<img src="https://github.com/user-attachments/assets/93f0bae1-0b74-4075-8291-a73f0dbdfdac" />


## Transfer Learning on Resnet-50 <a id="learn"></a>

In this section, we focus on applying fine-tuning and feature extraction methods of transfer learning using the ResNet-50 model specifically for the class "ship" from the CIFAR-10 dataset.

| Original Image | Preprocessed Image |
| -------- | ------- |
| <img src="https://github.com/user-attachments/assets/dfc2b371-3145-4a4d-aec8-72cac380bade" /> | <img src="https://github.com/user-attachments/assets/e6144ded-d12e-4085-b319-b11d3b2375af" /> |

## Finetuned Model <a id="finetune"></a>

Fine-tuning involves unfreezing the top layers of the pre-trained ResNet-50 model and jointly training both the newly added layers and the last layers of the original model. 
This allows the model to learn specific features relevant to the class "ship," improving its ability to recognize ships accurately.

### Intermediate Activations

<img src="https://github.com/user-attachments/assets/535bd4f5-969e-4389-be90-e8dc8583a163" />

<img src="https://github.com/user-attachments/assets/734c52f4-d354-4f78-9e97-1b3a986e95e0" />

<img src="https://github.com/user-attachments/assets/7cf882ba-c919-4213-ae52-1cc9e4414aa7" />

### Covnet Filters

<img src="https://github.com/user-attachments/assets/aeeae386-4c19-4a39-b291-fe86e2ff2c54" />

<img src="https://github.com/user-attachments/assets/89c68008-858d-45b6-989d-cc2b92f586ba" />

<img src="https://github.com/user-attachments/assets/a28ee51d-931f-4a22-a841-36a708132605" />


## Feature Extraction Model <a id="extraction"></a>

Feature extraction involves using the pre-trained ResNet-50 model as a fixed feature extractor, where the final classification layer is replaced with a new layer tailored to the class "ship."
By leveraging the feature representations learned by ResNet-50 during pre-training on a large dataset, we can effectively classify ships with high accuracy.

### Intermediate Activations

<img src="https://github.com/user-attachments/assets/b1366fcd-453d-4ca7-a258-4883fdd3aab4" />

<img src="https://github.com/user-attachments/assets/60a3287c-e875-4b68-91d8-de30bddaf1c3" />

<img src="https://github.com/user-attachments/assets/0062ebd0-623a-49f3-973c-cf25f0b9e72e" />

### Covnet Filters

<img src="https://github.com/user-attachments/assets/abaabb4d-da91-4ad2-97ba-536b56a6fe51" />

<img src="https://github.com/user-attachments/assets/766d2f2b-5f68-430b-9ff4-76f4abeeb3a0" />

<img src="https://github.com/user-attachments/assets/1ea17ca5-48aa-4c31-add0-775d13b6bd35" />
