# colab-dvc

# Install dvc
- ```pip install dvc[all]```

# to PUSH data with DVC into GDRIVE
- create the git repo
- ``` git clone <repo> ```
- inside the git repo --> ```dvc init```
- ```git status```
- ```git commit -m "Initialize DVC"```
- add data --> ```dvc add data``` _data is name of folder_
- ```git add ...``` --> This can be copied from the output of above command
- ```git commit -m "Add raw data"```
- Now Add the storage --> ```dvc remote add -d storage gdrive://<drive_token>```
- ```git add .dvc/config```
- ```git commit -m "Configure remote storage"```
- Now push the data in drive --> ```dvc push```
- Finally don't forget to ```git push```

# to PULL data with DVC from GDRIVE
- list the data ---> ```dvc list <git repo>```
  pull --> ```dvc pull```
  
  
