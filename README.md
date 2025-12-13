# project--DS512-513
# Project DS512–513  
## Walmart Weekly Sales Analysis

โครงงานนี้เป็นส่วนหนึ่งของรายวิชา **DS512 / DS513 (Data Analytics)**  
มีวัตถุประสงค์เพื่อวิเคราะห์ข้อมูลยอดขายรายสัปดาห์ของ Walmart  
เพื่อค้นหาแนวโน้ม (Insight) และปัจจัยที่ส่งผลต่อยอดขาย

---

## 📊 Dataset Overview

- **Dataset:** Walmart Weekly Sales
- **ช่วงเวลา:** 2010 – 2012
- **Target Variable:** Weekly_Sales
- **Granularity:** รายสัปดาห์ แยกตาม Store และ Department

---

## 🧾 Data Dictionary

| Column Name | Type | Description |
|------------|------|-------------|
| Store | Integer | รหัสสาขา Walmart |
| Dept | Integer | รหัสแผนกสินค้า |
| Date | Date | วันที่ของข้อมูลรายสัปดาห์ |
| Weekly_Sales | Float | ยอดขายรายสัปดาห์ (Target) |
| IsHoliday | Boolean | ระบุว่าสัปดาห์นั้นเป็นวันหยุดหรือไม่ |
| Temperature | Float | อุณหภูมิเฉลี่ย (°F) |
| Fuel_Price | Float | ราคาน้ำมัน |
| MarkDown1–5 | Float | ตัวแปรโปรโมชัน (บางช่วงมีค่า missing) |
| CPI | Float | ดัชนีราคาผู้บริโภค |
| Unemployment | Float | อัตราการว่างงาน |
| Size | Integer | ขนาดของสาขา |
| Type | Category | ประเภทของสาขา (A, B, C) |

---

## 🔍 Exploratory Data Analysis (EDA)

### 1. ภาพรวมยอดขายทั้งหมด
![Total Weekly Sales](picture/totol_weeklysales.png)

### 2. ยอดขายแยกตามแผนก
![Weekly Sales by Department](picture/weekly_sales_department.png)

### 3. เปรียบเทียบยอดขายช่วงวันหยุด vs ไม่ใช่วันหยุด
![Holiday vs Non-Holiday](picture/weely_sales_holiday_vs_non.png)

### 4. Correlation Matrix
![Correlation Matrix](picture/correlation%20metrix.png)

---

## 📈 Key Insights

- ยอดขายมี **Seasonality ชัดเจน** โดยเฉพาะช่วงปลายปี
- ความแตกต่างของยอดขายระหว่าง **Department มีผลสูง**
- ตัวแปรภายนอก เช่น CPI, อุณหภูมิ และราคาน้ำมัน  
  มีความสัมพันธ์กับยอดขายค่อนข้างต่ำ
- Promotion (MarkDown) ส่งผลต่อยอดขายเฉพาะบางช่วง

---

## 🛠️ Project Structure

```text
project--DS512-513/
│
├── data/          # ไฟล์ข้อมูล
├── notebook/      # Jupyter Notebook
├── picture/       # รูปกราฟที่ใช้ใน EDA
│   ├── dashboard.png
│   ├── correlation metrix.png
│   ├── totol_weeklysales.png
│   ├── weekly_sales_department.png
│   └── weely_sales_holiday_vs_non.png
│
└── README.md
