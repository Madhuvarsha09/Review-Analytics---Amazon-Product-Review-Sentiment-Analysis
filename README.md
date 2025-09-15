# Review-Analytics---Amazon-Product-Review-Sentiment-Analysis
Perfect 👍 I’ll take your draft and restructure it with **clean GitHub-style alignment**,
emojis for crispness, consistent formatting, and proper markdown hierarchy.
Here’s your polished **README.md**:

---

# 📊 ReviewAnalytics – Amazon Product Review Sentiment Analysis 🛒⭐

A modern **web application** that analyzes sentiment from Amazon product reviews using **AI-powered insights**.
Built with a **React frontend** and **Flask backend** during my internship.

---

## 🚀 Features

* 🔍 **Product Search** – Search any Amazon product and fetch comprehensive reviews
* 🤖 **AI Sentiment Analysis** – Polarity scoring with NLP (positive, negative, neutral)
* 📊 **Interactive Charts** – Pie charts showing sentiment distribution
* 🎨 **Modern UI** – Responsive glassmorphism-based design
* ⚡ **Real-time Analysis** – Instant insights with live scraping
* 📝 **Review Display** – Detailed review cards with sentiment indicators

---

## 📋 Table of Contents

* [Features](#-features)
* [Tech Stack](#-tech-stack)
* [Installation](#-installation)
* [Usage](#-usage)
* [API Documentation](#-api-documentation)
* [Project Structure](#-project-structure)
* [Configuration](#-configuration)
* [Deployment](#-deployment)
* [Contributing](#-contributing)
* [License](#-license)
* [Troubleshooting](#-troubleshooting)
* [Support](#-support)
* [Future Enhancements](#-future-enhancements)

---

## 🛠 Tech Stack

### 🔹 Frontend

* ⚛️ React 18 – Modern UI framework
* 🎨 Tailwind CSS – Utility-first CSS framework
* 📈 Chart.js – Interactive charts
* 📊 React Chart.js 2 – React wrapper for Chart.js

### 🔹 Backend

* 🐍 Flask – Python web framework
* 🌐 BeautifulSoup4 – Web scraping library
* 🔑 ScraperAPI – Professional scraping service
* 🧠 TextBlob – Natural language processing
* 🔄 Flask-CORS – Cross-origin support

---

## 📦 Installation

### ✅ Prerequisites

* Python **3.8+**
* Node.js **16+**
* npm or yarn

---

### ⚙️ Backend Setup

```bash
# Clone repository
git clone <repository-url>
cd major_major

# Navigate to backend
cd backend

# Create and activate virtual environment
python -m venv venv

# On Windows
venv\Scripts\activate
# On macOS/Linux
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

Create a `.env` file in the `backend` directory:

```
SCRAPER_API_KEY=your_scraper_api_key_here
```

Run the backend server:

```bash
python app.py
```

📍 Backend runs on: `http://localhost:5000`

---

### 🎨 Frontend Setup

```bash
cd frontend

# Install dependencies
npm install

# Start development server
npm start
```

📍 Frontend runs on: `http://localhost:3000`

---

## 🎯 Usage

### 🌐 Web Application

1. Open your browser → `http://localhost:3000`
2. Enter a product name (e.g., `"iPhone"`, `"laptop"`, `"headphones"`)
3. Click **Search**
4. View results:

   * 📊 Sentiment distribution chart
   * 📝 Review cards with sentiment tags
   * ⭐ Sentiment polarity scores

### 🔌 API Usage

**Get Product Reviews**

```bash
GET /api/reviews?product=<product_name>
```

Example:

```bash
curl "http://localhost:5000/api/reviews?product=iphone"
```

Response:

```json
{
  "product": "iphone",
  "query_type": "search",
  "reviews": [
    {
      "product": "Apple iPhone 13",
      "review": "Great phone with excellent camera quality...",
      "title": "Product Review",
      "rating": null,
      "sentiment": "positive",
      "polarity": 0.8
    }
  ],
  "total_reviews": 15
}
```

---

## 📚 API Documentation

### **Endpoints**

#### `GET /api/reviews`

Fetches product reviews with sentiment analysis.

**Parameters:**

* `product` *(required)* → Name of product

**Response:**

* `product` → Product name
* `query_type` → Always `"search"`
* `reviews` → Array of review objects
* `total_reviews` → Count of reviews

**Review Object:**

* `product` – Product name
* `review` – Review text
* `title` – Review title
* `rating` – Product rating (if available)
* `sentiment` – Positive / Negative / Neutral
* `polarity` – Sentiment score (-1 to 1)

#### `GET /`

Health check endpoint.

Response:

```json
{
  "message": "Amazon Review Scraper API is running!",
  "usage": {
    "search_by_name": "/api/reviews?product=iphone"
  }
}
```

---

## 📁 Project Structure

```
major_major/
├── backend/
│   ├── app.py               # Main Flask app
│   ├── requirements.txt     # Python dependencies
│   ├── scrapers/
│   │   └── scraper_api.py   # Amazon scraping logic
│   └── sentiment.py         # Sentiment analysis module
├── frontend/
│   ├── public/
│   │   └── index.html       # Template
│   ├── src/
│   │   ├── App.js           # Root React component
│   │   ├── index.js         # Entry point
│   │   ├── index.css        # Global styles
│   │   └── components/
│   │       ├── SearchBar.js       # Search input
│   │       ├── ReviewsList.js     # Review cards
│   │       └── SentimentChart.js  # Chart component
│   ├── package.json         # Node.js dependencies
│   └── tailwind.config.js   # Tailwind config
└── README.md                # Documentation
```

---

## 🔧 Configuration

### Environment Variables

Create `.env` in `backend/`:

```
SCRAPER_API_KEY=your_scraper_api_key_here
```

### ScraperAPI Setup

* Sign up at [ScraperAPI](https://www.scraperapi.com)
* Get your API key
* Add it to `.env`

---

## 🚀 Deployment

### Backend

#### ▶️ Heroku

```bash
# Install Heroku CLI
heroku create your-app-name
git push heroku main
```

#### ▶️ PythonAnywhere

* Upload backend files
* Set up web app
* Add environment variables

### Frontend

#### ▶️ Build & Deploy

```bash
cd frontend
npm run build
```

Deploy to **Netlify** or **Vercel**:

* Connect repo
* Set build command: `npm run build`
* Publish directory: `build`

---

## 🤝 Contributing

1. 🍴 Fork the repo
2. 🌿 Create feature branch → `git checkout -b feature/amazing-feature`
3. 💬 Commit → `git commit -m "Add feature"`
4. 🚀 Push → `git push origin feature/amazing-feature`
5. 🔄 Open Pull Request

---

## 📝 License

Licensed under **MIT License** – see [LICENSE](LICENSE).

---

## 🐛 Troubleshooting

* **❌ ScraperAPI Key Error** → Check `.env` file and API key validity
* **⚠️ CORS Issues** → Ensure backend runs on `5000` and Flask-CORS is enabled
* **🔍 No Reviews Found** → Try another product / verify API plan
* **❌ Frontend Not Loading** → Run `npm install` + check backend status
* **🐞 Debug Mode** → Run:

  ```bash
  python app.py
  ```

---

## 📞 Support

* Check **Troubleshooting** section
* Review **API Documentation**
* Open a GitHub **Issue**

---

## 🔮 Future Enhancements

* 🛒 Support multiple e-commerce platforms
* 🎯 Advanced filtering & search options
* 📂 Export reviews (CSV / JSON)
* 🔐 User authentication & saved history
* 📱 Mobile app version

---

💡 *Made with ❤️ by MADHU VARSHA M C*
📌 *For educational purposes. Please respect Amazon’s Terms of Service.*

---

Would you like me to also **add GitHub badges** (React ⚛️, Flask 🐍, License 📄, Internship recognition 🎓) at the top of the README so it looks even more professional?
