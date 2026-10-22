# Mess Meal Management System 🍲

A lightweight, browser-based single-page application (SPA) designed to simplify mess/hostel meal management, daily grocery expense tracking, inventory monitoring, and monthly cost settlements.

Built using plain HTML, CSS, and vanilla JavaScript—no external dependencies or backend framework required. All data is persisted locally in the user's browser via `localStorage`.

---

## 🌟 Key Features

*   **User Authentication & Security**:
    *   Simple client-side registration and login workflow using `localStorage`.
    *   Session management with login/logout support.
*   **Interactive Dashboard**:
    *   Monthly snapshot featuring overall totals for meals, bazar expenses, deposits, and active members.
    *   Visual deposit collection percentage progress ring.
    *   Dynamic **Member Balance Board** showcasing individual due or advance statuses.
    *   **Low Stock Radar** to quickly highlight items running low or out of stock.
*   **Member Management**:
    *   Add, edit, or remove mess members.
    *   Toggle member status between `Active` and `Inactive`.
*   **Daily Meal & Recipe Tracking**:
    *   Record daily meal counts (Breakfast, Lunch, Dinner) per member with options for fractional meals (e.g., `0.5`).
    *   Pre-defined meal menu options (Khichuri, Porota, Fish Meal, Meat Meal).
    *   **Automated Stock Consumption**: Deducts required stock items dynamically based on built-in meal recipes when saving meals.
*   **Bazar Expense / Expense Tracker**:
    *   Log daily grocery purchases along with buyer names, amounts, and notes.
    *   Automatic calculation of the monthly meal rate ($\text{Meal Rate} = \frac{\text{Total Bazar Expense}}{\text{Total Meals}}$).
*   **Inventory & Stock Management**:
    *   Track raw ingredient stock levels (e.g., Rice, Dal, Oil, Eggs, Meat).
    *   Manual stock adjustment and usage logging.
    *   Automatic measurement unit conversions ($\text{grams} \rightarrow \text{kg}$, $\text{ml} \rightarrow \text{liters}$, etc.).
    *   Real-time low stock and out-of-stock indicators.
*   **Bua / Cook Bill Splitter**:
    *   Set fixed cook/maid fees for any month.
    *   Automatically splits the bill equally among all active mess members.
*   **Member Deposits**:
    *   Record individual member payment advances/deposits.
*   **Monthly Calculation & Settlement**:
    *   Generates a breakdown detailing meal count, meal cost, cook share, total deposits, and final balance ($\text{Due}$ / $\text{Advance}$) for each member.
    *   Built-in printer-friendly format (`window.print()`) for offline receipt distribution.
*   **Data Backup & Restore**:
    *   Export mess records to a downloadable `.json` file.
    *   Import existing JSON backup files to restore data.
    *   One-click option to load pre-populated **Demo Data**.

---

## 📁 File Structure

```text
.
├── index.html   # Main HTML layout, login forms, and tabbed dashboard markup
├── style.css    # Custom responsive CSS styles, animations, theme design, and print stylesheet
└── script.js    # Application logic, data structures, recipe engine, DOM rendering, and localStorage state management
```

---

## 🚀 Getting Started

Since this project relies purely on standard web technologies without external dependencies, no installation or package managers (like npm or yarn) are required.

### Quick Start Options

1. **Direct Browser Open**:
   * Double-click `index.html` or drag and drop it into any modern web browser (Google Chrome, Mozilla Firefox, Microsoft Edge, Safari).

2. **Using a Local Server (Optional)**:
   * If you prefer running a local server using VS Code's **Live Server** extension or Python:
     ```bash
     # Using Python 3
     python -m http.server 8000
     ```
   * Open `http://localhost:8000` in your browser.

---

## 💡 How to Use

1. **Create an Account**:
   * On first launch, click **Register**, create a username and password, then sign in.
2. **Setup Members**:
   * Navigate to the **Members** tab to add all mess residents.
3. **Add Stock / Grocery Expenses**:
   * Head over to the **Stock** tab to record existing ingredients, or log daily shopping under the **Bazar** tab.
4. **Log Daily Meals**:
   * Select a member, date, meal menu, and meal counts in the **Meals** tab. *Note: Ensure adequate stock is present, as recipes auto-deduct ingredients.*
5. **Manage Maid/Bua Costs**:
   * Enter the total maid fee in the **Bua Bill** tab.
6. **Record Deposits**:
   * As members pay money to the manager/bazar-shopper, enter amounts under the **Deposits** tab.
7. **Generate Monthly Settlement**:
   * Open the **Monthly Bill** tab to review final balance calculations. Use the **Print Monthly Bill** button to save or print physical copies.
8. **Backup Your Data**:
   * Go to the **Backup** tab periodically to **Export Data as JSON** for safekeeping.

---

## 🛠️ Technology Stack

* **HTML5**: Semantic markup structures.
* **CSS3**: Custom properties (CSS variables), Grid/Flexbox layouts, keyframe animations, and `@media print` rules.
* **JavaScript (ES6+)**: Functional logic, dynamic DOM generation, custom item unit conversions, and data persistence via `window.localStorage`.

---

## 📄 License

This project is free to use and modify for personal or educational purposes.