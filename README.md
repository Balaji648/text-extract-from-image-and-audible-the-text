🧠 Text Extract from Image and Audible the Text

This project extracts text from an image and converts it into audible speech. It combines Optical Character Recognition (OCR) and Text-to-Speech (TTS) technologies to help users easily read and listen to text found in images — useful for visually impaired users, document reading, or automation tasks.


---

🚀 Features

🖼️ Image to Text Extraction using OCR (pytesseract)

🔊 Text to Speech Conversion using TTS (pyttsx3 or gTTS)

📁 Supports various image formats (JPG, PNG, JPEG)

🧾 Simple CLI or GUI-based interface

💡 Lightweight and easy to use



---

🛠️ Tech Stack

Python 3.8+

Libraries:

pytesseract → For extracting text from images

Pillow → For handling image files

pyttsx3 / gTTS → For converting text to speech

os, cv2 (optional) → For file handling and image preprocessing




---

⚙️ Installation

1. Clone the Repository

git clone https://github.com/<your-username>/text-extract-from-image-and-audible-the-text.git
cd text-extract-from-image-and-audible-the-text

2. Install Dependencies

pip install -r requirements.txt

3. Install Tesseract OCR

Windows:

Download and install from Tesseract GitHub Releases

Add Tesseract to your system PATH.


Linux:

sudo apt install tesseract-ocr


---

▶️ Usage

Run the script:

python main.py

Example:

1. Upload or specify an image file


2. The program extracts the text


3. The text is read aloud using speech synthesis




---

📂 Project Structure

text-extract-from-image-and-audible-the-text/
│
├── main.py                 # Main application script
├── requirements.txt        # List of dependencies
├── assets/                 # Folder for sample images
├── output/                 # Folder to store extracted text or audio (optional)
└── README.md               # Project documentation


---

🧩 Example Code Snippet

import pytesseract
from PIL import Image
import pyttsx3

# Load image
img = Image.open('sample.jpg')

# Extract text from image
text = pytesseract.image_to_string(img)
print("Extracted Text:", text)

# Convert to speech
engine = pyttsx3.init()
engine.say(text)
engine.runAndWait()


---

📸 Sample Output

Input Image:
🖼️ A picture containing printed or handwritten text

Extracted Text:

The quick brown fox jumps over the lazy dog.

Audio Output:
🔊 Text spoken aloud via TTS engine

📝 License

This project is licensed under the MIT License — free to use and modify with attribution.
