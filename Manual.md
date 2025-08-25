# Minecraft LAN Server (Beginner Friendly) 🚀

This is a simple beginner-friendly **Minecraft LAN server package**.  
You don’t need to mess with commands or confusing stuff — just follow the steps below.  

👉 **New releases are committed here after Mojang updates their official `server.jar`:**  
https://www.minecraft.net/en-us/download/server  

---

## 📌 How to Start the Server
1. Inside this folder, you’ll see two files:
   - **Run with GUI** → Recommended (shows a control window with buttons).
   - **Run no GUI** → Advanced (just a command window, no buttons).

   Beginners should use **Run with GUI**.

2. Double-click your choice:
   - The server will start.
   - A new world will generate automatically (unless you set a custom seed).

---

## ☕ Install Java (Required)
- This server requires Java to run.
- Download and install **Adoptium JDK 21** (Recommended):  
  👉 https://adoptium.net/  
- After installing, double-click the run file again.

---

## 🌱 Using a Custom Seed
1. Go into the **Server** folder.
2. Open the file **server.properties** with Notepad.
3. Find this line: level-seed=123456789
4. Replace the numbers with your own seed, for example: level-seed=herobrine
5. Save and restart the server.

---

## ⚙️ Basic Settings You Can Change
All settings are inside **server.properties**. Examples:

- `gamemode=survival` → change to `creative` or `adventure`.  
- `difficulty=easy` → change to `peaceful`, `normal`, or `hard`.  
- `max-players=20` → set how many players can join.  
- `white-list=true` → only allow players listed in whitelist.json.  
- `motd=My Server` → the server name shown in Multiplayer.  

---

## 🎮 How to Join the Server
1. Make sure both you and your friends are on the same Wi-Fi/LAN.  
2. Start the server.  
3. In Minecraft, go to: **Multiplayer → Direct Connect**.  
4. Enter the **host computer’s IP Address** (find it by typing `ipconfig` in Command Prompt).  
5. Done! 🎉  

---

## 🌍 Play Online with Friends (Port Forwarding)
If your friends are **NOT** on the same Wi-Fi/LAN:

**Option 1 (Easy) → ngrok**  
- Download ngrok → https://ngrok.com/  
- Create a free account and install it.  
- Run this command (replace `25565` with your port):  ngrok tcp 25565
- Share the generated address (like `tcp://x.tcp.ngrok.io:12345`) with your friends.  

**Option 2 → Manual Router Port Forwarding** (advanced).  

---

## 🧩 Mods & Plugins
- Use **https://minekeep.net** for an easy way to add mods/plugins.  
- For Forge/Fabric → just drop mods into the `mods` folder.  
- For Spigot/Paper → use the `plugins` folder.  

---

## 💾 World Management & Backups
- Your world is saved inside the **world** folder.  
- To replace your world with a new one → delete the **world** folder and restart the server.  
- To back up your world → copy the **world** folder to a safe place.  

---

## ⚡ RAM & Performance
By default, the server may use limited RAM.  
You can edit the `.bat` run files to give more memory: java -Xmx2G -Xms4G -jar server.jar  

This example gives the server 2GB max and 1GB min RAM.  

If laggy:
- Lower `view-distance` in server.properties.  
- Reduce `max-players`.  
- Don’t allocate more than **half your PC’s RAM**.  

---

## 🛡 Server Security & Admin
- To become admin (OP):  op YourMinecraftName
- To remove admin:
- - Use whitelist.json if you only want friends to join.  
- `online-mode=false` → allows cracked clients (⚠️ not recommended).  

---

## 📜 Useful Commands (for Admins/OPs)
- `/gamemode creative [player]`  
- `/difficulty hard`  
- `/time set day`  
- `/weather clear`  
- `/tp Player1 Player2`  
- `/give Player minecraft:diamond 64`  

---

## 🛠 Tips & Notes
- The **Server** folder contains all configs, worlds, and logs.  
- First run may take longer (generating files).  
- If the server crashes → check `logs/latest.log`.  
- To add mods/plugins, use Forge, Fabric, Spigot, or Paper.  

---

## ⚡ Quick Troubleshooting
- **Server won’t start?** → Check Java installation (Adoptium JDK 21).  
- **Friends can’t join?** → Check firewall or use ngrok.  
- **Laggy server?** → Lower view-distance or allocate more RAM.  
- **Stuck on “Loading world”?** → Delete `session.lock` inside world folder.  
- **Port forwarding doesn’t work?** → Use ngrok as an alternative.  

---

## 📚 Extra Resources
- Minecraft Wiki (Server Setup): https://minecraft.fandom.com/wiki/Tutorials/Setting_up_a_server  
- Minekeep (Mods/Plugins): https://minekeep.net  
- Java Download (Adoptium): https://adoptium.net  
- ngrok Port Forwarding: https://ngrok.com  

---

## 👑 Credits
Made by **Eterxnerl(Shauryax)** — a custom beginner-friendly Minecraft LAN server.  
New releases are updated whenever Mojang publishes a new server.jar! 🎉  


