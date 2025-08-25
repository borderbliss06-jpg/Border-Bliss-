<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Border Bliss | Sweet Bliss in Every Bite</title>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Roboto:wght@400;700&display=swap" rel="stylesheet">
<style>
/* Global Styles */
body {margin:0; font-family:'Roboto',sans-serif; background:#ffeef6; color:#3e2c2a;}
a {text-decoration:none; color:inherit;}
img {max-width:100%; display:block; border-radius:15px;}
button {cursor:pointer; border:none; padding:12px 25px; border-radius:50px; background:linear-gradient(45deg,#ffb6c1,#ffc0cb); color:#3e2c2a; font-weight:bold; font-size:1rem; transition:0.3s; box-shadow: 0 5px 10px rgba(0,0,0,0.1);}
button:hover {transform:translateY(-3px) scale(1.05); background:linear-gradient(45deg,#ff9fbf,#ffb6c1);}

/* Header */
header {display:flex; justify-content:space-between; align-items:center; padding:20px 30px; background:#ffd9e8; position:sticky; top:0; z-index:100; box-shadow:0 4px 10px rgba(0,0,0,0.05);}
.logo {font-family:'Pacifico',cursive; font-size:2.2rem; color:#ff77a9;}
nav a {margin-left:20px; font-weight:700; font-size:1rem; transition:0.3s; border-radius:25px; padding:5px 10px;}
nav a:hover {background:#ffcee6;}

/* Hero */
.hero {background:linear-gradient(135deg,#ffc0cb,#ffb6c1); text-align:center; padding:150px 20px; color:#fff; border-bottom:5px solid #ff77a9; position:relative; box-shadow:0 5px 15px rgba(0,0,0,0.05);}
.hero h1 {font-family:'Pacifico',cursive; font-size:3rem; margin-bottom:20px; color:#fff;}
.hero p {font-size:1.2rem; margin-bottom:30px; color:#fff;}

/* Sections */
.section-title {font-size:2rem; margin-bottom:40px; text-align:center; color:#ff77a9;}
.flavors-grid, .cart-items {display:grid; grid-template-columns:repeat(auto-fit,minmax(220px,1fr)); gap:20px; max-width:1200px; margin:0 auto;}
.flavor-card {background:#ffe3f0; border-radius:25px; padding:20px; text-align:center; transition:0.3s; box-shadow:0 8px 15px rgba(0,0,0,0.1);}
.flavor-card:hover {transform:translateY(-5px) scale(1.05); box-shadow:0 10px 20px rgba(0,0,0,0.15);}
.flavor-card h3 {margin-bottom:10px; color:#ff77a9;}
.flavor-card p {margin:5px 0; font-weight:bold;}

/* About & Contact */
.about, .contact {padding:80px 20px; text-align:center;}
.about p {max-width:700px; margin:0 auto; line-height:1.6; color:#3e2c2a;}
.contact form {max-width:500px; margin:0 auto; display:flex; flex-direction:column;}
.contact input, .contact textarea {padding:15px; margin-bottom:20px; border-radius:15px; border:1px solid #ffc0cb; font-size:1rem; resize:none;}

/* Cart & Checkout */
#cart {padding:40px 20px; max-width:1200px; margin:0 auto;}
.cart-item {display:flex; justify-content:space-between; align-items:center; background:#ffe3f0; padding:15px; border-radius:20px; margin-bottom:15px; box-shadow:0 5px 10px rgba(0,0,0,0.05);}
#checkoutForm {max-width:500px; margin:40px auto; display:none; text-align:left;}

/* Footer */
footer {background:#ffd9e8; text-align:center; padding:20px; margin-top:50px; color:#ff77a9; font-weight:bold;}

/* Responsive */
@media(max-width:600px){header{flex-direction:column;} nav a{margin:10px 0;}}
</style>
</head>
<body>

<!-- Header -->
<header>
    <div class="logo">Border Bliss 💖</div>
    <nav>
        <a href="#home">Home</a>
        <a href="#flavors">Flavors</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
        <a href="#cart">Cart 🛒</a>
    </nav>
</header>

<!-- Hero -->
<section class="hero" id="home">
    <div class="hero-content">
        <h1>Sweet Bliss in Every Bite 🍫</h1>
        <p>Handmade chocolates crafted with love 💕</p>
        <button onclick="document.getElementById('flavors').scrollIntoView({behavior:'smooth'})">Shop Now ✨</button>
    </div>
</section>

<!-- Flavors -->
<section id="flavors">
    <h2 class="section-title">Our Flavors 🌸</h2>
    <div class="flavors-grid" id="flavorsGrid"></div>
</section>

<!-- About -->
<section class="about" id="about">
    <h2 class="section-title">About Border Bliss 💖</h2>
    <p>Border Bliss started as a teen’s dream to make chocolate magical for everyone. Every piece is handmade with love, care, and the finest ingredients. Sweeten your moments with our premium chocolate delights 🍫✨.</p>
</section>

<!-- Contact -->
<section class="contact" id="contact">
    <h2 class="section-title">Contact Us 📬</h2>
    <form action="mailto:border.bliss.06@gmail.com" method="post" enctype="text/plain">
        <input type="text" name="name" placeholder="Your Name" required>
        <input type="email" name="email" placeholder="Your Email" required>
        <textarea name="message" placeholder="Your Message" rows="5" required></textarea>
        <button type="submit">Send Message 💌</button>
    </form>
</section>

<!-- Cart & Checkout -->
<section id="cart">
    <h2 class="section-title">Your Cart 🛒</h2>
    <div class="cart-items" id="cartItems">
        <p style="text-align:center; grid-column:1/-1;">Your cart is empty.</p>
    </div>
    <p style="text-align:center; font-weight:bold;" id="totalPrice"></p>

    <div id="checkoutForm">
        <h3>Checkout ✨</h3>
        <form id="orderForm" action="mailto:border.bliss.06@gmail.com" method="post" enctype="text/plain">
            <input type="text" name="name" placeholder="Your Name" required>
            <input type="email" name="email" placeholder="Your Email" required>
            <input type="text" name="phone" placeholder="Phone Number" required>
            <textarea name="address" placeholder="Delivery Address" rows="4" required></textarea>
            <textarea name="orderDetails" id="orderDetails" hidden></textarea>
            <button type="submit">Place Order 💖</button>
        </form>
    </div>
</section>

<footer>© 2025 Border Bliss 💕 | Contact: border.bliss.06@gmail.com</footer>

<script>
// Flavors Data
const flavors = [
    {name:"Velvet Almond Crunch", price:120, img:"https://images.unsplash.com/photo-1606107557195-0e29a4b5b4aa?auto=format&fit=crop&w=400&q=80"},
    {name:"Rose Kiss Bliss", price:130, img:"https://images.unsplash.com/photo-1599785209707-2a3f9c1f70c0?auto=format&fit=crop&w=400&q=80"},
    {name:"Caramel Horizon", price:140, img:"https://images.unsplash.com/photo-1627328715728-882d70e78b53?auto=format&fit=crop&w=400&q=80"},
    {name:"Mystic Mint", price:125, img:"https://images.unsplash.com/photo-1617196039094-3f36cfb43264?auto=format&fit=crop&w=400&q=80"}
];

const flavorsGrid = document.getElementById("flavorsGrid");
const cartItems = document.getElementById("cartItems");
const totalPriceEl = document.getElementById("totalPrice");
const checkoutForm = document.getElementById("checkoutForm");
let cart = [];

// Render Flavors
function renderFlavors() {
    flavors.forEach((flavor,index)=>{
        const card = document.createElement("div");
        card.className="flavor-card";
        card.innerHTML=`
            <img src="${flavor.img}" alt="${flavor.name}">
            <h3>${flavor.name}</h3>
            <p>₹${flavor.price}</p
