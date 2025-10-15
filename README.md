# 💬 Chatbot Springboard — Streamlit + Ollama Chat App

An interactive **ChatGPT-like chatbot** built with **Streamlit**, integrated with **Ollama** for local LLM inference, and enhanced with **OCR (Optical Character Recognition)** capabilities using **Tesseract**.
Users can chat with models like `phi3`, `mistral`, and `llama2`, upload images for text extraction, and manage multiple chat sessions — all in a modern ChatGPT-style interface.

---

## 🚀 Features

✅ **ChatGPT-like interface** – Modern, minimal, and responsive UI
✅ **Multiple Models** – Choose between `phi3`, `mistral`, or `llama2`
✅ **Chat History & Pinned Chats** – Organize and revisit old conversations
✅ **Image Upload with OCR** – Extract text from uploaded images using Tesseract
✅ **Interactive Buttons** – Summarize, translate, or explain responses
✅ **Auto-scroll and smooth streaming responses** – Real-time assistant typing effect
✅ **Dark UI theme** – Aesthetic and easy on the eyes

---

## 🧰 Tech Stack

| Component          | Technology                                                                         |
| ------------------ | ---------------------------------------------------------------------------------- |
| **Frontend / UI**  | [Streamlit](https://streamlit.io/)                                                 |
| **Backend (LLM)**  | [Ollama](https://ollama.ai)                                                        |
| **OCR Engine**     | [Tesseract OCR](https://github.com/tesseract-ocr/tesseract)                        |
| **Language**       | Python 3.10+                                                                       |
| **Libraries Used** | `requests`, `pytesseract`, `Pillow`, `uuid`, `json`, `time`, `base64`, `streamlit` |

---

## 🖥️ Setup Instructions

### 1️⃣ Prerequisites

* **Python 3.10+**
* **Ollama** installed and running locally
  👉 [Download Ollama](https://ollama.ai/download)
* **Tesseract OCR** installed
  👉 [Download for Windows](https://github.com/UB-Mannheim/tesseract/wiki)
* **pip** (Python package manager)

---

### 2️⃣ Clone the Repository

```bash
git clone https://github.com/saiBharath14/chatbot_springboard.git
cd chatbot_springboard
```

---

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

If you don’t have a `requirements.txt`, create one with:

```bash
streamlit
requests
pytesseract
Pillow
uuid
```

---

### 4️⃣ Configure Tesseract Path

In your Python file, make sure the path to `tesseract.exe` is correctly set:

```python
pytesseract.pytesseract.tesseract_cmd = r"C:\\Program Files\\Tesseract-OCR\\tesseract.exe"
```

Change the path if Tesseract is installed elsewhere.

---

### 5️⃣ Start Ollama

Run this command in a **separate terminal** before launching Streamlit:

```bash
ollama serve
```

You can also preload a model (e.g., `phi3`):

```bash
ollama pull phi3
```

---

### 6️⃣ Run the Streamlit App

```bash
streamlit run app.py
```

Replace `app.py` with your script filename if different.

---

## 🧠 Usage

1. Select a model from the sidebar (`phi3`, `mistral`, or `llama2`)
2. Type your prompt and press **Enter**
3. Use **“Explain More”**, **“Summarize”**, or **“Translate”** buttons on assistant replies
4. Click **➕** to upload an image for OCR
5. Extracted text will automatically appear in the chat
6. Manage chats in the sidebar – create new, pin, or clear old ones

---

## 📸 OCR Example

* Upload an image (e.g., a scanned document or screenshot)
* The app extracts and displays the recognized text directly in the chat

Example output:

```
🧾 Extracted Text:
This is a sample OCR extraction using Tesseract!
```

---

## ⚙️ Configuration Tips

* If the app cannot connect to Ollama, ensure it’s running at:

  ```
  http://localhost:11434
  ```
* You can modify the timeout or stream parameters in:

  ```python
  requests.post("http://localhost:11434/api/chat", ...)
  ```
* The UI uses custom CSS for a ChatGPT-like design; feel free to tweak color variables.

---

## 🧾 Example Folder Structure

```
chatbot_springboard/
│
├── app.py                 # Main Streamlit app
├── requirements.txt       # Dependencies
├── README.md              # Project documentation
└── assets/                # (Optional) images or icons
```

---

## 🌟 Future Enhancements

* 🔊 Text-to-Speech integration
* 💾 Export chat history as PDF or Markdown
* 🌐 Multilingual translation support
* 🧠 Integration with vector databases for memory

---

## 🧑‍💻 Author

**Venkata Sai Bharath**
💼 GitHub: [saiBharath14](https://github.com/saiBharath14)

---

## 🪪 License

This project is licensed under the **MIT License** — feel free to modify and share.

---
