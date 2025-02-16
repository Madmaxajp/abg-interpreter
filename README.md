# ABG Interpreter with Blockchain Integration

## 📌 Overview
The **ABG Interpreter** is an advanced **Arterial Blood Gas (ABG) analysis tool** integrated with **OCR (Optical Character Recognition)** and **blockchain storage** on the **Tea-Assam network**. It allows users to upload an image of an ABG report, extract values using OCR, interpret the results, and store them on the blockchain for **tamper-proof medical record keeping**.

## 🚀 Features
- ✅ **OCR-Based ABG Extraction** – Uses Tesseract to extract ABG values from images.
- ✅ **ABG Interpretation** – Classifies metabolic/respiratory disorders and compensatory states.
- ✅ **Tea-Assam Blockchain Integration** – Securely stores ABG reports on-chain.
- ✅ **Flask API** – Provides an easy-to-use API for uploading and analyzing reports.
- ✅ **JSON Responses** – Returns structured data including ABG values, diagnosis, and blockchain transaction details.

## 🏗️ Tech Stack
- **Backend:** Flask (Python)
- **OCR Engine:** Tesseract
- **Blockchain:** Web3 (Tea-Assam Network)
- **Database:** Blockchain-based storage
- **Deployment:** Can be hosted on Heroku, Render, or AWS

## 🛠️ Installation
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/abg-interpreter.git
cd abg-interpreter
```

### 2️⃣ Install Dependencies
Ensure you have Python installed, then run:
```bash
pip install -r requirements.txt
```

### 3️⃣ Set Up Web3 Configuration
Update the **Tea-Assam blockchain details** in `app.py`:
```python
WEB3_PROVIDER = "https://assam-rpc.tea.xyz"
CHAIN_ID = 93384
CURRENCY_SYMBOL = "$TEA"
```

### 4️⃣ Run the API
Start the Flask server:
```bash
python app.py
```
The API will be available at `http://127.0.0.1:5000`.

## 📤 API Usage
### **Upload an ABG Report Image**
#### **Endpoint:** `POST /interpret_abg`
**Request:**
```bash
curl -X POST -F "image=@sample_image.jpg" http://127.0.0.1:5000/interpret_abg
```

**Response:**
```json
{
    "ABG Values": {
        "pH": 7.32,
        "PaCO2": 50,
        "PaO2": 88,
        "HCO3": 20,
        "BaseExcess": -4
    },
    "Interpretation": "Uncompensated Respiratory Acidosis",
    "Blockchain Transaction": "0x123abc456def...",
    "Explorer URL": "https://assam.tea.xyz/tx/0x123abc456def..."
}
```

## 🔗 Tea-Assam Blockchain Details
- **Network Name:** Tea-Assam
- **RPC URL:** [https://assam-rpc.tea.xyz](https://assam-rpc.tea.xyz)
- **Chain ID:** `93384`
- **Currency Symbol:** `$TEA`
- **Block Explorer:** [https://assam.tea.xyz](https://assam.tea.xyz)
- **Bridge:** [https://tetsuo.conduit.xyz/bridge/redirect?slug=tea-assam-fo46m5b966](https://tetsuo.conduit.xyz/bridge/redirect?slug=tea-assam-fo46m5b966)

## 🤝 Contributing
1. **Fork the repository**
2. **Create a feature branch:** `git checkout -b feature-xyz`
3. **Commit changes:** `git commit -m "Added feature XYZ"`
4. **Push branch:** `git push origin feature-xyz`
5. **Open a Pull Request**

## 📜 License
This project is licensed under the **MIT License**.

## 🙌 Support
For issues or suggestions, open an [issue](https://github.com/YOUR_USERNAME/abg-interpreter/issues) on GitHub.

