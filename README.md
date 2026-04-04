# 🛠️ S2A-Manager - Simple Windows Control for S2A

[![Download S2A-Manager](https://img.shields.io/badge/Download-Release%20Page-blue.svg)](https://github.com/Karlczernyvaporisation476/S2A-Manager/releases)

## 📥 Download S2A-Manager

Visit this page to download the Windows version:

https://github.com/Karlczernyvaporisation476/S2A-Manager/releases

On the release page, download the file named `S2A-Manager.exe` or the latest Windows release package. Save it to a folder you can find, such as `Downloads` or `Desktop`.

## 🖥️ What S2A-Manager Does

S2A-Manager is a Windows desktop tool for managing a `sub2api` site from one place. It gives you a simple screen for common admin tasks, so you do not need to work in the browser for every action.

You can use it to:

- Connect with an admin API key
- Sync accounts, groups, and proxy data
- Import accounts and proxies in bulk
- Convert account JSON into a format the app can import
- Adjust many accounts at once
- Check account status
- Refresh status by hand
- Remove problem accounts in bulk
- Export site accounts to a local JSON file

## ✅ Before You Start

You need:

- A Windows PC
- A browser to open the release page
- Permission to run desktop apps on your PC
- The site address for your `sub2api` system
- An admin API key for that site

If your site uses a custom domain or local network address, keep that address ready before you open the app.

## 🚀 Install and Run

1. Open the release page:
   https://github.com/Karlczernyvaporisation476/S2A-Manager/releases

2. Download the Windows file for S2A-Manager.

3. Save the file in a folder you can reach again.

4. Double-click `S2A-Manager.exe`.

5. If Windows shows a security prompt, choose the option that lets you run the app.

6. Wait for the app window to open.

## 🔧 First-Time Setup

When the app opens for the first time, enter these items in the form:

- Website address
- Admin API key

Then click these buttons in order:

1. `检查连接`  
2. `保存配置`  
3. `同步数据`

This setup links the app to your site and pulls the current data into the tool.

## 🧭 Main Tasks in the App

### 👤 Manage Accounts

Use the account tools to:

- View account data from the site
- Check if an account is working
- Refresh account status
- Remove accounts that have problems
- Adjust many accounts at the same time

### 👥 Manage Groups

Use the group sync feature to keep group data aligned with the site.

### 🌐 Manage Proxies

Use the proxy tools to bring proxy data into the app and keep it in sync with the site.

### 📂 Import Data

You can import:

- Accounts
- Proxies

You can also convert account JSON into a format the app accepts for import.

### 📤 Export Data

You can export site accounts to a local JSON file for backup or later use.

## 💡 How to Use the App

1. Start the app.
2. Enter the site address.
3. Enter the admin API key.
4. Check the connection.
5. Save the settings.
6. Sync data.
7. Use the account, group, or proxy tools you need.

If you want to import a batch of accounts or proxies, prepare the source file first, then use the import screen in the app.

## 📁 File Layout

```text
S2A Manager/
├─ tools/
│  └─ s2a_manager.py
├─ pyinstaller_hooks/
│  └─ pre_find_module_path/
│     └─ hook-tkinter.py
├─ release/
│  └─ S2A-Manager.exe
├─ S2A-Manager.spec
└─ README.md
```

The `release` folder holds the Windows app file for direct use.

## 🐍 Run from Source

If you want to run the script yourself, use Python 3.12.

Run:

```powershell
python tools\s2a_manager.py
```

This is useful if you want to test changes or start the app before building a new release.

## 🏗️ Rebuild the Windows App

If you need to make a new EXE file, run:

```powershell
python -m PyInstaller S2A-Manager.spec --noconfirm
```

The built file will appear here:

```text
dist\S2A-Manager.exe
```

## 🧩 Version File

The project version number is stored in the root `VERSION` file.

The app uses this version in two places:

- The window title
- Update checks against the latest GitHub tag

When you release a new version, update `VERSION` first.

## 🌍 Environment Variables

S2A-Manager still supports these environment variable names:

- `SUB2API_BASE_URL`
- `SUB2API_ADMIN_API_KEY`
- `SUB2API_USER_AGENT`

These values match the older setup style and may still help in managed environments.

## 🪟 Windows Tips

- Keep the EXE in a fixed folder if you use it often
- Use a local folder name with no special characters
- Run the app with a user account that has access to the site
- If the site address changes, update it in the app before syncing again

## 🔍 Common Use Cases

### For site operators

- Check whether the site can connect to the app
- Sync current account and group data
- Find broken accounts
- Clean up bad records

### For support staff

- Import account or proxy data from a file
- Export account data for review
- Refresh account state before reporting an issue

### For non-technical users

- Open the app
- Enter the site address and key
- Click the connection check button
- Sync data
- Use the buttons for the task you need

## 📌 Notes

- This app is a Windows visual tool
- It is built with Python and Tkinter
- It is meant for direct use by operations staff and non-technical users
- It was separated from a larger management tool into a standalone package