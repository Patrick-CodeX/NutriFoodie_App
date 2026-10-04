<div align="center">

# 🍽️ NutriFoodie

### A Smarter, Cleaner Dining Menu Tracker for Georgia State University (GSU)

[![Flutter](https://img.shields.io/badge/Flutter-%2302569B.svg?style=for-the-badge&logo=Flutter&logoColor=white)](https://flutter.dev/)
[![Dart](https://img.shields.io/badge/dart-%230175C2.svg?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev/)
[![License: Custom](https://img.shields.io/badge/License-Proprietary%20%2F%20Custom-orange.svg?style=for-the-badge)](LICENSE)

<p align="center">
  <b>Tired of clunky web menus and guessing when your favorite campus meals are served?</b><br>
  NutriFoodie transforms the raw Nutrislice API into a fast, organized, and notification-driven dashboard.
</p>

</div>

---

## 🌟 The Purpose

The default Nutrislice web experience can be cluttered, slow, and hard to navigate on mobile devices. Students often miss out on special dishes (like **Passports**, **BBQ Brisket**, or **Sushi**) because there is no built-in way to track menu rotations across the week.

**NutriFoodie** solves this by:
1. **Structuring Menu Items into Clear Stations** (Passports, Almost Home, Bakery, Grill, Deli, Salad Bar, etc.).
2. **Providing an Instant Weekly Favorite Scanner & Local Alerts** so you never miss your favorite dish.
3. **Offering Instant Search & Custom Dietary/Allergen Badges** that make checking ingredients effortless.
4. **Respecting Campus Schedules** (Piedmont Central operates 7 days/week; Piedmont North operates Mon–Fri).

---

## ✨ Key Features

| Feature | Description |
| :--- | :--- |
| 🏷️ **Dynamic Station Mapping** | Accurately groups dishes under their respective station headers using Nutrislice's internal `menu_info` position mapping. |
| 📂 **Collapsible Station Accordions** | Expand or collapse entire stations (or use the one-tap **Expand All / Collapse All** toggle) to remove screen clutter. |
| 🎛️ **Station Filter Ribbon** | Toggle entire food sections on/off (e.g., hide Deli Condiments or Salad Toppings). |
| 🔍 **Live Search Bar** | Filter dishes in real time by name, category, or allergen. |
| ⭐ **Food Watchlist & Star System** | Star any dish with a single tap to track future occurrences. |
| 🔔 **Weekly Schedule Alerts** | Scans Breakfast, Lunch, and Dinner across the full week to notify you exactly what day and meal your favorites appear. |
| 🥗 **Clear Dietary & Allergen Badges** | Instant visual tags for Vegan (`🌱`), Vegetarian (`🥗`), Halal (`☪️`), Gluten-Free (`🌾`), Dairy (`🥛`), Pork (`🥓`), and more. |

---

## 🏗️ How It Works (Technical Architecture)

NutriFoodie communicates directly with the official GSU Nutrislice REST endpoints, that allows the app to pull in present and presumed future dishes:

### 1. Relational `menu_info` ➔ `menu_items` Ingestion
Unlike standard flat menu lists, Nutrislice returns menu metadata inside a `menu_info` object keyed by dynamic section IDs (which vary between campuses and meal periods).

## 📱 Supported Dining Locations
Campus Location	Slug	School ID	Schedule
Piedmont Central	piedmont-central	46511	Monday – Sunday
Piedmont North	piedmont-north	46513	Monday – Friday

## 📦 Dependencies
http — REST API communication.
intl — Date formatting and calendar math.
shared_preferences — Persistent storage for starred items and user settings.
flutter_local_notifications — Local system notification scheduling.
timezone — Accurate timezone-aware alert triggers.

## 🤝 Contributing
Contributions, feature requests, and issue reports are welcome!
Feel free to check the Issues page if you want to contribute, and let me know of any requests.
