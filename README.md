# Power Bi - Calendar Table
The Power BI Calendar Table is a pre-built date dimension that instantly adds time intelligence to your data models.
![image](https://github.com/user-attachments/assets/57bd6136-1e4d-433d-b86f-fad383f3c20f)
# Calendar Table Import Guide

A simple guide for extracting Calendar table from one PBIX and importing it into another.

---

## 1. Open the Source PBIX & Copy the Query

1. In Power BI Desktop, open your **.pbix** file.  
2. Go to **Transform data** → **Power Query Editor**.  
3. In the Queries pane, right-click on downloaded **Calendar** pbix file's query and choose **Advanced Editor**.  
4. Select all the M code, copy it to your clipboard, then close the editor.

---

## 2. Paste into the Target PBIX

1. Open the other Power BI file where you want to reuse the calendar.  
2. Go to **Transform data** → **Power Query Editor**.  
3. On the **Home** tab, click **New Source** → **Blank Query**.  
4. Right-click the new query, choose **Advanced Editor**, paste in the M code you copied, and click **Done**.  
5. Rename this query to **Calendar** (or another name you prefer).

---

## 3. Validate & Mark as Date Table

1. In Power Query, ensure each column (Date, Year, Month, etc.) has the correct data type.  
2. Click **Close & Apply** to load it back into the main model.  
3. In Model view, select the **Calendar** table, then on the ribbon choose **Table Tools** → **Mark as Date Table**, and pick your **Date** column.

---

## 4. Create Relationships

1. In Model view, drag **Calendar[Date]** onto each fact table’s date field (e.g., **Tasks[DueDate]**, **Tasks[StartDate]**) to create relationships.  
2. Configure the relationship as **Many-to-One** with **Single** cross-filter direction.

---

## 5. Refresh & Test

1. Refresh the model to ensure your calendar and fact tables load correctly.  
2. Build a quick visual (e.g., a slicer or table) using **Calendar** fields to confirm everything’s working.

---

That’s it! Your Calendar table is now fully available in the new PBIX, ready for slicers, time intelligence, and any custom visuals.
