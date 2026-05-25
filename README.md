# Internet Group Chat PWA 🌐💬

A high-performance, real-time group PWA chat application built with **Node.js, Express, and Socket.IO**. Fully optimized and ready to deploy to the public internet!

## ✨ Features
- **Real-Time Messaging**: Instant chat using WebSockets (Socket.IO).
- **File & Image Sharing**: Share documents and media seamlessly.
- **Copy Button**: Small, highly responsive top-right button to copy messages or file links dynamically.
- **Premium Image Preview**: Beautiful image thumbnails with full-screen, click-to-view support.
- **PWA Ready**: Completely installable on iOS, Android, or Desktop, including native sharing support (Android Share Target).

---

## 🚀 Easy Deployment Guides

Here are the simplest ways to deploy this application to the internet for free.

### Option 1: Deploying on Render (Recommended)
[Render](https://render.com/) is a fantastic hosting provider that supports Node.js WebSockets natively.

1. Create a free account on [Render](https://render.com/).
2. Push this project folder to your private **GitHub** repository.
3. On Render, click **New +** and select **Web Service**.
4. Connect your GitHub repository.
5. Configure the service:
   - **Name**: `my-internet-group-chat`
   - **Runtime**: `Node`
   - **Build Command**: `npm install`
   - **Start Command**: `npm start`
6. Click **Advanced** and add the following **Environment Variables**:
   - `NODE_ENV` = `production`
   - `PORT` = `3000` (Render will override this automatically, which is fine)
7. Click **Create Web Service**. Your app will be live on a secure `https://[name].onrender.com` URL in a few minutes!

> 💡 **Persistent Volumes on Render (Highly Recommended for File Sharing)**:
> Since free Render containers have an ephemeral disk (files uploaded will get deleted whenever the server sleeps or restarts), you should add a **Persistent Disk Volume** to preserve uploads:
> 1. In your Render Web Service dashboard, go to **Volumes**.
> 2. Click **Add Volume**.
> 3. Set:
>    - **Name**: `uploads-volume`
>    - **Mount Path**: `/opt/render/project/src/uploads` (or whatever the path is to your uploads folder)
>    - **Size**: `1 GB` (free)
> 4. Save and let it redeploy!

---

### Option 2: Deploying on Railway
[Railway](https://railway.app/) is extremely fast and has built-in volume mounting.

1. Sign up on [Railway.app](https://railway.app/).
2. Install the Railway CLI or connect your GitHub repository.
3. Set the start script to `npm start`.
4. In your project settings, add the environment variable `NODE_ENV=production`.
5. Under your service settings, click **Mount Volume** to mount a disk to `/uploads` so shared files are permanently saved.

---

## 💻 Running Locally

To run the internet version locally on your computer for testing:

1. Open your terminal in the `internet-chat` folder.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Run the development server:
   ```bash
   npm start
   ```
4. Open your browser and go to `http://localhost:3000`.
