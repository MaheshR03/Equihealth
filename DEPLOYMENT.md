# 🚀 EquiHealth Deployment Guide

## 🌐 Deployment Options

### **🥇 Recommended: Render (Best for Beginners)**

Render is perfect for EquiHealth because it offers:
- **Free tier** with sufficient resources for healthcare applications
- **Automatic HTTPS** and custom domains
- **Seamless GitHub integration** for continuous deployment
- **Persistent disk storage** for ML models
- **Environment variables** for secure configuration

#### **Deploy to Render:**

1. **Prepare your repository**
   ```bash
   # Create a Procfile in your root directory
   echo "web: python app.py" > Procfile
   
   # Update app.py to use environment PORT
   # Add this line to app.py:
   # app.run(host='0.0.0.0', port=int(os.environ.get('PORT', 5000)))
   ```

2. **Create account and connect**
   - Sign up at [render.com](https://render.com)
   - Connect your GitHub repository
   - Select "Web Service" as service type

3. **Configure deployment**
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `python app.py`
   - **Python Version**: 3.8+
   - **Environment Variables**:
     ```
     FLASK_ENV=production
     SECRET_KEY=your-secure-secret-key-here
     ```

4. **Deploy**
   - Click "Create Web Service"
   - Automatic deployment from GitHub pushes

### **🚀 Alternative: Railway**

Modern platform with excellent Python support:

1. **Install Railway CLI**
   ```bash
   npm install -g @railway/cli
   railway login
   ```

2. **Deploy from project directory**
   ```bash
   railway deploy
   ```

### **🐍 Alternative: PythonAnywhere**

Python-focused hosting platform:

1. **Upload files** via web interface
2. **Install packages** in Bash console:
   ```bash
   pip3.8 install --user -r requirements.txt
   ```
3. **Configure web app** in Web tab
4. **Set WSGI file** to point to your Flask app

### **☁️ Advanced: Heroku**

Enterprise-grade platform (paid):

1. **Install Heroku CLI**
2. **Create app**
   ```bash
   heroku create your-equihealth-app
   ```
3. **Deploy**
   ```bash
   git push heroku main
   ```

### **📋 Pre-Deployment Checklist**

Before deploying, ensure you have:

- [ ] **Updated requirements.txt** with all dependencies
- [ ] **Environment variables** for sensitive data
- [ ] **Production-ready Flask configuration**
- [ ] **Static file serving** properly configured
- [ ] **Database connection** (if using external DB)
- [ ] **ML model files** included in repository
- [ ] **HTTPS redirect** enabled
- [ ] **Error handling** for production environment

### **🔧 Production Configuration**

Create a `config.py` file for production settings:

```python
import os

class Config:
    SECRET_KEY = os.environ.get('SECRET_KEY') or 'dev-secret-key'
    FLASK_ENV = os.environ.get('FLASK_ENV') or 'development'
    DEBUG = False if FLASK_ENV == 'production' else True
```

Update your `app.py`:

```python
import os
from config import Config

app.config.from_object(Config)

if __name__ == '__main__':
    port = int(os.environ.get('PORT', 5000))
    app.run(host='0.0.0.0', port=port, debug=app.config['DEBUG'])
```

### **🔒 Security Considerations**

- **Environment Variables**: Store sensitive data (API keys, secret keys)
- **HTTPS**: Ensure SSL/TLS encryption for data transmission
- **Input Validation**: Sanitize all user inputs
- **File Upload Limits**: Restrict file sizes and types
- **Rate Limiting**: Implement request throttling for API endpoints
- **Session Security**: Use secure session configurations

### **📊 Monitoring & Analytics**

Post-deployment monitoring:

- **Uptime Monitoring**: Use services like UptimeRobot
- **Error Tracking**: Implement logging for production errors
- **Performance**: Monitor response times and resource usage
- **User Analytics**: Track usage patterns and feature adoption
3. Configure web app to point to app.py

## Production Checklist
- [ ] Environment variables set
- [ ] HTTPS enabled
- [ ] Error logging configured
- [ ] File upload limits set
- [ ] Database backup (if applicable)
- [ ] Domain configured (optional)

## Troubleshooting

### Common Issues:
1. **Import errors**: Check requirements.txt
2. **Port binding**: Ensure app.py uses PORT environment variable
3. **File paths**: Use relative paths for static files
4. **Memory limits**: Optimize ML model loading

### Support:
- Check deployment logs in platform dashboard
- Verify all environment variables are set
- Test locally with production configuration
