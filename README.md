# Video Game Genre Classifier

A deep learning image classifier that predicts a video game's genre from a screenshot, built using transfer learning with a fine-tuned ResNet-18 model.

## How to Run

This project runs on [Google Colab](https://colab.research.google.com/) and requires a free Kaggle account to download the dataset.

### Step 1: Set up Kaggle API token

1. Create a free account at [kaggle.com](https://www.kaggle.com) if you don't have one
2. Go to **Settings → API Tokens → Generate New Token**
3. Copy the token string that is generated

### Step 2: Open the notebook in Google Colab

1. Upload the `.ipynb` file to [Google Colab](https://colab.research.google.com/)
2. Go to **Runtime → Change runtime type → T4 GPU** and click Save

### Step 3: Run the notebook

1. In **Cell 2** — add the token string copied in **Step 1**
2. Run all cells top to bottom

### Step 4: Try the demo

The final cell launches a Gradio interface. Upload any game screenshot and the model will predict its genre with confidence scores.

## Dataset

[Game Sub Categorized Android Apps Screenshots](https://www.kaggle.com/datasets/uzairkhan45/game-sub-categorized-android-apps-screenshots) — Kaggle dataset with 1,000 labeled screenshots per genre.
