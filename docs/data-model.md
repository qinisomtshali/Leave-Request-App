# 📊 Data Model – HearConnect Leave Request App

This document outlines the structure and purpose of the SharePoint lists used in the app.

---

<details>
<summary><strong>📁 LeaveRequests</strong> – Main record of leave applications</summary>

<table>
  <thead>
    <tr>
      <th>Field</th><th>Type</th><th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Title</td><td>Text</td><td>Leave request title</td></tr>
    <tr><td>EmployeeName</td><td>Person</td><td>Submitter’s display name</td></tr>
    <tr><td>EmployeeEmail</td><td>Text</td><td>Used in workflows</td></tr>
    <tr><td>LeaveType</td><td>Choice</td><td>Annual, Sick, etc.</td></tr>
    <tr><td>StartDate / EndDate</td><td>Date</td><td>Leave duration</td></tr>
    <tr><td>TotalDays</td><td>Number</td><td>Calculated duration</td></tr>
    <tr><td>Reason</td><td>Multiline Text</td><td>Optional explanation</td></tr>
    <tr><td>Status</td><td>Choice</td><td>Pending / Approved / Rejected</td></tr>
    <tr><td>Manager</td><td>Person</td><td>Request reviewer</td></tr>
    <tr><td>Attachment</td><td>File</td><td>Proof (e.g. sick note)</td></tr>
    <tr><td>RequestDate</td><td>Date</td><td>Auto-generated timestamp</td></tr>
  </tbody>
</table>

</details>

---

<details>
<summary><strong>🧮 LeaveBalance</strong> – Tracks individual leave balances</summary>

<table>
  <thead>
    <tr>
      <th>Field</th><th>Type</th><th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Employee</td><td>Person</td><td>Person linked to the row</td></tr>
    <tr><td>AnnualLeave</td><td>Number</td><td>Available days</td></tr>
    <tr><td>SickLeave</td><td>Number</td><td>Available days</td></tr>
    <tr><td>StudyLeave</td><td>Number</td><td>Available days</td></tr>
    <tr><td>FamilyResponsibility</td><td>Number</td><td>Available days</td></tr>
    <tr><td>MaternityLeave</td><td>Number</td><td>Available days</td></tr>
    <tr><td>UnpaidLeave</td><td>Number</td><td>Tracks unpaid requests</td></tr>
    <tr><td>LastUpdated</td><td>Date</td><td>For auditing changes</td></tr>
  </tbody>
</table>

</details>

---

<details>
<summary><strong>📆 PublicHolidays</strong> – Prevents leave on non-working days</summary>

<table>
  <thead>
    <tr>
      <th>Field</th><th>Type</th><th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Title</td><td>Text</td><td>Holiday name</td></tr>
    <tr><td>Date</td><td>Date</td><td>Non-working day</td></tr>
    <tr><td>Notes</td><td>Text</td><td>Optional info</td></tr>
  </tbody>
</table>
</details>

---

<details>
<summary><strong>🔐 UserRoles</strong> – Controls access and visibility</summary>

<table>
  <thead>
    <tr>
      <th>Field</th><th>Type</th><th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Title</td><td>Text</td><td>Role name (Manager, HR, etc.)</td></tr>
    <tr><td>User</td><td>Person</td><td>Assigned staff member</td></tr>
    <tr><td>Department</td><td>Text</td><td>Optional grouping field</td></tr>
  </tbody>
</table>

</details>

---

> 💡 These lists are modular and portable for reuse in other Microsoft 365 environments.
