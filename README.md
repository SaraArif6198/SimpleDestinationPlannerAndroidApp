# DestinationPlannerApp

A simple Android application to plan travel destinations. Users can enter a destination and optional notes, view the details in a separate screen, open the location in Google Maps, or share it with others.

[![Java](https://img.shields.io/badge/Language-Java-orange)](https://www.java.com/)
[![Android SDK](https://img.shields.io/badge/Android%20SDK-yes-brightgreen)](https://developer.android.com/studio)
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

---

## Features

- **Input destination and notes:** Users can enter a travel destination and additional notes.
- **Intent-based navigation:** MainActivity sends the destination details to DisplayActivity using explicit Intents.
- **View destination details:** DisplayActivity shows the destination and notes.
- **Open in Maps:** Open the entered destination in Google Maps using an implicit Intent.
- **Share destination:** Share the destination and notes through other apps (SMS, Email, social media).

---

## Screenshots

*(Include screenshots of MainActivity and DisplayActivity here if available.)*

---


## How It Works

1. **MainActivity**  
   - Users input the destination and optional notes.
   - The "Plan Destination" button validates the input and starts **DisplayActivity**, passing the data via an **explicit Intent**.

2. **DisplayActivity**  
   - Receives the destination and notes from MainActivity.
   - Displays the information in TextViews.
   - **Open in Maps:** Constructs a `geo:` URI and launches an implicit Intent to open Google Maps.
   - **Share Destination:** Creates an implicit `ACTION_SEND` Intent to share the destination details with other apps.

3. **AndroidManifest.xml**  
   - Declares both activities.
   - MainActivity is set as the launcher.
   - DisplayActivity is non-exported for security.

---

## Usage

1. Clone or download the repository.
2. Open it in Android Studio.
3. Build and run the app on an emulator or physical device.
4. Enter a destination and optional notes in the main screen.
5. Tap "Plan Destination" to see details.
6. Use "Open in Maps" or "Share Destination" buttons as needed.

---

## Technologies Used

- Java
- Android SDK
- Android Studio
- Intents (Explicit & Implicit)

---

## Notes

- If no notes are provided, `(No notes)` will be displayed.
- The app prefers Google Maps for navigation but falls back to any available map application if Google Maps is not installed.

---

## Author

**Sara Arif** – Developed as part of an Android learning project.

---

