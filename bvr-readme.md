conda create -n wineq python=3.8 -y
conda activate wineq
touch requirements.txt
pip install -r requirements.txt

python template.py

DOWNLOAD DATA FILE
https://drive.google.com/drive/folders/18zqQiCJVgF7uzXgfbIJ-04zgz1ItNfF5?usp=sharing


git init
dvc init
dvc add data_given/winequality.csv
git add .
git status
git commit -m "First commit"
git add . && git commit -m "update readme file"

git remote add origin https://github.com/sudhakar-mr/project_app.git
git branch -M main
git push -u origin main