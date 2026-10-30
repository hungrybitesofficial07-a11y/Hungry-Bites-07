# Hungry-Bites-07
Restaurant 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hungry Bites | Good Food. Great Vibes.</title>
  <style>
    :root {
      --primary-red: #E50914;
      --accent-orange: #FF6B00;
      --dark-navy: #0F172A;
      --bg-warm: #FAF8F5;
      --card-bg: #FFFFFF;
      --text-main: #1E293B;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background-color: var(--bg-warm);
      color: var(--text-main);
      padding-bottom: 110px;
    }

    /* Header */
    header {
      background-color: var(--card-bg);
      text-align: center;
      padding: 20px 16px;
      border-bottom: 3px solid var(--accent-orange);
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
    }

    .brand-title {
      font-size: 2.2rem;
      font-weight: 900;
      color: var(--dark-navy);
      letter-spacing: -0.5px;
    }

    .brand-title span {
      color: var(--primary-red);
    }

    .tagline {
      font-size: 0.85rem;
      color: var(--accent-orange);
      font-weight: 700;
      margin-top: 4px;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    /* Container */
    .container {
      max-width: 600px;
      margin: 0 auto;
      padding: 16px;
    }

    /* Payment Banner */
    .payment-info {
      background: #EFF6FF;
      border: 1px dashed var(--accent-orange);
      border-radius: 12px;
      padding: 14px;
      margin-bottom: 20px;
      text-align: center;
    }

    .payment-info h4 {
      font-size: 0.95rem;
      color: var(--dark-navy);
      margin-bottom: 6px;
    }

    .upi-id {
      font-size: 1rem;
      font-weight: 800;
      color: var(--primary-red);
      background: #FFFFFF;
      padding: 6px 14px;
      border-radius: 8px;
      display: inline-block;
      box-shadow: 0 2px 6px rgba(0,0,0,0.05);
    }

    .section-title {
      font-size: 1.25rem;
      color: var(--dark-navy);
      margin: 24px 0 12px;
      border-left: 4px solid var(--primary-red);
      padding-left: 10px;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    .sub-section-title {
      font-size: 1.05rem;
      color: var(--accent-orange);
      margin: 16px 0 8px;
      font-weight: 700;
    }

    /* Food Item Card */
    .menu-card {
      background: var(--card-bg);
      border-radius: 12px;
      padding: 10px 12px;
      margin-bottom: 10px;
      display: flex;
      align-items: center;
      gap: 12px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.04);
    }

    .item-img {
      width: 75px;
      height: 75px;
      border-radius: 10px;
      object-fit: cover;
      background-color: #E2E8F0;
      flex-shrink: 0;
    }

    .item-details {
      flex: 1;
    }

    .item-details h4 {
      font-size: 0.95rem;
      color: var(--dark-navy);
      font-weight: 700;
    }

    .item-details p {
      font-size: 0.8rem;
      color: #64748B;
      margin-top: 2px;
    }

    .price {
      font-weight: 800;
      color: var(--primary-red);
      margin-top: 4px;
      font-size: 0.95rem;
    }

    .add-btn {
      background-color: var(--accent-orange);
      color: white;
      border: none;
      padding: 8px 14px;
      border-radius: 20px;
      font-weight: 700;
      cursor: pointer;
      white-space: nowrap;
      transition: background 0.2s;
    }

    .add-btn:active {
      transform: scale(0.95);
      background-color: var(--primary-red);
    }

    /* Fixed Floating Cart Bar */
    .cart-bar {
      position: fixed;
      bottom: 0;
      left: 0;
      right: 0;
      background: var(--dark-navy);
      color: white;
      padding: 14px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 -4px 16px rgba(0,0,0,0.2);
      max-width: 600px;
      margin: 0 auto;
      z-index: 1000;
      border-top-left-radius: 16px;
      border-top-right-radius: 16px;
    }

    .checkout-btn {
      background-color: #25D366;
      color: white;
      border: none;
      padding: 10px 18px;
      border-radius: 25px;
      font-weight: 700;
      font-size: 0.9rem;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .total-price {
      font-size: 1.15rem;
      font-weight: 800;
      color: #FFFFFF;
    }
  </style>
</head>
<body>

  <header>
    <div class="brand-title">Hungry <span>Bites</span></div>
    <div class="tagline">Good Food. Great Vibes.</div>
  </header>

  <div class="container">
    
    <!-- UPI Payment Info Box -->
    <div class="payment-info">
      <h4>💳 Accept Payments via GPay / PhonePe / Paytm / UPI</h4>
      <div class="upi-id">UPI ID: 6300103574@paytm</div>
    </div>

    <!-- 1. HEALTHY MORNING MENU -->
    <h3 class="section-title">Healthy Morning Menu</h3>
    
    <div class="menu-card">
      <img src="22408.png" alt="Green Tea" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Green Tea</h4>
        <p>1 Cup</p>
        <div class="price">₹35</div>
      </div>
      <button class="add-btn" onclick="addToCart('Green Tea', 35)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22409.jpg" alt="Flavoured Liquor Tea" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Flavoured Liquor Tea</h4>
        <p>1 Cup</p>
        <div class="price">₹25</div>
      </div>
      <button class="add-btn" onclick="addToCart('Flavoured Liquor Tea', 25)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22409.jpg" alt="Milk Tea" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Milk Tea</h4>
        <p>1 Cup</p>
        <div class="price">₹20</div>
      </div>
      <button class="add-btn" onclick="addToCart('Milk Tea', 20)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22410.jpg" alt="Black Coffee" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Black Coffee</h4>
        <p>1 Cup</p>
        <div class="price">₹20</div>
      </div>
      <button class="add-btn" onclick="addToCart('Black Coffee', 20)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22411.jpg" alt="Black Coffee Shots" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Black Coffee Shots</h4>
        <p>1 Cup</p>
        <div class="price">₹35</div>
      </div>
      <button class="add-btn" onclick="addToCart('Black Coffee Shots', 35)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22426.jpg" alt="Milk Coffee" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Milk Coffee</h4>
        <p>1 Cup</p>
        <div class="price">₹25</div>
      </div>
      <button class="add-btn" onclick="addToCart('Milk Coffee', 25)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22414.jpg" alt="Cheese Sandwich" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Cheese Sandwich</h4>
        <p>1 Plate</p>
        <div class="price">₹35</div>
      </div>
      <button class="add-btn" onclick="addToCart('Cheese Sandwich', 35)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22416.jpg" alt="Egg Sandwich" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Egg Sandwich</h4>
        <p>1 Plate</p>
        <div class="price">₹35</div>
      </div>
      <button class="add-btn" onclick="addToCart('Egg Sandwich', 35)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22418.jpg" alt="Egg Cheese Sandwich" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Egg Cheese Sandwich</h4>
        <p>1 Plate</p>
        <div class="price">₹45</div>
      </div>
      <button class="add-btn" onclick="addToCart('Egg Cheese Sandwich', 45)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22420.jpg" alt="Egg Toast" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Egg Toast</h4>
        <p>1 Plate</p>
        <div class="price">₹35</div>
      </div>
      <button class="add-btn" onclick="addToCart('Egg Toast', 35)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22421.jpg" alt="Boiled Egg" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Boiled Egg</h4>
        <p>1 Piece</p>
        <div class="price">₹15</div>
      </div>
      <button class="add-btn" onclick="addToCart('Boiled Egg', 15)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22423.jpg" alt="Parathas with Curry" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Parathas with Curry</h4>
        <p>1 Plate</p>
        <div class="price">₹35</div>
      </div>
      <button class="add-btn" onclick="addToCart('Parathas with Curry', 35)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22424.jpg" alt="Egg Curry" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Egg Curry</h4>
        <p>1 Plate</p>
        <div class="price">₹25</div>
      </div>
      <button class="add-btn" onclick="addToCart('Egg Curry', 25)">+ Add</button>
    </div>

    <!-- 2. EVENING DELIGHTS -->
    <h3 class="section-title">Evening Delights</h3>
    
    <div class="sub-section-title">Veg - Tasty Veggies</div>
    
    <div class="menu-card">
      <img src="22495.jpg" alt="French Fries" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>French Fries</h4>
        <p>1 Plate</p>
        <div class="price">₹55</div>
      </div>
      <button class="add-btn" onclick="addToCart('French Fries', 55)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22496.jpg" alt="Paneer Pakoda" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Paneer Pakoda</h4>
        <p>1 Plate</p>
        <div class="price">₹65</div>
      </div>
      <button class="add-btn" onclick="addToCart('Paneer Pakoda', 65)">+ Add</button>
    </div>

    <div class="sub-section-title">Firey Non-Vegs</div>

    <div class="menu-card">
      <img src="22497.jpg" alt="Tandoori Chicken Pakoda" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Tandoori Chicken Pakoda</h4>
        <p>1 Plate</p>
        <div class="price">₹65</div>
      </div>
      <button class="add-btn" onclick="addToCart('Tandoori Chicken Pakoda', 65)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22500.jpg" alt="Lemon Chicken Pakoda" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Lemon Chicken Pakoda</h4>
        <p>1 Plate</p>
        <div class="price">₹65</div>
      </div>
      <button class="add-btn" onclick="addToCart('Lemon Chicken Pakoda', 65)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22506.jpg" alt="The Royal Crunch Legs" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>The Royal Crunch Legs</h4>
        <p>1 Plate (4 Pcs)</p>
        <div class="price">₹225</div>
      </div>
      <button class="add-btn" onclick="addToCart('The Royal Crunch Legs', 225)">+ Add</button>
    </div>

    <div class="sub-section-title">The Junglee Jumbos</div>

    <div class="menu-card">
      <img src="22507.jpg" alt="Paneer Jumbo Roll" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Paneer Jumbo Roll</h4>
        <p>1 Roll</p>
        <div class="price">₹75</div>
      </div>
      <button class="add-btn" onclick="addToCart('Paneer Jumbo Roll', 75)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22508.jpg" alt="Paneer Cheesy Jumbo Roll" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Paneer Cheesy Jumbo Roll</h4>
        <p>1 Roll</p>
        <div class="price">₹95</div>
      </div>
      <button class="add-btn" onclick="addToCart('Paneer Cheesy Jumbo Roll', 95)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22509.jpg" alt="Jumbo Double-Egg Roll" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Jumbo Double-Egg Roll</h4>
        <p>1 Roll</p>
        <div class="price">₹65</div>
      </div>
      <button class="add-btn" onclick="addToCart('Jumbo Double-Egg Roll', 65)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22512.webp" alt="Jumbo Chicken Roll" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Jumbo Chicken Roll</h4>
        <p>1 Roll</p>
        <div class="price">₹85</div>
      </div>
      <button class="add-btn" onclick="addToCart('Jumbo Chicken Roll', 85)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22513.webp" alt="Jumbo Egg Chicken Roll" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Jumbo Egg Chicken Roll</h4>
        <p>1 Roll</p>
        <div class="price">₹115</div>
      </div>
      <button class="add-btn" onclick="addToCart('Jumbo Egg Chicken Roll', 115)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22514.jpg" alt="Jumbo Chicken Cheesy Roll" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Jumbo Chicken Cheesy Roll</h4>
        <p>1 Roll</p>
        <div class="price">₹99</div>
      </div>
      <button class="add-btn" onclick="addToCart('Jumbo Chicken Cheesy Roll', 99)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22515.jpg" alt="Jumbo Egg Chicken Cheesy Roll" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Jumbo Egg Chicken Cheesy Roll</h4>
        <p>1 Roll</p>
        <div class="price">₹129</div>
      </div>
      <button class="add-btn" onclick="addToCart('Jumbo Egg Chicken Cheesy Roll', 129)">+ Add</button>
    </div>

    <!-- 3. KITCHEN'S SPECIAL -->
    <h3 class="section-title">Kitchen's Special</h3>

    <div class="sub-section-title">Sher Shawarmas</div>

    <div class="menu-card">
      <img src="22517.jpg" alt="Special Chicken Shawarma" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Special Chicken Shawarma</h4>
        <p>1 Piece</p>
        <div class="price">₹135</div>
      </div>
      <button class="add-btn" onclick="addToCart('Special Chicken Shawarma', 135)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22519.jpg" alt="Special Cheesy Chicken Shawarma" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Special Cheesy Chicken Shawarma</h4>
        <p>1 Piece</p>
        <div class="price">₹155</div>
      </div>
      <button class="add-btn" onclick="addToCart('Special Cheesy Chicken Shawarma', 155)">+ Add</button>
    </div>

    <div class="sub-section-title">Killer Kebabs</div>

    <div class="menu-card">
      <img src="22520.jpg" alt="Chicken Malai Kabab" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Chicken Malai Kabab</h4>
        <p>8 Pieces</p>
        <div class="price">₹199</div>
      </div>
      <button class="add-btn" onclick="addToCart('Chicken Malai Kabab', 199)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22521.jpg" alt="Chicken Hariyali Kabab" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Chicken Hariyali Kabab</h4>
        <p>8 Pieces</p>
        <div class="price">₹185</div>
      </div>
      <button class="add-btn" onclick="addToCart('Chicken Hariyali Kabab', 185)">+ Add</button>
    </div>

    <div class="menu-card">
      <img src="22522.jpg" alt="Chicken Aachari Kabab" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Chicken Aachari Kabab</h4>
        <p>8 Pieces</p>
        <div class="price">₹185</div>
      </div>
      <button class="add-btn" onclick="addToCart('Chicken Aachari Kabab', 185)">+ Add</button>
    </div>

    <div class="sub-section-title">Winter Warmth</div>

    <div class="menu-card">
      <img src="22523.jpg" alt="Hot Chocolate" class="item-img" onerror="this.src='https://via.placeholder.com/75?text=Food'">
      <div class="item-details">
        <h4>Hot Chocolate</h4>
        <p>1 Glass</p>
        <div class="price">₹125</div>
      </div>
      <button class="add-btn" onclick="addToCart('Hot Chocolate', 125)">+ Add</button>
    </div>

  </div>

  <!-- Floating Cart Bar -->
  <div class="cart-bar">
    <div>
      <span style="font-size: 0.8rem; color: #94A3B8;">Total:</span>
      <div class="total-price" id="total-amount">₹0</div>
    </div>
    <button class="checkout-btn" onclick="sendWhatsAppOrder()">
      💬 Order & Pay via UPI
    </button>
  </div>

  <script>
    const PHONE_NUMBER = "916300103574"; 
    const UPI_ID = "6300103574@paytm";

    let cart = [];
    let total = 0;

    function addToCart(name, price) {
      cart.push({ name, price });
      total += price;
      document.getElementById('total-amount').innerText = `₹${total}`;
    }

    function sendWhatsAppOrder() {
      if (cart.length === 0) {
        alert("Please add at least one item to your cart before ordering!");
        return;
      }

      let message = "Hello Hungry Bites! 👋\nI would like to place an order:\n\n";
      cart.forEach((item, index) => {
        message += `${index + 1}. ${item.name} - ₹${item.price}\n`;
      });
      message += `\n*Total Amount: ₹${total}*`;
      message += `\n\n💳 *Payment via UPI:* ${UPI_ID}`;
      message += `\n(I will send the payment screenshot here after paying).`;

      const encodedMessage = encodeURIComponent(message);
      window.open(`https://wa.me/${PHONE_NUMBER}?text=${encodedMessage}`, '_blank');
    }
  </script>

</body>
</html>
