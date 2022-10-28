# SMS-Spam-Classifier

### End to End Machine Learning Project | SMS Spam Classifier | Front-end - Streamlit | Heroku Deployment 

### VS Code Steps - 

>> Create a local Folder
>> Create a Repo on github --> Add Readme.md - Select Python - Add a License
>> Open Cmd --> cd into local folder --> git clone github repo
>> Go to repo folder on local machine --> Right click - Git bash Here - code .
>> Vscode will open with the folder as working directory
>> Ctrl+Shift+P --> Select base pythn=3.8.8 interpreter --> Open Terminal
>> Select Cmd or Git ( or powershell)  accoridng to the project
```
conda create -n <my_env_name> python=3.8.8 -y
```
```
conda info --envs
```
```
conda activate <my_env_name>
```
===========================================================================

### Anaconda Steps - 

1. Open anaconda prompt
2. Base environment - 
```
conda create -n <my_env_name> python=3.8.8 -y
```
```
conda activate <my_env_name>
```
3. Create a local Folder
4. Copy the path --> cd in anaconda prompt to the path (D:\)
```
 jupyter notebook
```
===========================================================================

### Create and Install requirements.txt
```
pip install -r requirements.txt
```

### Setup your Github account
```
git config --global user.name "mustafamadraswala"
```
```
git config --global user.email "museychamp@gmail.com"
```

### Push all the changes and code to Github -
Add all the files to github - 
```
git add .
```

Check status of your files -
```
git status
```

Commit all the files to github by pushing the fies from local to  thestaging environment -
```
git commit -m "This is my first commit includes requirement.txt and readme.md file"
```

Or do both tthe steps together -
```
git add . && git commit -m "This is my first commit"
```

Push everything to github -
```
git push origin main
```
=============================================================================

### Execute the sms-spam-detection.ipynb file to get 2 pickle files
#### 1. vectorizer.pkl 2. model.pkl

### Create a python file for your streamlit application
```
touch app.py
````
### Use the streamlit library to make a simple front end page
### Execute the app.py file in vscode
```
streamlit run app.py
```

=============================================================================

### Deploy to Heroku
1. Create a Procfile in folder in VScode -
```
web: gunicorn app:app
```

If using Streamlit -
```
web: sh setup.sh && streamlit run app.py
```

2. Create a setup.sh file -
ps - Required for streamlit implementation

3. Add nltk.txt file with the corpus names mentioned inside it (stopwords, punkt, wordcloud)
ps - Required for heroku implementation

4. Push final commit to github
5. Go to Heroku - Create an app sms-spam-classifier-mm
6. Connect the app with github repo
7. Deploy branch on heroku
