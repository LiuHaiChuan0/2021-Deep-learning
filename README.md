# HCMT: A Novel Hierarchical Cross-Modal Transformer for Abnormal Behavior Recognition

This repository is the official implementation of HCMT, a novel hierarchical cross-modal transformer designed for the recognition of abnormal behavior. HCMT leverages cross-modal features to enhance the recognition accuracy in complex campus environments.

## Installation

To set up your environment for HCMT, follow these steps:

```bash
# Clone the repository and enter the HCMT directory
git clone https://github.com/LiuHaiChuan0/2021-Deep-learning/tree/main/HCMT
cd HCMT/
#Unzip the file Visual.zip

# Create a virtual environment and activate it
python3 -m venv venvast
source venvast/bin/activate

# Install the required dependencies
pip install -r requirements.txt

# Install MMAction2 via MIM
pip install git+https://github.com/open-mmlab/mim.git
mim install mmaction2
```

## Usage

### Step 1: Train the audio branch TAST

To train the TAST model, run the following command:

```bash
sh Audio/egs/CABRH8/run.sh
```

### Step 2: Train the visual branch TST

To train the TST-L model on 4 GPUs with validation, execute:

```bash
sh visual/tools/dist_train.sh configs/recognition/TST/TST-L.py 4 --validate
```

### Step 3: Test the fusion HCMT

After training, you can test the model and generate a report on accuracy using:

```bash
python tools/analysis/report_accuracy.py --scores result/TST-L+.pkl result/TAST.pkl --datalist Audio/egs/CABRH8/data/val1.txt --coefficient 1 1
```

## Contributing

We welcome contributions to improve HCMT! Please feel free to submit pull requests or open issues to discuss improvements or report bugs.

