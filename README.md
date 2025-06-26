
# 💇‍♀️ Beauty Salon Database Management System

This project is a real-world simulation of how a multi-branch beauty salon manages its day-to-day operations using a robust and well-designed relational database system.

From booking appointments and maintaining customer profiles to handling inventory, memberships, staff performance, and billing — our system provides a centralized, efficient, and normalized solution to meet the dynamic needs of a modern beauty salon.

Built as part of an academic group project, the system was developed in structured phases:

1. A practical scenario-driven approach that mirrors real business logic

2. A complete ER diagram, relational model, and normalization proofs

3. An optimized SQL schema with integrity constraints and realistic data

4. 25+ advanced queries solving real-world analytical and managerial needs

## 👩‍💼 Project Contributors
- Yashasvi Jadav (202301069)
- Jhil Patel (202301090)
- Sanya Vaishnavi (202301117)
- Sadana Dharavath (202301121)

---

### 📌 Phase 1: Scenario Ideation
We began by understanding the real-world workflows of a beauty salon and translated them into system-level actors and use cases.

Defined user roles and responsibilities across:

- Customers: Book services, review staff, rate appointments, and redeem membership offers, browse and purchase products.

- Staff: Manage appointments, perform services, and maintain schedules.

- Admins: Oversee branches, assign staff, manage services/products,watch stocks and handle financial reports.

- Visitors: Explore available services, offers, and salon locations.

📄 Refer: Scenario Description.pdf

---

### 🧠 Phase 2: ER Diagram
In this phase, we converted our scenario into an Entity-Relationship (ER) diagram to model the system's logical structure.

Key highlights:

- Captures core entities such as Customer, Staff, Administrator, Service, Product, Membership, Branch, and Supplier.

- Represents relationships like:

   1. Books_Appointment (Customer ↔ Service)
   2. Purchase (Customer ↔ Product)
   3. Used_For (Service ↔ Product)
   4. Supplies (Supplier ↔ Product)
   5. Offered_By (Branch ↔ Service)
   6. Provides (Staff ↔ Service)
   7. Premium_Customers (Customer ↔ Membership)

- Includes:

   - Many-to-many relationships
   - Aggregation via billing
   - Supervisory hierarchy in staff roles (SupervisorID)

📄 Refer: Normalization+ER+Relational.pdf (ER section)

---

### 🧱 Phase 3: Relational Model

In this phase, the ER diagram was translated into a complete relational schema using SQL table definitions. Each relationship and entity was converted into a normalized table with appropriate constraints.

Key features:

- Over 20 well-structured tables with clear relationships and unique identifiers.

- Primary keys and foreign keys properly defined with ON DELETE and ON UPDATE cascading rules.

- Composite keys used for many-to-many relations like Books_Appointment, Purchase, Provides, etc.

- Integrity constraints such as CHECK (e.g., for rating, stock, and discount limits) to ensure valid data entries.

- Branch_ID included in key transactional tables like Purchase and Books_Appointment for branch-specific tracking and analytics.

📄 Refer: 
- Normalization.pdf
- ERD.pdf
- Relational_Model.pdf

---

### 🔍 Phase 4: Normalization

To ensure data consistency and avoid redundancy, all relations in the schema were normalized up to BCNF.
- 1NF: Atomic columns
- 2NF: Removed partial dependencies from composite keys
- 3NF & BCNF: No transitive or non-key dependencies

📄 Refer : Normalization Proof Section in PDF

---

### 🧪 Phase 5: Schema Implementation

This phase involved translating the relational model into SQL scripts to create the actual database structure.

-  Schema implemented using PostgreSQL with primary keys, foreign keys, CHECK constraints, and cascading rules.

- Insert scripts populated the tables with realistic sample data representing customers, appointments, services, products, staff, bills, and more.

- Composite keys were used in many-to-many relationships to preserve data integrity.

📂 Refer:
- DDLScript.txt
- INSERTScript.txt

---

### 🧠 Phase 6: Real-Life Analytical Queries
We developed a set of advanced SQL queries to extract actionable insights from the database — mimicking real salon reporting and analysis scenarios.

Key focus areas:

1.  Customer behavior: loyalty tracking, birthday campaigns, product-only purchases

2. Sales insights: top services, revenue per branch, monthly trends

3. Inventory monitoring: low stock alerts, product usage vs. supply

4. Staff analytics: top-rated employees, experience-based filters

5. Forecasting patterns: peak hours, inactive customers, seasonal trends

📂 Refer: DBMS_queries.txt

---

## 📂 Repository Overview

```
├── README.md
├── Scenario Description.pdf
├── Normalization.pdf
├── ERD.pdf
├── Relational_Model.pdf
├── DDLScript.txt
├── INSERTScript.txt
├── DBMS_queries.txt
```

---

## 🛠 Technologies
- PostgreSQL (DDL, DML)
- Draw.io (ERD,Relational_Model)
- Query testing: pgAdmin
- Document format: PDF & TXT

---
## 📌Conclusion
Working on this project helped us translate a real-world scenario into a structured and efficient database system. Through each phase—right from mapping user needs and designing relationships to writing complex queries—we strengthened our understanding of core database principles like normalization, integrity constraints, and data analytics. The outcome is a practical, scalable solution that reflects both technical learning and real-world application.

##  📌Acknowledgment

We would like to express our sincere gratitude to our faculty guide and the DBMS course TAs for their guidance and support throughout this project. Their insights and feedback played a crucial role in shaping our understanding of real-world database systems. We also appreciate the collaborative efforts of our teammates, whose consistent contributions made this project a success.



