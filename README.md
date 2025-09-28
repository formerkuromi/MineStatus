# OnlineToStatus by formerkuromi

<p align="center">
    <a href="https://github.com/formerkuromi/OnlineToStatus/releases/tag/1.6.1">
    <img src="https://img.shields.io/badge/Release-1.6.1-blue.svg">
  </a>
    <a href="https://opensource.org/licenses/Apache-2.0">
    <img src="https://img.shields.io/badge/Open%20Source-purple.svg">
  </a>
  <a href="https://www.java.com">
    <img src="https://img.shields.io/badge/java_version-1.8.0-red">
  </a>
  <a href="https://github.com/formerkuromi/OnlineToStatus/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-Apache%20License%202.0-yellow.svg">
  </a>
</p>

---

## Requirements
- **Java 1.8.0**

---

## Features
- Display the online count of any Minecraft JE server  
- Show player growth since the last status update  
- Show growth in the last hour  
- Show the online record for the past hour  
- Display the all-time online record  
- Set a custom update frequency for status checks  
- Show status update time/date in your preferred format  
- Auto-start when the server reboots  
- Simple configuration with full setup instructions  
- Easy installation  

---

## Usage
<a href="https://github.com/formerkuromi/OnlineToStatus/releases/download/1.6.1/OnlineToStatus.jar">
    <img src="https://img.shields.io/github/downloads/formerkuromi/OnlineToStatus/total?color=6ff00">
</a>

#### Linux:

```bash
# Run the script
$ java -jar OnlineToStatus.jar

# After the first run, config.yml will be created next to OnlineToStatus.jar — you must configure it.
# help.yml will also be generated — this file contains instructions for configuring the script.
```

#### Windows:

```bash
# After downloading OnlineToStatus.jar:
# Create a '.bat' file in the same directory and insert this command:
java -jar OnlineToStatus.jar

# Run the script by launching the '.bat' file.
# After the first run, config.yml will be created next to OnlineToStatus.jar — you must configure it.
# help.yml will also be generated — this file contains instructions for configuring the script.
```

---

## Security
- Use this at your own risk.  
#### If you run the script on the same dedicated machine as your Minecraft server and it gets hacked, your VK token could be stolen. What to do?
1. Register a new VK account *(preferably with a phone number, add a profile picture and domain name to avoid bans)*, make it an editor in your VK group, and get a **User Token** from it (this token only allows managing groups). Run the script using this token.  
2. Buy a cheap separate VPS.  
3. The safest method: create a new VK account and host the script on a VPS.  

#### How to reset a stolen token?
1. Go to **VK Settings → Security → "End all sessions"** (this will reset all tokens).  
2. Change your account password.  

---

## Config
> Full configuration details are available [HERE](https://github.com/formerkuromi/OnlineToStatus/blob/main/src/main/resources/help.yml)<br>
> Date/time format details are available [HERE](https://github.com/formerkuromi/OnlineToStatus/blob/main/timeFormat.md)

```yml
vk:
  # Group ID where online status will be displayed (digits only)
  # !!! Only an Admin or Editor can change the group status.
  group_id: "200934694"

  # VK User Token
  # {Why User Token? Because VK only allows it this way.}
  # {Where to get one? - https://vk.cc/c4F4lp}
  user_token: "your_vk_user_token_here"

minecraft:
  # IP of the Minecraft server to fetch online count from
  ip: "mc.hypixel.net"
  port: 25565

# Status update interval in seconds (recommended >= 60 to avoid VK limits)
delay: 45

# Status text template
# %online% - current online
# %max_online% - maximum possible online on the server
# %growth% - change since last update
# %time% - current time (formatted by 'time_format')
# %growth_hour% - online growth in the last hour
# %record_hour% - online record in the last hour
# %record_all% - all-time online record
statusText: "Online: %online% / %max_online% {%growth%} Hour: {%growth_hour%}, Record (hour): {%record_hour%} | All-time: {%record_all%} | %time%"

# Date format for %time%
time_format: "dd.MM.yyyy HH:mm:ss"
```

---

## FAQ
**Where should I run the script?**  
For permanent use, run it on a VPS or dedicated server.  

**Why is this script better than a plugin?**  
- No extra load on the Minecraft server (uses sockets).  
- Can fetch online data from any server just by IP.  
- Simply better 🙃  

**Can I run it on the same dedicated server as Minecraft?**  
Yes, in a separate terminal window. Use `localhost` as IP if running on the same machine.  

**Can I make the status go to the next line?**  
No, VK does not allow multi-line statuses.  

**When is the next update?**  
Soon :D  

---

## Version
- Script: **1.6.1**  
- VK API: **5.130**  

---

## Links
- [Java 8](https://www.java.com)  
- Author: [Charles_Grozny](https://github.com/formerkuromi)  

---

## Screenshots
<a href='' title=''><img style="width:100%" src='https://i.ibb.co/dcG1mNB/2021-07-05-01-21.png' alt=''  /></a>
<a href='' title=''><img style="width:100%" src='https://i.ibb.co/WcLt0cN/image.png' alt=''  /></a>
<a href='' title=''><img style="width:100%" src='https://i.ibb.co/0c32zMz/IMG-20210705-013505.jpg' alt=''  /></a>
