<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title B>Desi बालक - T-Shirts</title B>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&family=Rajdhani:wght@700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Rajdhani', sans-serif;
      background-color: #ffdf2a;
    }
    header {
      background-color: #ffffff;
      color: #080806;
      text-align: center;
      padding: 20px 0;
      font-family: 'Orbitron', sans-serif;
      font-size: 4rem;
      letter-spacing: 2px;
    }
    .balak {
      color: #2a13fa;
      font-family: 'Rajdhani', sans-serif;
    }
    .hero {
      background-image: url("https://www.ultraupdates.com/2014/08/t-shirt-mockup-psd-templates/");
      background-size: cover;
      background-position: center;
      color: white;
      height: 60vh;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      text-shadow: 2px 2px 5px #000;
    }
    .hero h1 {
      font-size: 3rem;
      
    }
    .hero p {
      font-size: 1.2rem;
      margin: 10px 0;
    }
    .btn {
      background-color: #1E90FF;
      color: rgb(16, 16, 16);
      padding: 12px 24px;
      border: none;
      border-radius: 25px;
      cursor: pointer;
      font-size: 1rem;
      margin-top: 10px;
      transition: background 0.3s ease;
    }
    .btn:hover {
      background-color: #156ec4;
    }
    .products {
      padding: 40px 20px;
      text-align: center;
    }
    .products h2 {
      font-size: 2rem;
      margin-bottom: 20px;
    }
    .product-grid {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 20px;
    }
    .card {
      background: rgb(255, 255, 255);
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      width: 250px;
      overflow: hidden;
    }
    .card img {
      width: 100%;
      height: 300px;
      object-fit: cover;
    }
    .card .info {
      padding: 15px;
    }
    .info h3 {
      margin: 0;
      font-size: 1.2rem;
    }
    .info p {
      color: #0c0b0b;
      margin: 8px 0;
    }

    /* Cart Section */
    #cartSection {
      display: none;
      padding: 30px;
      text-align: center;
    }
    #cartItems {
      margin: 20px auto;
      max-width: 600px;
      text-align: left;
      background: #ffffff;
      padding: 20px;
      border-radius: 10px;
    }
    .cart-item {
      display: flex;
      justify-content: space-between;
      border-bottom: 1px solid #e8de2d;
      padding: 10px 0;
    }

    .footer {
      background-color: #ffffff;
      color: rgb(249, 246, 246);
      text-align: center;
      padding: 20px;
      margin-top: 40px;
    }
  </style>
</head>
<body>

  <header><b>
    Desi <span class="balak">बालक</span>
    </b>
  </header>

  <section class="hero">
    <h1>Wear Your Desi Swag</h1>
    <p>Bold. Blue. भारतीय.</p>
    <button class="btn" onclick="viewCart()">🛒 View Cart</button>
  </section>

  <section class="products">
    <h2>Featured T-Shirts</h2>
    <div class="product-grid">
      <div class="card">
        <img src="papa.jpg" />
        <div class="info">
          <h3>adult round necK</h3>
          <p>₹599</p>
          <button class="btn" onclick="addToCart('Desi Vibes Tee', 499)">Buy Now</button>
        </div>
      </div>
      <div class="card">
        <img src="small-tshirt-flatlay-mockup-00157 (1).jpg" alt="T-shirt 2" />
        <div class="info">
          <h3>kids round neck</h3>
          <p>₹499</p>
          <button class="btn" onclick="addToCart('बालक Bold Tee', 599)">Buy Now</button>
        </div>
      </div>
      <div class="card">
        <img src="FUN TIME (11).png" "/>
        <div class="info">
          <h3>ADULT POLO </h3>
          <p>₹699</p>
          <button class="btn" onclick="addToCart('Urban Hindi Drop', 699)">Buy Now</button>
        </div>
      </div>
    </div>
  </section>

  <!-- Cart Section -->
  <section id="cartSection">
    <h2>Your Cart</h2>
    <div id="cartItems"></div>
    <p><strong>Total: ₹<span id="totalAmount">0</span></strong></p>
    <button class="btn" onclick="checkout()">Proceed to Checkout</button>
  </section>

  <div class="footer">
    &copy; 2025 Desi बालक. All rights reserved.
  </div>

  <script>
    let cart = [];

    function addToCart(name, price) {
      cart.push({ name, price });
      alert(`${name} added to cart!`);
    }

    function viewCart() {
      document.getElementById("cartSection").style.display = "block";
      const cartItemsDiv = document.getElementById("cartItems");
      const totalAmountSpan = document.getElementById("totalAmount");

      cartItemsDiv.innerHTML = "";
      let total = 0;

      cart.forEach((item, index) => {
        total += item.price;
        cartItemsDiv.innerHTML += `
          <div class="cart-item">
            <span>${item.name}</span>
            <span>₹${item.price}</span>
          </div>
        `;
      });

      totalAmountSpan.innerText = total;
    }

    function checkout() {
      if (cart.length === 0) {
        alert("Your cart is empty!");
        return;
      }
      alert("Thank you for shopping with Desi बालक! (This is a test checkout)");
      cart = [];
      document.getElementById("cartSection").style.display = "none";
    }
  </script>

</body>
</html>
<h1>contact us on  9891457097</h1>

