### README

# Object Detection with YOLOv9-C on TACO Dataset

## Project Overview
This project focuses on the comparative analysis of advanced object detection models applied to the TACO (Trash Annotations in Context) dataset. Our primary goal is to evaluate the effectiveness of different models in detecting waste in natural environments. Among the models tested are DETR, Faster R-CNN, RetinaNet, and YOLOv9, with a specific focus on the fine-tuning and implementation of YOLOv9-C (Compact).

## YOLOv9-C: Fine-Tuning and Implementation
### Introduction
YOLOv9, developed by Ultralytics, represents the latest advancement in real-time object detection, improving upon previous versions (YOLOv3, YOLOv4, etc.). YOLOv9 introduces new techniques such as Programmable Gradient Information (PGI) and Generalized Efficient Layer Aggregation Network (GELAN), which significantly enhance efficiency and accuracy.

### Architecture and Innovations
YOLOv9 maintains the end-to-end approach of its predecessors but optimizes the internal structure to reduce computational complexity and improve performance (mAP). The architecture is based on:
- **Programmable Gradient Information (PGI)**: Designed to address the information bottleneck that occurs during data passage through neural network layers. PGI uses an auxiliary reversible branch to retain key information, ensuring that deep features can maintain essential information for the specific task, resulting in more accurate gradients during backpropagation.
- **Generalized Efficient Layer Aggregation Network (GELAN)**: Aggregates information from multiple convolutional layers, enhancing feature extraction. GELAN's design allows for flexible integration of various computational blocks, making YOLOv9 adaptable to a wide range of applications without sacrificing speed or accuracy.

### Specifics of YOLOv9-C
In this project, we utilized the YOLOv9-C (Compact) variant. YOLOv9-C is a well-balanced version that approaches the accuracy of more powerful models while maintaining a good balance between complexity and performance. With parameters totaling 25.3 million and 102.1 billion floating-point operations (FLOPs), YOLOv9-C is designed to deliver high performance without excessive computational resource requirements. This makes it particularly suitable for applications requiring high precision, such as real-time object detection in industrial or security contexts where hardware resources are sufficient but not unlimited.

### Implementation and Performance
YOLOv9-C was tested and pre-trained on the COCO train2017 dataset, demonstrating superior detection capabilities for both small and large objects due to the combination of PGI and GELAN. This model is ideal for real-time applications where precision and speed are crucial.

## Dataset TACO
### Overview
The TACO (Trash Annotations in Context) dataset is a valuable resource for detecting waste in various environmental contexts. It comprises a diverse collection of images of litter, annotated in different settings, making it highly relevant for testing the generalization and robustness of object detection models.

### Dataset Characteristics
TACO includes images of waste such as plastic, metal, glass, paper, and other materials, captured in environments ranging from beaches and parks to urban areas. The images come with detailed annotations specifying the type and location of the waste, providing a rich dataset for training machine learning algorithms.

### Use in Our Project
For our project, we mapped all annotations to a single "trash" class to focus on detection rather than classification. This approach allows us to evaluate the models' effectiveness in identifying waste in various scenarios, facilitating clean-up and maintenance efforts. Data augmentation techniques were implemented to increase image variety, enhancing the model's ability to generalize to new, unseen images.

### Reasons for Choosing TACO
- **Variety of Images**: The diverse environmental situations and types of waste ensure comprehensive and varied model training.
- **Quality of Annotations**: Precise and detailed annotations are crucial for developing an accurate detection model.
- **Flexibility**: The dataset's structure allowed for easy adaptation to our detection-focused project.
- **Community and Collaboration**: TACO is supported by an active community of researchers and volunteers, ensuring the dataset remains up-to-date and relevant.
- **Documentation and Resources**: Extensive documentation and resources facilitate the integration and use of TACO in research and development projects.

## Conclusion
The fine-tuning of YOLOv9-C on the TACO dataset has demonstrated significant improvements in both accuracy and efficiency for real-time waste detection applications. The combination of advanced techniques such as PGI and GELAN, along with a robust dataset like TACO, makes YOLOv9-C an excellent choice for high-precision, real-time object detection tasks. 

Report Link : https://api.wandb.ai/links/pirati/b69hf7zy