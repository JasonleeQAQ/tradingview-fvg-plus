# ⚡ Imbalance Detector for TradingView
### Imbalance Detection Indicator (Pine Script v6) | FVG / Opening Gaps / Volume Imbalance + Fill Tracking + Dashboard + Alerts

> A TradingView **imbalance detection indicator**.  
> It detects **Fair Value Gaps (FVG)**, **Opening Gaps (OG)**, and **Volume Imbalances (VI)** in one script, and adds **fill progress tracking**, **optional auto-delete after full fill**, **dashboard statistics**, and **built-in alerts** to help you analyze price imbalance structures more systematically.

---

## ✨ Features

### 🔹 1) All-in-One Imbalance Detection
Supports three major imbalance types:

- **FVG (Fair Value Gap)**
- **OG (Opening Gap)**
- **VI (Volume Imbalance)**

Each type supports:
- Bullish / bearish detection
- Custom colors
- Optional minimum width filter
- Configurable extension length

---

### 🔹 2) 📦 FVG Zone Visualization + Midline
For FVGs, the script automatically draws:
- Zone boxes
- Mid reference lines

This makes it easier to identify:
- Gap range
- Midpoint reaction areas
- Subsequent fill behavior

---

### 🔹 3) 📊 FVG Fill Progress Tracking (Fill Strength %)
Advanced FVG tracking features include:

- Automatic fill progress calculation (`0% ~ 100%`)
- Fill percentage labels on chart
- Adjustable transparency for filled portion
- Adjustable fill-strength label text size
- Optional auto-delete after full fill

This is especially useful for intraday monitoring.

---

### 🔹 4) ⚙️ Highly Configurable (Grouped Inputs)
Inputs are organized into clear groups for better UX:

- **FVG**
- **OG**
- **VI**
- **Dashboard**

Multiple width filter methods are supported:
- `Points`
- `%`
- `ATR`

---

### 🔹 5) 🧮 Dashboard Statistics
Optional dashboard panel to summarize imbalance behavior:

- Bullish count
- Bullish filled ratio
- Bearish count
- Bearish filled ratio

Configurable options:
- Position: Top Right / Bottom Right / Bottom Left
- Text size: Tiny / Small / Normal

---

### 🔹 6) 🔔 Built-in Alert Conditions
Includes multiple `alertcondition` entries for TradingView Alerts:

- Bullish FVG
- Bearish FVG
- Bullish OG
- Bearish OG
- Bullish VI
- Bearish VI

---

## 🖼️ Preview (Recommended Screenshots)
<img width="1793" height="928" alt="image" src="https://github.com/user-attachments/assets/7e202351-79c0-4f60-aa79-60baf7b59f51" />
<img width="772" height="1612" alt="image" src="https://github.com/user-attachments/assets/dc50f33e-39f3-49b9-b858-1a6b128c4b66" />
🚀 Installation (TradingView)

Open TradingView

Go to Pine Editor

Create a new script and clear the default code

Copy the script from this repository (e.g. fvg.pine)

Click Add to chart

Adjust parameters based on your market, timeframe, and workflow

🧩 Inputs (Grouped Overview)

Below is a practical grouped overview of the main inputs. You can refine this further based on your own release version.

1) Fair Value Gap (FVG)
Parameter	Description	Default
FVG toggle	Show / hide FVG detection	true
Bull/Bear FVG colors	FVG zone colors	Blue / Red
Minimum Width	Enable minimum-width filter	false
Width Threshold	Minimum width value	0
Width Method	Points / % / ATR	Points
Extend FVG	Extend FVG zones to the right	0
Filled Portion Transparency	Transparency for filled area overlay	70
Fill Strength Text Size	Fill percentage label size	Small
Max FVG Count	Maximum visible FVG zones	300
Delete After Fully Filled	Remove FVG after full fill	true
2) Opening Gap (OG)
Parameter	Description	Default
Show OG	Show / hide opening gaps	true
Bull/Bear OG colors	OG zone colors	Blue / Red
Minimum Width	Enable minimum-width filter	false
Width Threshold	Minimum width value	0
Width Method	Points / % / ATR	Points
Extend OG	Extend OG zones to the right	0
3) Volume Imbalance (VI)
Parameter	Description	Default
Show VI	Show / hide volume imbalance zones	true
Bull/Bear VI colors	VI zone colors	Blue / Red
Minimum Width	Enable minimum-width filter	false
Width Threshold	Minimum width value	0
Width Method	Points / % / ATR	Points
Extend VI	Extend VI zones to the right	5
4) Dashboard
Parameter	Description	Default
Show Dashboard	Toggle statistics panel	false
Dashboard Position	Top Right / Bottom Right / Bottom Left	Bottom Right
Dashboard Size	Tiny / Small / Normal	Tiny
🧠 How It Works
✅ Unified Imbalance Detection Framework

The script uses a shared detection function to handle:

Whether a specific imbalance type is enabled

Width filtering (Points / % / ATR)

Detection conditions for the imbalance

This makes the logic more consistent across FVG / OG / VI and easier to extend.

✅ FVG (Fair Value Gap) Detection Logic

Bullish FVG: current low > high[2] with confirmation condition on the middle candle

Bearish FVG: current high < low[2] with confirmation condition on the middle candle

Excludes some overlaps with OG logic to reduce duplicate markings

After detection, it draws:

Zone box

Midline

Fill overlay box

Dynamic fill percentage label

✅ OG (Opening Gap) Detection Logic

Bullish OG: current low > high[1]

Bearish OG: current high < low[1]

Displayed as semi-transparent labeled boxes (OG).

✅ VI (Volume Imbalance) Detection Logic

Uses neighboring candle body/position relationships to detect bullish/bearish imbalances, rendered as dotted border zones.
Supports the same minimum width filtering mechanism as FVG / OG.

✅ Fill Tracking & Statistics

The script maintains arrays to track imbalance zones and dynamically updates:

Filled / unfilled status

Fill percentage

Post-fill display behavior (keep / delete)

Dashboard counts and fill ratios

🔔 Alerts

The script includes the following built-in alert conditions (available in TradingView Alerts):

FVG

Bullish FVG

Bearish FVG

OG

Bullish OG

Bearish OG

VI

Bullish VI

Bearish VI

✅ Usage: In TradingView, create an Alert, select this indicator, and choose one of the conditions above.

📌 Notes

This indicator is for learning, research, and chart assistance only

Not financial advice

Imbalance zones (FVG / OG / VI) do not guarantee a fill or immediate reversal

Consider combining signals with:

Market structure / trend context

Volume

Support / resistance

Timeframe confluence

Risk management
⭐ Support

If this project helps you, consider giving it a Star ⭐
Issues and PRs are welcome!
