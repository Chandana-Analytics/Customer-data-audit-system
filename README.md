# 📊 Customer Data Quality Audit & Reporting System
<img width="1485" height="741" alt="Dashboard_screenshot" src="https://github.com/user-attachments/assets/13221115-c591-49d2-9505-0b45f1734cc1" />

## **Project Purpose**
I built this system to audit a dataset of **2,240 customer records**. My goal wasn't just to "clean" the data, but to create a repeatable engine that gives stakeholders a transparent look at how much they can actually trust their database before they use it for reporting.

## **Why I skipped Pivot Tables**
I made a deliberate choice to **bypass Pivot Tables** for the audit logic. Instead, I built the architecture using manual formulas ('IF', 'AND', 'OR', 'LEN'). 

**The reason is simple:** I wanted full control. By building the logic manually, I could account for specific edge cases—like weird birth years or inconsistent income entries—that automated tools sometimes miss. It’s a bit more work up front, but it makes the whole system 100% auditable and much more precise.

## **Audit Findings**
* **The "Dirty" Data:** I flagged **30 critical errors** that were buried in the raw data.
* **Where the errors are:** Most of the issues were concentrated in the **Income** and **Birth Year** fields. It's a clear sign that the manual entry process there is a bit weak.
* **Data Health Score:** The final score came out to **98.66%**. It sounds high, but that 1.34% error gap in financial fields can actually cause a lot of trouble in a final report.
 
<img width="1418" height="308" alt="Audit_conclusion" src="https://github.com/user-attachments/assets/1ee0d07f-8654-490d-a89c-83bcc126398c" />

## **💡 My Insights**
* **The Income Problem:** Over 80% of the errors were in the Income field. This tells me the entry form probably needs better validation rules (like dropdowns) to stop typos at the source.
* **Human Error:** The birth year issues were mostly manual entry inconsistencies. It’s a classic case of human error being the main driver of data decay.
* **Business Risk:** Even a small error rate can mess up marketing segments. Fixing these 30 records is a small task, but it makes the final insights way more reliable.

## **The Setup**
The diagnostic logic feeds directly into a **Dynamic Dashboard**. This allows a manager to see the "health" of the data at a glance without having to dig through thousands of rows of formulas.

---
**Explore the project:** 'customer_data_quality_audit.xlsx' 
*(Note: I’ve set the Dashboard as the default view so you can see the results immediately.)*
