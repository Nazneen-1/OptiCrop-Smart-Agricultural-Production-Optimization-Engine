# OptiCrop

Demo: https://opticrop-smart-agricultural-production-q73f.onrender.com/

OptiCrop is a crop recommendation web app that helps users choose the most suitable crop based on soil and weather conditions. Enter the seven core agricultural parameters, and the app returns an instant ML-based recommendation.

<details open>
<summary><strong>Quick highlights</strong></summary>

- Fast crop prediction through a Flask web app.
- Trained on 2,200+ records with 22 crop classes.
- Built with a clean, responsive UI for easy use on desktop and mobile.
- Includes ready-to-run model artifacts in `data_collection_analysis`.

</details>

<details>
<summary><strong>What you can do here</strong></summary>

- Learn how the system works.
- Run the app locally in a few commands.
- Open the crop form and get a recommendation immediately.
- Inspect the input fields and understand what each one means.

</details>

## Try It Fast

<details open>
<summary><strong>1. Install and run</strong></summary>

```bash
git clone https://github.com/Nazneen-1/OptiCrop-Smart-Agricultural-Production-Optimization-Engine.git
cd OptiCrop-Smart-Agricultural-Production-Optimization-Engine
pip install flask scikit-learn pandas numpy jupyter
cd data_collection_analysis
python app.py
```

Then open `http://127.0.0.1:5000/` in your browser.

</details>

<details>
<summary><strong>2. Predict a crop</strong></summary>

Open the <strong>Find Your Crop</strong> page and fill in these values:

| Input | Description | Example |
| --- | --- | --- |
| Nitrogen (N) | Soil nitrogen level | `90` |
| Phosphorus (P) | Soil phosphorus level | `42` |
| Potassium (K) | Soil potassium level | `43` |
| Temperature | Average temperature in °C | `20.8` |
| Humidity | Relative humidity in % | `82.0` |
| pH Level | Soil pH | `6.5` |
| Rainfall | Rainfall in mm | `202.9` |

</details>

<details>
<summary><strong>3. If the model files are missing</strong></summary>

The app expects `model.pkl` and `scaler.pkl` inside `data_collection_analysis`. If they are missing, run the model-building notebook or script in that folder to regenerate them.

</details>

## Features

- Instant crop recommendations from seven agricultural inputs.
- Flask backend with simple route-based navigation.
- Polished UI with clear labels and a responsive layout.
- Support for 22 crop classes.
- Error handling for missing model files or invalid prediction input.

## How It Works

1. You enter soil and weather conditions.
2. The app scales the values with the saved preprocessing pipeline.
3. The ML model predicts the best crop for those conditions.
4. The result is shown immediately on the same page.

## App Pages

| Page | Route | Purpose |
| --- | --- | --- |
| Home | `/` | Landing page with project overview |
| About | `/about` | Explains the goal and working of OptiCrop |
| Project | `/project` | Project-focused information |
| Find Your Crop | `/findyourcrop` | Crop prediction form |

## Tech Stack

- Backend: Python, Flask
- ML: scikit-learn
- Data handling: Pandas, NumPy
- Frontend: HTML5, CSS3, Font Awesome, Google Fonts

## Dataset Snapshot

- Records: 2,200 agricultural samples
- Features: N, P, K, temperature, humidity, pH, rainfall
- Labels: 22 crop varieties

## Project Structure

```text
OptiCrop/
├── README.md
├── Crop_recommendation.csv
└── data_collection_analysis/
    ├── app.py
    ├── model.pkl
    ├── scaler.pkl
    ├── model building.ipynb
    ├── model building.py
    └── templates/
        ├── home.html
        ├── about.html
        ├── project.html
        └── findyourcrop.html
```

## Troubleshooting

<details>
<summary><strong>The app does not start</strong></summary>

Check that your virtual environment is active and that Flask is installed.

</details>

<details>
<summary><strong>I get a model loading error</strong></summary>

Verify that `model.pkl` and `scaler.pkl` exist in `data_collection_analysis`.

</details>

<details>
<summary><strong>The prediction looks wrong</strong></summary>

Make sure each field is filled with a numeric value and that the units roughly match the examples shown in the form.

</details>

## Goal

OptiCrop is designed to make crop selection faster, clearer, and more data-driven so users can make better farming decisions with less guesswork.
