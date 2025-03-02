# Simple Chatbot in PyTorch

This repository contains a simple chatbot implementation using PyTorch. The chatbot is trained on predefined intents and responses, allowing it to recognize patterns and reply accordingly. A graphical user interface (GUI) has been added to enhance user interaction.

## Installation

### Create a Virtual Environment
You can use either `venv` or `conda` to create an isolated environment for this project.

#### Using `venv`
```sh
mkdir chatbot_project
cd chatbot_project
python3 -m venv venv
```

#### Activate the Virtual Environment

- **Mac / Linux:**
  ```sh
  source venv/bin/activate
  ```
- **Windows:**
  ```sh
  venv\Scripts\activate
  ```

### Install Dependencies
Install PyTorch and required libraries:
```sh
pip install torch torchvision torchaudio
pip install nltk
pip install tkinter
```

If you encounter issues related to NLTK, install `punkt`:
```sh
python -c "import nltk; nltk.download('punkt')"
```

## Usage

### Train the Model
To train the chatbot model, run:
```sh
python train.py
```
This will generate a `data.pth` file, which contains the trained model weights.

### Run the Chatbot GUI
After training, launch the chatbot's graphical interface:
```sh
python app.py
```

## Customization
You can modify `intents.json` to customize the chatbot’s responses. This file defines the chatbot's possible intents, patterns, and responses.

Example:
```json
{
  "intents": [
    {
      "tag": "greeting",
      "patterns": [
        "Hi",
        "Hey",
        "Hello",
        "Good day"
      ],
      "responses": [
        "Hello! How can I assist you?",
        "Hey there! Need any help?"
      ]
    }
  ]
}
```

After modifying `intents.json`, re-run `train.py` to update the model.

## About

This chatbot uses a feedforward neural network with two hidden layers. It is designed for easy customization and can be extended for different use cases. The addition of a GUI provides a more interactive and user-friendly experience.

Feel free to contribute and enhance the chatbot!

