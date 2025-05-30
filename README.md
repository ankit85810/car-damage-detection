# Car Damage Detection 🚗🔍

A web application that uses a deep learning model to detect the type of vehicle damage from images. Built with **Streamlit** and **PyTorch**, this app classifies car damage into six categories based on front or rear damage conditions.

## 🚀 Features

- Upload a car image (`.jpg` or `.png`) and get instant predictions.
- Uses a fine-tuned **ResNet-50** model for accurate classification.
- Trained on custom data with transfer learning.
- Lightweight interface using Streamlit.

## 🧠 Model Overview

The model is a custom ResNet-50 where:
- All layers except `layer4` and the final fully connected layers are frozen.
- Trained on 6 vehicle damage categories:
  - Front Breakage
  - Front Crushed
  - Front Normal
  - Rear Breakage
  - Rear Crushed
  - Rear Normal

The best-performing model was selected after experimenting with CNNs and EfficientNet in the [training notebook](./damage-prediction.ipynb).

## 🗂 Project Structure

```
car-damage-detection/
│
├── app.py                # Streamlit frontend
├── model_helper.py       # Model definition and prediction
├── requirements.txt      # Dependencies
├── damage-prediction.ipynb # Model training experiments
└── model/
    └── saved_model.pth   # Trained ResNet model
```

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/car-damage-detection.git
cd car-damage-detection

# (Optional) Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

# Install dependencies
pip install -r requirements.txt
```

## ▶️ Run the App

```bash
streamlit run app.py
```

Then, open your browser and navigate to `http://localhost:8501`.

## 🧪 Example Usage

1. Launch the app.
2. Upload an image of a vehicle's front or rear.
3. The app will display the image and its predicted damage class.

## 📚 Requirements

See `requirements.txt`:

```
streamlit==1.40.1
Pillow==9.5.0
torch==2.5.1
torchvision==0.20.1
```

## 👤 Author

- **Your Name** – [your-email@example.com](mailto:your-email@example.com)

## 📝 License

This project is licensed under the MIT License.