# Yeast Calculator for Pizzeria Kintari

A simple web utility to calculate yeast quantities for pizza dough. It uses flour weight as the primary input for all calculations, providing a straightforward way to build a recipe.

## Features

* **Flour-Based:** All calculations are based on the initial flour weight.
* **Adjustable Parameters:** Allows for the adjustment of key variables:
    * Flour Weight (kg)
    * Dough Hydration (%)
    * Salt Content (% relative to flour)
    * Ambient Temperature (°C)
    * Desired Leavening Time (hours)
* **Dual Yeast Calculation:** Instantly provides the required quantities for both **Fresh Yeast** and **Active Dry Yeast**.
* **Total Dough Weight Calculation:** Automatically calculates the final weight of the dough based on the specified inputs.
* **Bilingual Interface:** Features a toggle between **Italian (IT)** and **English (EN)**.
* **Responsive Design:** Works on both desktop and mobile devices.
* **Transparent Formulas:** Includes a section that shows the formulas used for the calculations.

## Usage Instructions

1.  **Launch the application** by opening the `index.html` file in a modern web browser.
2.  **Select the desired language** using the IT/EN toggle switch located in the top-right corner of the interface.
3.  **Input the dough parameters** in the provided fields on the left-hand side:
    * Begin with the **Flour Weight**.
    * Set the target **Hydration** and **Salt** percentages.
    * Enter the current **Ambient Temperature** and the desired **Leavening Hours**.
4.  **Review the results**, which are displayed instantly on the right-hand side. The calculator will output:
    * The final **Total Dough Weight**.
    * The required amount of **Fresh Yeast** in grams.
    * The required amount of **Active Dry Yeast** in grams.
5.  (Optional) Expand the "Show Calculation Formulas" section to review the underlying mathematical logic.

## Technology Stack

* **HTML5:** Provides the core structure for the application.
* **Tailwind CSS:** Utilized for styling.
* **Vanilla JavaScript:** Powers all calculation logic and interactivity.

## Calculation Formulas

The calculator uses the following formulas:

1.  **Fresh Yeast Calculation:**
    ```
    Fresh Yeast (g) = (Flour Weight (kg) * 500) / (Temperature (°C) * Hours)
    ```

2.  **Dry Yeast Conversion:**
    ```
    Dry Yeast (g) = Fresh Yeast (g) / 3
    ```

3.  **Total Dough Weight Calculation:**
    ```
    Water (kg) = Flour Weight * (%Hydration / 100)
    Salt (kg) = Flour Weight * (%Salt / 100)
    Total Weight (kg) = Flour Weight + Water + Salt
    ```
    *Note: The weight of the yeast is considered negligible in the final dough weight calculation.*

## License

This project is open source and is made available under the [MIT License](https://opensource.org/licenses/MIT).

---
*A utility for Pizzeria Kintari.*
