

```
░█▀▀░█▀▀░█▀█░█▀▀░▀█▀░█▀█░▀█▀░░░░░█▀▄░█▀█░█▀▀░▀█▀░█▀▀░█▀▀
░█░█░█▀▀░█░█░▀▀█░░█░░█░█░░█░░▄▄▄░█▀▄░█▀█░▀▀█░░█░░█░░░▀▀█
░▀▀▀░▀▀▀░▀▀▀░▀▀▀░▀▀▀░▀░▀░░▀░░░░░░▀▀░░▀░▀░▀▀▀░▀▀▀░▀▀▀░▀▀▀
```
<h1 align="center">🌍 GeoSINT CTF — Hunter's Guide 🕵️‍♂️</h1>

<p align="center">
   <img src="https://img.shields.io/badge/OSINT-Geolocation-black?style=for-the-badge&logo=googlemaps" />
   <img src="https://img.shields.io/badge/CTF-Writeup-red?style=for-the-badge&logo=hackthebox" />
   <img src="https://img.shields.io/badge/Recon-Ready-blue?style=for-the-badge&logo=linux" />
</p>

---

## 🚀 Mission Brief
GeoSINT challenges throw you into the wild with a single clue — an **image, landmark, or a piece of text**.  
Your task: **hunt down the exact location** using pure OSINT and recon skills.  
This isn’t guessing. It’s methodical **digital tracking**.

---

## 🧭 Recon Protocols

### 🔍 Step 1 — Observe
- Scan the picture like a hawk.  
- Signs, languages, road marks, license plates, architecture, vegetation.  
- Check **shadow angles** → hemisphere clue.  

### 🛰️ Step 2 — Reverse Image Search
- Tools:
  - Google Lens  
  - Yandex Images (god-tier for landmarks)  
  - TinEye  
- Break the image into parts if whole search fails.  

### 🗂️ Step 3 — Metadata Sweep
If raw file provided:
```bash
exiftool challenge.jpg
```
- Look for GPS, camera model, editing traces.  

### 🗺️ Step 4 — Map Recon
- Google Maps / Earth  
- OpenStreetMap  
- Street View (match skylines, roads, unique objects).  

### 🌐 Step 5 — Cross-Reference
- Identify text language.  
- Match vehicle plates, country codes, domains, currency symbols.  

### ✅ Step 6 — Validation
- Confirm landmark from multiple angles.  
- Double-check coordinates before flagging.  

---

## 🛠️ Recon Arsenal
- **Image Forensics**: `exiftool`, `strings`, FotoForensics  
- **Reverse Search**: Yandex, Google Lens, TinEye  
- **Mapping**: Google Maps, Earth, OpenStreetMap  
- **Communities**: r/OSINT, GeoGuessr  

---

## ⚔️ Sample Hunt
📸: Random tower with Cyrillic text  
1. Script spotted → Eastern Europe  
2. Yandex search → Riga TV Tower  
3. Street View match → ✅  
4. Flag:  
```  
CTF{56.9496,24.1052}  
```

---

## 🔥 Hunter Tips
- Tiny details crack cases (trees, poles, windows).  
- File names sometimes leak hints.  
- Shadow = hemisphere.  
- Vehicle type = cultural fingerprint.  

---

## 🎯 Endgame
GeoSINT = Patience + OSINT + Eye for Detail.  
Get fast, get sharp, and hunt locations like a ghost.  

---

### ⚡ Flag Format
```
CTF{latitude,longitude}
```
or
```
CTF{placename}
```
(*depends on challenge rules*)
