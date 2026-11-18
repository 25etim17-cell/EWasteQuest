# E-Waste Quest

**Small drops. Big impact.**

E-Waste Quest is a mobile app that makes it easy and rewarding for University of Hyderabad students to drop their old electronics in the right bin. Scan a QR code on a collection bin, log what you dropped, earn points, and help your hostel climb the leaderboard.

*IE209 Skill Development, University of Hyderabad, "Ship It" project.*

---

## The problem

Old chargers, earphones, phones and laptops pile up in hostel rooms or end up in ordinary dustbins. Most students do not know where to put them, and nothing rewards them for doing the right thing.

This is a global issue too: the UN Global E-waste Monitor 2024 reports about 62 million tonnes of e-waste generated worldwide in 2022, with only 22.3% formally collected and recycled.

## Who it is for

- **Hostel students**, who have old electronics and want a simple way to dispose of them.
- **Hostel and campus coordinators**, who run the bins and collection drives and need to see how much is being collected.

## Features

- **Quick profile:** enter a nickname and pick your hostel. The app remembers you next time.
- **Scan a collection bin:** scan the QR code on a bin (format `EWQ|BINxx`). The server checks that the bin is real and active.
- **Log your drop:** choose the item type and quantity (charger/cable, earphones, phone, laptop and more).
- **Safety checks:** batteries must go in the separate battery box, and devices must be wiped before dropping. If the user says "Not yet", nothing is submitted.
- **Points with a daily limit:** points depend on item type and quantity. The limit of 10 items per person per day is enforced on the server, so it cannot be bypassed.
- **Hostel leaderboard:** hostels compete on total points, and you can see your hostel's rank on the home screen.
- **Our Impact:** shows how many items of each type were collected, the materials they may contain, and the weight weighed so far.
- **Collection drives:** shows upcoming collection drives on campus.

## Screenshots

| Profile setup | Home |
|---|---|
| ![Profile setup screen](screenshots/01-profile-setup.jpg) | ![Home screen with points and hostel rank](screenshots/02-home.jpg) |
| Choose a nickname and hostel. | Points, hostel rank and the main actions. |

| Our Impact | Hostel Leaderboard |
|---|---|
| ![Our Impact screen](screenshots/03-our-impact.jpg) | ![Hostel leaderboard screen](screenshots/04-hostel-leaderboard.jpg) |
| Items collected and the materials they may contain. | Hostels ranked by points. |

## How it works

1. The student scans a bin QR code in the app.
2. The app sends the request to a Google Apps Script web app, which reads and writes a Google Sheet (tabs: Bins, ItemTypes, Drops, Users, Weighings, Drives).
3. The server validates the bin, item type and daily limit, then adds points.
4. The leaderboard, impact page and drives list are read back from the same Sheet.

## Tools used

- **MIT App Inventor** (blocks) for the Android app
- **Google Sheets** as the database
- **Google Apps Script** as the web API (backend)
- **QR codes** on the collection bins
- **Flourish** for the data story

## Links

- **App (APK download):** https://ai2a.appinventor.mit.edu/b/2lv91
- **Data story (Flourish):** https://public.flourish.studio/story/3856515/
- **Demo video:** [ADD VIDEO LINK HERE]
- **QR code to install the app:** [ADD QR IMAGE HERE]

## Team

| Role | Name | What they did |
|---|---|---|
| R1 | Ayush | [ADD ROLE] |
| R2 | Keerthi | [ADD ROLE] |
| R3 | Suraj | App developer (App Inventor blocks) |
| R4 | Charan | Backend: Google Sheet and Apps Script |
| R5 | Nitin | [ADD ROLE] |

## Known limitations

- The nickname is used as the user ID, so two users with the same nickname would share points.
- The API key is stored inside the app, so it is not a high-security setup.
- Material notes on the Impact page are general estimates, not measurements for a specific device.
