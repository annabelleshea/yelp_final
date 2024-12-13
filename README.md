# yelp_final
### 
The dataset used is the Yelp Open dataset that's available here: https://www.yelp.com/dataset

The datasets we decided were relevant to keep were the review (5.34 GB), business (118.9 MB), and user (3.36 GB) json files. Since the review dataset was too big to load into VSCode, we had to split it into 3 separate json files to be able to load it. This was done in the **review_split.py** file.

We then used the code in the **downsample.py** file to sample 1/5 of the reviews made by users with 5 or more reviews. This created a smaller dataset to work with.

To further shrink the size of the dataset, we decided to only keep reviews about restaurants/food establishments in the **filter.py file**.

The 2 Jupyter Notebook files contain the code we used for cleaning and proprocessing the filtered and downsampled restaurant data (**Cleaning.ipynb**) and to build the final KNN model (**FinalModel.ipynb**).

When deploying on Streamlit, we chose the GitHub option and set the **yelp_app.py** file (which contains the code for the app UI) as the main file path. The **requirements.txt** file ensures the Streamlit app downloads the needed packages to run the code in the yelp_app.py file. The yelp_app.py calls the **best_knn_model.pkl** file to make the prediction based on user inputs in the app.
###


