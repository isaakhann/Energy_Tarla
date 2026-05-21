# 🚀 Project Setup Guide

This repository contains both the backend and frontend components. Follow the instructions below to set up your local development environment on macOS.

---

## 📂 Project Structure
* **/backend**: Python-based API (FastAPI/Flask)
* **/frontend**: React/Node.js web application

---

## 🐍 Backend Setup

The backend uses a Python virtual environment to keep dependencies isolated.

1.  **Navigate to the backend directory:**
    ```bash
    cd backend
    ```

2.  **Create and activate the virtual environment:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install Python dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Launch the backend server:**
    ```bash
    source run.sh
    ```

---

## ⚛️ Frontend Setup

The frontend is managed via npm. Ensure you have Node.js installed.

1.  **Navigate to the frontend directory:**
    ```bash
    cd ../frontend
    ```

2.  **Install Node dependencies:**
    ```bash
    npm install
    ```

3.  **Configure Mapbox (required for the map after login):**
    ```bash
    cp .env.example .env
    ```
    Edit `.env` and set `REACT_APP_MAPBOX_ACCESS_TOKEN` to a [Mapbox public access token](https://account.mapbox.com/access-tokens/). Restart `npm start` after changing `.env`.

4.  **Start the development server:**
    ```bash
    npm start
    ```

Default login: username `admin`, password `admin` (stored in the browser’s local storage).

---

## 🛠 Troubleshooting & Tips

### Script Permissions
If you encounter a `Permission denied` error when trying to run the backend script, grant execution permissions with:
```bash
chmod +x run.sh