# Classroom Student Behavior Recognition Using An Intelligent Sensing Framework

This repository is the official implementation of CSBR, a novel hierarchical cross-modal transformer designed for the recognition of abnormal behavior. CSBR leverages cross-modal features to enhance the recognition accuracy in classroom environments. The code will be released as open source.

## Installation

To set up your environment for CSBR, follow these steps:

1. **Clone the repository** and navigate to the project directory:
    ```bash
    git clone https://github.com/LiuHaiChuan0/2021-Deep-learning/CSBR.git
    cd CSBR
    ```

2. *(Optional)* **Unzip** any prepackaged file assets (e.g., preprocessed data or pretrained models) if provided (e.g., `Visual.zip` or `Audio.zip`):
    ```bash
    unzip Visual.zip
    ```

3. **Create a virtual environment** (recommended) and activate it:
    ```bash
    python3 -m venv venv_isf
    source venv_isf/bin/activate
    ```

4. **Install required dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

5. *(Optional)* If you use [MMAction2](https://github.com/open-mmlab/mmaction2) or other OpenMMLab tools for model training, you can install it via [MIM](https://github.com/open-mmlab/mim) (modify if not needed):
    ```bash
    pip install git+https://github.com/open-mmlab/mim.git
    mim install mmaction2
    ```

## Usage

### Step 1: Train the Audio Branch (ATST)

If your framework separates audio and visual training, navigate to the audio branch code folder and run:
```bash
sh Audio/egs/CSBR10/run.sh
  ```
### Step 2:Train the Visual Branch (TST)
```bash
sh visual/tools/dist_train.sh configs/recognition/TST/TST.py 2 --validate
  ```
### Step 3: Test the Fusion (MFT)
```bash
python tools/analysis/report_accuracy.py \
    --scores result/TST-L+.pkl result/ATST.pkl \
    --datalist Audio/egs/CSBR10/data/val_list.txt
  ```

## Contributing

We welcome contributions to improve CSBR! Please feel free to submit pull requests or open issues to discuss improvements or report bugs.
