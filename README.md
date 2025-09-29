# Sales Dashboard Application Documentation

## 1. Overview

The **Sales Dashboard** is a custom Salesforce Lightning Application designed for BrightTech Solutions' management team. Its primary purpose is to centralize sales performance monitoring, track leads and opportunities, and provide quick insights into key sales metrics and underperforming areas.

| Component | Description |
| :--- | :--- |
| **App Name** | `Sales Dashboard` |
| **Deployment Environment** | Salesforce Lightning Experience (Desktop & Phone) |
| **Intended Users** | Sales Managers and Management Team |

---

## 2. Key Features and Navigation

This application utilizes **Standard Navigation** and is anchored by a custom Home Page tailored for immediate data visualization.

### Navigation Tabs

The app's navigation menu is configured with the following key tabs:

| Tab Name | Purpose |
| :--- | :--- |
| **Home (Sales Dashboard)** | The custom landing page; designed with key components (charts, reports, and recent records) to provide an immediate summary of sales performance. |
| **Opportunities** | Standard tab for tracking and managing open, closed, and pending sales deals. |
| **Accounts** | Standard tab for managing customer and partner organizations. |
| **Leads** | Standard tab for tracking and qualifying potential customer records. |
| **Reports** | Standard tab providing access to all sales-related reports and dashboards. |

### Custom Home Page Components

The custom `Sales Dashboard Home Page` is built using the **Lightning App Builder** and features high-priority components designed to provide managers with a quick performance snapshot:

| Component | Function |
| :--- | :--- |
| **Key Deals - Recent Opportunities** | A **List View** component filtered to display high-value or recently updated opportunities, such as: *Express Logistics Portable Truck Generators* and *Express Logistics and Transport*. |
| **Quarterly Performance** | A **Report Chart** component visually tracking the sales pipeline against a set goal (R665 000 goal). It displays progress over time for Closed deals and the combined value of Closed and high-probability Open opportunities ($>70\%$ probability). |
| **Chatter Feed** | A standard **Chatter** component for team collaboration, allowing users to discuss key performance indicators and deals directly on the dashboard. |

---

## 3. Deployment and Access Configuration

The **Sales Dashboard** app is deployed for end-user access via specific profile and permission set assignments.

### Profile and Permission Set Summary

Access is managed by assigning the custom **`Sales Dashboard Access`** permission set to the base **`Test User Profile`**.

| Setting | Details |
| :--- | :--- |
| **Base Profile** | `Test User Profile` (Cloned from **Salesforce - Minimum Access**) |
| **Permission Set** | `Sales Dashboard Access` |
| **App Visibility** | Visible for `Test User Profile` |

### Permissions Granted via "Sales Dashboard Access"

The custom permission set provides the necessary data access for management-level users to view and modify sales data.

| Object | CRUD Operations Enabled | Field Access | Data Access |
| :--- | :--- | :--- | :--- |
| **Accounts** | Create, Read, Update, Delete (CRUD) | Read and Write access to **all** Fields | View and Modify **All** Records |
| **Opportunities**| Create, Read, Update, Delete (CRUD) | Read and Write access to **all** Fields | View and Modify **All** Records |
| **Leads** | Create, Read, Update, Delete (CRUD) | Read and Write access to **all** Fields | View and Modify **All** Records |

---

## 4. Testing and Verification

The application's successful deployment and access controls were verified using a dedicated test account.

| Test User Details | Result |
| :--- | :--- |
| **Test User Name** | New Test User |
| **Assigned Profile** | Test User Profile |
| **Access Verification** | User successfully logged in and was able to access the `Sales Dashboard` app via the App Launcher. All configured tabs and the custom Home Page loaded correctly. |
