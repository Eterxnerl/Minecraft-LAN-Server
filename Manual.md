# 📘 Minecraft LAN Server - Manual

Welcome to the **Minecraft LAN Server** manual! 🎉  
This guide will walk you through everything you need — from downloading, extracting, and running the server to customizing your world and connecting with friends.

---

## 📦 1. Download & Extract

1. Go to the [Releases](../../releases/latest) page.  
2. Download the latest `Minecraft-LAN-Server.zip`.  
3. Extract the contents anywhere you like (Desktop, Documents, or a dedicated folder).  
   - Inside the extracted folder, you’ll see:  
     - `Run with GUI.bat` → Beginner-friendly way to start the server  
     - `Run no GUI.bat` → Console-only mode (for advanced users)  
     - `server.jar` → The actual Minecraft server file  
     - `server.properties` → World and server settings  
     - `eula.txt` → Minecraft’s End User License Agreement  
     - `manual.md` (this file) → The guide you’re reading  

---

## 🚀 2. Starting the Server

There are two ways to run the server:

- **Run with GUI** → Recommended ✅  
  - Just double-click `Run with GUI.bat`  
  - A server control panel will open with options to stop/restart  
- **Run no GUI** → Advanced ❌  
  - Double-click `Run no GUI.bat`  
  - Runs in a plain console window (uses less RAM)

⚠️ Important: The first time you start, it may take a few minutes while the world generates.

---

## 🌍 3. Setting a Custom Seed

1. Open the `Server` folder.  
2. Find the file `server.properties`.  
3. Open it with a text editor (Notepad works).  
4. Look for the line:  level-seed=123456789
5. 5. Replace `123456789` with the seed you want.  
6. Save and close the file.  
7. Restart the server for changes to apply.

---

## 🔌 4. Playing with Friends (LAN + Online)

### 🖥️ Local Network (LAN)
- Make sure all players are connected to the same Wi-Fi or LAN.  
- Run the server, then other players can **Direct Connect** using your local IP (example: `192.168.x.x`).  

### 🌐 Online (Friends Anywhere)
If you want friends outside your network to join:  
1. Use **Ngrok** to port-forward easily:
- Download [Ngrok](https://ngrok.com/).  
- Run:  
  ```
  ngrok tcp 25565
  ```
- Share the link Ngrok gives you (like `0.tcp.ngrok.io:xxxxx`).  

2. Or use **MineKeep.net** for a simpler setup:  
- No technical setup needed  
- Easy mod installation support  

---

## ⚙️ 5. Installing Mods (Optional)

1. Install [Adoptium Java 17+](https://adoptium.net/) (needed for modern servers).  
2. Download **Forge** or **Fabric** mod loader.  
3. Place mod `.jar` files in the `mods/` folder inside your server directory.  
4. Restart your server and enjoy mods with friends! 🎮

---

## 📑 6. Files Explained

- `server.jar` → Core Minecraft server  
- `Run with GUI.bat` → Beginner-friendly start option  
- `Run no GUI.bat` → Console-based start option  
- `server.properties` → Edit game rules, seed, difficulty, etc.  
- `eula.txt` → Confirms Minecraft’s license (already set to true ✅)  
- `logs/` → Stores server logs (useful for troubleshooting)  
- `world/` → Your generated Minecraft world (created after first launch)  

---

## 🛠️ 7. Troubleshooting

- **Server closes immediately** → Check if `eula.txt` says `eula=true`.  
- **Friends can’t join online** → Make sure you’re using Ngrok or MineKeep.net.  
- **Out of memory errors** → Edit `Run with GUI.bat` and increase `-Xmx` (RAM). Example:  java -Xmx2G -Xms1G -jar server.jar


---

## 🎉 8. Enjoy!

That’s it! You’ve successfully set up your own **Minecraft LAN Server**.  
Now grab your friends, share your world, and start building together 🏰⚔️🌍  

---

## 📜 License

This project is licensed under the **GPL-3.0 License**.  
See [LICENSE](LICENSE) for details.

   
