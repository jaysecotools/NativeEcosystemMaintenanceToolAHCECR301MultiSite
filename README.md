# Native Ecosystem Maintenance Tool

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![AHCECR301](https://img.shields.io/badge/AHCECR301-Compliant-green.svg)](https://training.gov.au/Training/Details/AHCECR301)

A comprehensive, offline-first web application for managing native ecosystem sites, designed to meet AHCECR301 compliance requirements. This tool provides multi-site management, interactive mapping, species tracking, maintenance planning, and reporting capabilities—all within your browser.

## ✨ Features

- **🏢 Multi-Site Management**: Create, edit, and switch between multiple ecosystem sites with isolated data for each.
- **🗺️ Interactive Mapping**:
  - View site zones, vegetation, and weed locations on an interactive map.
  - **Edit Mode**: Draw polygons, markers, and lines directly on the map.
  - Categorize and color-code features (Zones, Vegetation, Weeds, Points of Interest).
  - Save all map edits persistently for each site.
- **📝 Site Assessments**: Record detailed assessments including ecosystem components, health ratings, and identified threats.
- **🌿 Species Register**: Maintain a searchable database of flora and fauna species with their status (Native, Weed, Endangered, etc.) and observation history.
- **📅 Maintenance Plan**: Schedule, track, and complete maintenance activities with a visual calendar and categorized task lists (Upcoming, Completed, Overdue).
- **🔭 Monitoring**: Log fauna sightings and vegetation surveys, complete with charts to visualize trends.
- **📄 Compliance & Reporting**: Track compliance against a built-in checklist and generate reports (PDF, Excel, Word) for compliance, maintenance, monitoring, and health trends.
- **⚙️ Data Management**: Export all data for backup or sharing, with built-in test data reset functionality.
- **💾 Offline-First**: All data is stored in the browser's `localStorage`, allowing the app to work without an active internet connection.

## 🚀 Getting Started

### Prerequisites

This is a pure HTML/CSS/JavaScript application. No build tools or server-side setup are required. You just need:

- A modern web browser (Chrome, Firefox, Edge, Safari).
- An active internet connection for the first load to fetch CSS/JS libraries from CDNs.

### Installation

1.  **Download the `index.html` file** from this repository.
2.  Save it to a location on your computer (e.g., `Documents/my-eco-tool/index.html`).
3.  **Double-click the `index.html` file** to open it in your web browser.

That's it! The application will load and initialize with sample data.

## 💻 Usage Guide

### 1. Sites
- Use the dropdown in the sidebar to switch between sites.
- Click the **gear icon** next to the dropdown to **Manage Sites** (Add, Edit, Delete, or Configure Map Center).
- All data (assessments, species, activities) is specific to the currently selected site.

### 2. Dashboard
The Dashboard provides a high-level overview:
- **Statistics Cards**: Upcoming tasks, total assessments, species count, and compliance percentage.
- **Upcoming Tasks**: A list of pending maintenance activities.
- **Site Health Indicators**: A radar chart showing key ecosystem metrics over time.
- **Compliance Checklist**: A quick view of your progress.

### 3. Interactive Map (Key Feature)
- **View Layers**: Use the buttons (`Zones`, `Vegetation`, `Weeds`) on the map to toggle different data layers.
- **Edit Mode**: Click the **Edit Mode** button on the map. Green control buttons will appear.
    - Draw polygons (for zones), markers (for points of interest), or lines.
    - After drawing a shape, a modal will appear. Fill in the **Name** and **Category**, choose a **Color**, and add a description.
    - Click **Save Feature** to add it to your map for the current site.
- **Edit/Delete Features**: Click on any custom-drawn feature to open a popup, then click the **Edit** button to modify or delete it.
- **Save**: Click the **Save** button to persist all map changes to `localStorage`.

### 4. Site Assessment
- Click **New Assessment** to record an evaluation.
- Fill in the date, assessor, description, ecosystem components present, and overall health.
- Select identified threats from the list.
- View all previous assessments in the table.

### 5. Species Register
- Click **New Species** to add a plant, animal, or fungus to the register.
- Fill in scientific name, common name, type, and conservation status.
- Upload an image for the species.
- The register helps track native, weed, and threatened species on your site.

### 6. Maintenance Plan
- **New Activity**: Schedule tasks like weed control, revegetation, or surveys.
- **Activity Tables**: View tasks grouped by status (Upcoming, Completed, Overdue).
- **Calendar View**: See all scheduled activities in a monthly, weekly, or daily calendar layout.

### 7. Monitoring
- Log **Fauna Sightings** and **Vegetation Surveys** through dedicated forms.
- Charts provide visual trends for fauna sightings and vegetation cover.
- All monitoring entries are listed in a searchable table.

### 8. Reports
- Generate reports in **PDF**, **Excel (XLSX)**, or **Word (DOC)** format.
- Report types include Compliance, Maintenance Summary, Monitoring Summary, and more.
- Generated reports are saved to the app's history and can be previewed or downloaded again.

### 9. Legislation & Settings
- **Legislation Tab**: Reference information on relevant Australian environmental laws (EPBC Act, State/Territory legislation).
- **Settings Tab**:
    - Update your user profile.
    - Manage all sites.
    - Export all data, create a backup, or reset to test data.

## 🛠️ Technology Stack

- **Core**: HTML5, CSS3, JavaScript (ES6+)
- **UI Framework**: Bootstrap 5.3
- **Icons**: Bootstrap Icons
- **Mapping**: Leaflet.js, Leaflet Geoman (for drawing/editing)
- **Charts**: Chart.js
- **Calendar**: FullCalendar
- **Reporting**: jsPDF, SheetJS (XLSX)
- **Storage**: Browser `localStorage`

## 📊 Data Persistence

All data is saved in your browser's `localStorage`. This means:
- **No account or login required.**
- The app works completely offline after the initial load.
- Data is specific to the browser and device you are using.
- **To move data between computers**, use the **Export All Data** button in Settings, then import the JSON file (import functionality is planned).

## 📝 Known Issues & Next Steps

As noted in the source code comments, here are the current limitations and planned enhancements:

### To Complete / Fix
- [ ] **Data Import**: Add functionality to import previously exported JSON data.
- [ ] **User Guide**: Create `UserGuide.html` (the current link opens a blank tab).
- [ ] **User Authentication**: Implement for multi-user setups.
- [ ] **Cross-Browser Testing**: Verify Leaflet Geoman tools and FullCalendar on Safari and mobile devices.

### Enhancements to Consider
- [ ] Cloud backup/sync.
- [ ] Offline support via Service Workers.
- [ ] GPS integration for mobile devices.
- [ ] Email notifications for upcoming tasks.
- [ ] QR code scanning for species/plot identification.
- [ ] CSV data export.

### Known Minor Issues
- [!] Map may need a manual resize when switching sites (refreshing the tab fixes it).
- [!] Photo preview URLs are temporary; images do not persist after a page reload.
- [!] FullCalendar can be slow to refresh with many activities.
- [!] Print styles need refinement for better report layouts.

### Testing Status
- [✓] Desktop: Chrome, Firefox, Edge
- [?] Mobile responsiveness (needs testing on tablets/phones)
- [?] Safari compatibility (unverified for Leaflet and FullCalendar)

## 🤝 Contributing

Contributions are welcome! If you'd like to help fix a bug or implement a new feature, please feel free to submit a pull request or open an issue.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgements

- Built to support compliance with the **AHCECR301 - Maintain native ecosystem** unit of competency.
- Uses open-source libraries from Leaflet, Bootstrap, Chart.js, FullCalendar, jsPDF, and SheetJS.
- Map data &copy; [OpenStreetMap](https://www.openstreetmap.org/copyright) contributors.
