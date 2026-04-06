# Ticket Management System – Project Walkthrough

## 📖 Project Overview

The Ticket Management System is a business application built using Microsoft Power Apps with SharePoint Online as the backend data source.

The application is designed to streamline ticket creation, tracking, and resolution within an organization. It provides a centralized interface for managing tickets with real-time status updates, filtering capabilities, and KPI insights.

### 🎯 Objective

The goal of this project is to:

- Digitize manual ticket tracking processes
- Provide visibility into ticket status and workload
- Enable efficient ticket lifecycle management
- Build a scalable low-code solution using Power Platform

  
### 🏗️ Architecture
🔹 Frontend
- Built using Canvas App in Power Apps
- Layout with multiple screens:
- Landing Dashboard
- Ticket Details Screen
- Create Ticket Screen

🔹 Backend
- SharePoint List used as the data source
- Stores all ticket-related information

## 🗂️ Data Model (SharePoint)
Column Name	Type	Description
ID	Auto Number	Unique Ticket ID
Subject	Single Line Text	Ticket title
Description	Multi-line Text	Issue details
Department	Choice	IT, HR, Finance
Status	Choice	New, In Progress, On Hold, Closed
Priority	Choice	Low, Medium, High
Created By	Person	Ticket creator
Date Created	Date	Ticket creation date
Date Closed	Date	Ticket closure date


#### 🖥️ Application Walkthrough
### 🔹 1. Landing Screen (Dashboard): This is the main screen of the application.

#### ✅ Features:
- Left Navigation Panel
- All Tickets
- New Tickets
- In Progress
- On Hold
- Closed
- Tickets Older than 3 Days
- Opened Today
- Closed Today
- KPI Cards (Top Section)
- Total Tickets
- New Tickets
-In Progress
- Closed Tickets
- Tickets Gallery
- Displays list of tickets


####  Each row includes:
- Subject
- Status
- Priority
- Department
- Navigation


Clicking arrow icon → opens Ticket Details screen

### 🔹 2. Create New Ticket Screen: This screen allows users to raise a new ticket.

#### ✅ Input Fields:
- Created By (Auto-filled)
- Subject
- Description
- Department (Dropdown)
- Priority (Dropdown)


#### ✅ Functionality:
- On clicking Create Ticket:
- Data is submitted to SharePoint
- New record is created
- User is redirected to dashboard


### 🔹 3. Ticket Details Screen: This screen shows complete information about a selected ticket.

#### ✅ Read-Only Fields:
- Ticket ID
- Subject
- Description
- Created Date
- Closed Date

#### ✅ Editable Fields:
- Status
- Assigned To
- Department
- Priority
- Internal Comments
✅ Actions:
User updates ticket details
Clicks Save → updates SharePoint list
