# The-Local-shop
<!DOCTYPE html>  <html lang="en">  
<head>  
  <meta charset="UTF-8" />  
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />  
  <title>The Local Shop</title>  
  <style>  
    :root {  
      --green-900: #083d1f;  
      --green-800: #0d4d2a;  
      --green-700: #12633a;  
      --green-600: #198a4c;  
      --green-500: #1fa35f;  
      --green-100: #eefaf3;  
      --orange: #ffb31a;  
      --text: #1d2b27;  
      --muted: #5f6d68;  
      --white: #ffffff;  
      --shadow: 0 10px 30px rgba(18, 44, 32, 0.1);  
      --radius: 18px;  
    }  * { box-sizing: border-box; }  

html { scroll-behavior: smooth; }  

body {  
  margin: 0;  
  font-family: Arial, Helvetica, sans-serif;  
  color: var(--text);  
  background: linear-gradient(180deg, #f7faf8 0%, #eef8f1 100%);  
}  

img { max-width: 100%; display: block; }  

a { text-decoration: none; }  

button, input, textarea {  
  font: inherit;  
}  

.container {  
  width: min(1160px, calc(100% - 32px));  
  margin: 0 auto;  
}  

header {  
  position: sticky;  
  top: 0;  
  z-index: 100;  
  background: rgba(8, 61, 31, 0.96);  
  backdrop-filter: blur(8px);  
  color: var(--white);  
  border-bottom: 1px solid rgba(255,255,255,0.08);  
}  

.nav {  
  display: flex;  
  align-items: center;  
  justify-content: space-between;  
  min-height: 76px;  
  gap: 20px;  
}  

.brand {  
  display: flex;  
  align-items: center;  
  gap: 10px;  
  font-weight: 700;  
  letter-spacing: 0.02em;  
  font-size: 1.2rem;  
}  

.brand-badge {  
  width: 38px;  
  height: 38px;  
  border-radius: 12px;  
  background: linear-gradient(135deg, #3fc77f, #0e7a3d);  
  display: grid;  
  place-items: center;  
  font-size: 1.1rem;  
}  

.nav-links {  
  display: flex;  
  align-items: center;  
  gap: 20px;  
  flex-wrap: wrap;  
}  

.nav-links a {  
  color: rgba(255,255,255,0.85);  
  font-size: 0.96rem;  
}  

.nav-btn {  
  border: none;  
  border-radius: 12px;  
  background: var(--white);  
  color: var(--green-800);  
  padding: 11px 18px;  
  font-weight: 700;  
  cursor: pointer;  
  transition: transform 0.2s ease, box-shadow 0.2s ease;  
  box-shadow: 0 10px 20px rgba(0,0,0,0.08);  
}  

.nav-btn:hover {  
  transform: translateY(-1px);  
}  

.hero {  
  position: relative;  
  background:  
    linear-gradient(95deg, rgba(7, 34, 20, 0.88), rgba(8, 61, 31, 0.6)),  
    url('https://i.ibb.co/9kFMx9gN/Screenshot-20261013-074426-Chrome.jpg') center/cover no-repeat;  
  color: var(--white);  
  min-height: 530px;  
  display: flex;  
  align-items: center;  
}  

.hero-inner {  
  display: grid;  
  grid-template-columns: 1.2fr 0.8fr;  
  gap: 40px;  
  align-items: center;  
  width: min(1160px, calc(100% - 32px));  
  margin: 0 auto;  
  padding: 60px 0;  
}  

.hero-copy {  
  max-width: 700px;  
}  

.tag {  
  display: inline-block;  
  background: rgba(255,255,255,0.12);  
  border: 1px solid rgba(255,255,255,0.2);  
  padding: 8px 14px;  
  border-radius: 999px;  
  font-size: 0.82rem;  
  font-weight: 600;  
  margin-bottom: 18px;  
}  

.hero h1 {  
  margin: 0;  
  font-size: clamp(2.2rem, 5vw, 4.3rem);  
  line-height: 1.06;  
  letter-spacing: -0.04em;  
}  

.hero p {  
  font-size: 1.08rem;  
  color: rgba(255,255,255,0.82);  
  max-width: 560px;  
  margin: 18px 0 30px;  
}  

.hero-actions {  
  display: flex;  
  gap: 16px;  
  flex-wrap: wrap;  
}  

.primary-btn, .secondary-btn, .shop-btn, .cart-action, .remove-btn {  
  border: none;  
  border-radius: 12px;  
  cursor: pointer;  
  font-weight: 700;  
  transition: transform 0.2s ease, filter 0.2s ease, box-shadow 0.2s ease;  
}  

.primary-btn, .shop-btn {  
  background: linear-gradient(135deg, var(--green-500), var(--green-700));  
  color: var(--white);  
  padding: 14px 22px;  
  box-shadow: 0 12px 26px rgba(26, 129, 78, 0.3);  
}  

.secondary-btn {  
  background: rgba(255,255,255,0.1);  
  color: var(--white);  
  border: 1px solid rgba(255,255,255,0.2);  
  padding: 14px 22px;  
}  

.primary-btn:hover, .secondary-btn:hover, .shop-btn:hover, .cart-action:hover, .remove-btn:hover {  
  transform: translateY(-1px);  
  filter: brightness(1.02);  
}  

.hero-stats {  
  display: grid;  
  grid-template-columns: repeat(3, minmax(0, 1fr));  
  gap: 16px;  
  margin-top: 28px;  
  max-width: 520px;  
}  

.stat-box {  
  background: rgba(255,255,255,0.08);  
  border: 1px solid rgba(255,255,255,0.12);  
  border-radius: 14px;  
  padding: 16px 14px;  
  text-align: center;  
}  

.stat-box strong {  
  display: block;  
  font-size: 1.6rem;  
  margin-bottom: 4px;  
}  

.stat-box span {  
  color: rgba(255,255,255,0.76);  
  font-size: 0.8rem;  
}  

.hero-card {  
  background: rgba(255,255,255,0.08);  
  border: 1px solid rgba(255,255,255,0.13);  
  border-radius: 20px;  
  padding: 20px;  
  box-shadow: var(--shadow);  
  backdrop-filter: blur(8px);  
}  

.mini-box {  
  background: rgba(255,255,255,0.08);  
  border-radius: 14px;  
  padding: 14px;  
  margin-top: 12px;  
}  

.mini-box h3 {  
  margin: 0 0 8px;  
  font-size: 1rem;  
}  

.mini-box p {  
  margin: 0;  
  font-size: 0.9rem;  
  color: rgba(255,255,255,0.74);  
}  

.promo-badge {  
  display: inline-flex;  
  align-items: center;  
  gap: 8px;  
  background: rgba(255,179,26,0.15);  
  color: #fff4d6;  
  border: 1px solid rgba(255,179,26,0.35);  
  border-radius: 999px;  
  padding: 8px 12px;  
  font-weight: 700;  
  margin-bottom: 12px;  
  font-size: 0.8rem;  
}  

main {  
  padding: 36px 0 50px;  
}  

.section-head {  
  display: flex;  
  justify-content: space-between;  
  align-items: end;  
  gap: 16px;  
  margin-bottom: 22px;  
  flex-wrap: wrap;  
}  

.section-head h2 {  
  margin: 0;  
  font-size: clamp(1.7rem, 3vw, 2.4rem);  
  letter-spacing: -0.03em;  
}  

.section-head p {  
  margin: 0;  
  color: var(--muted);  
}  

.filters {  
  display: flex;  
  gap: 10px;  
  flex-wrap: wrap;  
  margin: 18px 0 22px;  
}  

.filter-btn {  
  border: 1px solid #dcebe1;  
  background: #f4faf6;  
  color: var(--green-800);  
  border-radius: 999px;  
  padding: 10px 16px;  
  font-weight: 700;  
  cursor: pointer;  
  transition: all 0.2s ease;  
}  

.filter-btn.active {  
  background: var(--green-800);  
  color: var(--white);  
  border-color: var(--green-800);  
}  

.products {  
  display: grid;  
  grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));  
  gap: 22px;  
}  

.card {  
  background: var(--white);  
  border-radius: var(--radius);  
  box-shadow: var(--shadow);  
  overflow: hidden;  
  border: 1px solid rgba(18, 54, 36, 0.06);  
  transition: transform 0.2s ease, box-shadow 0.2s ease;  
}  

.card:hover {  
  transform: translateY(-3px);  
  box-shadow: 0 16px 32px rgba(18, 44, 32, 0.12);  
}  

.card img {  
  width: 100%;  
  height: 200px;  
  object-fit: cover;  
  background: #edf7f0;  
}  

.card-body {  
  padding: 18px 16px 16px;  
}  

.card-body h3 {  
  margin: 0 0 8px;  
  font-size: 1.18rem;  
}  

.price-row {  
  display: flex;  
  align-items: center;  
  justify-content: space-between;  
  gap: 10px;  
  margin-bottom: 12px;  
}  

.price {  
  font-weight: 800;  
  font-size: 1.5rem;  
  color: var(--green-700);  
}  

.old-price {  
  color: var(--muted);  
  font-size: 0.95rem;  
  text-decoration: line-through;  
}  

.card-btn {  
  width: 100%;  
  padding: 12px 14px;  
  border-radius: 12px;  
  background: linear-gradient(135deg, var(--green-500), var(--green-700));  
  color: var(--white);  
  border: none;  
  font-weight: 700;  
  cursor: pointer;  
}  

.info-grid {  
  display: grid;  
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));  
  gap: 18px;  
  margin-top: 16px;  
}  

.feature {  
  background: var(--white);  
  border-radius: var(--radius);  
  padding: 22px 18px;  
  box-shadow: var(--shadow);  
  border: 1px solid rgba(18, 54, 36, 0.05);  
}  

.feature .icon {  
  width: 46px;  
  height: 46px;  
  display: grid;  
  place-items: center;  
  background: var(--green-100);  
  color: var(--green-800);  
  border-radius: 12px;  
  font-size: 1.4rem;  
  margin-bottom: 14px;  
}  

.feature h3 {  
  margin: 0 0 8px;  
  font-size: 1.1rem;  
}  

.feature p {  
  margin: 0;  
  color: var(--muted);  
  line-height: 1.6;  
}  

.cart-layout {  
  display: grid;  
  grid-template-columns: 1.2fr 0.8fr;  
  gap: 22px;  
  margin-top: 28px;  
}  

.panel {  
  background: var(--white);  
  border-radius: 22px;  
  box-shadow: var(--shadow);  
  padding: 24px 20px;  
  border: 1px solid rgba(18, 54, 36, 0.04);  
}  

.panel h2 {  
  margin-top: 0;  
  margin-bottom: 18px;  
  font-size: clamp(1.4rem, 2vw, 2rem);  
}  

.cart-items {  
  display: flex;  
  flex-direction: column;  
  gap: 12px;  
}  

.cart-row {  
  display: grid;  
  grid-template-columns: 1.2fr auto auto auto;  
  align-items: center;  
  gap: 12px;  
  padding: 14px 12px;  
  border: 1px solid #ebf0eb;  
  border-radius: 14px;  
  background: linear-gradient(180deg, #ffffff, #f8fdf9);  
}  

.cart-row strong {  
  font-size: 0.98rem;  
}  

.cart-row .item-price {  
  color: var(--green-700);  
  font-weight: 700;  
}  

.qty-controls {  
  display: flex;  
  align-items: center;  
  gap: 8px;  
}  

.cart-action {  
  width: 30px;  
  height: 30px;  
  border-radius: 8px;  
  border: none;  
  background: #edf8f1;  
  color: var(--green-800);  
  font-weight: 800;  
  font-size: 1.1rem;  
  cursor: pointer;  
}  

.remove-btn {  
  padding: 8px 10px;  
  background: #fff3f3;  
  color: #b32d2d;  
  border: 1px solid #ffd6d6;  
  border-radius: 10px;  
  font-size: 0.78rem;  
}  

.cart-summary {  
  margin-top: 18px;  
  padding-top: 16px;  
  border-top: 1px solid #edf0ee;  
}  

.summary-row {  
  display: flex;  
  justify-content: space-between;  
  align-items: center;  
  padding: 8px 0;  
  font-size: 1rem;  
}  

.summary-row.total {  
  font-size: 1.35rem;  
  font-weight: 800;  
  color: var(--green-900);  
}  

.empty-cart {  
  color: var(--muted);  
  font-size: 1rem;  
  padding: 12px 0;  
}  

.form-fields {  
  display: grid;  
  gap: 14px;  
}  

label {  
  display: block;  
  font-weight: 700;  
  margin-bottom: 6px;  
  color: var(--green-900);  
}  

input, textarea {  
  width: 100%;  
  border: 1px solid #dfeadf;  
  background: #f9fbf9;  
  border-radius: 12px;  
  padding: 13px 14px;  
  color: var(--text);  
  outline: none;  
  transition: border-color 0.2s ease, box-shadow 0.2s ease;  
}  

input:focus, textarea:focus {  
  border-color: var(--green-600);  
  box-shadow: 0 0 0 3px rgba(25, 138, 76, 0.12);  
}  

textarea {  
  min-height: 120px;  
  resize: vertical;  
}  

.order-actions {  
  display: flex;  
  flex-wrap: wrap;  
  gap: 12px;  
  margin-top: 18px;  
}  

.wa-btn {  
  background: linear-gradient(135deg, #16a34a, #0f8e3f);  
  color: var(--white);  
}  

.email-btn {  
  background: linear-gradient(135deg, #0d4d2a, #083d1f);  
  color: var(--white);  
}  

.helper-text {  
  margin-top: 16px;  
  color: var(--muted);  
  font-size: 0.94rem;  
  line-height: 1.6;  
}  

footer {  
  background: #0d2c1e;  
  color: rgba(255,255,255,0.9);  
  padding: 28px 0 36px;  
  margin-top: 40px;  
}  

.footer-inner {  
  display: flex;  
  justify-content: space-between;  
  align-items: center;  
  gap: 18px;  
  flex-wrap: wrap;  
}  

.footer-brand {  
  font-weight: 800;  
  font-size: 1.2rem;  
}  

.footer-meta {  
  color: rgba(255,255,255,0.7);  
  line-height: 1.7;  
}  

@media (max-width: 860px) {  
  .hero-inner,  
  .cart-layout {  
    grid-template-columns: 1fr;  
  }  

  .nav {  
    align-items: flex-start;  
    padding: 16px 0;  
  }  

  .nav-links {  
    display: none;  
  }  

  .hero {  
    min-height: auto;  
  }  

  .hero-inner {  
    padding: 42px 0;  
  }  
}  

@media (max-width: 560px) {  
  .hero-stats {  
    grid-template-columns: 1fr;  
  }  

  .section-head {  
    align-items: flex-start;  
  }  

  .cart-row {  
    grid-template-columns: 1fr;  
    text-align: left;  
  }  

  .order-actions {  
    flex-direction: column;  
  }  

  .primary-btn, .secondary-btn, .shop-btn, .wa-btn, .email-btn {  
    width: 100%;  
    justify-content: center;  
  }  
}

  </style>  
</head>  
<body>  
  <header>  
    <div class="container nav">  
      <div class="brand">  
        <div class="brand-badge">🛒</div>  
        <span>The Local Shop</span>  
      </div>  <nav class="nav-links" aria-label="Main navigation">  
    <a href="#products">Products</a>  
    <a href="#features">Benefits</a>  
    <a href="#cart">Cart</a>  
    <a href="#order">Order</a>  
  </nav>  

  <button class="nav-btn" onclick="document.getElementById('cart').scrollIntoView({behavior:'smooth'})">  
    Cart (<span id="count">0</span>)  
  </button>  
</div>

  </header>    <section class="hero">  
    <div class="hero-inner">  
      <div class="hero-copy">  
        <div class="tag">Fresh finds • Best prices</div>  
        <h1>Everything you need, all in one place.</h1>  
        <p>  
          From daily essentials to family favorites, discover affordable groceries and household products delivered with care.  
        </p>  <div class="hero-actions">  
      <button class="primary-btn" onclick="document.getElementById('products').scrollIntoView({behavior:'smooth'})">  
        Shop Now  
      </button>  
      <button class="secondary-btn" onclick="document.getElementById('order').scrollIntoView({behavior:'smooth'})">  
        Place Order  
      </button>  
    </div>  

    <div class="hero-stats">  
      <div class="stat-box">  
        <strong>500+</strong>  
        <span>Happy customers</span>  
      </div>  
      <div class="stat-box">  
        <strong>30 min</strong>  
        <span>Fast delivery</span>  
      </div>  
      <div class="stat-box">  
        <strong>4.9/5</strong>  
        <span>Customer rating</span>  
      </div>  
    </div>  
  </div>  

  <div class="hero-card">  
    <div class="promo-badge">🔥 Weekend offer</div>  
    <h2 style="margin:0 0 10px;font-size:2rem;">Save up to 30%</h2>  
    <div class="mini-box">  
      <h3>Best Sellers</h3>  
      <p>Daily Grocery Pack, Snack Pack, Kitchen Essentials</p>  
    </div>  
    <div class="mini-box">  
      <h3>Delivery</h3>  
      <p>Fast local delivery across your area</p>  
    </div>  
  </div>  
</div>

  </section>    <main class="container">  
    <div class="section-head">  
      <div>  
        <h2 id="products">Shop Our Products</h2>  
      </div>  
      <p>Fresh quality with everyday savings</p>  
    </div>  <div class="filters" id="filters" aria-label="Product filters">  
  <button class="filter-btn active" data-filter="all">All</button>  
  <button class="filter-btn" data-filter="grocery">Groceries</button>  
  <button class="filter-btn" data-filter="snacks">Snacks</button>  
  <button class="filter-btn" data-filter="home">Home</button>  
</div>  

<div class="products" id="productList"></div>  

<div class="section-head" style="margin-top: 40px;">  
  <div>  
    <h2 id="features">Why choose us</h2>  
  </div>  
</div>  

<div class="info-grid">  
  <article class="feature">  
    <div class="icon">✅</div>  
    <h3>Trusted Quality</h3>  
    <p>Only the best essentials and fresh products carefully selected for your family.</p>  
  </article>  

  <article class="feature">  
    <div class="icon">🚚</div>  
    <h3>Fast Delivery</h3>  
    <p>We deliver quickly in your area so your essentials reach you on time.</p>  
  </article>  

  <article class="feature">  
    <div class="icon">💰</div>  
    <h3>Affordable Prices</h3>  
    <p>Best value deals on daily necessities, snacks, and home essentials.</p>  
  </article>  

  <article class="feature">  
    <div class="icon">📞</div>  
    <h3>Easy Ordering</h3>  
    <p>Order directly through WhatsApp or email in just a few clicks.</p>  
  </article>  
</div>  

<div class="cart-layout">  
  <section class="panel" id="cart">  
    <h2>🛒 Your Shopping Cart</h2>  
    <div class="cart-items" id="cartItems">  
      <div class="empty-cart">Your cart is empty. Add some great products.</div>  
    </div>  

    <div class="cart-summary">  
      <div class="summary-row">  
        <span>Items</span>  
        <strong><span id="itemCount">0</span></strong>  
      </div>  
      <div class="summary-row total">  
        <span>Total</span>  
        <span>₹<span id="total">0.00</span></span>  
      </div>  
    </div>  
  </section>  

  <section class="panel" id="order">  
    <h2>📦 Customer Details</h2>  

    <form id="orderForm">  
      <div class="form-fields">  
        <div>  
          <label for="name">Full Name *</label>  
          <input id="name" required placeholder="Your full name" />  
        </div>  

        <div>  
          <label for="phone">Phone Number *</label>  
          <input id="phone" type="tel" required placeholder="Your phone number" />  
        </div>  

        <div>  
          <label for="address">Delivery Address *</label>  
          <textarea id="address" required placeholder="Village, town, PIN code"></textarea>  
        </div>  
      </div>  

      <div class="order-actions">  
        <button type="button" class="primary-btn wa-btn" onclick="orderWhatsApp()">Order via WhatsApp</button>  
        <button type="button" class="primary-btn email-btn" onclick="orderEmail()">Order via Email</button>  
      </div>  

      <p class="helper-text">  
        Please check your order details, then send the message in WhatsApp or your email app to confirm the order.  
      </p>  
    </form>  
  </section>  
</div>

  </main>    <footer>  
    <div class="container footer-inner">  
      <div>  
        <div class="footer-brand">The Local Shop</div>  
        <div class="footer-meta">Fresh Finds, Best Prices</div>  
      </div>  
      <div class="footer-meta">  
        Email: nizanur@gmail.com<br />  
        WhatsApp: +91 9395026609  
      </div>  
    </div>  
  </footer>    <script>  
    const SHOP_EMAIL = "nizanur@gmail.com";  
    const WHATSAPP = "919395026609";  
  
    const products = [  
      {  
        id: 1,  
        name: "Daily Grocery Pack",  
        price: 99,  
        category: "grocery",  
        image: "https://i.ibb.co/7xShCVjf/Screenshot-20261013-072524-Chrome.jpg"  
      },  
      {  
        id: 2,  
        name: "Crunchy Snack Pack",  
        price: 40,  
        category: "snacks",  
        image: "https://i.ibb.co/Wp56S2kp/Screenshot-20261013-072451-Chrome.jpg"  
      },  
      {  
        id: 3,  
        name: "Kitchen Essentials",  
        price: 75,  
        category: "home",  
        image: "https://i.ibb.co/bjtsLbd5/Screenshot-20261013-072543-Chrome.jpg"  
      },  
      {  
        id: 4,  
        name: "Fresh Fruit Basket",  
        price: 120,  
        category: "grocery",  
        image: "https://images.unsplash.com/photo-1542838132-92c53300491e?auto=format&fit=crop&w=800&q=80"  
      },  
      {  
        id: 5,  
        name: "Family Snack Box",  
        price: 65,  
        category: "snacks",  
        image: "https://images.unsplash.com/photo-1514996937319-344454492b37?auto=format&fit=crop&w=800&q=80"  
      },  
      {  
        id: 6,  
        name: "Cleaning Care Kit",  
        price: 150,  
        category: "home",  
        image: "https://images.unsplash.com/photo-1581578731548-c64695cc6952?auto=format&fit=crop&w=800&q=80"  
      }  
    ];  
  
    let cart = {};  
    let activeFilter = "all";  
  
    try {  
      cart = JSON.parse(localStorage.getItem("localShopCart") || "{}");  
    } catch {  
      cart = {};  
    }  
  
    function saveCart() {  
      localStorage.setItem("localShopCart", JSON.stringify(cart));  
      renderCart();  
    }  
  
    function renderProducts() {  
      const currentProducts = activeFilter === "all"  
        ? products  
        : products.filter(product => product.category === activeFilter);  
  
      document.getElementById("productList").innerHTML = currentProducts.map(product => `  
        <article class="card">  
          <img src="${product.image}" alt="${product.name}" />  
          <div class="card-body">  
            <h3>${product.name}</h3>  
            <div class="price-row">  
              <span class="price">₹${product.price}</span>  
              <span class="old-price">₹${product.price + 20}</span>  
            </div>  
            <button class="card-btn" onclick="addToCart(${product.id})">Add to Cart</button>  
          </div>  
        </article>  
      `).join("");  
    }  
  
    function addToCart(id) {  
      cart[id] = (cart[id] || 0) + 1;  
      saveCart();  
    }  
  
    function changeQuantity(id, delta) {  
      cart[id] = (cart[id] || 0) + delta;  
  
      if (cart[id] <= 0) {  
        delete cart[id];  
      }  
  
      saveCart();  
    }  
  
    function clearCart() {  
      cart = {};  
      saveCart();  
    }  
  
    function renderCart() {  
      let count = 0;  
      let total = 0;  
      let content = "";  
  
      products.forEach(product => {  
        const qty = cart[product.id] || 0;  
        if (qty > 0) {  
          count += qty;  
          total += qty * product.price;  
  
          content += `  
            <div class="cart-row">  
              <div>  
                <strong>${product.name}</strong>  
                <div class="item-price">₹${product.price}</div>  
              </div>  
              <div class="qty-controls">  
                <button class="cart-action" aria-label="Decrease quantity" onclick="changeQuantity(${product.id}, -1)">−</button>  
                <span>${qty}</span>  
                <button class="cart-action" aria-label="Increase quantity" onclick="changeQuantity(${product.id}, 1)">＋</button>  
              </div>  
              <div class="item-price">₹${(qty * product.price).toFixed(2)}</div>  
              <button class="remove-btn" onclick="changeQuantity(${product.id}, -999)">Remove</button>  
            </div>  
          `;  
        }  
      });  
  
      document.getElementById("cartItems").innerHTML = content || '<div class="empty-cart">Your cart is empty. Add some great products.</div>';  
      document.getElementById("count").textContent = count;  
      document.getElementById("total").textContent = total.toFixed(2);  
      document.getElementById("itemCount").textContent = count;  
  
      // Keep clear cart button if needed  
    }  
  
    function buildMessage() {  
      if (!document.getElementById("orderForm").reportValidity()) {  
        return null;  
      }  
  
      const items = products.filter(product => (cart[product.id] || 0) > 0);  
  
      if (!items.length) {  
        alert("Please add products to your cart first.");  
        return null;  
      }  
  
      const name = document.getElementById("name").value.trim();  
      const phone = document.getElementById("phone").value.trim();  
      const address = document.getElementById("address").value.trim();  
  
      const lines = items.map(product => {  
        const qty = cart[product.id];  
        return `${product.name} x ${qty} = ₹${(qty * product.price).toFixed(2)}`;  
      });  
  
      const total = items.reduce((sum, product) => sum + (cart[product.id] * product.price), 0);  
  
      return `ORDER REQUEST - The Local Shop  
  
Name: ${name}  
Phone: ${phone}  
Address: ${address}  
  
Items:  
${lines.join("\n")}  
  
Total: ₹${total.toFixed(2)}  
  
Please confirm availability and delivery charges.`;  
    }  
  
    function orderWhatsApp() {  
      const message = buildMessage();  
      if (message) {  
        window.open(`https://wa.me/${WHATSAPP}?text=${encodeURIComponent(message)}`, "_blank");  
      }  
    }  
  
    function orderEmail() {  
      const message = buildMessage();  
      if (message) {  
        window.location.href = `mailto:${SHOP_EMAIL}?subject=${encodeURIComponent("Order Request - The Local Shop")}&body=${encodeURIComponent(message)}`;  
      }  
    }  
  
    document.querySelectorAll(".filter-btn").forEach(button => {  
      button.addEventListener("click", () => {  
        activeFilter = button.dataset.filter;  
        document.querySelectorAll(".filter-btn").forEach(btn => btn.classList.toggle("active", btn === button));  
        renderProducts();  
      });  
    });  
  
    renderProducts();  
    renderCart();  
  </script>  </body>  
</html>  Is ka structure do
