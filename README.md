## 📊 Excel Data Cleaning Workflow

This repository documents a robust Excel-based workflow for transforming raw, messy datasets into clean, structured, and analysis-ready formats. The process is designed for executive dashboards, client reporting, and integration with Power BI or Python pipelines.

---

### 🔧 Key Cleaning Operations

#### 1. **Duplicate Removal**
- Removed duplicate rows based on `Customer ID` to ensure unique customer records.

#### 2. **Blank Cell Handling**
- Replaced all blank cells with `"Data Not Available"` to preserve schema integrity and avoid null errors in downstream tools.

#### 3. **Text Extraction**
- Used `=RIGHT()` and `=LEFT()` functions to extract substrings from product codes, region tags, and embedded metadata.

#### 4. **Conditional Formatting**
- Applied logic-driven formatting using:
  ```excel
  =CHOOSE(MATCH(LOWER(A1), {"one","two","three","four","five","six","seven","eight","nine","ten","twenty"}, 0), 1,2,3,4,5,6,7,8,9,10,20)
  ```
  - Converts textual numbers to numeric values for sorting, filtering, and dashboard use.

#### 5. **Column Merging**
- Combined multiple columns using:
  ```excel
  =Column1 & " - " & Column2
  ```
  - Useful for creating composite keys, full names, or branded labels.

#### 6. **Data Type Normalization**
- Standardized column data types (e.g., text to number, date formatting) to ensure compatibility with Power BI and Python.

---

### ⚙️ Power Query Editor Enhancements

Used **Power Query Editor** for advanced cleaning:
- Removed duplicates and blanks at query level.
- Split and merged columns dynamically.
- Applied transformations with reusable steps.
- Ensured modularity for future automation.

---

### 🧪 Additional Techniques
- Applied filters to isolate outliers and invalid entries.
- Used `=TRIM()` to remove hidden characters.
- Designed cleanup logic anticipating ambiguous, merged, or embedded data.

---

### 📁 Files Included
- `RawData.xlsx` – Original dataset with inconsistencies.
- `CleanedData.xlsx` – Final cleaned version ready for analysis.


---

### 🚀 Use Cases
- Executive dashboards
- Client reporting
- Market analysis pipelines
- eCommerce operations
- Investment strategy datasets

---

### 🧠 Author
**Muhammad Eis**  
Part-qualified CA Inter | Data Strategist  
Architecting modular, branded, and cinematic data storytelling systems for international executive roles.

