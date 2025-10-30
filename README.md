# Movie Recommendation System
A movie recommendation system using the **Movielens 100k dataset** combined with the **TMDB API**.  

---

## Project Structure
```bash
ML_Movie_Recommendation_System/
│
├── README.md                # Project's introduction as well as installation and use guide
├── requirements.txt         # Required libraries
│
├── data/
│ ├── movielens datasets/    # The Datasets used for this project
│ ├── unprocessed/           # Unprocessed Datas
│ └── processed/             # Processed Datas
│
├── notebooks/               # EDA notebooks
│ ├── CBF_EDA.ipynb
│ ├── eda_cf.ipynb
│ ├── MRS-2.ipynb
│ └── Comparision.ipynb      # Comparision between models
│
├── src/                     # Source codes
│ ├── data_processing_cbf.py # Data preprocessing
│ ├── data_processing_cf.py
│ ├── train_cbf.py           # Model training scripts
│ ├── train_cf.py
│ ├── predict_cbf.py         # Predictions based on model scripts
│ ├── predict_cf.py
│ └── predict_hybrid.py
│
├── models/                  # Trained and saved models
│ └── svd_tuned_model.joblib                 
│
└── reports/                 # Report, images and charts 
  └── figures/ 
    └── screenshot/          # Example screenshots used in README.md
```

## Installation

```bash
pip install -r requirements.txt
```

## Usage

To launch the Streamlit web application:
1. Make sure you are in the project directory, type open CMD in project folder to open the command prompt. Then run the command below:

```bash
python -m run app.py
```
2. If done correctly, you will be shown a line of text that says *"You can now view your Streamlit app in your browser."* as well as your Local URL and Netowrk URL.

Example:
![Example Result 1](/figures/screenshot/ExampleResult1.jpg)

Then, you will be redirected to the Streamlit web application. Wait for the model to finish loading and will see the main interface showing up like this:
![Example Result 2](/figures/screenshot/ExampleResult2.jpg)

3. To start getting the movie recommendation: 
    - Select a model you want to try out from the sidebar of the top left *(CBF, CF or Hybrid)*
    - Type in the movie you want to find. Here I chose **Iron Man (2008)** for the example:
    ![SelectMovie](/figures/screenshot/MovieSelect.jpg)
    - Use the slider right below to adjust the range of the ratings. Then click on **"Save rating"** *(Lưu Đánh giá)* and the result will be displayed in the form of tables. 
    - Here are the examples of Top 10 Recommendation for **Iron Man *(2008)***:

###### Result based on CBF model:
![Example Result 3](/figures/screenshot/ExampleResult3.jpg)

###### Result based on CF model:
![Example Result 4](/figures/screenshot/ExampleResult4.jpg)

###### Result based on Hybrid model:
![Example Result 5](/figures/screenshot/ExampleResult5.jpg)

## Author
*This project was implemented by students as part of a coursework assignment.*

- **Course module**: ELC3006_50K29.1
- **Carried out by:**
       *- Ho Tuan Anh*
        *- Nguyen Quang Huy*
        *- Phan Trong Nghia*
        *- Tran Van Nhat*
