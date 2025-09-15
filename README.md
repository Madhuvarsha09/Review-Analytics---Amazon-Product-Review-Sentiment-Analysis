# Review-Analytics---Amazon-Product-Review-Sentiment-Analysis
ReviewAnalytics - Amazon Product Review Sentiment Analysis
A modern web application that analyzes sentiment from Amazon product reviews using AI-powered insights. Built with React frontend and Flask backend.

ReviewAnalytics React Flask Python

🚀 Features
Product Search: Search for any product on Amazon to get comprehensive reviews
AI Sentiment Analysis: Advanced sentiment analysis with polarity scoring
Interactive Charts: Beautiful pie charts showing sentiment distribution
Modern UI: Clean, responsive design with glassmorphism effects
Real-time Analysis: Instant sentiment analysis of customer reviews
Review Display: Detailed review cards with sentiment indicators
📋 Table of Contents
Features
Tech Stack
Installation
Usage
API Documentation
Project Structure
Contributing
License
🛠 Tech Stack
Frontend
React 18 - Modern UI framework
Tailwind CSS - Utility-first CSS framework
Chart.js - Interactive charts and graphs
React Chart.js 2 - React wrapper for Chart.js
Backend
Flask - Python web framework
BeautifulSoup4 - Web scraping library
ScraperAPI - Professional web scraping service
TextBlob - Natural language processing
Flask-CORS - Cross-origin resource sharing
📦 Installation
Prerequisites
Python 3.8 or higher
Node.js 16 or higher
npm or yarn
Backend Setup
Clone the repository

git clone <repository-url>
cd major_major
Navigate to backend directory

cd backend
Create virtual environment

python -m venv venv
Activate virtual environment

# On Windows
venv\Scripts\activate

# On macOS/Linux
source venv/bin/activate
Install dependencies

pip install -r requirements.txt
Set up environment variables Create a .env file in the backend directory:

SCRAPER_API_KEY=your_scraper_api_key_here
Run the backend server

python app.py
The backend will run on http://localhost:5000

Frontend Setup
Navigate to frontend directory

cd frontend
Install dependencies

npm install
Start the development server

npm start
The frontend will run on http://localhost:3000

🎯 Usage
Web Application
Open your browser and go to http://localhost:3000
Enter a product name in the search bar (e.g., "iPhone", "laptop", "headphones")
Click Search to analyze reviews
View results:
Sentiment distribution chart
Detailed review cards
Sentiment analysis scores
API Usage
Get Product Reviews
GET /api/reviews?product=<product_name>
Example:

curl "http://localhost:5000/api/reviews?product=iphone"
Response:

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
📚 API Documentation
Endpoints
GET /api/reviews
Retrieves product reviews with sentiment analysis.

Parameters:

product (required): Product name to search for
Response:

product: Product name
query_type: Type of query (always "search")
reviews: Array of review objects
total_reviews: Total number of reviews
Review Object:

product: Product name
review: Review text
title: Review title
rating: Product rating (if available)
sentiment: Sentiment label ("positive", "negative", "neutral")
polarity: Sentiment polarity score (-1 to 1)
GET /
Health check endpoint.

Response:

{
  "message": "Amazon Review Scraper API is running!",
  "usage": {
    "search_by_name": "/api/reviews?product=iphone"
  }
}
📁 Project Structure
major_major/
├── backend/
│   ├── app.py                 # Main Flask application
│   ├── requirements.txt      # Python dependencies
│   ├── scrapers/
│   │   └── scraper_api.py   # Amazon scraping logic
│   └── sentiment.py          # Sentiment analysis module
├── frontend/
│   ├── public/
│   │   └── index.html       # HTML template
│   ├── src/
│   │   ├── App.js           # Main React component
│   │   ├── index.js         # React entry point
│   │   ├── index.css        # Global styles
│   │   └── components/
│   │       ├── SearchBar.js      # Search input component
│   │       ├── ReviewsList.js   # Reviews display component
│   │       └── SnetimentChart.js # Chart component
│   ├── package.json         # Node.js dependencies
│   └── tailwind.config.js   # Tailwind configuration
└── README.md               # This file
🔧 Configuration
Environment Variables
Create a .env file in the backend directory:

SCRAPER_API_KEY=your_scraper_api_key_here
ScraperAPI Setup
Sign up at ScraperAPI
Get your API key from the dashboard
Add the API key to your .env file
🚀 Deployment
Backend Deployment
Using Heroku:

# Install Heroku CLI
heroku create your-app-name
git push heroku main
Using Python Anywhere:

Upload your backend files
Set up a web app
Configure environment variables
Frontend Deployment
Build for production:

cd frontend
npm run build
Deploy to Netlify/Vercel:

Connect your GitHub repository
Set build command: npm run build
Set publish directory: build
🤝 Contributing
Fork the repository
Create a feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m 'Add some amazing feature')
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request
📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

🐛 Troubleshooting
Common Issues
ScraperAPI Key Error:

Ensure your .env file is in the backend directory
Verify your ScraperAPI key is valid
CORS Errors:

Make sure the backend is running on port 5000
Check that Flask-CORS is properly configured
No Reviews Found:

Try different product names
Check if the product has reviews on Amazon
Verify your ScraperAPI plan allows the required requests
Frontend Not Loading:

Ensure all dependencies are installed (npm install)
Check if the backend is running
Verify the API URL in the frontend code
Debug Mode
Run the backend with debug mode enabled:

python app.py
Check the console for detailed error messages and API request logs.

📞 Support
If you encounter any issues or have questions:

Check the Troubleshooting section
Review the API Documentation
Open an issue on GitHub
🔮 Future Enhancements
 Support for multiple e-commerce platforms
 Advanced filtering options
 Export functionality
 User authentication
 Review history tracking
 Mobile app development
Made with ❤ by MADHU VARSHA M C

This project is for educational purposes. Please respect Amazon's terms of service and use responsibly.
