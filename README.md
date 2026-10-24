# Medicine-Price-Comparison-
Medicine price comparison project
# 💊 Medicine Price Comparison System

A **Streamlit-based medicine price comparison web application** that helps users compare medicine prices from different online pharmacy sources.

The application uses **SerpApi Google Shopping results** to fetch product information and displays medicine name, pharmacy/source, price, product image, and purchase link.

---

## 🚀 Features

- 🔎 Search for medicines by name
- 💰 Compare prices from different sources
- 🏪 Display pharmacy/company names
- 🖼️ Display product thumbnails
- 🔗 Provide purchase links
- 🏆 Automatically identify the best/lowest-price option
- 📊 Display price comparison charts
- 📈 Visualize prices using bar and pie charts
- 🇮🇳 Google Shopping search configured for India
- ⚡ Simple and user-friendly Streamlit interface

---

## 🛠️ Technologies Used

- **Python**
- **Streamlit**
- **SerpApi**
- **Pandas**
- **Matplotlib**
- **Google Shopping API**

---

## 📁 Project Structure

```text
Medicine-Price-Comparison/
│
├── app.py
├── e_pharmacy.png
├── README.md

```

---

# ⚙️ Installation & Setup

## 1. Clone the Repository

```bash
git clone https://github.com/your-username/medicine-price-comparison.git
```

Move into the project folder:

```bash
cd medicine-price-comparison
```

---

## 2. Create a Virtual Environment

### Windows

```bash
python -m venv venv
```

Activate it:

```bash
venv\Scripts\activate
```

### macOS/Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

If you don't have a `requirements.txt` file yet:

```bash
pip install streamlit serpapi pandas matplotlib
```

---

# 🔑 IMPORTANT: Add Your Own API Key

⚠️ **You MUST add your own SerpApi API key before running this project.**

Do **NOT** use someone else's API key or upload your API key to GitHub.

Get your API key from:

**SerpApi:** https://serpapi.com/

After creating your account, copy your API key.

### Add your API key in `app.py`

Find:

```python
client = serpapi.Client(api_key="YOUR_API_KEY")
```

Replace:

```python
"YOUR_API_KEY"
```

with your own SerpApi API key.

For example:

```python
client = serpapi.Client(api_key="YOUR_SERPAPI_API_KEY")
```

### ⚠️ Security Warning

Never commit your real API key to GitHub.

Instead of writing the API key directly in your source code, a better approach is to use **Streamlit Secrets**.

Create:

```text
.streamlit/
└── secrets.toml
```

Add:

```toml
SERPAPI_API_KEY = "YOUR_SERPAPI_API_KEY"
```

Then use:

```python
client = serpapi.Client(
    api_key=st.secrets["SERPAPI_API_KEY"]
)
```

Also add this to `.gitignore`:

```text
.streamlit/secrets.toml
.env
venv/
__pycache__/
```

---

# ▶️ Run the Application

Start the Streamlit application:

```bash
streamlit run app.py
```

Or:

```bash
python -m streamlit run app.py
```

The application will normally open at:

```text
http://localhost:8501
```

---

# 🧪 How to Use

1. Open the application.
2. Enter the **medicine name**.
3. Enter the number of price options you want to compare.
4. Click **Show Compare**.
5. The application fetches Google Shopping results.
6. Compare:
   - Pharmacy/source
   - Medicine name
   - Price
   - Purchase link
7. The application identifies the **best price option**.
8. Price comparison charts are displayed at the bottom.

---

# 📊 Example Workflow

```text
Enter Medicine Name
        ↓
Search Google Shopping
        ↓
SerpApi
        ↓
Retrieve Shopping Results
        ↓
Compare Medicine Prices
        ↓
Find Lowest Price
        ↓
Display Results + Charts
```

---

# 📸 Application Preview

Add screenshots of your application here:

```text
![Application Screenshot](screenshot.png)
```

# ⚠️ Disclaimer

This project is created for **educational and demonstration purposes**.

The displayed prices and product information are obtained from third-party search results and may change at any time.

Always verify medicine details, dosage, availability, seller information, and price from the actual pharmacy before purchasing.

This application does **not** provide medical advice or replace consultation with a qualified healthcare professional.

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a new branch:

```bash
git checkout -b feature/new-feature
```

3. Make your changes.
4. Commit your changes:

```bash
git commit -m "Add new feature"
```

5. Push the branch:

```bash
git push origin feature/new-feature
```

6. Create a Pull Request.

---

# 📄 License

This project is available for educational and personal use.

---

## 👨‍💻 Author

**Pranav Gupta**

Computer Science Student | AI/ML Enthusiast

---

⭐ If you found this project useful, consider giving the repository a **star**!
