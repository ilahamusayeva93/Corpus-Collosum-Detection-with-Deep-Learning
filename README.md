### Brain MRI Datasets

This project utilizes two prominent brain MRI datasets, each serving distinct purposes in neuroimaging research. The datasets, namely OASIS and CC-ABIDE, contribute valuable resources for understanding brain structures and abnormalities.

### OASIS Dataset

The **OASIS (Open Access Series of Imaging Studies)** dataset is a comprehensive collection of neuroimaging data provided by Washington University in St. Louis, funded by the National Institute on Aging. This dataset includes various MRI modalities, such as T1-weighted, T2-weighted, and proton density images, along with corresponding demographic information.

- **Access Link:** [OASIS Dataset](https://www.oasis-brains.org/)

### CC-ABIDE Dataset

The **CC-ABIDE (Corpus Callosum in Autism Brain Imaging Data Exchange)** dataset is a specialized collection within the larger ABIDE initiative, focusing on the corpus callosum region. ABIDE itself aims to facilitate research on autism spectrum disorders through the sharing of brain imaging data.

- **Access Link:** [CC-ABIDE Dataset](https://sites.google.com/site/hpardoe/cc_abide)

### Dataset Usage in the Project

#### Data Organization:

- Both OASIS and CC-ABIDE datasets are used in the project.
- Images are organized into specific folders, differentiating between corpus callosum and brain MRI images.

#### Preprocessing and Labeling:

- Images undergo preprocessing steps, including resizing and normalization.
- Bounding box coordinates of the corpus callosum are detected and labeled following the YOLO format.

#### Model Configuration and Training:

- A YOLO model is configured and trained using the labeled datasets.
- The configuration includes parameters such as dataset paths, image size, batch size, and model architecture details.

### Project Workflow

#### Data Extraction:

- Zip files (abide_imgs.zip and oasis_imgs.zip) are extracted to obtain the raw MRI images.

#### Data Organization:

- Images are categorized based on filenames into "corpus callosum" and "brain MRI" folders.

#### Image Processing Functions:

- Functions for image visualization, resizing, and corpus callosum detection are implemented.

#### Dataset Organization:

- Both datasets are organized into specific folders (/content/organized_abide and /content/organized_oasis).

#### Label Generation:

- Bounding box coordinates of the corpus callosum are normalized and stored in text files.

#### Data Analysis and Validation:

- The script provides insights into the length and content of organized datasets for quality checks.

#### YOLO Model Configuration and Training:

- A YAML configuration file (yolov5_config.yaml) is created for model training.
- The YOLOv8n model is configured and trained using the specified parameters.

### Conclusion

By leveraging these diverse brain MRI datasets, the project aims to develop an effective pipeline for corpus callosum detection, contributing to advancements in neuroimaging and autism research. Researchers and practitioners can utilize the provided resources to access and explore these valuable datasets.






### For Second Part of the Code
#### Datasets Preprocessing
The provided code processes raw images from two datasets, "abide_dataset" and "oasis_dataset." It converts tiff images to numpy arrays, resizes them to a specified dimension (128x128), and creates corresponding full and segmented image arrays. The processed datasets are then saved as "all.pkl" for further use.

#### Train-Validation-Test Split
The dataset is split into training, validation, and test sets. The training set constitutes 70% of the data, the validation set 10%, and the test set 20%. The resulting splits are saved as "train-and-val.pkl" and "test.pkl," respectively.

#### Data Augmentation
A data augmentation step involves translation and rotation of images to enhance the dataset. Translation is applied in both x and y directions, and rotation is performed at various angles. The augmented dataset is saved for training.

#### Preprocessing and Normalization
Prior to training, the mean and standard deviation of pixel values across all full images are calculated. The full images in all sets (train, validation, and test) are then normalized using these statistics.

#### Model Architecture
The deep learning model is a convolutional neural network (CNN) for image segmentation. It consists of multiple convolutional and pooling layers, followed by upsampling and concatenation layers. The model employs dropout and batch normalization for regularization.

#### Loss Function and Training
The model uses a custom dice coefficient loss function for training. It is trained for 1000 epochs with a batch size of 32 and an Adam optimizer. Model checkpoints and CSV logging are utilized during training.

#### Evaluation and Results
The model's performance is evaluated using the test set, and the results are visualized. The test accuracy and additional metrics are reported, and a grid of original images, ground truth, and predicted results is plotted for qualitative assessment.

### File Structure
- `abide_dataset/` and `oasis_dataset/`: Raw image datasets
- `all.pkl`: Processed dataset
- `train-and-val.pkl`: Train and validation sets
- `test.pkl`: Test set
- `train-augmented-{index}.pkl`: Augmented training sets
- `saved_model_filename`: Model checkpoints
- `csv_logger_training`: CSV log file
- `result_imgs_folder`: Folder for saving result images

### Execution
1. Run the dataset preprocessing code.
2. Execute the train-validation-test split and save datasets.
3. Perform data augmentation and save augmented training sets.
4. Normalize datasets using the mean and standard deviation.
5. Set up the model architecture and training parameters.
6. Train the model and save checkpoints.
7. Evaluate the model on the test set and visualize results.

Note: Adjust file paths as needed for your environment.














