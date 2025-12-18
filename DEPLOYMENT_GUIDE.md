# 🚀 Deployment Guide - Al Adhwa Lesson Plan Generator

## Option 1: Deploy to Render.com (RECOMMENDED - 100% Free)

### Step 1: Prepare Your Files
1. Download all project files to your computer
2. Create a GitHub account if you don't have one (free)
3. Create a new repository and upload all files

### Step 2: Deploy to Render
1. Go to [render.com](https://render.com) and sign up (free)
2. Click "New +" → "Web Service"
3. Connect your GitHub repository
4. Configure:
   - **Name**: `aladhwa-lessonplan-generator`
   - **Environment**: Python 3
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `gunicorn app:app`
   - **Plan**: Free

5. Click "Create Web Service"
6. Wait 5-10 minutes for deployment
7. Your app will be live at: `https://aladhwa-lessonplan-generator.onrender.com`

### Step 3: Share with Teachers
Copy your Render URL and share it with all teachers!

---

## Option 2: Deploy to Railway.app (Free, Very Easy)

### Step 1: Sign Up
1. Go to [railway.app](https://railway.app)
2. Sign up with GitHub (free)

### Step 2: Deploy
1. Click "New Project" → "Deploy from GitHub repo"
2. Select your repository
3. Railway auto-detects Python and deploys
4. Get your URL: `https://your-app.up.railway.app`

---

## Option 3: Deploy to PythonAnywhere (Free Tier)

### Step 1: Sign Up
1. Go to [pythonanywhere.com](https://www.pythonanywhere.com)
2. Create free account

### Step 2: Upload Files
1. Go to "Files" tab
2. Upload all project files
3. Go to "Consoles" → "Bash"
4. Run: `pip install -r requirements.txt --user`

### Step 3: Configure Web App
1. Go to "Web" tab
2. Click "Add a new web app"
3. Choose "Flask"
4. Set path to your `app.py`
5. Click "Reload"
6. Your URL: `https://yourusername.pythonanywhere.com`

---

## Option 4: Local Network Deployment (School Server)

### For School IT Department:

#### Requirements
- Windows/Linux server with Python 3.9+
- Network access for teachers

#### Installation
```bash
# 1. Install Python 3.9+
# Download from python.org

# 2. Install dependencies
cd aladhwa-lessonplan-generator
pip install -r requirements.txt

# 3. Run the application
python app.py

# App will be available at:
# http://your-server-ip:5000
```

#### Make it Always Running (Windows)
1. Create `start_app.bat`:
```batch
@echo off
cd C:\path\to\aladhwa-lessonplan-generator
python app.py
pause
```

2. Add to Windows Task Scheduler to run on startup

#### Make it Always Running (Linux)
1. Create systemd service `/etc/systemd/system/aladhwa-lessonplan.service`:
```ini
[Unit]
Description=Al Adhwa Lesson Plan Generator
After=network.target

[Service]
User=www-data
WorkingDirectory=/path/to/aladhwa-lessonplan-generator
ExecStart=/usr/bin/python3 app.py
Restart=always

[Install]
WantedBy=multi-user.target
```

2. Enable and start:
```bash
sudo systemctl enable aladhwa-lessonplan
sudo systemctl start aladhwa-lessonplan
```

---

## 🔥 Quick Testing (Before Deployment)

### Test Locally First
1. Open Terminal/Command Prompt
2. Navigate to project folder:
```bash
cd aladhwa-lessonplan-generator
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Run application:
```bash
python app.py
```

5. Open browser: `http://localhost:5000`
6. Test the form and generation

---

## 📊 Monitoring & Maintenance

### Check if App is Running
- Render: Dashboard shows status
- Railway: Dashboard shows logs
- PythonAnywhere: Web tab shows status
- Local: Open URL in browser

### View Logs
- Render: Click "Logs" tab
- Railway: Click "Deployments" → "View logs"
- PythonAnywhere: "Files" → "Log files"

### Update the App
1. Make changes to your files
2. Push to GitHub
3. Render/Railway auto-deploys
4. PythonAnywhere: Re-upload files and reload

---

## 🆘 Troubleshooting

### Problem: App won't start
**Solution**: Check logs for errors, usually missing dependencies

### Problem: Forms not submitting
**Solution**: Check browser console (F12) for JavaScript errors

### Problem: Generated files not downloading
**Solution**: Ensure `output/` folder has write permissions

### Problem: Slow generation
**Solution**: Normal - AI generation takes 1-2 minutes

---

## 🎯 Best Deployment for Your Needs

| Platform | Best For | Speed | Difficulty |
|----------|----------|-------|------------|
| **Render** | Public access, reliable | ⭐⭐⭐⭐⭐ | Easy |
| **Railway** | Quick setup, auto-deploy | ⭐⭐⭐⭐⭐ | Very Easy |
| **PythonAnywhere** | Simple, beginner-friendly | ⭐⭐⭐ | Easy |
| **School Server** | Private network, full control | ⭐⭐⭐⭐ | Medium |

**Recommendation**: Use **Render.com** for best balance of features and ease!

---

## 📱 Sharing with Teachers

### Create QR Code
1. Go to [qr-code-generator.com](https://www.qr-code-generator.com)
2. Enter your deployed URL
3. Download QR code
4. Share in staff meetings or emails

### Email Template
```
Subject: 🎓 NEW: AI Lesson Plan Generator - Free for All Teachers!

Dear Colleagues,

We're excited to introduce the Al Adhwa AI Lesson Plan Generator!

🔗 Access Link: [YOUR_DEPLOYED_URL]

✨ Features:
- Generates complete lesson plans in 2 minutes
- Differentiated tasks (DOK levels 1-4)
- Includes worksheets, rubrics, and PowerPoint
- UAE/ADEK aligned
- 100% FREE to use

Simply click the link, fill the form, and download your package!

Best regards,
[Your Name]
```

---

## 🔐 Security Tips

1. **Don't share sensitive data** in generated files
2. **Use HTTPS** (automatic on Render/Railway)
3. **Regular backups** of template files
4. **Monitor usage** through platform dashboards

---

## ✅ Post-Deployment Checklist

- [ ] App is accessible via URL
- [ ] School logo displays correctly
- [ ] Form accepts all inputs
- [ ] Generation completes successfully
- [ ] ZIP file downloads properly
- [ ] Word documents open correctly
- [ ] PowerPoint displays properly
- [ ] Shared URL with all teachers
- [ ] Created QR code for easy access
- [ ] Bookmarked admin dashboard

---

**Need Help?** Contact your school IT department or refer to platform documentation.

**Congratulations!** 🎉 Your teachers now have a powerful AI lesson planning tool!
