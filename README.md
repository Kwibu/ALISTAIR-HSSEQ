# 🚛 Driver Safety Check-In System

This is a simple web-based form for truck drivers to check in before watching daily safety videos. Submitted data is stored in a Google Sheet via Google Apps Script.

---

## 📝 How It Works

1. **Driver opens the form webpage**
2. Enters:
   - Full Name
   - Truck Number
3. Data is submitted via a Google Apps Script and saved to the response spreadsheet.
4. After 1 second, the form **automatically redirects** to a safety video hosted on Google Drive.

---

## 💻 Technologies Used

- HTML/CSS
- Google Apps Script (for data storage)
- Google Sheets (as a backend database)
- Google Drive (for video hosting)

---

## 📂 Live Links

- ✅ [Live Google Form (alternative version)](https://forms.gle/q7ndkZejMq1AnXJC8)
- 📊 [View Attendance Sheet](https://docs.google.com/spreadsheets/d/17c0H7_7loaY0qWzBciaPpNOT6vGcJiOqqEMpFQGHw4A/edit?usp=sharing)
- 🎬 [Today’s Safety Video](https://drive.google.com/file/d/11dizfdhwsutrjiVhZbkSqJEz7q0OwscD/view)

---

## 📁 Project Files

### `index.html`
```html
<!-- Form with redirection after data submission -->
<form id="checkinForm">
  ...
</form>

<script>
  fetch('https://script.google.com/macros/s/YOUR_DEPLOYED_SCRIPT_ID/exec', { method: 'POST', body: formData });
  setTimeout(() => {
    window.location.href = "https://drive.google.com/file/d/11dizfdhwsutrjiVhZbkSqJEz7q0OwscD/view";
  }, 1000);
</script>
