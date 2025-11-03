# 🚀 Quick Start Guide

Get your Machine Learning Notes website up and running in 5 minutes!

---

## ⚡ Super Quick Start (TL;DR)

```bash
# 1. Build the site
python3 build.py

# 2. Open in browser
cd site && python3 -m http.server 8000

# 3. Visit http://localhost:8000
```

That's it! Your website is running! 🎉

---

## 📋 Prerequisites

Before you start, make sure you have:

- ✅ Python 3.7 or higher
- ✅ pip (Python package manager)
- ✅ Git (for version control)
- ✅ A web browser

### Check Your Python Version
```bash
python3 --version
# Should show: Python 3.7.x or higher
```

---

## 🛠️ Step-by-Step Setup

### Step 1: Install Dependencies

First time only - install required Python packages:

```bash
# Install from requirements.txt
pip install -r requirements.txt
```

This installs:
- `markdown` - Converts .md files to HTML
- `Pygments` - Syntax highlighting for code

### Step 2: Build the Website

Generate HTML files from markdown:

```bash
python3 build.py
```

You should see:
```
Wrote 4Q1.html
Wrote 4Q2.html
Wrote 4Q3.html
...
Wrote Q28.html
Generated index.html with modern UI
Site generated in: /workspaces/Machine-learning-notes/site
```

### Step 3: Start Local Server

```bash
cd site
python3 -m http.server 8000
```

You should see:
```
Serving HTTP on 0.0.0.0 port 8000 (http://0.0.0.0:8000/) ...
```

### Step 4: Open in Browser

Visit: **http://localhost:8000**

You should see:
- 🎓 Machine Learning Notes header
- Search bar
- Filter tabs
- All question cards

---

## 🎯 First Time Tour

### 1. Browse Questions
- Scroll through the cards on the main page
- Each card shows a question with unit and marks

### 2. Try Search
- Type "machine" in the search bar
- Watch questions filter in real-time

### 3. Filter by Unit
- Click "Unit 1" tab
- See only Unit 1 questions

### 4. Open a Question
- Click any question card
- Read the full answer
- Click "Back to Questions" to return

### 5. Bookmark a Question
- Click the bookmark icon (🔖) on any card
- See it change to a star (⭐)
- Notice the count increase in header

### 6. View Bookmarks
- Click the "Bookmarks" button in header
- See your saved questions
- Click any to navigate

### 7. Test Mobile View
- Resize your browser window
- Or open on your phone
- Watch the layout adapt

---

## 📱 Access from Phone

### Option 1: Same Network

1. Find your computer's IP address:
   ```bash
   # On Linux/Mac
   hostname -I
   # or
   ifconfig | grep "inet "
   ```

2. On your phone, open browser and go to:
   ```
   http://YOUR_IP:8000
   ```
   Example: `http://192.168.1.100:8000`

### Option 2: Deploy Online

See [DEPLOYMENT.md](DEPLOYMENT.md) for full deployment guide.

Quick deploy to Netlify:
1. Push to GitHub
2. Go to netlify.com
3. Sign in with GitHub
4. Import repository
5. Deploy!

---

## 🔄 Making Changes

### Add a New Question

1. **Create markdown file**
   ```bash
   # Create Q29.md
   vim Q29.md
   ```

2. **Add to QUESTION_MAP in build.py**
   ```python
   QUESTION_MAP = {
       # ... existing questions ...
       'Q29.md': ('Your question title', 'Unit 4', '8 marks'),
   }
   ```

3. **Rebuild**
   ```bash
   python3 build.py
   ```

4. **Refresh browser**
   - Question appears automatically!

### Edit Existing Question

1. **Edit the .md file**
   ```bash
   vim Q4.md
   # Make your changes
   ```

2. **Rebuild**
   ```bash
   python3 build.py
   ```

3. **Refresh browser**
   - Changes appear immediately!

### Change Styling

1. **Edit CSS**
   ```bash
   vim static/style.css
   ```

2. **Rebuild**
   ```bash
   python3 build.py
   ```

3. **Hard refresh browser**
   - Ctrl+Shift+R (Windows/Linux)
   - Cmd+Shift+R (Mac)

---

## 🐛 Troubleshooting

### "Command not found: python3"
**Solution**: Try `python` instead:
```bash
python --version
python build.py
```

### "No module named 'markdown'"
**Solution**: Install dependencies:
```bash
pip install markdown Pygments
# or
pip install -r requirements.txt
```

### "Address already in use"
**Solution**: Port 8000 is taken, use different port:
```bash
python3 -m http.server 8001
```
Then visit http://localhost:8001

### "Permission denied"
**Solution**: Use sudo or different port:
```bash
python3 -m http.server 8080
```

### Website loads but no styling
**Solution**: Check that static folder exists:
```bash
ls site/static/
# Should show: script.js  style.css
```

If missing, rebuild:
```bash
python3 build.py
```

### Bookmarks not saving
**Solution**: 
- Check browser console for errors (F12)
- Try a different browser
- Clear browser cache

### Mobile view not working
**Solution**:
- Clear browser cache
- Try incognito/private mode
- Check responsive design mode (F12 → Toggle device toolbar)

---

## 💡 Pro Tips

### Development Workflow

1. **Keep server running**
   ```bash
   cd site && python3 -m http.server 8000
   ```

2. **In another terminal, make changes**
   ```bash
   vim Q4.md
   python3 build.py
   ```

3. **Refresh browser** to see changes

### Using Virtual Environment (Recommended)

```bash
# Create virtual environment
python3 -m venv .venv

# Activate it
source .venv/bin/activate  # Linux/Mac
.venv\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt

# Now build and run
python3 build.py
cd site && python3 -m http.server 8000

# When done, deactivate
deactivate
```

### Git Workflow

```bash
# Stage changes
git add .

# Commit with message
git commit -m "Added Q29 and updated styling"

# Push to GitHub
git push origin main

# If deployed on Netlify, it auto-deploys!
```

---

## 📚 Learn More

- [FEATURES.md](FEATURES.md) - Detailed feature guide
- [DEPLOYMENT.md](DEPLOYMENT.md) - Deploy to internet
- [VISUAL_GUIDE.md](VISUAL_GUIDE.md) - Visual tour
- [IMPLEMENTATION_SUMMARY.md](IMPLEMENTATION_SUMMARY.md) - Technical details

---

## ✅ Checklist

Before sharing with others:

- [ ] Built the site successfully
- [ ] Tested locally (http://localhost:8000)
- [ ] Tried search functionality
- [ ] Tested bookmark feature
- [ ] Checked on mobile device
- [ ] All questions accessible
- [ ] No console errors (F12)
- [ ] Deployed online (optional)

---

## 🎉 Success!

If you can see the website at http://localhost:8000 with:
- ✅ Header with "ML Notes"
- ✅ Search bar
- ✅ Filter tabs
- ✅ Question cards
- ✅ Bookmark functionality

**Congratulations! Your website is working perfectly! 🎊**

---

## 🆘 Need Help?

1. **Read the error message** - Often tells you what's wrong
2. **Check documentation** - See other .md files
3. **Google the error** - Someone probably solved it
4. **Check browser console** - F12 key, look for red errors
5. **Try incognito mode** - Rules out cache issues

---

## 🌟 Next Steps

1. ✅ Bookmark your favorite questions
2. ✅ Test on your phone
3. ✅ Share with classmates (deploy online)
4. ✅ Customize colors (edit style.css)
5. ✅ Add more questions (create new .md files)

---

**Happy Studying! 📖✨**

*The website is fast, modern, and ready to help you ace your Machine Learning exam!* 🚀
