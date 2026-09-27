# End-to-End Reproduction Guidee
1. Enviroment setup and Installing dependencies:
```
# Create virtual environment
python -m venv venv

# Activate environment (Windows PowerShell)
.\venv\Scripts\activate

# Install dependencies
pip install --upgrade pip
pip install -r requirements.txt
```
  If .pyd files are restricted by Windows Security policies, unblock the virtual environment files:
```
# To unblock
Get-ChildItem -Path ".\venv" -Recurse | Unblock-File
```
2. Datasets in folder:
```
dataset/
├── train/
│   ├── train_source1.tsv
│   ├── train_source2.tsv
│   ├── train_source3.tsv
│   └── train_ground_truth.tsv
└── test/
    ├── test_source1.tsv
    ├── test_source2.tsv
    └── test_source3.tsv
```
3. Pipeline Execution:
  run full pipeline:
   ```
   # in powershell:
   python code/business_entity_resolution/src/app.py
   # in code editor:
   cd src
   python app.py
   ```
4. Outputs:
   upon complete execution of code their will be new directory in folder named as "outputs" thic will contain:
   1. candidate_pairs.tsv # which is generated using inverted index prefix blocking.
   2. matching_pairs.tsv # in this there are high precision entities that are predicted using LightBGM
