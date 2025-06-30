# 👥 Roles and Permissions – HearConnect Leave Request App

This document defines the different user roles and their capabilities within the app.

---

<details>
  <summary><strong>👤 Employee</strong> – Submits leave and views balances</summary>

<table>
  <tr>
    <th>✅ Can:</th>
    <td>
      <ul>
        <li>Submit leave requests</li>
        <li>Track request status</li>
        <li>Attach sick notes or documents</li>
        <li>View their leave balances</li>
        <li>See team calendar (read-only)</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>❌ Cannot:</th>
    <td>
      <ul>
        <li>Approve or reject requests</li>
        <li>Edit other users’ submissions</li>
        <li>Change leave balances</li>
      </ul>
    </td>
  </tr>
</table>
</details>

---

<details>
  <summary><strong>👨‍💼 Manager</strong> – Reviews and approves leave requests</summary>

<table>
  <tr>
    <th>✅ Can:</th>
    <td>
      <ul>
        <li>View team requests</li>
        <li>Approve, reject, or comment on requests</li>
        <li>Receive notifications (Teams/email)</li>
        <li>Access team calendar</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>❌ Cannot:</th>
    <td>
      <ul>
        <li>Modify leave balances</li>
        <li>Change other user roles</li>
      </ul>
    </td>
  </tr>
</table>
</details>

---

<details>
  <summary><strong>🧑‍💼 HR / Admin</strong> – Maintains balance and compliance</summary>

<table>
  <tr>
    <th>✅ Can:</th>
    <td>
      <ul>
        <li>Adjust leave balances</li>
        <li>View all user requests</li>
        <li>Monitor compliance and logs</li>
        <li>Assign roles or override issues</li>
      </ul>
    </td>
  </tr>
  <tr>
    <th>❌ Cannot:</th>
    <td>
      <ul>
        <li>Submit leave for employees (unless configured)</li>
      </ul>
    </td>
  </tr>
</table>
</details>

---

<details>
  <summary><strong>🔧 System Admin</strong> – Maintains technical environment</summary>

<table>
  <tr>
    <th>✅ Can:</th>
    <td>
      <ul>
        <li>Deploy and update app versions</li>
        <li>Maintain flows, connections, permissions</li>
        <li>Support users with technical issues</li>
      </ul>
    </td>
  </tr>
</table>
</details>

---

> ℹ️ Role enforcement is implemented using:
> - SharePoint list filtering
> - Power Apps conditional logic
> - Power Automate role-based flows
