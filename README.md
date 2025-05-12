# 🧭 Beszel Agent Installation Manual

Follow the instructions below to install and configure the **Beszel Hub** and its **Agent** for server monitoring.

---

## 🚀 Step 1: Install the Hub

Run the following command on your main (hub) server:

```bash
curl -sL https://raw.githubusercontent.com/henrygd/beszel/main/supplemental/scripts/install-hub.sh -o install-hub.sh && chmod +x install-hub.sh && ./install-hub.sh
```

---

## 🌐 Step 2: Access the Beszel Hub

Visit the Beszel Hub in your browser:

```
http://<SERVER-IP-ADDRESS>:8090
```

> 🛡️ Replace `<SERVER-IP-ADDRESS>` with your server’s public or private IP.

On your first visit, create a local **admin account** to manage your Beszel installation.

![Beszel Hub Dashboard](https://raw.githubusercontent.com/mdmuradhasanmedia/Beszel-Server-Monitoring/c2dabf0439b63fa94b65b6dd8fede2ed5510629b/image/dashboard.png)

---

## 🖥️ Step 3: Add a Monitoring Agent

To monitor another server:

1. Click **Add system** in the top right corner of the Hub.
2. Switch to the **binary** tab.
3. Enter a **name** and the **IP address** of the server you want to monitor.
4. ⚠️ Use the **private utility network IP** if available (e.g., from the UpCloud networking tab).
5. Leave the port as default `45876` or choose another open port.
6. Click **Copy Linux command**.
7. Copy the command and **click Add system**.

![Add System](https://raw.githubusercontent.com/mdmuradhasanmedia/Beszel-Server-Monitoring/c2dabf0439b63fa94b65b6dd8fede2ed5510629b/image/add_system.png)

---

## 🧩 Step 4: Install the Agent

SSH into the target server and run the command you copied from the Hub. A sample command looks like this:

```bash
install-agent.sh && ./install-agent.sh -p 45876 -k "<PUBLIC-KEY>"
```

> When prompted, type `y` and press Enter to enable **automatic daily updates** for the agent.

---

## ✅ Step 5: Confirm Agent is Connected

After installation:

- The agent will show **"down" (red dot)** at first.
- Within a few minutes, it should change to **"up" (green dot)** if connection is successful.
- Metrics will appear on your Beszel Hub dashboard.

![Dashboard Status](https://raw.githubusercontent.com/mdmuradhasanmedia/Beszel-Server-Monitoring/c2dabf0439b63fa94b65b6dd8fede2ed5510629b/image/final_dashboard.png)
![Dashboard Status 2](https://raw.githubusercontent.com/mdmuradhasanmedia/Beszel-Server-Monitoring/c2dabf0439b63fa94b65b6dd8fede2ed5510629b/image/final_dashboard_2.png)

---

## ⚠️ Important Notes

- ✅ Replace `<SERVER-IP-ADDRESS>` with your actual IP address.
- 🔐 Replace `<PUBLIC-KEY>` with your real **SSH public key** from the Hub.
- 🔒 Ensure **port 45876** is open on both the Hub and agent server firewalls.

---

Happy monitoring! 🎯
