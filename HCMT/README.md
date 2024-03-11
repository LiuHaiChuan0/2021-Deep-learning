This repo is the official implementation of “HCMT: A novel hierarchical cross-modal transformer for recognition of abnormal behavior".

Step 1: Installation
cd HCMT/ 
python3 -m venv venvast
source venvast/bin/activate
1.	pip install -r requirements.txt 
2.	Install MMAction2
pip install git+https://github.com/open-mmlab/mim.git
mim install mmaction2

Step 2. Train the TAST model.
sh Audio/egs/CABRH8/run.sh

Step 3. Train the TST-L model
sh visual/tools/dist_train.sh configs/recognition/TST/TST-L.py 4  --validate

Step 4. Test model
python tools/analysis/report_accuracy.py --scores result/TST-L+.pkl result/TAST.pkl --datalist Audio/egs/CABRH8/data/val1.txt --coefficient 1 1



