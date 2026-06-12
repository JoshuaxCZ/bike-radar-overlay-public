# Bike Radar Overlay — User Guide

---

## 1. Introduction

### 1.1 What is Bike Radar Overlay?

Bike Radar Overlay is a free Android application for cyclists that displays data from cycling radars (Garmin Varia, Coospo TR70 and other supported devices) as a floating overlay over any navigation app.

**Key features:**
- Displays vehicles behind the cyclist as colored dots or car silhouettes
- Threat level color coding: green (far), orange (medium), red (near)
- GPS speed display as a speedometer
- Cyklocomputer on lock screen (with phone locked)
- Navigation support (OsmAnd, Bike Route Planner)

### 1.2 Why Bike Radar Overlay?

- **Safety:** Shows vehicles behind you, even when you can't look over your shoulder
- **Versatility:** Works over any navigation app
- **Tracking:** Allows tracking how many vehicles have overtaken you during a ride
- **Lock screen:** Shows speed, vehicles, distance and navigation even on a locked screen

---

## 2. System Requirements

- **Android:** 8.0 (API 26) or newer
- **Bluetooth LE:** Required for radar connection
- **GPS:** Required for speed measurement
- **Notification access:** For OsmAnd integration
- **Overlay permission:** For display over navigation

---

## 3. Installation

### 3.1 Installation from Google Play Store

1. Open Google Play Store on your phone
2. Search for: **Bike Radar Overlay**
3. Click **Install**
4. After download, click **Open**

### 3.2 Installation from APK file

1. Download APK from GitHub
2. Transfer APK to phone (e.g., via USB or email)
3. Open file and enable installation from unknown sources
4. Click **Install**

---

## 4. First Launch and Setup

### 4.1 After App Launch

1. The app will prompt for required permissions:
   - **Allow overlay** — for display over navigation
   - **GPS** — for speed measurement
   - **Bluetooth** — for radar connection
   - **Notifications** — for OsmAnd integration (optional)

2. Grant all required permissions

### 4.2 Connecting the Radar

1. Turn on your radar (Garmin Varia, Coospo TR70 or other supported device)
2. In the app, click **Find Radar**
3. Wait for BLE device list to appear
4. Tap your device (e.g., "Varia RTL515" or "Coospo TR70")
5. Allow pairing in Android dialog

After pairing, the radar automatically connects and starts displaying data.

### 4.3 Configuration Settings

In the main screen you can configure:

| Setting | Description |
|---------|-------------|
| **Smart Screen** | Automatic screen wake-up on vehicle detection |
| **Keep screen on** | Screen stays on during the entire ride |
| **Show speed widget** | Display GPS speed |
| **Sound alerts** | Beeps on vehicle detection |
| **Hide strip when clear** | Strip collapses to battery indicator when road is clear |
| **Units** | km/h or mph (imperial units) |

**Important:** After changing settings, restart the radar (**Stop Radar** then **Start**).

---

## 5. Main Screen

### 5.1 Connection Status

| Status | Description |
|--------|-------------|
| **Ready** | App is ready for radar connection |
| **Connecting** | Connection to radar is in progress |
| **Connected** | Radar is connected and tracking vehicles |
| **Disconnected** | Radar is disconnected |

### 5.2 Navigation Menu (bottom-left corner)

| Item | Description |
|------|-------------|
| **Overlay — edit layout** | Move and resize the strip |
| **Lock screen — edit layout** | Move the strip on lock screen |
| **Sound alerts** | Configure sounds |
| **Navigation** | Configure navigation (OsmAnd, BRP) |
| **PRO features** | Pro version explanation (when active) |
| **Features** | All features overview |
| **Manual** | This manual |
| **Ride History** | View recorded rides |

---

## 6. Basic Features

### 6.1 Radar Strip

**What is the radar strip?**

The radar strip is a thin bar that appears at the top of the screen. It displays:

- **Radar battery** (e.g., "85") — top-left corner
- **Vehicles** — as dots or car silhouettes

**Threat Level Color Codes:**

| Color | Distance | Meaning |
|-------|----------|---------|
| 🟢 **Green** | > 100 m | Vehicle is far away |
| 🟠 **Orange** | 50–100 m | Vehicle is approaching |
| 🔴 **Red** | < 50 m | Vehicle is near |

**Note:** Distances are approximate and depend on the radar.

### 6.2 Speedometer (speed widget)

**What is the speedometer?**

The speedometer is a window showing current speed that can be placed anywhere on screen.

**How to switch modes:**

A single tap on the speedometer cycles through:
1. **Speed** — current GPS speed (e.g., "27 km/h")
2. **Trip** — current ride distance (e.g., "12.3 km")
3. **ODO** — total distance (e.g., "847.5 km")

**How to resize:**

1. Enable **Edit Layout**
2. Tap **Edit overlay size**
3. In the lower panel, find **+** and **−** buttons for speedometer
4. Use **+** to grow, **−** to shrink
5. Tap **Save Layout**

### 6.3 Edit Layout

**What can be adjusted:**

| Element | Adjustments |
|---------|-------------|
| **Radar strip** | Position (drag), width, height, dot size, style (dots/silhouettes) |
| **Speedometer** | Position (drag), size (width/height) |

**How to edit:**

1. Tap **Edit Layout**
2. Blue canvas and lower panel appear
3. **Drag** the strip and speedometer to desired position
4. **Adjust size** using sliders in panel
5. Tap **Save Layout** (in panel)

**Tip:** Panel always appears when clicking on strip or speedometer (when in edit mode).

---

## 7. Lock Screen and Smart Screen

### 7.1 Lock Screen Display

**What is the lock screen display?**

The lock screen display is a "cyklocomputer" shown on the locked screen. Allows monitoring speed, vehicles, navigation and distance without unlocking the phone.

**How to enable:**

1. Enable **Smart Screen** or **Keep screen on** in settings
2. Lock phone during ride (click side button, screenshot, or gesture)
3. Screen automatically wakes up on vehicle detection or navigation proximity

**What lock screen shows:**

| Section | Information |
|---------|-------------|
| **Top** | Radar battery (number) + vehicles (dots) |
| **Middle** | Speed (27 km/h), vehicle count (2), distance (85 m) |
| **Bottom** | Trip (14.2 km) + ODO (1284 km) |
| **Navigation** | Arrow, distance, instructions, ETA |

### 7.2 Smart Screen

**What is Smart Screen?**

Smart Screen automatically wakes the screen on vehicle detection behind you or navigation proximity.

**How Smart Screen works:**

1. **Wake on vehicle:** When radar detects nearby vehicle, screen wakes up
2. **Wake on navigation:** When near maneuver (< 200 m), screen wakes up
3. **Turn off:** After timeout (configurable in settings), screen turns off

**Smart Screen Settings:**

| Setting | Description |
|---------|-------------|
| **Smart Screen ON** | Enable/disable Smart Screen |
| **Timeout** | Time screen stays on (5–60 seconds) |

### 7.3 Keep Screen On

**What is Keep Screen On?**

This feature keeps the screen on during the entire ride. Use when you need everything always visible.

**Note:** Smart Screen and Keep Screen On cannot be used simultaneously — enabling one automatically disables the other.

---

## 8. Sound Alerts

### 8.1 Five Alert Types

| Event | Description | When played |
|-------|-------------|-------------|
| **New vehicle** | New vehicle | When radar detects new vehicle |
| **Threat LOW** | Low threat | When vehicle is far |
| **Threat MEDIUM** | Medium threat | When vehicle approaches |
| **Threat HIGH** | High threat | When vehicle is near |
| **All clear** | All clear | When vehicles disappear |

### 8.2 Configuring Alerts

Each alert has three parameters:

| Parameter | Range | Description |
|-----------|-------|-------------|
| **Frequency** | 200–4000 Hz | Tone height (number in Hz) |
| **Beep count** | 1–3 | How many times it beeps |
| **Duration** | 50–500 ms | How long one beep lasts |

**How to configure:**

1. Tap **Sound Alerts**
2. Tap **Preview** for each alert to hear result
3. Adjust parameters using sliders or input fields
4. Tap **Save** (if visible) or **Back**

### 8.3 Example Configurations

**Fast alert (high threat):**
- Frequency: 2000 Hz
- Count: 1
- Duration: 100 ms

**Warning (low threat):**
- Frequency: 800 Hz
- Count: 2
- Duration: 150 ms

---

## 9. Navigation

### 9.1 Supported Apps

| App | Method | Required Permissions |
|-----|--------|---------------------|
| **OsmAnd** | Notification | Notification access |
| **Bike Route Planner** | Broadcast | None (explicit broadcast) |

### 9.2 OsmAnd Setup

1. In app, tap **Navigation**
2. Enable **OsmAnd**
3. Open **Android Settings** → **Special Access** → **Notification Access**
4. Enable **Bike Radar Overlay**

### 9.3 Bike Route Planner (BRP) Setup

1. In app, tap **Navigation**
2. Enable **Bike Route Planner**
3. In BRP, open **Navigation settings**
4. Enable **Send navigation data to Bike Radar**

### 9.4 What Navigation Shows

| Element | Description |
|---------|-------------|
| **Arrow** | Direction (↑ straight, ← left, → right, etc.) |
| **Distance** | Distance to maneuver (e.g., "320 m") |
| **Instruction** | "Turn left", "Roundabout", etc. |
| **Street** | Street name |
| **ETA** | Time to arrival (e.g., "8.3 km | 24 min | 14:47") |

**Distance Colors:**
- **White** | > 100 m
- **Yellow** | ≤ 100 m
- **Red** | ≤ 50 m

---

## 10. Ride History

### 10.1 What is Recorded

Each ride (minimum 10 minutes) is recorded with:

- Start date and time
- Total distance (trip)
- Total duration
- Number of detected vehicles
- Screen management mode (Smart Screen / Keep ON)
- Battery savings (for Smart Screen)

### 10.2 How to Browse History

1. Tap **Ride History** in menu
2. All recorded rides appear in list
3. Each ride shows:
   - Date and time
   - Distance and duration
   - Vehicle count
   - Battery savings bar (green = time screen was off due to Smart Screen)

### 10.3 Aggregate Statistics

At the top of history you see:
- **Total number of rides**
- **Total hours**
- **Average battery savings** (only for Smart Screen rides)

---

## 11. Pro Features (Future)

### 11.1 What is Pro Version?

Pro version is a paid app version that:
- Removes 100-vehicle session limit
- Enables unlimited Smart Screen
- Shows lock screen UI always (no wake-up needed)
- Gains access to future features

### 11.2 How to Get Pro Version

Pro version will be available in Google Play Store for a one-time fee (~€2.99). Currently, the app runs in **DONATION MODE**, meaning all features are free.

---

## 12. Troubleshooting

### 12.1 Radar Not Connecting

**Problem:** App searches but finds no devices.

**Solution:**
1. Ensure radar is on and in range (max 200 m)
2. Restart radar (turn off/on)
3. Restart Bluetooth on phone
4. In app, tap **Forget** then **Find Radar** again

### 12.2 Distance Not Accurate

**Problem:** Displayed distance differs from actual.

**Note:** Distance is approximate and depends on:
- Radar type (Garmin Varia vs Coospo TR70)
- Radar direction (directed away from vehicles)
- Environment (urban canyon, forests)

### 12.3 Smart Screen Not Waking Up

**Problem:** Screen doesn't wake on vehicle detection.

**Solution:**
1. Check **Smart Screen** is enabled in settings
2. Enable **Allow exception from doze mode** in battery settings
3. Ensure app has no background restrictions (in battery settings)

### 12.4 Sound Not Playing

**Problem:** Some or all sounds don't play.

**Solution:**
1. Check phone volume
2. Check sound settings in app
3. Restart radar (**Stop Radar**, then **Start**)
4. Ensure app has no background restrictions (in battery settings)

### 12.5 Speedometer Not Showing Speed

**Problem:** Speedometer is empty or shows "--".

**Solution:**
1. Enable **GPS** in settings
2. Wait 10–30 seconds for GPS signal
3. Move or go to area with better GPS signal (outside)

### 12.6 App Freezes or Unresponsive

**Problem:** App doesn't run properly.

**Solution:**
1. Close app (long press Home/Recent apps, swipe away)
2. Restart app
3. If problem persists, uninstall and reinstall

---

## 13. Support

### 13.1 How to Get Support

If you have an issue not covered in this guide:

1. In app, tap **Log** at bottom of main screen
2. Tap **Copy** and attach log to message
3. Email to: joshuaxcz@gmail.com or create issue on GitHub

### 13.2 GitHub

- **Repository:** https://github.com/JoshuaxCZ/VARIA_RADAR
- **Issues:** https://github.com/JoshuaxCZ/VARIA_RADAR/issues

---

## 14. Credits

Thank you for using Bike Radar Overlay!

This app was created to increase cyclist safety and make cycling more enjoyable. If it helped you, consider supporting development via Ko-fi or the future Pro version.

---

**Version:** 0.9.42  
**Date:** 2026-06-12  
**Copyright:** © 2026 David Urbancik
