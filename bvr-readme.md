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


python src/get_data.py
git add src/get_data.py && git commit -m "added get_data.py"
git push -u origin main

python src/load_data.py
git add src/load_data.py && git commit -m "added load_data.py"
git push -u origin main

python src/split_data.py
git add . && git commit -m "added split_data.py"
git push -u origin main

python src/train_and_evaluate.py
git add . && git commit -m "train and evaluate"
git push -u origin main

Update train and evaluate python code and dvc yaml
dvc repro

git add . && git commit -m "joblib created"
git push -u origin main

mkdri report
touch report/params.json
touch report/scores.json

update metrics in dvc.yaml


git add . && git commit -m "metrics"
git push -u origin main

Make changes in params values to renegenerate new stores.

dvc params diff
dvc repro
dvc params diff


TOX Testing

touch tox.ini
Update tox.ini file


mkdir tests
touch tests/__init__.py
touch tests/conftest.py
touch tests/test_config.py

Add a testcase in test_config.py

pytest -v


tox -r (THIS WILL REBUILD TOX FROM SCRATCH - DOWNLOADS ALL DEPENDENCIES ONCE AGAIN)



pip install jupyterlab
jupyter-lab notebooks/


Add exception class to test_config.py and run "tox"


Update tox.ini file to add flask8 commands and run "tox"


Create Flask application
-----------------------
  mkdir -p prediction_service/model
  mkdir webapp
  touch app.py
  touch prediction_service/__init__.py
  touch prediction_service/prediction.py
  mkdir -p webapp/static/css
  mkdir -p webapp/static/script
  touch webapp/static/css/main.css
  touch webapp/static/script/index.js
  mkdir -p webapp/templates
  touch webapp/templates/index.html
  touch webapp/templates/404.html
  touch webapp/templates/base.html

