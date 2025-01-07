<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MATIN Topup</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #6A1B9A;
      color: white;
    }
    .main-container {
      max-width: 1200px;
      margin: auto;
      padding: 20px;
    }
    .header, .footer {
      text-align: center;
      background-color: #7B1FA2;
      padding: 20px;
      border-radius: 10px;
      margin-bottom: 20px;
    }
    .input-section {
      text-align: center;
      margin-bottom: 20px;
    }
    .input-section input {
      padding: 10px;
      margin: 10px;
      width: 200px;
      border: none;
      border-radius: 5px;
    }
    .input-section button {
      padding: 10px 20px;
      background-color: #007BFF;
      border: none;
      border-radius: 5px;
      color: white;
      font-size: 16px;
      cursor: pointer;
    }
    .input-section button:hover {
      background-color: #0056b3;
    }
    .pricing-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 15px;
    }
    .pricing-card {
      background-color: #7B1FA2;
      padding: 15px;
      border-radius: 10px;
      text-align: center;
      cursor: pointer;
      transition: transform 0.2s;
    }
    .pricing-card:hover {
      transform: scale(1.05);
      background-color: #8E24AA;
    }
    .pricing-card p {
      margin: 0;
    }
    .button-section {
      text-align: center;
      margin-top: 20px;
    }
    .button-section button {
      padding: 10px 20px;
      background-color: #007BFF;
      border: none;
      border-radius: 5px;
      color: white;
      font-size: 16px;
      cursor: not-allowed; /* Default: Disabled */
      margin: 10px;
    }
    .button-section button.enabled {
      cursor: pointer;
      background-color: #0056b3; /* Active style */
    }
    .button-section button:hover.enabled {
      background-color: #003a75;
    }
    .total-display {
      text-align: center;
      margin-top: 30px;
    }
  </style>
</head>
<body>
  <div class="main-container">
    <!-- Header Section -->
    <div class="header">
      <h1>MATIN</h1>
      <p>បញ្ចូលពេជ្រ Mobile Legends: Bang Bang</p>
      <p>ធានាសុវត្តិភាព100%</p>
      លឿនរហ័សទាន់ចិត្ត
    </div>

    <!-- Input Section -->
    <div class="input-section">
      <input type="text" id="gameId" placeholder="Use ID">
      <input type="text" id="serverId" placeholder="Server ID">
      <button onclick="checkId()">Check</button>
    </div>

    <!-- Pricing Section -->
    <div>
      <h3>Choose Your Package</h3>
      <div class="pricing-grid">
        <div class="pricing-card" onclick="selectPackage(1.35)">
          💎
          <p>$1.35</p>
          <p>Weekly Pass</p>
        </div>
        <div class="pricing-card" onclick="selectPackage(2.70)">
          💎
          <p>$2.70</p>
          <p>Weekly Pass</p>
          ×2
        </div>
        <div class="pricing-card" onclick="selectPackage(4.05)">
          💎
          <p>$4.05</p>
          <p>Weekly Pass</p>
          ×3
        </div>
        <div class="pricing-card" onclick="selectPackage(5.40)">
          💎
          <p>$5.40</p>
          <p>Weekly Pass</p>
          ×4
        </div>
        <div class="pricing-card" onclick="selectPackage(6.75)">
          💎
          <p>$6.75</p>
          <p>Weekly Pass</p>
          ×5
          </div>
        <div class="pricing-card" onclick="selectPackage(0.97)">
          💎
          <p>$0.97</p>
          <p>56 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(1.25)">
          💎
          <p>$1.25</p>
          <p>86 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(2.45)">
          💎
          <p>$2.45</p>
          <p>172 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(3.55)">
          💎
          <p>3.55</p>
          <p>257 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(4.55)">
          💎
          <p>$4.55</p>
          <p>343 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(5.75)">
          💎
          <p>$5.75</p>
          <p>429 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(7.00)">
          💎
          <p>$7.00</p>
          <p>514 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(8.50)">
          💎
          <p>6.75</p>
          <p>Weekly Pass</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(8.00)">
          💎
          <p>$8.00</p>
          <p>600 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(9.00)">
          💎
          <p>$9.00</p>
          <p>706 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(12.00)">
          💎
          <p>$12.00</p>
          <p>878 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(13.00)">
          💎
          <p>$13.00</p>
          <p>963 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(14.00)">
          💎
          <p>$14.00</p>
          <p>1049 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(16.00)">
          💎
          <p>$16.00</p>
          <p>1135 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(17.50)">
          💎
          <p>$17.50</p>
          <p>1220 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(19.50)">
          💎
          <p>$19.50</p>
          <p>1412 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(22.00)">
          💎
          <p>$22.00</p>
          <p>1584 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(24.00)">
          💎
          <p>$24.00</p>
          <p>1755 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(30.00)">
          💎
          <p>$30.00</p>
          <p>2195 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(35.00)">
          💎
          <p>$35.00</p>
          <p>2538 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(40.00)">
          💎
          <p>$40.00</p>
          <p>2901 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(50.00)">
          💎
          <p>$50.00</p>
          <p>3688 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(59.00)">
          💎
          <p>$59.00</p>
          <p>6238 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(75.00)">
          💎
          <p>$75.00</p>
          <p>5532 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(85.00)">
          💎
          <p>$85.00</p>
          <p>6238 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(95.00)">
          💎
          <p>$95.00</p>
          <p>6944 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(105.00)">
          💎
          <p>$105.00</p>
          <p>11484 Daimond</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(8.50)">
          💎
          <p>$8.50</p>
          <p>Twillight Pass</p>
          </div>
        <div class="pricing-card" onclick="selectPackage(0.90)">
          💎
          <p>$0.90</p>
          <p>Super valur</p>
          <p>pass</p>
          ដាក់បានតែម្ដងទេ
          </div>
        <div class="pricing-card" onclick="selectPackage(1.00)">
          💎
          <p>$1.00</p>
          <p>50💎Free50💎</p>
          ដាក់បានតែម្ដងទេ
          </div>
        <div class="pricing-card" onclick="selectPackage(2.50)">
          💎
          <p>$2.50</p>
          <p>150💎Free150💎</p>
           ដាក់បានតែម្ដងទេ
          </div>
        <div class="pricing-card" onclick="selectPackage(4.00)">
          💎
          <p>$4.00</p>
          <p>250💎Free250💎</p>
           ដាក់បានតែម្ដងទេ
          </div>
        <div class="pricing-card" onclick="selectPackage(7.00)">
          💎
          <p>$7.00</p>
          <p>500💎Free500💎</p>
          ដាក់បានតែម្ដងទេ
        </div>
      </div>
    </div>

    <!-- Total Display -->
    <div class="total-display">
      <h3>Total: $<span id="total">0.00</span></h3>
    </div>

    <!-- Payment Section -->
    <div class="button-section">
      <button id="khqrButton" onclick="payWithKHQR()" disabled>Pay with KHQR</button>
      <button id="abaButton" onclick="payWithABAPay()" disabled>Pay with ABA Pay</button>
    </div>

    <!-- Footer Section -->
    <div class="footer">
      <p>© Matin Topup, 2025. All rights reserved.</p>
    </div>
  </div>

  <script>
    let isChecked = false;

    // Validate Game ID and Server ID
    function checkId() {
      const gameId = document.getElementById('gameId').value.trim();
      const serverId = document.getElementById('serverId').value.trim();

      if (!gameId || !serverId) {
        alert('Please fill in both Game ID and Server ID!');
        isChecked = false;
      } else {
        alert(`Game ID: ${gameId}, Server ID: ${serverId} are valid.`);
        isChecked = true;
      }
    }

    // Update total price
    function selectPackage(price) {
      const totalElement = document.getElementById('total');
      totalElement.textContent = price.toFixed(2);

      // Enable payment buttons only if IDs are checked
      const khqrButton = document.getElementById('khqrButton');
      const abaButton = document.getElementById('abaButton');
      
      if (isChecked) {
        khqrButton.disabled = false;
        abaButton.disabled = false;

        khqrButton.classList.add('enabled');
        abaButton.classList.add('enabled');
      } else {
        alert('Please validate Game ID and Server ID before selecting a package!');
      }
    }

    // Redirect to KHQR payment
    function payWithKHQR() {
      const total = document.getElementById('total').textContent;
      if (parseFloat(total) === 0) {
        alert('Please select a package before proceeding to KHQR payment!');
      } else {
        alert(`Redirecting to KHQR payment for $${total}...`);
        window.location.href = `https://qrco.de/bffZUE`;
      }
    }

    // Redirect to ABA Pay
    function payWithABAPay() {
      const total = document.getElementById('total').textContent;
      if (parseFloat(total) === 0) {
        alert('Please select a package before proceeding to ABA Pay!');
      } else {
        alert(`Redirecting to ABA Pay for $${total}...`);
        window.location.href = `https://pay.ababank.com/StKtnRYkJUURcdJ2A`;
      }
    }
  </script>
</body>
</html>
