# 🏥 EquiHealth - Healthcare Analytics Platform

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)](https://flask.palletsprojects.com/)
[![Machine Learning](https://img.shields.io/badge/ML-XGBoost-orange.svg)](https://xgboost.readthedocs.io/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **Empowering data-driven healthcare decisions through advanced analytics and visualization**

EquiHealth is a comprehensive web-based healthcare analytics platform that leverages machine learning to analyze health metrics, predict outcomes, and visualize healthcare accessibility across different regions. The platform enables healthcare professionals, policymakers, and researchers to make informed decisions based on comprehensive data analysis.

## 🌟 Features

### 📊 **Data Analytics & Visualization**
- **Interactive Data Upload**: Support for CSV files with flexible column mapping
- **Real-time Data Processing**: Instant analysis of healthcare metrics
- **Interactive Geographic Visualization**: Plotly-powered maps with hover functionality and zoom capabilities
- **User-Specific Data Management**: Session-based data isolation for multi-user support
- **Comprehensive Reports**: Detailed analytics with downloadable results and scrollable data tables

### 🤖 **Machine Learning Capabilities**
- **Predictive Modeling**: XGBoost-powered health outcome predictions with hyperparameter optimization
- **Risk Assessment**: Advanced algorithms for healthcare risk evaluation
- **Data Standardization**: Automated preprocessing and feature scaling with StandardScaler
- **Model Persistence**: Trained models saved for consistent predictions using joblib serialization
- **Real-time Predictions**: Live model inference on uploaded healthcare data

### 🎨 **Modern User Interface**
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Glassmorphism UI**: Modern, professional interface with backdrop blur effects and transparent overlays
- **Intuitive Navigation**: Fixed navigation bars with context-aware links and smooth transitions
- **Session-Based Authentication**: Secure user login/signup with password hashing and session management
- **Flash Message System**: Real-time user feedback with animated notifications
- **Accessibility**: High contrast design with enhanced readability and ARIA compliance

### 📈 **Healthcare Metrics Analysis**
- **Disease Tracking**: TB, Diabetes, Malaria, HIV/AIDS incidence analysis
- **Public Health Indicators**: Infant Mortality Rate (IMR) monitoring
- **Vaccination Coverage**: Immunization rate tracking and analysis
- **Socioeconomic Factors**: Income level correlation with health outcomes

## 🚀 Getting Started

### Prerequisites

- **Python 3.8+**
- **pip** (Python package installer)
- **Modern web browser** (Chrome, Firefox, Safari, Edge)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/MaheshR03/equihealth.git
   cd equihealth
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   python app.py
   ```

4. **Access the platform**
   Open your browser and navigate to `http://localhost:5000`

## 🛠️ Tech Stack

### **Backend Technologies**
- **Flask** - Lightweight WSGI web application framework
- **Python** - Core programming language
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing library
- **Scikit-learn** - Machine learning utilities and preprocessing

### **Machine Learning**
- **XGBoost** - Gradient boosting framework for predictive modeling
- **StandardScaler** - Feature normalization and standardization
- **Pickle** - Model serialization and persistence

### **Data Visualization**
- **Plotly Integration** - Interactive maps with hover tooltips and zoom functionality
- **HTML Map Generation** - Dynamic visualization files for user-specific data
- **Responsive Iframes** - Seamless integration of interactive content
- **Color-coded Visualizations** - Intuitive data representation with prediction-based coloring

### **Frontend Technologies**
- **HTML5** - Semantic markup language with modern form elements
- **CSS3** - Advanced styling with glassmorphism effects, animations, and responsive grids
- **JavaScript** - Interactive user interface elements, form validation, and enhanced UX
- **Responsive Design** - Mobile-first approach with flexible layouts and adaptive navigation

### **Development Tools**
- **Flask Debug Mode** - Development server with hot reload and error tracking
- **CSV Processing** - Flexible data import capabilities with intelligent column mapping
- **Static File Serving** - Efficient asset delivery with proper MIME type handling
- **Session Management** - Secure user authentication with Werkzeug password hashing
- **Interactive Maps** - Plotly-powered visualizations with user-specific file generation

## 📋 Usage Guide

### **1. User Authentication**
- Create an account or login to access personalized features
- Secure session management ensures data privacy and user isolation
- Password protection with industry-standard hashing

### **2. Data Upload**
- Navigate to the **Upload** page (authentication required)
- Prepare your CSV file with required healthcare columns:
  - District, Latitude, Longitude
  - TB Incidence, Diabetes Prevalence
  - Malaria Incidence, HIV/AIDS Prevalence
  - IMR, Vaccination Rate, Income Level
- Upload your CSV file for real-time analysis and ML predictions

### **3. View Results**
- Access the **Report** page to view processed data in interactive tables
- Download analysis results in CSV format with user-specific predictions
- Review ML-generated scores and comprehensive health metrics

### **4. Interactive Geographic Analysis**
- Visit the **Map** page for dynamic visual representation
- Hover over data points to see detailed district information and predictions
- Zoom and pan through interactive maps powered by Plotly
- Analyze healthcare accessibility patterns across regions

### **5. Resource Access**
- Browse the **Resources** page for external health databases
- Access WHO, CDC, and Indian health ministry data
- Find relevant research and policy documents

## 🏗️ Project Structure

```
equihealth/
├── app.py                 # Main Flask application with authentication & ML integration
├── requirements.txt       # Python dependencies (updated with Plotly)
├── README.md             # Comprehensive project documentation
├── health_data.csv       # Sample healthcare dataset
├── predictions.csv       # ML model output
├── test_upload.csv       # Sample test data for demonstrations
├── health-data/          # Model storage directory
│   ├── predictionmodel.pkl # Trained XGBoost model
│   └── scaler.pkl        # StandardScaler for feature normalization
├── static/               # Static assets
│   ├── styles.css        # Enhanced stylesheet with glassmorphism design
│   ├── scripts.js        # JavaScript for interactive UX features
│   ├── health_data.csv   # Sample data for download
│   └── maps/             # User-specific interactive map storage
│       └── *.html        # Plotly-generated interactive maps per user
├── templates/            # HTML templates with unified navigation
│   ├── frontpage.html    # Modern landing page
│   ├── login.html        # User authentication interface
│   ├── signup.html       # User registration interface
│   ├── upload.html       # Data upload interface with validation
│   ├── report.html       # Analysis results with scrollable tables
│   ├── result.html       # Prediction results with professional styling
│   ├── show-map.html     # Interactive geographic visualization
│   ├── resource.html     # External resources and links
│   └── about.html        # Platform information and features
└── healthcare_access_xgboost_model.ipynb     # ML model development notebook (XGBoost training)
```

## 🔬 Machine Learning Pipeline

### **Data Preprocessing**
1. **Column Standardization**: Flexible mapping of CSV columns to expected features with intelligent name recognition
2. **Missing Value Handling**: Intelligent imputation for incomplete data with validation checks
3. **Feature Scaling**: StandardScaler normalization for optimal model performance and consistency
4. **Data Validation**: Comprehensive checks for data integrity and user-friendly error messages
5. **User Data Isolation**: Session-based data management ensuring privacy and multi-user support

### **Model Architecture**
- **Algorithm**: XGBoost Classifier with hyperparameter optimization using RandomizedSearchCV
- **Training Pipeline**: SMOTE-ENN for class balancing and robust model training
- **Feature Engineering**: Automated creation of derived health indicators and geographic features
- **Cross-validation**: 5-fold validation ensures model generalization and reliability
- **Model Persistence**: Joblib serialization for consistent inference across sessions

### **Prediction Output**
- **Health Risk Classifications**: Multi-class predictions (Very Low to Very High Access)
- **Interactive Visualizations**: Real-time map generation with color-coded predictions
- **Confidence Metrics**: Statistical measures of prediction reliability and model performance
- **Regional Comparisons**: Benchmarking against similar geographic areas and historical data

## 🎯 Key Advantages

### **🚀 Performance**
- **Fast Processing**: Optimized algorithms for real-time analysis with efficient data pipelines
- **Scalable Architecture**: Handles datasets from small studies to national surveys with session management
- **Efficient Memory Usage**: Streamlined data processing pipelines with user-specific storage
- **Interactive Visualizations**: Plotly-powered maps with smooth zoom and hover functionality

### **👥 User Experience**
- **Intuitive Interface**: No technical expertise required with guided workflows
- **Responsive Design**: Works seamlessly across all devices with adaptive layouts
- **Comprehensive Authentication**: Secure login system with session-based data isolation
- **Real-time Feedback**: Interactive flash messages and progress indicators

### **🔒 Reliability**
- **Robust Error Handling**: Graceful handling of edge cases with user-friendly error messages
- **Data Validation**: Comprehensive input verification with intelligent column mapping
- **Model Persistence**: Consistent predictions across sessions using trained XGBoost models
- **Session Security**: Protected user data with secure password hashing and session management

### **🌐 Accessibility**
- **Web-based Platform**: No software installation required with modern browser support
- **Cross-platform Compatibility**: Works on Windows, macOS, and Linux with responsive design
- **Multi-format Support**: Flexible CSV import with intelligent column recognition
- **Interactive Features**: Hover tooltips, zoom controls, and accessible navigation

## 📊 Use Cases

### **Healthcare Policy**
- **Resource Allocation**: Identify underserved regions requiring healthcare investment
- **Program Evaluation**: Assess effectiveness of public health interventions
- **Trend Analysis**: Monitor long-term health outcome improvements

### **Research Applications**
- **Epidemiological Studies**: Analyze disease patterns and correlations
- **Health Equity Research**: Investigate healthcare disparities
- **Predictive Analytics**: Forecast future healthcare needs

### **Clinical Decision Support**
- **Population Health**: Understand community health profiles
- **Risk Stratification**: Identify high-risk patient populations
- **Intervention Planning**: Target resources for maximum impact

## 🤝 Contributing

We welcome contributions to improve EquiHealth! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

For questions, suggestions, or support:

- **Email**: contact@equihealth.com
- **Documentation**: [Project Wiki](https://github.com/MaheshR03/equihealth/wiki)
- **Issues**: [GitHub Issues](https://github.com/MaheshR03/equihealth/issues)

## 🔮 Future Enhancements

- **Enhanced ML Models**: Deep learning integration for complex health pattern recognition
- **Real-time Data Feeds**: Live healthcare data integration from government APIs
- **Advanced Analytics Dashboard**: Comprehensive KPI tracking and trend analysis
- **API Development**: RESTful endpoints for external systems and third-party integrations
- **Multi-language Support**: Internationalization for global healthcare applications
- **Mobile Application**: Native iOS and Android apps with offline capability
- **Advanced Visualizations**: 3D geographic rendering and time-series animations
- **Collaborative Features**: Multi-user data sharing and team-based analysis tools

---

## 📅 Recent Updates (July 2025)

### **🎯 Major Enhancements Implemented:**

✅ **Interactive Map Visualization**
- Upgraded from static matplotlib to dynamic Plotly maps
- Added hover functionality showing district details and predictions
- Implemented zoom and pan capabilities for detailed exploration

✅ **User Authentication & Session Management**
- Complete login/signup system with secure password hashing
- Session-based data isolation for multi-user support
- User-specific map generation and data storage

✅ **Enhanced User Interface**
- Consistent navigation across all pages with context-aware links
- Professional glassmorphism design with backdrop blur effects
- Responsive layouts optimized for all device sizes

✅ **Improved Data Pipeline**
- Intelligent CSV column mapping with flexible naming conventions
- Real-time ML predictions using trained XGBoost models
- Enhanced error handling with user-friendly feedback messages

✅ **Technical Infrastructure**
- Plotly integration for interactive visualizations
- User-specific file generation for maps and reports
- Enhanced CSS framework with modern styling patterns

---

<div align="center">

**Built with ❤️ for better healthcare outcomes**

[Website](https://equihealth.com) • [Documentation](https://docs.equihealth.com) • [Demo](https://demo.equihealth.com)

</div>

## 🚀 Deployment

Ready to deploy EquiHealth to production? Check out our comprehensive deployment guide:

**📋 [View Complete Deployment Guide](DEPLOYMENT.md)**

### Quick Deploy Options:
- **🥇 Render** (Recommended for beginners - Free tier with HTTPS)
- **🚀 Railway** (Modern platform with excellent Python support)
- **🐍 PythonAnywhere** (Python-focused hosting)
- **☁️ Heroku** (Enterprise-grade platform)

The deployment guide includes:
- Step-by-step instructions for each platform
- Production configuration setup
- Security considerations
- Monitoring and analytics setup
- Pre-deployment checklist

---

