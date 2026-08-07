# An Under-Mattress Noncontact Millimeter-Wave System for Continuous Cardiac Monitoring and Arrhythmia Screening

The available data and code of the manuscript.

---

# ➡️ Folder Structure Overview

The folder consists of three parts:

## 📊 data_sample

* Each CSV file containing radio displacement samples includes 30-second sample segments at a sampling rate of 50 Hz.
* A file named 'disp_mask.ipynb' demonstrates the process of masking displacement waveforms
* Part of the publicly available laboratory data is shown here, including 10 sample records each from 15 subjects.

## 🕹️ code

* In 'Data' folder, the unlabelled radio displacement samples from five centres consist of the pre-training dataset. The labelled radio displacement samples from two hostiptals consist of the fine-tuning dataset. *Due to institutional restrictions regarding patient privacy, the complete dataset is not publicly available. Access requests can be directed to the corresponding author of our paper, with an expected response time of up to 60 days. Alternatively, if you have relevant clinical data, you can try building your own .pt pre-training and fine-tuning dataset, consisting of a series of 30-second displacement samples.*
* In 'Module' folder, some basic python files as network modules are listed.
* In 'base_model.py' file, the network architecture is defined.
* **Run 'Pre_traing.py' file, you can get a pre-trained model** after putting the right pre-training dataset into the corresponding file path.
* **Run 'fine_tune_LoRA.py' file, you can get the finetuned results** regarding to the specific arrhythmia after putting the right fine-tuning dataset into the corresponding file path. A pipeline of PVC classification is shown.
* A **pre-trained model weight file** for testing multi-task purposes can be downloaded from the [link](https://drive.google.com/file/d/1ug1Vr2LDI8F_H6uLwddRFSwp2l_fe46d/view?usp=sharing). *You can apply this weight file to the fine-tuning dataset built by yourself.*
* It is recommended to change your execution path to the current system directory of code. This allows you to avoid modifying the relative import paths of these files when running Python scripts.

## 🔧 Installation

Install Python 3.9 or higher version and necessary dependencies.

`pip install -r requirements.txt `

---

# 🔥 Pre-traing and Fine-tunning neraul network

## 1️⃣ Wash the unlabelled data as the pre-training dataset.

## 2️⃣ Run the pre-training process to get the foundation model.

## 3️⃣ Fine-tune the foundation model to downstream tasks.

---

# ❤️ Acknowledgments

[Contactless Cardiac Detection of Arrhythmia Based on Distribution Encoding Network With Microwave Biomedical Radar](https://ieeexplore.ieee.org/document/11398845)

For more insteresting information, welcome refer to Changzhan's [lab website](https://changzhan.sjtu.edu.cn/).
