<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AW ALI STORE</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,sans-serif;
}

body{
    background:#f5f5f5;
    color:#222;
}

header{
    background:#050505;
    color:white;
    padding:18px;
    text-align:center;
    position:sticky;
    top:0;
    z-index:10;
}

.logo{
    color:#d4af37;
    font-size:30px;
    font-weight:bold;
}

nav{
    margin-top:12px;
}

nav a{
    color:white;
    text-decoration:none;
    margin:0 8px;
    font-size:14px;
}

.hero{
    background:linear-gradient(135deg,#000,#292929);
    color:white;
    text-align:center;
    padding:70px 20px;
}

.hero h1{
    color:#d4af37;
    font-size:40px;
    margin-bottom:15px;
}

.hero p{
    font-size:18px;
    margin-bottom:25px;
}

.btn{
    display:inline-block;
    background:#d4af37;
    color:#000;
    padding:12px 22px;
    border-radius:7px;
    text-decoration:none;
    font-weight:bold;
}

.section{
    padding:45px 20px;
    text-align:center;
}

.section h2{
    font-size:30px;
    margin-bottom:25px;
}

.search{
    width:90%;
    max-width:500px;
    padding:14px;
    border:1px solid #ddd;
    border-radius:8px;
    margin-bottom:30px;
    font-size:16px;
}

.products{
    display:flex;
    flex-wrap:wrap;
    justify-content:center;
    gap:20px;
}

.product{
    background:white;
    width:270px;
    padding:20px;
    border-radius:12px;
    box-shadow:0 4px 15px rgba(0,0,0,.1);
}

.product-image{
    height:150px;
    background:#eee;
    border-radius:10px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:65px;
    margin-bottom:15px;
}

.product h3{
    margin-bottom:10px;
}

.price{
    color:#d4af37;
    font-size:22px;
    font-weight:bold;
    margin:12px 0;
}

.about{
    background:white;
}

.contact{
    background:#111;
    color:white;
}

.contact h2{
    color:#d4af37;
}

footer{
    background:#000;
    color:white;
    text-align:center;
    padding:18px;
}
</style>
</head>

<body>

<header>
    <div class="logo">AW ALI STORE</div>

    <nav>
        <a href="#home">Home</a>
        <a href="#products">Products</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
    </nav>
</header>

<section class="hero" id="home">
    <h1>ALI STORE</h1>
    <p>Quality Products • Best Deals • Easy Shopping</p>
    <a href="#products" class="btn">Shop Now</a>
</section>

<section class="section" id="products">
    <h2>Our Products</h2>

    <input
        class="search"
        type="text"
        placeholder="Search products..."
        onkeyup="searchProducts()"
        id="searchBox"
    >

    <div class="products" id="productList">

        <div class="product">
            <div class="product-image">⌚</div>
            <h3>Smart Watch</h3>
            <p>Stylish smart watch for everyday use.</p>
            <div class="price">Coming Soon</div>
            <a class="btn" href="#contact">View Product</a>
        </div>

        <div class="product">
            <div class="product-image">🎧</div>
            <h3>Wireless Headphones</h3>
            <p>Wireless headphones with quality sound.</p>
            <div class="price">Coming Soon</div>
            <a class="btn" href="#contact">View Product</a>
        </div>

        <div class="product">
            <div class="product-image">🎮</div>
            <h3>Gaming Accessories</h3>
            <p>Gaming accessories for gamers.</p>
            <div class="price">Coming Soon</div>
            <a class="btn" href="#contact">View Product</a>
        </div>

    </div>
</section>

<section class="section about" id="about">
    <h2>About ALI STORE</h2>
    <p>
        Welcome to ALI STORE. We are building an online store
        where customers can find useful and quality products
        at competitive prices.
    </p>
</section>

<section class="section contact" id="contact">
    <h2>Contact ALI STORE</h2>
    <p>For product information and orders, contact us on WhatsApp.</p>

    <br>

    <a
        class="btn"
        href="https://wa.me/923000000000"
        target="_blank">
        WhatsApp
    </a>
</section>

<footer>
    © 2026 AW ALI STORE — All Rights Reserved
</footer>

<script>
function searchProducts(){
    let input = document.getElementById("searchBox").value.toLowerCase();
    let products = document.querySelectorAll(".product");

    products.forEach(function(product){
        let name = product.innerText.toLowerCase();

        if(name.includes(input)){
            product.style.display = "block";
        }else{
            product.style.display = "none";
        }
    });
}
</script>

</body>
</html>
