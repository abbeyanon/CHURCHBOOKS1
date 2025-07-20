# CHURCHBOOKS1

**CHURCHBOOKS1** is the master Frappe-based monorepo for managing a unified church ERP and LMS system. It integrates two modular apps as Git submodules:

- `cfms_plus`: Church Finance and Management System  
- `lms_app`: Learning Management System for discipleship and training

---

## 📦 Apps Included

- [`cfms_plus`](https://github.com/abbeyanon/cfms_plus): Enhanced Church Finance & ERP App  
- [`lms_app`](https://github.com/abbeyanon/lms_app): A modular LMS for churches  

---

## ✨ Features

### 1. `cfms_plus`: Church Finance & ERP

- Church branch(Company) setup with automatic Chart of Accounts
- Member registration with unique auto-generated Member IDs
- Church event and program management with workflows
- Attendance tracking for events & services
- Integration of giving with member profiles and auto-generated journal entries
- Scheduled tasks for automated event updates
- Fixtures: Custom Roles, Workflows, Scripts, Templates, and Workspaces

### 2. `lms_app`: Learning Management System

- Course and program creation  
- Trainer and student enrollment workflows  
- Certificate generation  
- Event-driven training sessions  
- Role-based permissions and approvals  

---

## ⚙️ Installation Guide

> **Prerequisites:**  
> - Working Frappe Bench setup  
> - Installed ERPNext  
> - Created site (e.g., `tuku_pay`)  

### 🛠 Steps

```bash
# Step 1: Clone the master repository with submodules
git clone --recurse-submodules https://github.com/abbeyanon/CHURCHBOOKS1.git
cd CHURCHBOOKS1

# Step 2: Copy submodule apps to your bench apps directory
cp -r apps/cfms_plus ~/frappe-bench/apps/
cp -r apps/lms_app ~/frappe-bench/apps/

# Step 3: Install apps into your site
cd ~/frappe-bench
bench --site your_site_name install-app cfms_plus
bench --site your_site_name install-app lms_app

# Step 4: Migrate and start
bench --site your_site_name migrate
bench start
