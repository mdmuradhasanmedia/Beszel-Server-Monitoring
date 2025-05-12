# Beszel-Server-Monitoring
Set up basic server monitoring with Beszel on UpCloud

# 🧭 Agent Installation Manual

This repository provides a simple, browser-friendly **HTML user manual** to help users install and run the Agent and Hub using shell scripts.

You can either follow the **web-based manual** or use the instructions below.

---

## 🌐 View the Manual Online

Once GitHub Pages is enabled, you can view the user manual here:

👉 **https://yourusername.github.io/agent-manual/**  
*(Replace `yourusername` with your actual GitHub username)*

---

## 🚀 Quick Install Guide

### 🛠 Step 1: Install the Hub

Run the following command to download and execute the Hub installation script:

```bash
curl -sL https://raw.githubusercontent.com/henrygd/beszel/main/supplemental/scripts/install-hub.sh -o install-hub.sh && chmod +x install-hub.sh && ./install-hub.sh
```

---

### 🛰 Step 2: Install and Start the Agent

First, install the agent with:

```bash
install-agent.sh
```

Then start the agent with your **port number** and **public key**:

```bash
./install-agent.sh -p 45876 -k "<Your Public Key Here>"
```

🔐 Replace `<Your Public Key Here>` with your actual public key string.

---

## 📋 Notes

- You may need to use `sudo` depending on your system's user permissions.
- Make sure your system has required tools installed (like `curl`, `bash`, and `chmod`).
- All commands are meant to be run in a Unix/Linux terminal (Ubuntu recommended).

---

## 🌍 GitHub Pages Setup

To publish this manual as a website:

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under "Source", select the `main` branch and the `/root` folder.
4. Click **Save**.
5. GitHub will generate a link (e.g., `https://yourusername.github.io/agent-manual/`).

---

## 📂 Repository Structure

```
agent-manual/
│
├── index.html     # The web-based user manual
└── README.md      # This file
```

---

## 📞 Support

If you run into any issues during installation, contact your system administrator or the project maintainer.

