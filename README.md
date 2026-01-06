<!DOCTYPE html>
<html>
<head>
  <title>Holiday Calendar 2026</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f9f9f9;
      color: #333;
      padding: 20px;
    }

    h1 {
      color: #004578;
      text-align: center;
      margin-bottom: 20px;
    }

    label {
      font-weight: bold;
      margin-right: 10px;
    }

    select {
      padding: 6px 12px;
      font-size: 14px;
      border-radius: 4px;
      border: 1px solid #ccc;
      margin-bottom: 20px;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      background-color: #ffffff;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    th, td {
      border: 1px solid #ddd;
      padding: 10px 15px;
      text-align: left;
    }

    th {
      background-color: #004578;
      color: white;
    }

    tr:nth-child(even) {
      background-color: #f2f9ff;
    }

    tr:hover {
      background-color: #dceeff;
    }
  </style>
</head>
<body>

<h1>Holiday Calendar 2026</h1>

<label for="countryFilter">Select Country:</label>
<select id="countryFilter">
  <option value="All">All</option>
  <option value="United States">United States</option>
  <option value="United Kingdom">United Kingdom</option>
  <option value="India">India</option>
  <option value="Global">Global</option>
</select>

<table id="holidayTable">
  <thead>
    <tr><th>Holiday</th><th>Date</th><th>Country</th></tr>
  </thead>
  <tbody>
    <!-- United States -->
    <tr><td>New Year’s Day</td><td>01-Jan-2026</td><td>United States</td></tr>
    <tr><td>Independence Day</td><td>04-Jul-2026</td><td>United States</td></tr>
    <tr><td>Labor Day</td><td>07-Sep-2026</td><td>United States</td></tr>
    <tr><td>Thanksgiving</td><td>26-Nov-2026</td><td>United States</td></tr>
    <tr><td>Christmas Day</td><td>25-Dec-2026</td><td>United States</td></tr>

    <!-- United Kingdom -->
    <tr><td>New Year’s Day</td><td>01-Jan-2026</td><td>United Kingdom</td></tr>
    <tr><td>Good Friday</td><td>03-Apr-2026</td><td>United Kingdom</td></tr>
    <tr><td>Summer Bank Holiday</td><td>31-Aug-2026</td><td>United Kingdom</td></tr>
    <tr><td>Christmas Day</td><td>25-Dec-2026</td><td>United Kingdom</td></tr>

    <!-- India -->
    <tr><td>Republic Day</td><td>26-Jan-2026</td><td>India</td></tr>
    <tr><td>Independence Day</td><td>15-Aug-2026</td><td>India</td></tr>
    <tr><td>Diwali</td><td>08-Nov-2026</td><td>India</td></tr>
    <tr><td>Christmas Day</td><td>25-Dec-2026</td><td>India</td></tr>

    <!-- Global -->
    <tr><td>New Year’s Day</td><td>01-Jan-2026</td><td>Global</td></tr>
    <tr><td>International Workers’ Day</td><td>01-May-2026</td><td>Global</td></tr>
    <tr><td>Christmas Day</td><td>25-Dec-2026</td><td>Global</td></tr>
  </tbody>
</table>

<script>
  const dropdown = document.getElementById("countryFilter");
  const table = document.getElementById("holidayTable").getElementsByTagName('tbody')[0];

  dropdown.addEventListener("change", function() {
    const selected = this.value;
    for (let i = 0; i < table.rows.length; i++) {
      const row = table.rows[i];
      const country = row.cells[2].innerText;
      if (selected === "All" || country === selected) {
        row.style.display = "";
      } else {
        row.style.display = "none";
      }
    }
  });
</script>

</body>
</html>
