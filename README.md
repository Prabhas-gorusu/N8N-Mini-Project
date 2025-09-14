
# 📊 Attendance Automation Workflow (n8n)

This repository contains an **n8n workflow** that automates the process of monitoring student attendance, filtering absentees, and sending SMS notifications to parents/guardians.

---

## 🚀 Features

* ⏰ **Automated Scheduling** – Uses a **Cron Trigger** to run the workflow at a set time daily.
* 📑 **Fetch Attendance** – Reads student attendance records from a Google Sheet.
* 🧹 **Filter Absentees** – Identifies students marked as absent.
* ➗ **Split Students** – Processes each absentee individually.
* 📲 **Send SMS Alerts** – Sends an SMS notification to parents/guardians using **Twilio (or any SMS service)**.
* 📋 **Log Attendance Data** – Retrieves and logs rows for record-keeping.

---

## ⚙️ Workflow Overview

The workflow follows these steps:

1. **Cron Trigger** → Runs at a scheduled time (e.g., every morning at 9:00 AM).
2. **Fetch Attendance** → Reads data from a Google Sheet containing attendance records.
3. **Filter Absentees** → Filters out students who are marked **Absent**.
4. **Split Students** → Splits the list of absentees into individual items for processing.
5. **Send SMS** → Sends a customized **SMS alert** to each absentee’s parent/guardian.
6. **Get Row(s) in Sheet** → Reads and logs student details for reference or reporting.

---

## 🛠️ Requirements

* [n8n](https://n8n.io/) (self-hosted or cloud)
* Google Sheets integration (for attendance records)
* Twilio (or another SMS service) for sending messages

---

## 📥 Installation & Setup

1. Import the workflow JSON file into your **n8n instance**.
2. Configure credentials:

   * **Google Sheets** → Provide access to the attendance sheet.
   * **Twilio (or SMS provider)** → Enter API credentials for sending SMS.
3. Update workflow settings:

   * Set the **Cron Trigger** schedule.
   * Adjust the **Filter Absentees** logic to match your sheet’s “Absent” marker.
   * Customize SMS message content.

---

## 📊 Example Google Sheet Format

| Student Name   | Date       | Status  | Parent Contact |
| ---------------| ---------- | ------- | -------------- |
| Prabhas Gorusu | 2025-09-14 | Present | +916304761355    |
| Sharief SK     | 2025-09-14 | Absent  | +917893254003    |

---

## 📸 Workflow Screenshot

<img width="1919" height="1079" alt="Screenshot 2025-09-14 124010" src="https://github.com/user-attachments/assets/f4fee542-1ebf-4a13-a0da-204237cc626f" />


---

## 📌 Future Enhancements

* 📧 Email alerts in addition to SMS
* 📊 Attendance summary reports to teachers
* 🔔 Slack/WhatsApp notifications
* 📅 Weekly attendance statistics

---

## 📜 License

MIT License.
Feel free to use and adapt this workflow for your own projects.

---

👉 Do you want me to **export this workflow into JSON (n8n import file)** so you can include it in your repo, or just keep the README?
