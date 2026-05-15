# Video Game Genre Classifier

A deep learning image classifier that predicts a video game's genre from a screenshot, built using transfer learning with a fine-tuned ResNet-18 model.

## Genres

The model classifies screenshots into 6 genres:
- Action
- Adventure
- Puzzle
- Racing
- Sports
- Strategy

## Results

| Epoch | Loss   | Train Acc | Val Acc |
|-------|--------|-----------|---------|
| 1     | 1.4187 | 44.75%    | 59.33%  |
| 2     | 0.7558 | 75.27%    | 70.50%  |
| 3     | 0.3896 | 88.49%    | 74.25%  |
| 4     | 0.2107 | 93.90%    | 75.92%  |
| 5     | 0.1274 | 96.87%    | 75.92%  |

Final validation accuracy: **75.92%**

## How to Run

This project runs on [Google Colab](https://colab.research.google.com/) and requires a free Kaggle account to download the dataset.

### Step 1: Set up Kaggle API token

1. Create a free account at [kaggle.com](https://www.kaggle.com) if you don't have one
2. Go to **Settings → API Tokens → Create New Token**
3. Copy the token string that is generated

### Step 2: Open the notebook in Google Colab

1. Upload the `.ipynb` file to [Google Colab](https://colab.research.google.com/)
2. Go to **Runtime → Change runtime type → T4 GPU** and click Save

### Step 3: Run the notebook

1. Run **Cell 1** to install dependencies and imports
2. Run **Cell 2** — it will prompt you to upload your `kaggle.json` file. When prompted, select the file you downloaded in Step 1. The dataset will download and extract automatically.
3. Run all remaining cells in order from top to bottom

### Step 4: Try the demo

The final cell launches a Gradio interface. Upload any game screenshot and the model will predict its genre with confidence scores.

## Project Structure

```
├── game_genre_classifier.ipynb   # Main Colab notebook
└── README.md                     # This file
```

## Tech Stack

- Python 3
- PyTorch + torchvision
- ResNet-18 (pretrained on ImageNet, fine-tuned on game screenshots)
- Gradio (demo interface)
- scikit-learn (evaluation metrics)
- Google Colab (T4 GPU)

## Dataset

[Game Sub Categorized Android Apps Screenshots](https://www.kaggle.com/datasets/uzairkhan45/game-sub-categorized-android-apps-screenshots) — Kaggle dataset with 1,000 labeled screenshots per genre.
