# Styling Practice with Bootswatch & Tailwind CSS

Welcome to your post-lecture project! In this activity, you’ll create two versions of a small website for a fictional plant shop called **Leaf & Root** — one using **Bootswatch** and the other using **Tailwind CSS**.

---

## 🧠 Objectives
- Practice using Bootstrap + Bootswatch to style a webpage
- Practice using Tailwind CSS utility classes
- Reinforce concepts from the lecture: layout, header/footer, and cards

---

## ✅ Instructions

### Step 1: Create the Bootswatch Page
1. Inside `bootswatch-version/index.html`, build a simple page with:
   - A **header** (site name or navbar)
   - A **main section** with a card (image, title, text, button)
   - A **footer** with copyright info
2. Add a Bootswatch theme by replacing the Bootstrap CSS CDN:
   ```html
   <!-- bootswatch-version/index.html -->
   <!DOCTYPE html>
   <html lang="en">
   <head>
     <meta charset="UTF-8" />
     <meta name="viewport" content="width=device-width, initial-scale=1.0" />
     <title>Leaf & Root - Bootswatch</title>
     <!-- Replace [theme] with your choice, e.g., cerulean, cyborg, sketchy -->
     <link href="https://cdn.jsdelivr.net/npm/bootswatch@5.3.2/dist/[theme]/bootstrap.min.css" rel="stylesheet">
   </head>
   <body>
     <!-- Add header, card, and footer here -->
   </body>
   </html>
   ```

### Step 2: Create the Tailwind Page

#### Option A: Use Tailwind via NPM (Full Setup)
1. Create a new folder for your Tailwind project and run:
   ```bash
   npm init -y
   npm install -D tailwindcss
   npx tailwindcss init
   ```
2. Create a folder structure:
   ```
   tailwind-version/
   ├── index.html
   ├── styles/
   │   └── input.css
   └── dist/
       └── output.css
   ```
3. In `styles/input.css`, add:
   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```
4. Update your `package.json` with a build script:
   ```json
   "scripts": {
     "build": "npx tailwindcss -i ./styles/input.css -o ./dist/output.css --watch"
   }
   ```
5. Link the compiled CSS in `index.html`:
   ```html
   <link href="./dist/output.css" rel="stylesheet">
   ```
6. Build the CSS:
   ```bash
   npm run build
   ```

### Step 3: Compare and Reflect
- How does styling feel different with Bootswatch vs. Tailwind?
- Which do you prefer for custom design?

---

## 🧰 Helpful Resources

### 🔹 Bootswatch
- Browse themes: https://bootswatch.com/
- Bootstrap Docs: https://getbootstrap.com/docs/5.3/getting-started/introduction/

### 🔹 Tailwind CSS
- Tailwind Docs: https://tailwindcss.com/docs
- Tailwind Play (code playground): https://play.tailwindcss.com/
- Tailwind Cheat Sheet: https://nerdcave.com/tailwind-cheat-sheet

---

## 🌟 Bonus Challenge
Try creating a second card or making your layout responsive with Bootstrap's grid or Tailwind's flex/grid utilities!
