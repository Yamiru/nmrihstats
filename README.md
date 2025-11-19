# Simple NMRiH Stats (Updated Edition)

A lightweight point-based statistics plugin for **No More Room in Hell**, originally created by **Stevo.TVR** and now updated/maintained by **Yamiru**.  
Tracks kills, deaths, headshots, extractions, teamkills and provides **rank** and **top10** commands.

All stat data is stored in a configurable SQL database — works with SQLite or MySQL.

---

## Screenshot
![Desktop Screenshot](https://i.imgur.com/jCrs3mD.png)
---

## 🔧 Requirements

This plugin requires:

- **MetaMod:Source**  
- **SourceMod**

Both must be installed on your NMRiH server.

---

## 🎮 Features

- Zombie kill tracking  
- Headshot bonus  
- Extraction reward  
- Teamkill penalty  
- Rank and Top10 command outputs  
- Automatic stat saving  
- Name auto-update in database  
- Supports MySQL & SQLite (via SourceMod)

---

## ⚙️ Default Point Values

| Action              | Points |
|--------------------|--------|
| Zombie kill        | +1     |
| Headshot bonus     | +1     |
| Extraction         | +50    |
| Death              | –20    |
| Teamkill           | –20    |

---

## 📦 ConVars

```cfg
sm_stats_killpoints "1"
sm_stats_headshot_bonus "1"
sm_stats_deathpoints "-20"
sm_stats_tkpoints "-20"
sm_stats_extractionpoints "50"
sm_stats_start_at_avg "1"
```

---

## 📝 Commands

| Command | Description |
|--------|-------------|
| `sm_rank` | Shows your current rank |
| `sm_top10` | Shows top 10 players |
| `sm_stats_setpoints` `<points> <#userid|name>` | Admin: set player points |
| `sm_stats_setpoints_id` `<points> <steamid>` | Admin: set by SteamID |
| `sm_stats_reset` `[code]` | Admin: resets all stats (confirmation required) |

---

## 🛠 Database Setup

### **SQLite (default)**  
Works out of the box — no configuration needed.

### **MySQL (optional)**  
Create a section inside `addons/sourcemod/configs/databases.cfg`:

```json
"nmrihstats"
{
    "driver"          "mysql"
    "host"            "YOUR_HOST"
    "database"        "YOUR_DB"
    "user"            "YOUR_USER"
    "pass"            "YOUR_PASS"
    "port"            "3306"

    "timeout"         "3"
    "retry"           "2"
    "pool_timeout"    "45"
    "min_connections" "1"
    "max_connections" "3"
}
```

---

## 🕒 Changelog (Updated)

### **2025-01-01 — v0.5.1 (Yamiru Update)**  
- Fixed plugin warnings (deprecated SteamID functions)  
- Code cleanup, optimized string handling  
- Better performance with safer DB calls  
- No database schema changes (fully backward-compatible)


---

## 🧑‍💻 Credits

- **Original Author:** Stevo.TVR  
- **Updated & Maintained by:** Yamiru  
- AlliedModders Thread: https://forums.alliedmods.net/showthread.php?t=230459  
- GitHub Repo: https://github.com/Yamiru/nmrihstats
- Issues: https://github.com/Yamiru/nmrihstats/issues

---

## 📜 License

This project follows the original plugin licensing from AlliedModders.  
Please credit the original author when redistributing builds or forks.

