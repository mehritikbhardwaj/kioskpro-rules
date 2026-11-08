# KioskPro Rules & Dynamic Update Endpoint

This repository serves as the official dynamic rules, selectors, and cloud updates distribution endpoint for **KioskPro Banking & Kiosk Automation System**.

## 📌 Dynamic Rules (`kioskpro_rules.json`)
The client app automatically fetches `kioskpro_rules.json` from:
```text
https://raw.githubusercontent.com/mehritikbhardwaj/kioskpro-rules/main/kioskpro_rules.json
```

### How to push hotfixes without reinstalling:
1. Edit `kioskpro_rules.json` directly on GitHub.
2. Update selectors under `"selectors"` (e.g. `gps_connect`, `gps_get_location`, `gps_proceed`, `aeps_proceed`).
3. Commit changes. All active KioskPro installations across India will apply the new selectors dynamically within seconds.

### How to release a new app update:
1. Create a new GitHub Release with the tag (e.g., `v2.0.1`).
2. Attach `KioskPro.exe` and `KioskPro.exe.zip`.
3. Bump `"latestAppVersion"` to `"2.0.1"` in `kioskpro_rules.json`.
4. Client applications will silently download the update and apply it seamlessly upon restart.

---
**Verified Publisher:** Hritik Bhardwaj  
**Organization:** KioskPro Technologies  
**Contact:** 9212716009 | UPI: 9212716009@yescred
