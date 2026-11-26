
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Little Loop | Custom Bracelets</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial,sans-serif;background:#090909;color:white}
header{text-align:center;padding:25px 12px;background:#111;border-bottom:2px solid #d4af37}
.logo{font-size:36px;color:#e5c45b;font-weight:bold}
header p{color:#ddd;margin:8px}
nav{text-align:center;padding:15px}
nav a{color:#e5c45b;text-decoration:none;margin:10px;font-size:14px}
.hero{text-align:center;padding:65px 20px;background:linear-gradient(135deg,#191919,#352b15)}
.hero h1{font-size:38px;color:#f3d36a}
.hero p{color:#eee}
.btn{display:inline-block;background:#d4af37;color:#111;padding:13px 22px;border-radius:25px;text-decoration:none;font-weight:bold;margin-top:15px}
section{padding:30px 16px;text-align:center}
h2{color:#e5c45b}
.products{display:grid;grid-template-columns:repeat(2,1fr);gap:14px;max-width:650px;margin:auto}
.card{background:#191919;border:1px solid #705c28;border-radius:15px;padding:15px}
.emoji{font-size:48px}
.product-img {file_000000007044821182e0f57497afa488.webp
width:100%;
height:160px;
object-fit:cover;
border-radius:12px;
margin-bottom:10px;
}
.card h3{color:#f3d36a}
.price{color:#fff;font-weight:bold}
.card button{background:#d4af37;border:0;padding:10px 15px;border-radius:20px;font-weight:bold}
input,select{width:90%;max-width:350px;padding:13px;margin:8px;border-radius:8px;border:1px solid #d4af37;background:#191919;color:white}
footer{padding:25px;text-align:center;background:#111;color:#ccc}
</style>
</head>
<body>
<header>
<div class="logo">🌈 Little Loop</div>
<p>Your Name, Your Style, Your Little Loop!</p>
</header>
<nav>
<a href="#home">Home</a>
<a href="#shop">Shop</a>
<a href="#custom">Customise</a>
</nav>
<div class="hero" id="home">
<h1>Wear Your Name! 💖</h1>
<p>Colourful handmade bracelets made just for you.</p>
<a class="btn" href="#shop">Explore Collection</a>
</div>
<section id="shop">
<h2>Our Collections ✨</h2>
<div class="products">
<div class="card">
<img src="bracelet1.png"
alt="Little Loop bracelet"
class="product-img">
<h3>Rainbow Names</h3>
<p>Colourful name bracelets</p>
<p class="price">₹49</p>
<button onclick="choose('Rainbow Names',49)">Order Now</button>
</div>
<div class="card">
<div class="emoji">💚</div>
<h3>Neon Vibes</h3>
<p>Bright and funky bracelets</p>
<p class="price">₹59</p>
<button onclick="choose('Neon Vibes',59)">Order Now</button>
</div>
<div class="card">
<div class="emoji">😊</div>
<h3>Smiley Loops</h3>
<p>Happy little designs</p>
<p class="price">₹69</p>
<button onclick="choose('Smiley Loops',69)">Order Now</button>
</div>
<div class="card">
<div class="emoji">💕</div>
<h3>Bestie Loops</h3>
<p>Matching friendship pair</p>
<p class="price">₹119</p>
<button onclick="choose('Bestie Loops',119)">Order Now</button>
</div>
</div>
</section>
<section id="custom">
<h2>Make Your Own Bracelet 🎀</h2>
<p>Choose your name and favourite colour!</p>
<input id="customer" placeholder="Your name">
<input id="braceletName" placeholder="Name for bracelet">
<select id="colour">
<option>Rainbow</option>
<option>Pink</option>
<option>Blue</option>
<option>Green</option>
<option>Purple</option>
<option>Yellow</option>
</select>
<input id="product" placeholder="Selected collection" readonly>
<a class="btn" href="#" onclick="order();return false">Order on WhatsApp</a>
</section>
<footer>
<p>🌈 Little Loop</p>
<p>Made with love, one bead at a time! 💗</p>
</footer>
<script>
let selected="";
function choose(name,price){
selected=name;
document.getElementById('product').value=name+" - ₹"+price;
document.getElementById('custom').scrollIntoView({behavior:'smooth'});
}
function order(){
let customer=document.getElementById('customer').value.trim();
let name=document.getElementById('braceletName').value.trim();
let colour=document.getElementById('colour').value;
let product=document.getElementById('product').value||"Custom bracelet";
if(!customer||!name){alert("Please enter your name and bracelet name!");return;}
let message=`Hello Little Loop! I want to order a bracelet.%0ACustomer: ${customer}%0ABracelet name: ${name}%0AColour: ${colour}%0ACollection: ${product}`;
window.open("https://wa.me/919985459876?text="+message,"_blank");
}
</script>
</body>
</html>
