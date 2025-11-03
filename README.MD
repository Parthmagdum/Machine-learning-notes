# Quetions

# *UNIT 1*

### Unit 1 - 4 marks 
---
Q. Explain diffrent phases of predictive modeling (8 phases) [Click Here](4Q1.md)

Q. Advantages and Disadvantages of K-nearest neighbor algorithm [Click Here](4Q2.md)

Q. Define Machine Learning and explain features of machine learning [Click Here](4Q3.md)


### Unit 1 - 8 marks
---
Q. Explain Diffrence between Artificial Intelligence and Machine learning [Click Here](Q4.md)

Q. Explain Development steps in Machine Learning [Click Here](Q5.md)

Q. Explain K-nearest nighbor algorithm in detail [Click Here](Q6.md)

---


# *UNIT 2*

### Unit 2 - 4 marks
---
Q. State the goals of Machine Learning [Click Here](Q7.md)

Q. Write a note on speech Recognition and production recommendations [click here](Q8.md)

Q. Advantages and Disadvantages of machine learning [Click Here](Q9.md)

Q. Write a note on function approximation [Click Here](Q10.md)

### Unit 2 - 8 Marks
---
Q. Explain in detail the application of Machine learning [Click Here](Q11.md)

Q. What is the need for ML? Explain in detail classification of ML [Click Here](Q12.md)

Q. Explain steps to design a learning system [Click Here](Q13.md)

---
# *UNIT 3*
### Unit 3 - 4 marks
---
Q. Explain bias and variance with example[Click here](Q14.md)

Q. Write a short note on confusion matrix [Click here](Q15.md)

Q. How to treat data in ML [Click here](Q16.md)

Q. What is Data pre-processing? Why do we need it ? [Click here](Q17.md)

Q. Explain performance measures of ML [Click here](Q18.md)

Q. Write a note on bootstrap sampling [Click here](Q19.md)

Q. Difference between bagging and boosting [Click here](Q20.md)

Q. Write a note on bagging aggregatiion [Click here](Q21.md)

---
### Unit 3 - 8 marks
---

Q. Explain in detail types of ML [Click here](Q22.md)

Q. what is bias and variance ? Explain in detail [Click here](Q23.md)

Q. What is bias and variance and what is Bias-variance tradeof ? [Click here](Q24.md)

Q. Explain overfitting and underfitting in ML [Click here](Q25.md)


---
# *UNIT 4*
---

Q. State and prove baye's theorem with example [Click here](Q26.md)

Q. What is probability ? What are the rules of probability  [Click here](Q27.md)

Q. Difference between permutation and combination  [Click here](Q28.md)

---

## Notes website generator

This repository includes a modern static site generator that transforms markdown notes into an interactive, mobile-responsive website with the following features:

### ✨ Features

- **🎨 Modern Dark UI**: Beautiful dark theme with smooth animations and transitions
- **📱 Mobile Responsive**: Fully optimized for all device sizes (desktop, tablet, mobile)
- **🔖 Bookmark System**: Save your favorite questions with persistent localStorage
- **🔍 Smart Search**: Real-time search across all questions
- **🏷️ Filter by Unit**: Quick filtering by Unit 1, 2, 3, or 4
- **📊 Question Cards**: All questions displayed in an organized card layout
- **⚡ Fast Navigation**: Click any question card to view the answer
- **💾 Auto-save Bookmarks**: Bookmarks are saved in your browser and persist across sessions

### 🚀 Quick start to build the site locally:

1. (Optional but recommended) create and activate a Python virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Build the site:

```bash
python3 build.py
```

The generated site will be written to the `site/` directory. Open `site/index.html` in your browser to view.

Alternatively, start a local server:

```bash
cd site
python3 -m http.server 8000
```

Then open http://localhost:8000 in your browser.

### 📁 Files added:

- `build.py` — Enhanced generator script that converts each `.md` into an HTML page with modern UI
- `templates/base.html` — Responsive HTML template with bookmark functionality
- `static/style.css` — Modern dark theme with mobile-responsive design
- `static/script.js` — JavaScript for bookmarks, search, and filter functionality
- `requirements.txt` — Python dependencies (markdown, pygments)

### 🎯 How to use the website:

1. **Browse Questions**: All questions are displayed as cards on the main page
2. **Search**: Use the search bar to find specific questions
3. **Filter**: Click unit tabs to filter by Unit 1, 2, 3, or 4
4. **Bookmark**: Click the bookmark icon on any question card or question page
5. **View Bookmarks**: Click the bookmark button in the header to see all saved questions
6. **Mobile**: The site automatically adapts to your screen size

## Deploying on Netlify

This project includes a `netlify.toml` so Netlify can build and publish the site automatically.

What Netlify will run (configured in `netlify.toml`):

- Install Python dependencies from `requirements.txt`.
- Run `python3 build.py` to create the `site/` directory.
- Publish the `site/` directory as the website.

Quick steps to deploy:

1. Push your repository to GitHub (already done).
2. In Netlify, choose "New site from Git" and connect your GitHub account.
3. Select this repository (`PATILYASHH/Machine-learning-notes`).
4. Netlify will automatically pick up the `netlify.toml` build command and publish directory. If it doesn't, set the build command to:

```text
python3 -m pip install -r requirements.txt && python3 build.py
```

and set the publish directory to:

```text
site
```

Notes and tips
- If you prefer not to commit the generated `site/` files to the repo, add `site/` to `.gitignore` and remove the tracked files with `git rm -r --cached site` before pushing — Netlify will still build the site on its side using the `netlify.toml` build command.
- If your build requires a specific Python version, configure the Python version in the Netlify site UI (Environment > Build image settings) or include any runtime config required by your build environment.
