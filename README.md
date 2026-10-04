# Apex_planet.task-5
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>EasyShop - Online Shopping</title>

    <style>

        /* ================= BASIC ================= */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, sans-serif;
            background: #f5f7f8;
            color: #333;
        }

        button {
            cursor: pointer;
        }


        /* ================= HEADER ================= */

        header {
            background: #087f8c;
            color: white;
            padding: 18px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo {
            font-size: 28px;
            font-weight: bold;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 10px;
            font-weight: bold;
        }

        nav a:hover {
            text-decoration: underline;
        }

        .dark-btn {
            background: white;
            color: #087f8c;
            border: none;
            padding: 8px 12px;
            border-radius: 5px;
        }


        /* ================= HERO ================= */

        .hero {
            background: linear-gradient(135deg, #dff8fa, white);
            text-align: center;
            padding: 60px 20px;
        }

        .hero h1 {
            color: #087f8c;
            font-size: 40px;
            margin-bottom: 15px;
        }

        .hero p {
            font-size: 18px;
            margin-bottom: 25px;
        }

        .btn {
            background: #087f8c;
            color: white;
            border: none;
            padding: 12px 22px;
            border-radius: 6px;
            font-size: 15px;
        }

        .btn:hover {
            background: #055d66;
        }


        /* ================= SEARCH ================= */

        .search-box {
            text-align: center;
            padding: 25px;
            background: white;
        }

        .search-box input {
            width: 70%;
            max-width: 500px;
            padding: 13px;
            border: 1px solid #ccc;
            border-radius: 6px;
            font-size: 16px;
        }


        /* ================= CATEGORIES ================= */

        .categories {
            text-align: center;
            padding: 30px 20px;
        }

        .categories h2 {
            color: #087f8c;
            margin-bottom: 20px;
        }

        .category-btn {
            border: none;
            background: white;
            padding: 12px 20px;
            margin: 5px;
            border-radius: 20px;
            box-shadow: 0 2px 7px #ccc;
        }

        .category-btn:hover {
            background: #087f8c;
            color: white;
        }


        /* ================= PRODUCTS ================= */

        .products {
            padding: 40px 5%;
            text-align: center;
        }

        .products h2 {
            color: #087f8c;
            margin-bottom: 30px;
        }

        .product-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 25px;
        }

        .product {
            background: white;
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 3px 12px #ddd;
            transition: 0.3s;
            position: relative;
        }

        .product:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 18px #ccc;
        }

        .product-image {
            font-size: 65px;
            padding: 20px;
        }

        .product h3 {
            margin: 10px 0;
        }

        .product p {
            color: #666;
            font-size: 14px;
        }

        .price {
            color: #087f8c;
            font-size: 21px;
            font-weight: bold;
            margin: 12px;
        }

        .rating {
            color: #f5a623;
            margin-bottom: 12px;
        }

        .wishlist {
            position: absolute;
            right: 15px;
            top: 15px;
            border: none;
            background: none;
            font-size: 22px;
        }


        /* ================= CART ================= */

        .cart {
            background: #e5f7f8;
            padding: 40px 20px;
            text-align: center;
        }

        .cart h2 {
            color: #087f8c;
            margin-bottom: 20px;
        }

        #cartItems {
            max-width: 600px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            min-height: 50px;
        }

        .cart-item {
            display: flex;
            justify-content: space-between;
            padding: 10px;
            border-bottom: 1px solid #ddd;
        }

        .quantity-btn {
            border: none;
            background: #087f8c;
            color: white;
            padding: 4px 9px;
            margin: 3px;
            border-radius: 4px;
        }

        .cart-buttons {
            margin-top: 20px;
        }


        /* ================= DISCOUNT ================= */

        .discount {
            background: white;
            padding: 40px;
            text-align: center;
        }

        .discount h2 {
            color: #087f8c;
            margin-bottom: 15px;
        }

        .coupon {
            margin-top: 15px;
        }

        .coupon input {
            padding: 11px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }


        /* ================= ABOUT ================= */

        .about {
            background: white;
            padding: 45px 20px;
            text-align: center;
        }

        .about h2 {
            color: #087f8c;
            margin-bottom: 15px;
        }

        .about p {
            max-width: 750px;
            margin: auto;
            line-height: 1.7;
        }


        /* ================= CONTACT ================= */

        .contact {
            padding: 40px 20px;
            text-align: center;
        }

        .contact h2 {
            color: #087f8c;
            margin-bottom: 20px;
        }

        .contact input,
        .contact textarea {
            width: 90%;
            max-width: 500px;
            padding: 12px;
            margin: 7px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .contact textarea {
            height: 100px;
        }


        /* ================= NEWSLETTER ================= */

        .newsletter {
            background: #087f8c;
            color: white;
            text-align: center;
            padding: 40px 20px;
        }

        .newsletter h2 {
            margin-bottom: 10px;
        }

        .newsletter input {
            padding: 12px;
            width: 250px;
            border: none;
            border-radius: 5px;
            margin-top: 15px;
        }


        /* ================= FOOTER ================= */

        footer {
            background: #055d66;
            color: white;
            text-align: center;
            padding: 25px;
        }

        footer p {
            margin: 5px;
        }


        /* ================= DARK MODE ================= */

        .dark {
            background: #1d1d1d;
            color: white;
        }

        .dark .product,
        .dark .search-box,
        .dark .about,
        .dark #cartItems,
        .dark .discount {
            background: #2c2c2c;
            color: white;
        }

        .dark .product p {
            color: #ddd;
        }


        /* ================= RESPONSIVE ================= */

        @media (max-width: 1000px) {

            .product-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 600px) {

            header {
                flex-direction: column;
                gap: 15px;
            }

            nav {
                text-align: center;
            }

            nav a {
                display: inline-block;
                margin: 5px;
            }

            .hero h1 {
                font-size: 30px;
            }

            .product-container {
                grid-template-columns: 1fr;
            }

            .search-box input {
                width: 90%;
            }

            .newsletter input {
                width: 90%;
            }
        }

    </style>

</head>


<body>


    <!-- ================= HEADER ================= -->

    <header>

        <div class="logo">
            🛍️ EasyShop
        </div>

        <nav>

            <a href="#home">Home</a>

            <a href="#products">Products</a>

            <a href="#cart">Cart 🛒</a>

            <a href="#about">About</a>

            <a href="#contact">Contact</a>

        </nav>

        <button class="dark-btn" onclick="darkMode()">
            🌙 Dark Mode
        </button>

    </header>



    <!-- ================= HERO ================= -->

    <section class="hero" id="home">

        <h1>Welcome to EasyShop 🛍️</h1>

        <p>
            Find everything you need at one place!
        </p>

        <button class="btn" onclick="goToProducts()">
            Shop Now
        </button>

    </section>



    <!-- ================= SEARCH ================= -->

    <section class="search-box">

        <input
            type="text"
            id="search"
            placeholder="🔍 Search products..."
            onkeyup="searchProducts()"
        >

    </section>



    <!-- ================= CATEGORIES ================= -->

    <section class="categories">

        <h2>Shop by Category</h2>

        <button class="category-btn" onclick="filterProducts('all')">
            All
        </button>

        <button class="category-btn" onclick="filterProducts('fashion')">
            👕 Fashion
        </button>

        <button class="category-btn" onclick="filterProducts('electronics')">
            🎧 Electronics
        </button>

        <button class="category-btn" onclick="filterProducts('accessories')">
            ⌚ Accessories
        </button>

        <button class="category-btn" onclick="filterProducts('home')">
            🏠 Home
        </button>

    </section>



    <!-- ================= PRODUCTS ================= -->

    <section class="products" id="products">

        <h2>🔥 Popular Products</h2>

        <div class="product-container">


            <!-- PRODUCT 1 -->

            <div class="product" data-category="fashion">

                <button class="wishlist"
                    onclick="addWishlist('T-Shirt')">
                    ♡
                </button>

                <div class="product-image">👕</div>

                <h3>T-Shirt</h3>

                <p>Comfortable cotton T-shirt.</p>

                <div class="rating">
                    ⭐⭐⭐⭐⭐
                </div>

                <div class="price">₹499</div>

                <button class="btn"
                    onclick="addToCart('T-Shirt',499)">
                    Add to Cart
                </button>

            </div>



            <!-- PRODUCT 2 -->

            <div class="product" data-category="fashion">

                <button class="wishlist"
                    onclick="addWishlist('Jeans')">
                    ♡
                </button>

                <div class="product-image">👖</div>

                <h3>Denim Jeans</h3>

                <p>Stylish blue denim jeans.</p>

                <div class="rating">
                    ⭐⭐⭐⭐☆
                </div>

                <div class="price">₹899</div>

                <button class="btn"
                    onclick="addToCart('Denim Jeans',899)">
                    Add to Cart
                </button>

            </div>



            <!-- PRODUCT 3 -->

            <div class="product" data-category="electronics">

                <button class="wishlist"
                    onclick="addWishlist('Headphones')">
                    ♡
                </button>

                <div class="product-image">🎧</div>

                <h3>Headphones</h3>

                <p>Wireless music headphones.</p>

                <div class="rating">
                    ⭐⭐⭐⭐⭐
                </div>

                <div class="price">₹799</div>

                <button class="btn"
                    onclick="addToCart('Headphones',799)">
                    Add to Cart
                </button>

            </div>



            <!-- PRODUCT 4 -->

            <div class="product" data-category="electronics">

                <button class="wishlist"
                    onclick="addWishlist('Smartphone')">
                    ♡
                </button>

                <div class="product-image">📱</div>

                <h3>Smartphone</h3>

                <p>Modern smartphone with great features.</p>

                <div class="rating">
                    ⭐⭐⭐⭐☆
                </div>

                <div class="price">₹14,999</div>

                <button class="btn"
                    onclick="addToCart('Smartphone',14999)">
                    Add to Cart
                </button>

            </div>



            <!-- PRODUCT 5 -->

            <div class="product" data-category="accessories">

                <button class="wishlist"
                    onclick="addWishlist('Smart Watch')">
                    ♡
                </button>

                <div class="product-image">⌚</div>

                <h3>Smart Watch</h3>

                <p>Smart watch for everyday use.</p>

                <div class="rating">
                    ⭐⭐⭐⭐⭐
                </div>

                <div class="price">₹1,499</div>

                <button class="btn"
                    onclick="addToCart('Smart Watch',1499)">
                    Add to Cart
                </button>

            </div>



            <!-- PRODUCT 6 -->

            <div class="product" data-category="accessories">

                <button class="wishlist"
                    onclick="addWishlist('Sunglasses')">
                    ♡
                </button>

                <div class="product-image">🕶️</div>

                <h3>Sunglasses</h3>

                <p>Stylish sunglasses for outdoors.</p>

                <div class="rating">
                    ⭐⭐⭐⭐☆
                </div>

                <div class="price">₹599</div>

                <button class="btn"
                    onclick="addToCart('Sunglasses',599)">
                    Add to Cart
                </button>

            </div>



            <!-- PRODUCT 7 -->

            <div class="product" data-category="home">

                <button class="wishlist"
                    onclick="addWishlist('Table Lamp')">
                    ♡
                </button>

                <div class="product-image">💡</div>

                <h3>Table Lamp</h3>

                <p>Beautiful lamp for your study table.</p>

                <div class="rating">
                    ⭐⭐⭐⭐⭐
                </div>

                <div class="price">₹699</div>

                <button class="btn"
                    onclick="addToCart('Table Lamp',699)">
                    Add to Cart
                </button>

            </div>



            <!-- PRODUCT 8 -->

            <div class="product" data-category="home">

                <button class="wishlist"
                    onclick="addWishlist('Coffee Mug')">
                    ♡
                </button>

                <div class="product-image">☕</div>

                <h3>Coffee Mug</h3>

                <p>Beautiful ceramic coffee mug.</p>

                <div class="rating">
                    ⭐⭐⭐⭐☆
                </div>

                <div class="price">₹299</div>

                <button class="btn"
                    onclick="addToCart('Coffee Mug',299)">
                    Add to Cart
                </button>

            </div>



            <!-- PRODUCT 9 -->

            <div class="product" data-category="electronics">

                <button class="wishlist"
                    onclick="addWishlist('Laptop')">
                    ♡
                </button>

                <div class="product-image">💻</div>

                <h3>Laptop</h3>

                <p>Fast laptop for study and work.</p>

                <div class="rating">
                    ⭐⭐⭐⭐⭐
                </div>

                <div class="price">₹49,999</div>

                <button class="btn"
                    onclick="addToCart('Laptop',49999)">
                    Add to Cart
                </button>

            </div>



            <!-- PRODUCT 10 -->

            <div class="product" data-category="fashion">

                <button class="wishlist"
                    onclick="addWishlist('Backpack')">
                    ♡
                </button>

                <div class="product-image">🎒</div>

                <h3>Backpack</h3>

                <p>Strong backpack for college and travel.</p>

                <div class="rating">
                    ⭐⭐⭐⭐☆
                </div>

                <div class="price">₹999</div>

                <button class="btn"
                    onclick="addToCart('Backpack',999)">
                    Add to Cart
                </button>

            </div>

        </div>

    </section>



    <!-- ================= DISCOUNT ================= -->

    <section class="discount">

        <h2>🎁 Get Extra Discount</h2>

        <p>
            Use coupon code <b>EASY10</b> to get ₹100 off!
        </p>

        <div class="coupon">

            <input
                type="text"
                id="coupon"
                placeholder="Enter coupon code"
            >

            <button class="btn" onclick="applyCoupon()">
                Apply
            </button>

        </div>

    </section>



    <!-- ================= CART ================= -->

    <section class="cart" id="cart">

        <h2>🛒 Your Shopping Cart</h2>

        <div id="cartItems">
            Your cart is empty.
        </div>

        <br>

        <h3 id="total">
            Total: ₹0
        </h3>

        <div class="cart-buttons">

            <button class="btn" onclick="checkout()">
                💳 Checkout
            </button>

            <button class="btn" onclick="clearCart()">
                🗑️ Clear Cart
            </button>

        </div>

    </section>



    <!-- ================= ABOUT ================= -->

    <section class="about" id="about">

        <h2>About EasyShop</h2>

        <p>
            EasyShop is a simple online shopping website created
            using HTML, CSS and JavaScript. It provides users with
            different products, product search, categories,
            shopping cart, wishlist, discounts and checkout.
        </p>

    </section>



    <!-- ================= CONTACT ================= -->

    <section class="contact" id="contact">

        <h2>📞 Contact Us</h2>

        <input
            type="text"
            placeholder="Your Name"
        >

        <br>

        <input
            type="email"
            placeholder="Your Email"
        >

        <br>

        <textarea
            placeholder="Write your message..."
        ></textarea>

        <br>

        <button class="btn" onclick="sendMessage()">
            Send Message
        </button>

    </section>



    <!-- ================= NEWSLETTER ================= -->

    <section class="newsletter">

        <h2>📧 Subscribe to Our Newsletter</h2>

        <p>
            Get updates about new products and offers.
        </p>

        <input
            type="email"
            id="email"
            placeholder="Enter your email"
        >

        <button class="btn" onclick="subscribe()">
            Subscribe
        </button>

    </section>



    <!-- ================= FOOTER ================= -->

    <footer>

        <p>
            © 2026 EasyShop
        </p>

        <p>
            HTML | CSS | JavaScript
        </p>

        <p>
            Final Web Development Project
        </p>

    </footer>



    <!-- ================= JAVASCRIPT ================= -->

    <script>

        /* ================= CART ================= */

        let cart = [];

        let total = 0;

        let discount = 0;


        function addToCart(name, price) {

            cart.push({
                name: name,
                price: price
            });

            calculateTotal();

            displayCart();

            alert(name + " added to cart! 🛒");
        }


        function displayCart() {

            let cartBox =
                document.getElementById("cartItems");

            if (cart.length === 0) {

                cartBox.innerHTML =
                    "Your cart is empty.";

                return;
            }

            let output = "";

            cart.forEach(function(item, index) {

                output +=
                    "<div class='cart-item'>" +

                    "<span>" +
                    item.name +
                    " - ₹" +
                    item.price +
                    "</span>" +

                    "<span>" +

                    "<button class='quantity-btn' " +
                    "onclick='removeItem(" +
                    index +
                    ")'>❌</button>" +

                    "</span>" +

                    "</div>";

            });

            cartBox.innerHTML = output;
        }


        function removeItem(index) {

            cart.splice(index, 1);

            calculateTotal();

            displayCart();
        }


        function calculateTotal() {

            total = 0;

            cart.forEach(function(item) {

                total += item.price;

            });

            let finalTotal = total - discount;

            if (finalTotal < 0) {
                finalTotal = 0;
            }

            document.getElementById("total").innerHTML =
                "Total: ₹" + finalTotal;
        }


        function clearCart() {

            cart = [];

            discount = 0;

            calculateTotal();

            displayCart();

            alert("Cart cleared!");
        }


        /* ================= CHECKOUT ================= */

        function checkout() {

            if (cart.length === 0) {

                alert("Your cart is empty!");

                return;
            }

            let finalTotal = total - discount;

            if (finalTotal < 0) {
                finalTotal = 0;
            }

            alert(
                "🎉 Order placed successfully!\n\n" +
                "Total Amount: ₹" +
                finalTotal +
                "\n\nThank you for shopping with EasyShop!"
            );

            cart = [];

            discount = 0;

            calculateTotal();

            displayCart();
        }


        /* ================= COUPON ================= */

        function applyCoupon() {

            let code =
                document.getElementById("coupon")
                .value
                .toUpperCase();

            if (code === "EASY10") {

                if (discount === 0) {

                    discount = 100;

                    alert(
                        "🎉 Coupon applied!\n₹100 discount added."
                    );

                    calculateTotal();

                } else {

                    alert(
                        "Coupon already applied."
                    );
                }

            } else {

                alert(
                    "❌ Invalid coupon code."
                );
            }
        }


        /* ================= SEARCH ================= */

        function searchProducts() {

            let search =
                document.getElementById("search")
                .value
                .toLowerCase();

            let products =
                document.querySelectorAll(".product");

            products.forEach(function(product) {

                let name =
                    product.querySelector("h3")
                    .innerText
                    .toLowerCase();

                if (name.includes(search)) {

                    product.style.display = "block";

                } else {

                    product.style.display = "none";

                }

            });
        }


        /* ================= CATEGORY FILTER ================= */

        function filterProducts(category) {

            let products =
                document.querySelectorAll(".product");

            products.forEach(function(product) {

                if (
                    category === "all" ||
                    product.dataset.category === category
                ) {

                    product.style.display = "block";

                } else {

                    product.style.display = "none";

                }

            });
        }


        /* ================= WISHLIST ================= */

        function addWishlist(name) {

            alert(
                "❤️ " +
                name +
                " added to your wishlist!"
            );
        }


        /* ================= DARK MODE ================= */

        function darkMode() {

            document.body.classList.toggle("dark");

        }


        /* ================= SHOP NOW ================= */

        function goToProducts() {

            document.getElementById("products")
                .scrollIntoView({
                    behavior: "smooth"
                });
        }


        /* ================= CONTACT ================= */

        function sendMessage() {

            alert(
                "✅ Thank you! Your message has been sent."
            );
        }


        /* ================= NEWSLETTER ================= */

        function subscribe() {

            let email =
                document.getElementById("email").value;

            if (email === "") {

                alert(
                    "Please enter your email."
                );

            } else {

                alert(
                    "🎉 You are successfully subscribed!"
                );

                document.getElementById("email").value = "";
            }
        }

    </script>

</body>

</html>
