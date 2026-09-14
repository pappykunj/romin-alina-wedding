# 🚀 Deployment & Update Guide

A quick reference guide for deploying updates to **Firebase Hosting** and **GitHub Pages**.

---

## 📁 File Structure Overview
- `index.html` (Root) ➔ Used by **GitHub Pages**
- `public/index.html` ➔ Used by **Firebase Hosting**
- `wedding_invitation.jpg` & `engagement_invitation.jpg` ➔ High-res invitation card images (must exist in both root and `public/`)

---

## ⚡ Quick 1-Liner Deploy (Recommended)
Whenever you make changes to `index.html` or assets, run this single command to sync, commit, push to GitHub, and deploy to Firebase:

```bash
cp index.html wedding_invitation.jpg engagement_invitation.jpg public/ && git add . && git commit -m "Update website" && git push origin main && npx -y firebase-tools deploy
```

---

## 🛠️ Step-by-Step Guide

### Step 1: Sync Root Files to the `public/` Folder
Firebase serves files from the `public/` folder, while GitHub Pages serves from root (`/`). Sync your changes:
```bash
cp index.html wedding_invitation.jpg engagement_invitation.jpg public/
```

---

### Step 2: Push to GitHub (Updates GitHub Pages & Codebase)
```bash
git add .
git commit -m "Your update message"
git push origin main
```

---

### Step 3: Deploy to Firebase Hosting
```bash
npx -y firebase-tools deploy
```

---

## 🌐 Live URLs
- **Firebase Hosting**: [https://romin-alina.web.app](https://romin-alina.web.app)
- **GitHub Repository / Pages**: [https://github.com/pappykunj/romin-alina-wedding](https://github.com/pappykunj/romin-alina-wedding)
