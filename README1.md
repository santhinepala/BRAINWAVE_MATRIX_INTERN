<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Fashion Shop</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #f0f2f5;
    }
    header {
      background-color: #222;
      color: white;
      padding: 1rem;
      text-align: center;
    }
    nav {
      background: #333;
      display: flex;
      justify-content: center;
      padding: 0.5rem;
    }
    nav a {
      color: #fff;
      text-decoration: none;
      margin: 0 15px;
    }
    .products {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      padding: 20px;
      justify-content: center;
    }
    .card {
      background: white;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      overflow: hidden;
      width: 200px;
      transition: transform 0.2s ease;
    }
    .card:hover {
      transform: scale(1.05);
    }
    .card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }
    .card-body {
      padding: 15px;
      text-align: center;
    }
    .card-body h4 {
      margin: 10px 0;
    }
    .card-body button {
      background-color: #007bff;
      border: none;
      color: white;
      padding: 10px 15px;
      cursor: pointer;
      border-radius: 5px;
    }
    .cart-section {
      background: #fff;
      padding: 20px;
      margin: 20px;
      border-radius: 10px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Fashion Shop</h1>
    <p>Trendy Clothes at Best Prices</p>
  </header>
  <nav>
    <a href="#">Home</a>
    <a href="#">New Arrivals</a>
    <a href="#">Cart</a>
  </nav>

  <div class="products">
    <div class="card">
      <img src="https://via.placeholder.com/200x180?text=T-Shirt" alt="T-Shirt">
      <div class="card-body">
        <h4>T-Shirt</h4>
        <p>₹499</p>
        <button onclick="addToCart('T-Shirt', 499)">Add to Cart</button>
      </div>
    </div>
    <div class="card">
      <img src="https://via.placeholder.com/200x180?text=Jeans" alt="Jeans">
      <div class="card-body">
        <h4>Jeans</h4>
        <p>₹999</p>
        <button onclick="addToCart('Jeans', 999)">Add to Cart</button>
      </div>
    </div>
    <div class="card">
      <img src="https://via.placeholder.com/200x180?text=Jacket" alt="Jacket">
      <div class="card-body">
        <h4>Jacket</h4>
        <p>₹1499</p>
        <button onclick="addToCart('Jacket', 1499)">Add to Cart</button>
      </div>
    </div>
  </div>

  <div class="cart-section">
    <h2>Shopping Cart</h2>
    <ul id="cartList"></ul>
    <h3 id="cartTotal">Total: ₹0</h3>
  </div>

  <script>
    let cart = [];

    function addToCart(item, price) {
      cart.push({ item, price });
      updateCart();
    }

    function updateCart() {
      const list = document.getElementById('cartList');
      const totalText = document.getElementById('cartTotal');
      list.innerHTML = '';
      let total = 0;

      cart.forEach(product => {
        const li = document.createElement('li');
        li.textContent = `${product.item} - ₹${product.price}`;
        list.appendChild(li);
        total += product.price;
      });

      totalText.textContent = `Total: ₹${total}`;
    }
  </script>
</body>
</html>
