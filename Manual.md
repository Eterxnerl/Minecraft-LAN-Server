cat > README.md << 'EOF'
# 🚀 Minecraft LAN Server (Beginner Friendly)

[![Minecraft](https://img.shields.io/badge/Minecraft-Server-brightgreen)](https://www.minecraft.net/en-us/download/server)
[![Java](https://img.shields.io/badge/Java-Required-red)](https://adoptium.net/)
[![License](https://img.shields.io/badge/License-Free-brightgreen)](https://minecraft.net)
[![Download](https://img.shields.io/badge/Download-latest-blue)](https://www.minecraft.net/en-us/download/server)
[![Mods](https://img.shields.io/badge/Mods-Easy-orange)](https://minekeep.net)
[![Docs](https://img.shields.io/badge/Docs-Full-yellow)](https://minecraft.fandom.com/wiki/Tutorials/Setting_up_a_server)
[![Support](https://img.shields.io/badge/Support-Discord-blueviolet)](https://discord.gg)

A simple, **beginner-friendly Minecraft LAN server package**.  
No confusing commands — just follow the steps below and get playing! 🎮  

---

## 📖 Table of Contents
1. [Getting Started](#-getting-started)
2. [Install Java](#-install-java-required)
3. [Custom Seed](#-using-a-custom-seed)
4. [Server Settings](#-basic-settings-serverproperties)
5. [Joining the Server](#-how-to-join)
6. [Online Play](#-online-play-friends-not-on-lan)
7. [Mods & Plugins](#-mods--plugins)
8. [World Management](#-world-management--backups)
9. [Performance & RAM](#-ram--performance)
10. [Security & Admin](#-security--admin)
11. [Commands](#-useful-commands-for-adminsops)
12. [Tips & Notes](#-tips--notes)
13. [Troubleshooting](#-troubleshooting)
14. [Extra Resources](#-extra-resources)
15. [Fun Extras](#-fun-extras--tips)
16. [Credits](#-credits)

---

## 📌 Getting Started

<details>
<summary>Step 1: Choose How to Run the Server</summary>

Inside the folder:

- **Run with GUI** → ✅ Recommended (buttons & control window)  
- **Run no GUI** → ⚡ Advanced (command window only)  

💡 Beginners → use **Run with GUI**
</details>

<details>
<summary>Step 2: Start the Server</summary>

- Double-click your chosen file  
- New world generates automatically (unless custom seed is set)  
- First run may take 1–2 minutes (generating logs & configs)  
</details>

---

## ☕ Install Java (Required)
- Server requires **Java 21+**  
- Recommended: [Adoptium JDK 21](https://adoptium.net/)  
- Verify installation:  
\`\`\`bash
java -version
\`\`\`
- Run the `.bat` file again after installation  

---

## 🌱 Using a Custom Seed
1. Open **server.properties** in Notepad  
2. Find:
\`\`\`properties
level-seed=123456789
\`\`\`
3. Replace with your seed:
\`\`\`properties
level-seed=herobrine
\`\`\`
4. Save & restart server  

💡 **Tip:** Use random words or numbers for fun seeds.

---

## ⚙️ Basic Settings (server.properties)

| Setting | Description | Example |
|---------|------------|---------|
| gamemode | Default game mode | `survival`, `creative`, `adventure` |
| difficulty | Server difficulty | `peaceful`, `easy`, `normal`, `hard` |
| max-players | Max players | `20` |
| white-list | Only allow listed players | `true` |
| motd | Server name in Multiplayer | `My Server` |
| view-distance | Render distance | `6` |
| spawn-monsters | Spawn mobs | `true` |
| allow-flight | Players can fly | `false` |

<details>
<summary>Advanced Settings</summary>

- `enable-command-block=true` → allow command blocks  
- `pvp=true` → enable/disable player vs player  
- `spawn-npcs=true` → spawn villagers  
- `generate-structures=true` → villages, temples, etc.  

💡 **Tip:** Backup `server.properties` before editing.
</details>

---

## 🎮 How to Join
1. Same Wi-Fi/LAN  
2. Start server  
3. Minecraft → **Multiplayer → Direct Connect** > then type **'localhost'** and click join. 
4. Enter host **IP address** (`ipconfig` → IPv4). Use only if **localhost** doesn't work.   
5. Join & play! 🎉  

---

## 🌍 Online Play (Friends not on LAN)
<details>
<summary>Port Forwarding Options</summary>

**Option 1 → ngrok (Easy)**  
\`\`\`bash
ngrok tcp 25565
\`\`\`
- Share generated address with friends  

**Option 2 → Router Port Forwarding (Advanced)**  
- Forward port `25565` to host computer IP  
- Share public IP + port  

</details>

---

## 🧩 Mods & Plugins
<details>
<summary>Click to expand 🔧 Setup</summary>

- **Forge/Fabric:** put `.jar` in `mods` folder  
- **Spigot/Paper:** put plugins in `plugins` folder  
- Use [Minekeep](https://minekeep.net) for easy management  
- Only use compatible mods/plugins  

</details>

---

## 💾 World Management & Backups
- Worlds in `world` folder  
- Replace world → delete folder + restart  
- Backup → copy folder to safe place  

💡 **Pro Tip:** Backup often to prevent corruption/griefing  

---

## ⚡ RAM & Performance
- Edit `.bat` for RAM allocation:
\`\`\`bash
java -Xmx2G -Xms1G -jar server.jar
\`\`\`
- Max RAM: half PC’s total RAM  
- Reduce lag: lower `view-distance`, reduce `max-players`, use SSD  

---

## 🛡 Security & Admin
- OP yourself:
\`\`\`bash
op YourMinecraftName
\`\`\`
- Use `whitelist.json` to restrict friends  
- ⚠️ `online-mode=false` allows cracked clients (not recommended)  
- Protect server files: only share `.bat` and IP  

---

## 📜 Useful Commands (Admins/OPs)
<details>
<summary>Click to expand 🛠 Commands</summary>

\`\`\`bash
/gamemode creative [player]
/gamemode survival [player]
/difficulty easy|normal|hard
/time set day|night
/weather clear|rain|thunder
/tp Player1 Player2
/give Player minecraft:diamond 64
/kick Player
/ban Player
/pardon Player
/whitelist add Player
/whitelist remove Player
\`\`\`

</details>

---

## 🛠 Tips & Notes
- Server folder contains all configs, worlds, logs  
- First run generates files; be patient  
- Add mods/plugins via Forge/Fabric/Spigot/Paper  
- Backup regularly  
- Avoid allocating >50% of RAM  

---

## ⚡ Troubleshooting
<details>
<summary>Click to expand 🩹 Common Issues</summary>

- **Server won’t start?** → Check Java  
- **Friends can’t join?** → Check firewall / use ngrok  
- **Laggy server?** → Lower view-distance / more RAM  
- **Stuck “Loading world”?** → Delete `session.lock`  
- **Port forwarding fails?** → Use ngrok  

</details>

---

## 📚 Extra Resources
- [Minecraft Wiki – Server Setup](https://minecraft.fandom.com/wiki/Tutorials/Setting_up_a_server)  
- [Minekeep](https://minekeep.net)  
- [Adoptium Java](https://adoptium.net)  
- [ngrok](https://ngrok.com)  

---

## 🎉 Fun Extras & Tips
- Customize MOTD colors: `§aGreen §bBlue`  
- Mini-games using `/scoreboard`  
- Encourage friends to backup inventory  
- Try challenge worlds, survival games, or PvP arenas  

---

## 👑 Credits
Made by **Eterxnerl (Shauryax)** 💻  
Custom beginner-friendly Minecraft LAN server package  
New releases updated whenever Mojang publishes a `server.jar` 🎉
EOF
