# minorproject6---EXCEL
# Excel Minor Project 06 – Sales Operations Analytics

The Unlox Academy · DA/DS Track · 100 marks
Workbook: `Excel_Minor_Project_06.xlsx`

## What this is
Answers to all 30 questions on five raw data sheets (Orders, Customers, Products, Sales_Reps, Targets). Every answer is a live formula in its yellow cell, so it recalculates if the data changes. Data sheets are not modified.

## Sheet map (names do not match question numbers)
In this workbook the tab names are shifted, so match by question number, not by tab name.

| Tab name | Questions inside | Topic |
|---|---|---|
| Q2_Cleaning | Q1.1 – Q1.8 | Lookup functions |
| Q3_Aggregation | Q2.1 – Q2.6 | Data cleaning & quality |
| Q4_Pivot | Q3.1 – Q3.6 | Conditional aggregation |
| Q5_Advanced | Q4.1 – Q4.5 | Pivot-style analysis |
| Q1_Lookups | Q5.1 – Q5.5 | Advanced analysis |

## Helper columns
Because data sheets must not be changed, helpers sit on each question sheet, to the right of the answers (column H onward). Each block has a title in row 3 and headers in row 4. Order-level helpers run from row 5 to row 2004 (one row per order).

| Tab | Helpers |
|---|---|
| Q3_Aggregation | duplicate flag, missing-customer flag, is_active; customer name-space flag, first-time city flag |
| Q4_Pivot | order_date, city_clean, final_amount, category, segment, age; rep revenue totals (P:Q); Q3.5 workings (S:T) |
| Q5_Advanced | rep_id, city_clean, category, region, unit_price, unit_cost, profit_margin; month × rep grid (T:AX) |
| Q1_Lookups | rep revenue and rank (H:K); order details (M:Q); West revenue by product (S:U); top 5 reps (W:Y) |

## Formulas used
`VLOOKUP`, `INDEX/MATCH`, `SUMIFS`, `COUNTIFS`, `AVERAGEIFS`, `MAXIFS`, `COUNTIF`, `SUM`, `LARGE`, `RANK`, `TEXTJOIN`, `IF`, `IFERROR`, `PROPER`, `TRIM`, `LEN`.

## Answers (as calculated)
| Q | Answer | Q | Answer |
|---|---|---|---|
| 1.1 | CUST-0173 | 3.4 | 3,342,678.55 |
| 1.2 | Dumbbells 5kg | 3.5 | Below (23.3% of target) |
| 1.3 | Nisha Menon | 3.6 | 982,568.40 |
| 1.4 | 321255 | 4.1 | 1,314,107.39 |
| 1.5 | Electronics | 4.2 | 216,421.52 |
| 1.6 | Bronze | 4.3 | 14.02% |
| 1.7 | Sanjay Kapoor (South) | 4.4 | 6,459,442.98 |
| 1.8 | Amit Singh | 4.5 | 44.90% |
| 2.1 | 20 | 5.1 | Amit Singh |
| 2.2 | 15 | 5.2 | 18,050,689.60 |
| 2.3 | 6 | 5.3 | Smart Watch |
| 2.4 | 30 | 5.4 | Neha Desai \| Shalini Patel \| Deepak Shah \| Nisha Menon \| Arun Iyer |
| 2.5 | 174 | 5.5 | 22,134 |
| 2.6 | 58 | | |
| 3.1 | 1,217,239.01 | | |
| 3.2 | 723 | | |
| 3.3 | 13,981.40 | | |

## Assumptions and data notes
- **Duplicates:** 20 order IDs appear twice. Revenue questions use all rows, as worded, so duplicates are still counted.
- **Missing references:** 30 orders point to customers that do not exist. They have no segment or age, so they drop out of Q3.3 and Q3.6.
- **City names:** ship_city is cleaned with `PROPER(TRIM())` to fix case and spacing.
- **Q3.5:** R015 Nov-24 actual 97,394.65 vs target 418,857 = 23.3%, so the status is "Below".
- **Q4.5:** average of per-order margin `(unit_price − unit_cost) / unit_price` for Delhi orders. A pivot calculated field would give a weighted figure of about 45.97%.
- **Q1.6:** the discount slab table is in rows 18–21 of its sheet, not rows 20–24 as the question text says.

## Submission steps
1. Make your own copy of the master workbook with the link in the PDF.
2. Copy the answers and helper blocks into it, or upload this file to Google Sheets.
3. Rename the file with your full name, as the PDF instructs.
4. Submit the file or its share link through the LMS.
5.
