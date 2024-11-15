<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>C.E.M.S.S HOUSE POINTS 2024-2025</title>
  <style>
    /* General Styling */
    body {
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      text-align: center;
    }

    .container {
      max-width: 1200px; /* Larger container width */
      font-size: 1.2rem; /* Larger font for better readability */
      padding: 20px;
    }

    /* Title Styling */
    h2 {
      font-weight: bold;
      text-transform: uppercase;
      margin-bottom: 20px;
    }

    /* Table Styling */
    .table {
      width: 100%;
      border: 1px solid #000; /* Thin black border around the entire table */
      border-collapse: collapse; /* Ensures cells share borders */
    }

    .table th, .table td {
      padding: 10px; /* Padding inside the cells */
      text-align: center; /* Center-aligned text */
      border: 1px solid #000; /* Thin border between all cells */
    }

    /* Background Colors for Teams */
    .bg-green {
      background-color: #28a745; /* Green */
      color: black;
      font-weight: bold;
      text-transform: uppercase;
    }

    .bg-red {
      background-color: #dc3545; /* Red */
      color: black;
      font-weight: bold;
      text-transform: uppercase;
    }

    .bg-blue {
      background-color: #007bff; /* Blue */
      color: black;
      font-weight: bold;
      text-transform: uppercase;
    }

    /* Background Color for Non-Team Cells */
    .bg-light-brown {
      background-color: #d2b48c;
      color: black;
    }

    /* Bold and larger font for Total Heats */
    .table tr:last-child td {
      font-weight: bold;
      font-size: 1.5rem; 
    }

    /* Responsive Adjustments */
    @media (max-width: 768px) {
      h2 {
        font-size: 1.5rem;
      }

      .table-responsive {
        font-size: 0.9rem;
      }
    }
  </style>
</head>
<body>
  <div class="container mt-5">
    <div class="row justify-content-center">
      <div class="col-md-8 text-center">
        <h2 class="fw-bold">C.E.M.S.S HOUSE POINTS 2024-2025</h2>
      </div>
    </div>

    <!-- Dropdown to Select Class -->
    <div class="row justify-content-center mb-4">
      <div class="col-md-8">
        <form class="row g-3">
          <div class="col-md-6">
            <label for="selectClass" class="form-label">Select Class</label>
            <select id="selectClass" class="form-select" onchange="filterTable()">
              <option value="all">All Classes</option>
              <option value="class3">UNDER14 (CLASS 3)</option>
              <option value="class2">UNDER16 (CLASS 2)</option>
              <option value="class1">16 PLUS (CLASS 1)</option>
            </select>
          </div>
        </form>
      </div>
    </div>

    <!-- Points Table Section -->
    <div class="table-responsive">
      <table class="table">
        <thead class="table-dark">
          <tr>
            <th scope="col">CLASS</th>
            <th scope="col" class="bg-green">GREEN</th>
            <th scope="col" class="bg-red">RED</th>
            <th scope="col" class="bg-blue">BLUE</th>
            <th scope="col">EVENTS</th>
          </tr>
        </thead>
        <tbody>
          <tr class="class3">
            <td class="bg-light-brown">UNDER14 (CLASS 3)</td>
            <td class="bg-green">76</td>
            <td class="bg-red">82</td>
            <td class="bg-blue">84</td>
            <td class="bg-light-brown">Shot Put and H.J.</td>
          </tr>
          <tr class="class2">
            <td class="bg-light-brown">UNDER16 (CLASS 2)</td>
            <td class="bg-green">112</td>
            <td class="bg-red">129</td>
            <td class="bg-blue">107</td>
            <td class="bg-light-brown">Shot Put and H.J.</td>
          </tr>
          <tr class="class1">
            <td class="bg-light-brown">16 PLUS (CLASS 1)</td>
            <td class="bg-green">124</td>
            <td class="bg-red">87</td>
            <td class="bg-blue">111</td>
            <td class="bg-light-brown">Shot Put and H.J.</td>
          </tr>
          <!-- Total Heats Row -->
          <tr>
            <td class="bg-light-brown fw-bold">TOTAL HEATS</td>
            <td class="bg-green fw-bold">312</td>
            <td class="bg-red fw-bold">298</td>
            <td class="bg-blue fw-bold">302</td>
            <td class="bg-light-brown fw-bold">Date: Thurs 31-Oct-2024</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  <script>
    // Function to filter the table based on selected class
    function filterTable() {
      const selectedClass = document.getElementById("selectClass").value;
      const rows = document.querySelectorAll("tbody tr");

      rows.forEach((row, index) => {
        if (index === rows.length - 1) {
          // Always show the "Total Heats" row
          row.style.display = "";
        } else {
          if (selectedClass === "all") {
            row.style.display = "";
          } else {
            row.style.display = row.classList.contains(selectedClass) ? "" : "none";
          }
        }
      });
    }
  </script>
</body>
</html>
