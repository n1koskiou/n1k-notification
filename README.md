# N1K Notification System
This notification system was **inspired** by [Agency Script](https://agency-script.tebex.io/)

The script [Agency-Notification](https://agency-script.tebex.io/package/6937769)

## Features

- Modern **glass UI** with aurora glow, shimmer, and corner brackets.  
- **Sound effects** for info, success, and error notifications.  
- **Progress bar** with animated depletion.  
- **Discord-style footer timestamps** (date & time).  
- **Center-right notification placement**.  
- **Server-side and client-side triggers**.  
- Fully **configurable** via `config.lua`.  
- Compatible with **QBCore, ESX, QBOX, or standalone**.

---

## Installation

1. Place the folder `n1k-notification` in your server’s `resources` directory.  
2. Add the following to your `server.cfg`:

## CFG
3. `ensure n1k-notification`

---

## Usage
### Client-side Trigger
```
TriggerEvent("n1k-notification:client:show", {
    type = "success", -- success | info | error
    title = "Garage",
    text = "Your vehicle was stored successfully!",
    duration = 5000 -- duration in milliseconds
})
```
### Server-side Trigger
```
exports['n1k-notification']:Notify(src, 'error', 'Access Denied', 'You lack permission to open this door.', 5000)
```
### Test Command
```
RegisterCommand("testnotify", function(source, args, rawCommand)
    TriggerEvent("n1k-notification:client:show", {
        type = "info",
        title = "Test Notification",
        text = "This is a test notification from n1k-notification.",
        duration = 5000
    })
end, false)
```

---

## Configuration [Config.lua]

- Core: **QBCORE, ESX, QBOX, STANDALONE**.
- Debug: **Enable/disable** console logs.
- Sounds: **Enable/disable** and set volume.
- Logs: Server console log prefix.
- Footer: Show server name and timestamp.

---

## HTML & Sounds

- HTML folder contains the notification UI.
- Sounds folder contains:
- success.mp3
- error.mp3
- info.mp3

---

## Preview
![Notification Preview](preview.png)

---

## License

© 2025 N1K. All rights reserved.  
You may use and modify this resource for your FiveM server only. Redistribution or selling is prohibited without permission.




