# CE 7454 Project 1 Report: CelebAMask-HQ Face Parsing

This repository contains the implementation of several deep learning models for semantic segmentation, including the SegFormer model. The models were implemented using PyTorch, and Jupyter Notebooks (`.ipynb`) were used for code execution and analysis. All files and necessary scripts are provided to reproduce the results and experiments described in the project.

**The best result and all corresponding files are in the SegFormer folder**

## Prerequisites

To run the code, follow these steps:

1. **Set up a virtual environment:**

    ```bash
    python3 -m venv env
    source env/bin/activate
    ```

2. **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

The `requirements.txt` file contains all third-party libraries needed for the project.

## Running the Code

Once the environment is set up and dependencies are installed, you can use VSCode or any other Jupyter Notebook-compatible IDE. Follow these steps:

1. **Select the installed kernel** to execute the code in Jupyter Notebooks.
2. Each `.ipynb` file corresponds to a different model. The models are well-commented (some comments generated using LLMs), so you can easily run the code and see the results.
3. The following GPU requirements apply:
   - **SegFormer model** requires at least **20 GiB** of GPU RAM.
   - **Other models** require less than **12 GiB** of GPU RAM.

### Adjusting Hyperparameters

All hyperparameters are hard-coded into the model for simplicity and transparency. However, you are free to adjust them manually within the notebook if needed.

### Re-running Predictions

To regenerate the predicted masks:
1. Copy the corresponding model weights (provided in the subfolder of each model) into the same directory as the respective `.ipynb` file.
2. Run only the **test** section and the model name definition block of the notebook.

## Folder Structure

### Model Folders
Each model folder contains the following:

- **`.csv` file:** Records the optimisation process for the reported results.
- **`.pth` file:** Contains the model weights.
- ** Two`.txt`:** Text files showing the class-wise Intersection over Union (IOU) and overall mean IOU.
- **Test set masks (zip file):** Contains the test masks submitted for evaluation.
- **PDF (submission proof):** PDF printed from the submission website verifying the authenticity of the results.

### Optimisation Folder
Inside the `optimisation` folder, you can find `.ipynb` notebooks for generating convergence curves. These notebooks contain plotting code (initially generated by LLMs and refined by the author).

## Additional Files

- **`class_distribution.json`:** Records the frequency of each label in the dataset.
- **`mean_std.json`:** Contains the mean and standard deviation of the RGB channels in the training set.

## Hardware Requirements

- **SegFormer Model:** At least **20 GiB** of GPU RAM.
- **Other Models:** Less than **12 GiB** of GPU RAM.

## Contact

For any queries, please contact **Xinghe Chen** at:  
📧 [xinghe001@e.ntu.edu.sg](mailto:xinghe001@e.ntu.edu.sg)