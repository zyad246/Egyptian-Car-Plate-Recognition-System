# Egyptian Car Plate Recognition System


## Overview

This project focuses on detecting and extracting text from Egyptian car plate licenses using advanced deep learning models. It consists of three primary stages: training a YOLOv8 model for plate detection, testing the model on new data, and using PaddleOCR to extract text from the detected plates.

## Project Structure

### 1. **Training YOLOv8 Model**
   - **Dataset Preparation**:
     - The dataset is sourced from Roboflow, consisting of annotated images of Egyptian car plates. This dataset is structured in a way that optimizes it for training with YOLOv8.
     - The notebook includes steps to download, preprocess, and organize the data, ensuring that it is ready for model training.
   - **Model Training**:
     - YOLOv8, a state-of-the-art object detection model, is fine-tuned on the prepared dataset. The notebook includes code to configure the model’s hyperparameters, such as learning rate, batch size, and number of epochs.
     - The model is trained using these configurations, and its performance is monitored through key metrics.
   - **Performance Evaluation**:
     - The model’s performance is evaluated using metrics like Mean Average Precision (mAP) at different IoU thresholds. The training process is also visualized through plots that show loss curves, precision, recall, and mAP across epochs.
     - The notebook also generates confusion matrices and other visual tools to understand the model's strengths and weaknesses.

### 2. **Testing YOLOv8 Model**
   - **Loading the Trained Model**:
     - The trained YOLOv8 model is loaded and applied to new test images and videos. This section is crucial for validating the model’s generalization capability on unseen data.
   - **Detection and Cropping**:
     - The model is used to detect car plates in images. Upon detection, the plates are automatically cropped from the images and saved separately for further processing.
     - This process is automated to handle multiple images in batch mode, making it efficient for large datasets.
   - **Visualization and Analysis**:
     - The results of the detection process are visualized in the notebook, with side-by-side comparisons of original images and cropped plates. This helps in quick verification of the model's accuracy in real-world scenarios.
     - The notebook also includes code for saving the detection results, which can be used for further analysis or as inputs to other models (e.g., OCR).

### 3. **Text Extraction using PaddleOCR**
   - **Enhanced Image Processing**:
     - The notebook begins with processing the cropped car plate images to enhance their quality. Techniques such as contrast adjustment, denoising, and resizing are applied to improve the accuracy of OCR.
   - **OCR Implementation**:
     - PaddleOCR, a highly effective tool for text extraction, is used to extract characters from the processed images. The notebook includes steps to set up PaddleOCR and run it on the cropped plates.
   - **Text Processing and Output**:
     - The extracted text is further processed to separate characters and improve readability. This is particularly important for handling Arabic characters and ensuring that they are correctly interpreted.
     - Confidence scores for the extracted text are calculated, allowing for assessment of the OCR’s reliability. The text, along with these scores, is saved for downstream tasks such as database entry or further manual review.

## Results

- The YOLOv8 model achieves robust results on the custom dataset, with detailed performance metrics provided in the notebooks.
- The text extraction process, using PaddleOCR, is fine-tuned to ensure high accuracy, particularly for Arabic text present on Egyptian car plates.

## Acknowledgements

This project was a collaborative effort, and I would like to thank my team members for their invaluable contributions:

- **[Maria Anwar](https://github.com/MariAnwar)   - [LinkedIn](https://www.linkedin.com/in/maria-anwar-/)**
- **[Afnan Fathy](https://github.com/AfnanFathy22) - [LinkedIn](https://www.linkedin.com/in/afnan-fathy-014196229/)**

Your dedication and expertise were crucial to the success of this project.


## Contributing

Feel free to fork this repository, submit issues, and send pull requests. Contributions are welcome!

