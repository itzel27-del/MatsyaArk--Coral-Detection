# 🌊 Coral Bleaching Detection AI  

This project is a lightweight deep learning application for detecting **coral bleaching** using computer vision. It leverages a pre-trained PyTorch model (`coral_bleaching_lightweight.pt`) and provides a simple web interface built with **Flask** to upload and analyze coral reef images.  

---

## 📌 Features
- 🖼️ Upload coral reef images through the web app  
- 🤖 AI model predicts bleaching status (healthy vs. bleached)  
- ⚡ Lightweight and fast model optimized for deployment  
- 🎨 Frontend with `templates` (HTML) and `static` (CSS/JS)  

---

## 📂 Project Structure
├── static/ # CSS, JS, images

├── templates/ # HTML templates for Flask

├── app.py # Main Flask application

└── coral_bleaching_lightweight.pt # Pre-trained PyTorch model

yaml
Copy code

---

## 🚀 Tech Stack
- **Python 3.x**  
- **Flask** (web framework)  
- **PyTorch** (deep learning model)  
- **HTML/CSS/JavaScript** (frontend)  

---

## ⚙️ Installation & Setup

1. **Clone the repository**  
   ```bash
   git clone https://github.com/itzel27-del/MatsyaArk--Coral-Detection.git
   cd MatsyaArk--Coral-Detection
Create a virtual environment (recommended)

bash
Copy code
python -m venv venv
source venv/bin/activate    # On Linux/Mac
venv\Scripts\activate       # On Windows
Install dependencies

bash
Copy code
pip install -r requirements.txt
Run the app

bash
Copy code
python app.py
Open in browser
Go to: http://127.0.0.1:5000

🌍 Use Case
Coral reefs are critical ecosystems, but bleaching events caused by climate change threaten their survival.
This tool helps researchers, conservationists, and students quickly identify bleaching in reef images, aiding in monitoring, research, and awareness efforts.

📸 <img width="552" height="663" alt="image" src="https://github.com/user-attachments/assets/5b69e4ad-5b6b-4b57-bbea-98081639045c" />


🤝 Contributing
Contributions are welcome! Feel free to submit pull requests or open issues for improvements.

📜 License
This project is licensed under the MIT License – feel free to use and modify.
