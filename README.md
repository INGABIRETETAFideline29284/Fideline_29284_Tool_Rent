# ToolRent: Construction Power-Tool Rental & Deposit Tracker

**Student Name:** INGABIRE TETA Fideline
**Student ID:** 29284
**Course:** INSY 8311 – Database Development with PL/SQL
**Instructor:** Eric Maniraguha  
**Domain:** Business and Entrepreneurship  

## 1. Problem Statement
Hardware shops and equipment yards that rent out drills, generators, compactors, and concrete mixers frequently lose equipment, double-book tools, or fail to collect late-return fees because rentals are recorded in paper notebooks. Without automated tracking of security deposits and equipment condition, shop owners suffer revenue leakage and disputes over damaged or overdue tools.

## 2. Objectives
* **Main Objective:** Develop a normalized Oracle PL/SQL database system to automate power-tool rentals, security deposit tracking, and overdue penalty enforcement.
* **Specific Objectives:**
  1. Design a 3NF relational schema covering customers, tools, rentals, payments, and audit logs.
  2. Enforce database-level business rules using PL/SQL triggers to block renting unavailable or damaged tools.
  3. Automate rental fee, late penalty, and deposit refund calculations using PL/SQL procedures and functions.
  4. Build an interactive Oracle APEX / Streamlit user interface connected live to the Oracle database.

## 3. Data Source
* **Dataset:** [Commercial Tool Rental Data for 2016 and 2017 (Kaggle)](https://kaggle.com) — contains real-world tool categories, rental dates, durations, and pricing rates with no personally identifiable information (PII).

## 4. Planned Innovation
* **Option:** User Interface (Oracle APEX or Python Streamlit) connected live to the Oracle PDB.
* **Functionality:** Shop clerks will issue tools, log returns, and inspect overdue alerts through a web form that directly calls PL/SQL procedures (`prc_issue_rental`, `prc_process_return`), while business rules remain strictly enforced inside Oracle.

## 5. Planned Tables & PL/SQL Features
* **Tables (3NF):** `CUSTOMERS`, `TOOLS`, `RENTALS`, `PAYMENTS`, `RENTAL_AUDIT_LOG`.
* **Procedures & Functions:** `prc_issue_rental`, `prc_process_return`, `fn_calculate_rental_fee`, `fn_check_customer_standing`.
* **Triggers & Automation:** `trg_prevent_unavailable_rental` (blocks double-booking), `trg_rental_audit` (logs all changes), and `DBMS_SCHEDULER` nightly job to flag overdue rentals.

## 6. References (APA)
* Maillie, D. (2018). *Commercial Tool Rental Data for 2016 and 2017* [Data set]. Kaggle. https://kaggle.com
* National Institute of Statistics of Rwanda (NISR). (2025). *Rwanda Establishment Census & Construction Sector Activity Report*. https://statistics.gov.rw
* Oracle Corporation. (2023). *Oracle Database PL/SQL Language Reference*. https://oracle.com
* Patel, R., & Kumar, S. (2022). Relational database triggers and audit logging for financial accountability in SMEs. *International Journal of Database Management Systems*, 14(3), 12–24.
* Wang, Y., & Liu, H. (2021). Equipment rental inventory optimization and maintenance scheduling in construction supply chains. *Journal of Construction Engineering and Management*, 147(8).

