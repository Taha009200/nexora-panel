# NEXORA Railway Deployment Guide

## Complete Step-by-Step Deployment

---

## 1. Create Railway Project

1. Go to [https://railway.app](https://railway.app)
2. Sign up or log in to your account
3. Click **"New Project"**
4. Name your project `nexora`
5. Select **"Empty Project"** (we'll add services manually)

---

## 2. Add PostgreSQL

1. In your project, click **"New"** → **"Database"** → **"PostgreSQL"**
2. Railway will create a PostgreSQL instance (version 15)
3. Wait for it to be **READY** (green status)
4. Click on the PostgreSQL service
5. Go to **"Variables"** tab
6. Copy the `DATABASE_URL` value - it looks like:
   ```
   postgresql://user:password@host:port/railway
   ```
7. Save this value - you'll need it for the backend

---

## 3. Deploy Backend

### Option A: GitHub Integration (Recommended)

1. Push the `server/` directory to a GitHub repository
2. In Railway, click **"New"** → **"GitHub Repo"**
3. Select your repository
4. Railway will detect the `Dockerfile` and deploy automatically
5. Set the root directory to `server/` if needed

### Option B: Railway CLI
