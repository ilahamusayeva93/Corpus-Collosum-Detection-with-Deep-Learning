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
