# Pterodactyl Egg: Bot WhatsApp (NodeJS)

This repository contains a custom Egg for [Pterodactyl Panel](https://pterodactyl.io) specifically designed for hosting and running NodeJS-based WhatsApp Bots. It automates the deployment process by directly cloning from a Git repository and installing necessary dependencies.

**Author:** abuzycreative@gmail.com  
**Version:** PTDL_v2

## 🚀 Features

*   **Multi-Version NodeJS Support:** Choose from NodeJS versions 18, 19, 20, 21, 22, 23, 24, and 25 via Docker Images.
*   **Automated Git Deployment:** Automatically clones your bot's source code from GitHub, GitLab, or other Git providers during installation.
*   **Private Repository Support:** Authenticate and clone private repositories securely using a Username and Personal Access Token (PAT).
*   **Auto-Update:** Pulls the latest changes from your Git repository on server startup (if configured).
*   **Automated Dependency Management:** Automatically runs `npm install` and allows installing/uninstalling specific packages via environment variables.
*   **OS Dependencies Built-in:** Pre-installs essential build tools like `make`, `gcc`, `g++`, and `python` required by many NodeJS WhatsApp libraries (like Baileys or whatsapp-web.js).

## ⚙️ Configuration Variables

When creating a server using this Egg, you can configure the following environment variables:

| Variable Name | Description | Default Value | Required |
| :--- | :--- | :--- | :--- |
| **Command Run** (`CMD_RUN`) | The command used to start your bot. | `npm start` | Yes |
| **JS file** (`JS_FILE`) | The main file that starts the app (e.g., index.js). | `index.js` | Yes |
| **Git Repo Address** (`GIT_ADDRESS`) | The HTTPS URL of your Git repository (e.g., `https://github.com/user_name/repo_name`). | *None* | No |
| **Install Branch** (`BRANCH`) | The specific branch to install/clone. Leave blank for the default branch (usually `main` or `master`). | *None* | No |
| **Git Username** (`USERNAME`) | Your Git username (required if cloning a private repository). | *None* | No |
| **Git Access Token** (`ACCESS_TOKEN`) | Personal Access Token (PAT) used for authentication with private repositories. | *None* | No |

## 🛠️ How to Install (For Panel Admins)

1. Download the provided JSON file containing this Egg configuration.
2. Log in to your Pterodactyl Admin Control Panel.
3. Navigate to **Nests**.
4. Click the **Import Egg** button at the top right.
5. Select the downloaded JSON file and assign it to your desired Nest.
6. Click **Import**.

## 💻 How to Use (For Users)

1. Create a new server on your Pterodactyl Panel.
2. Select the Nest where this Egg was imported, and choose the **BOT WHATSAPP** Egg.
3. Select your desired NodeJS version under the Docker Image settings.
4. In the **Startup** tab, configure the environment variables:
    * Paste your bot's repository URL into **Git Repo Address**.
    * If it's a private repo, fill in **Git Username** and **Git Access Token**.
    * Adjust the **Command Run** if your bot doesn't use `npm start` (e.g., `node index.js`).
5. Click **Start**. The server will automatically clone your repo, install npm modules, and run your WhatsApp bot!
```eof

File `README.md` ini sudah siap digunakan dan diunggah ke repositori Anda. Jika ada bagian dokumentasi tambahan yang ingin ditambahkan (misalnya instruksi spesifik untuk library Baileys atau library WA lainnya), beri tahu saya!
