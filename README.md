<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Novitri Kuliner</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>

<style>
:root{
  --primary:#ff5722;
  --secondary:#e91e63;
  --bg:#f4f4f4;
}
*{margin:0;padding:0;box-sizing:border-box;font-family:Poppins}
body{background:var(--bg)}

nav{
  position:sticky;top:0;z-index:99;
  background:#fff;
  padding:14px 20px;
  display:flex;justify-content:space-between;align-items:center;
  box-shadow:0 6px 15px rgba(0,0,0,.1);
}
nav h1{color:var(--secondary);font-size:20px}

.hero{
  margin:15px;
  padding:90px 20px;
  border-radius:22px;
  background:
   linear-gradient(rgba(0,0,0,.55),rgba(0,0,0,.55)),
   url("pedas-nampol.jpg") center/cover no-repeat;
  color:#fff;
  text-align:center;
}
.hero h2{font-size:32px}

.section{margin:25px 15px}
.menu-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(160px,1fr));
  gap:15px;
}

.card{
  background:#fff;
  border-radius:18px;
  overflow:hidden;
  box-shadow:0 8px 20px rgba(0,0,0,.1);
}
.card img{
  width:100%;
  height:140px;
  object-fit:cover;
}
.card-content{padding:14px}
.card h3{font-size:15px;color:var(--secondary)}
.card small{font-size:12px;color:#dbcccc}
.card button{
  width:100%;
  margin-top:6px;
  padding:8px;
  border:none;
  border-radius:10px;
  background:linear-gradient(135deg,var(--primary),var(--secondary));
  color:#fff;
  font-size:13px;
}

.cart{
  background:#fff;
  margin:20px 15px;
  padding:18px;
  border-radius:20px;
}
.cart-item{
  display:grid;
  grid-template-columns:1fr auto auto;
  gap:8px;
  border-bottom:1px dashed #ccc;
  padding:8px 0;
  font-size:13px;
}
.total{text-align:right;font-weight:700;margin-top:10px}

.checkout,.pdf{
  width:100%;
  margin-top:10px;
  padding:12px;
  border:none;
  border-radius:14px;
  font-weight:700;
  color:#fff;
}
.checkout{background:#25D366}
.pdf{background:#444}
</style>
</head>

<body>

<nav>
  <h1>Novitri Kuliner</h1>
  <div>🛒 <span id="cartCount">0</span></div>
</nav>

<section class="hero">
  <h2>Pedasnya Nampol 🔥</h2>
  <p>Martabak • Mie • Jajanan</p>
</section>

<section class="section">
<div class="menu-grid">

<!-- MARTABAK 1 TELOR -->
<div class="card">
<img src="martabak.jpg">
<div class="card-content">
<h3>Martabak Telor (1 Telor)</h3>
<button onclick="add('Martabak Bakso (1)',5000)">Bakso • 5K</button>
<button onclick="add('Martabak Kornet (1)',7000)">Kornet • 7K</button>
<button onclick="add('Martabak Sosis (1)',7000)">Sosis • 7K</button>
<button onclick="add('Martabak Mix (1)',8000)">Mix • 8K</button>
</div>
</div>

<!-- MARTABAK 2 TELOR -->
<div class="card">
<img src="martabak.jpg">
<div class="card-content">
<h3>Martabak Telor (2 Telor)</h3>
<button onclick="add('Martabak Bakso (2)',10000)">Bakso • 10K</button>
<button onclick="add('Martabak Kornet (2)',14000)">Kornet • 14K</button>
<button onclick="add('Martabak Sosis (2)',14000)">Sosis • 14K</button>
<button onclick="add('Martabak Mix (2)',15000)">Mix • 15K</button>
</div>
</div>

<!-- MIE JEBEW -->
<div class="card">
<img src="mie-jebew.jpg">
<div class="card-content">
<h3>Mie Jebew</h3>
<small>Level 1–3</small>
<button onclick="add('Mie Jebew',10000)">Level 1 10K</button>
<button onclick="add('Mie Jebew',10000)">Level 2 10K</button>
<button onclick="add('Mie Jebew',10000)">Level 3 10K</button>
</div>
</div>

<!-- PANGSIT -->
<div class="card">
<img src="pangsit.jpg">
<div class="card-content">
<h3>Pangsit Chili Oil</h3>
<small>Isi 5 pcs </small>
<button onclick="add('Pangsit Chili Oil',10000)">Level 1 10K</button>
<button onclick="add('Pangsit Chili Oil',10000)">Level 2 10K</button>
<button onclick="add('Pangsit Chili Oil',10000)">Level 3 10K</button>
</div>
</div>

<!-- MIE NYEMEK -->
<div class="card">
<img src="mie-nyemek.jpg">
<div class="card-content">
<h3>Mie Nyemek</h3>
<button onclick="add('Mie Nyemek',8000)">level 1 8K</button>
<button onclick="add('Mie Nyemek',8000)">level 2 8K</button>
<button onclick="add('Mie Nyemek',8000)">level 3 8K</button>
</div>
</div>

<!-- SEBLAK -->
<div class="card">
<img src="seblak.jpg">
<div class="card-content">
<h3>Seblak</h3>
<button onclick="add('Seblak',10000)">Level 1 10K</button>
<button onclick="add('Seblak',10000)">Level 2 10K</button>
<button onclick="add('Seblak',10000)">Level 3 10K</button>
</div>
</div>

<!-- SEMPOL -->
<div class="card">
<img src="sempol.jpg">
<div class="card-content">
<h3>Sempol (3 pcs)</h3>
<button onclick="add('Sempol Keju',5000)">Keju</button>
<button onclick="add('Sempol Barbeque',5000)">Barbeque</button>
<button onclick="add('Sempol Chili Oil',5000)">Chili Oil</button>
</div>
</div>

<!-- PENTOL -->
<div class="card">
<img src="pentol.jpg">
<div class="card-content">
<h3>Pentol (4 pcs)</h3>
<button onclick="add('Pentol Keju',5000)">Keju</button>
<button onclick="add('Pentol Barbeque',5000)">Barbeque</button>
<button onclick="add('Pentol Chili Oil',5000)">Chili Oil</button>
</div>
</div>

</div>
</section>

<section class="cart">
<h3>🧾 Keranjang</h3>
<div id="cartList"></div>
<div class="total">Total: Rp <span id="total">0</span></div>
<button class="checkout" onclick="checkout()">Pesan via WhatsApp</button>
<button class="pdf" onclick="printPDF()">Cetak Nota PDF</button>
</section>

<script>
let cart={};

function add(n,p){
 if(!cart[n]) cart[n]={price:p,qty:0};
 cart[n].qty++; render();
}

function render(){
 let list=document.getElementById("cartList");
 let total=0,count=0;
 list.innerHTML="";
 for(let i in cart){
  let it=cart[i];
  total+=it.price*it.qty;
  count+=it.qty;
  list.innerHTML+=`
   <div class="cart-item">
     <span>${i}</span>
     <span>x${it.qty}</span>
     <span>Rp ${it.price*it.qty}</span>
   </div>`;
 }
 document.getElementById("total").innerText=total;
 document.getElementById("cartCount").innerText=count;
}

function checkout(){
 let msg="Halo, saya pesan:%0A";
 let total=0;
 for(let i in cart){
  let it=cart[i];
  msg+=`- ${i} x${it.qty}%0A`;
  total+=it.price*it.qty;
 }
 msg+=`%0ATotal: Rp ${total}`;
 window.open("https://wa.me/6281398437837?text="+msg);
}

function printPDF(){
 const {jsPDF}=window.jspdf;
 let pdf=new jsPDF();
 let y=20;
 pdf.text("NOVITRI KULINER",105,y,{align:"center"});
 y+=6; pdf.line(10,y,200,y); y+=8;
 for(let i in cart){
  let it=cart[i];
  pdf.text(`${i} x${it.qty}`,10,y);
  pdf.text(`Rp ${it.price*it.qty}`,190,y,{align:"right"});
  y+=7;
 }
 pdf.line(10,y,200,y); y+=8;
 pdf.text(`TOTAL : Rp ${document.getElementById("total").innerText}`,105,y,{align:"center"});
 pdf.save("nota-novitri-kuliner.pdf");
}
</script>

</body>
</html>
