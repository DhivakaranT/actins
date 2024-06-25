<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Products</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">

    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
        }
        .navbar {
            background-color: rgb(112, 102, 102);
            width: 100%;
            height: 75px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            position: fixed;
            top: 0;
            left: 0;
            z-index: 1000;
        }

        .logo {
            border-radius: 8%;
            height: 78px;
            width: 160px;
            margin-top: 0%;
            padding: auto;
        }

        .menu ul {
            display: flex;
            list-style-type: none;
            margin: 0;
            padding: 0;
        }

        .menu ul li {
            position: relative;
            margin-left: 20px;
        }

        .menu ul li a {
            text-decoration: none;
            color: rgb(14, 13, 13);
            padding: 10px 15px;
            transition: background-color 0.3s, color 0.3s;
        }

        .menu ul li a:hover {
            background-color: rgba(255, 255, 255, 0.2);
            color: orange;
        }

        .dropdown-menu {
            display: none;
            position: absolute;
            top: 100%;
            left: 0;
            background-color: rgb(112, 102, 102);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
            z-index: 1;
            list-style-type: none;
            padding: 0;
            margin: 0;
            width: 160px;
        }

        .dropdown-menu li {
            opacity: 0;
            transition: opacity 0.5s;
        }

        .dropdown-menu li a {
            padding: 12px 16px;
            text-decoration: none;
            display: block;
            color: rgb(14, 13, 13);
            background-color: rgb(112, 102, 102);
        }

        .dropdown-menu li a:hover {
            background-color: rgba(255, 255, 255, 0.2);
            color: orange;
        }

        /* Show dropdown menu on click */
        .dropdown:hover .dropdown-menu {
            display: block;
        }

        .dropdown-menu.show li {
            opacity: 1;
        }

        .menu ul {
            list-style-type: none;
            padding: 0;
            margin: 0;
        }

        .menu ul li {
            display: inline-block;
            position: relative;
        }

        .menu ul li a {
            text-decoration: none;
            padding: 10px 15px;
            display: block;
            color: #000;
        }

        .menu ul li .dropdown-content {
            display: none;
            position: absolute;
            background-color: #f8f6f4;
            box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.2);
            min-width: 150px;
            z-index: 1;
            top: 100%;
            left: 0;
        }

        .menu ul li .dropdown-content li {
            display: block;
        }

        .menu ul li .dropdown-content li a {
            padding: 10px 15px;
            color: orangered;
        }

        .menu ul li .dropdown-content li a:hover {
            background-color: #0c0c0c;
        }

        .menu ul li.dropdown:hover .dropdown-content {
            display: block;
        }

        .productcontainer {
            background-color: #f0a500;
            width: 1200px;
            max-width: 90vw;
            margin: auto;
            text-align: center;
            padding-top: 10px;
        }
        .productcontainer .title {
            margin-top: 5%;
            text-align: center;
            padding-top: 30px;
            font-size: 20px;
        }
        svg {
            width: 30px;
        }
        header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 20px 0;
        }
        .header .icon-cart {
            position: relative;
        }
        .header .icon-cart span {
            display: flex;
            width: 30px;
            height: 30px;
            background-color: red;
            justify-content: center;
            align-items: center;
            color: #fff;
            border-radius: 50%;
            position: absolute;
            top: 50%;
            right: 20px;
        }
        .listProduct {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        .listProduct .item {
            background-color: aliceblue;
            padding: 20px;
            border-radius: 20px;
            text-align: center;
        }
        .listProduct .item img {
            width: 90px;
            filter: drop-shadow(0 30px 30px #0009);
        }
        .listProduct .item h2 {
            font-weight: 500;
            font-size: large;
        }
        .listProduct .item .price {
            letter-spacing: 1px; /* Adjust as needed */
            font-size: small;
            margin-top: 10px;
        }
        footer {
            margin-top: 5%;
            background: url('images/footerImg.png') no-repeat center center/cover;
            color: white;
            padding: 40px 0;
            text-align: center;
        }

        .footer-container {
            color: black;
            margin-top: 0%;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            max-width: max-content;
            margin: 0 auto;
            text-align: left; 
            font-family: 'Times New Roman', Times, serif;
        }

        .footer-column {
            flex: 1;
            min-width: 250px;
            padding: 20px;
            margin-top: 260px;
        }

        .iconImg {
            margin-bottom: 0px;
            margin-right: 88.5%;
            margin-left: 0%;
            width: 150px;
            height: 70px;
        }

        .icon-text {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
        }

        .icon-text i {
            margin-right: 10px;
            font-size: 1.5em;
        }

        .icon-text h4 {
            margin: 0;
            font-size: 1.2em;
        }

        .companyAddress {
            text-align: left;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .footer-column h3 {
            margin-top: 0;
            font-size: 1.5em;
            margin-bottom: 20px;
        }

        .footer-column ul {
            list-style: none;
            padding: 0;
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column ul li a {
            color: rgb(14, 13, 13);
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-column ul li a:hover {
            color: #f0a500;
        }

        .social-icons a {
            margin: 0 10px;
            color: white;
            text-decoration: none;
            font-size: 1.5em;
            transition: color 0.3s;
        }

        .social-icons a:hover {
            color: #f0a500;
        }

        .footer-bottom {
            margin-top: 10%;
            padding: 20px 0;
            background-color: rgba(26, 37, 47, 0.9);
            color: #ccc;
            font-size: 0.9em;
            position: relative;
            z-index: 1;
        }

        @media (max-width: 768px) {
            .footer-column {
                flex: 1 1 100%;
                text-align: center;
            }

            .icon-text {
                justify-content: center;
            }

            .companyAddress {
                text-align: center;
            }
        }

        .email-link {
            color: rgb(0, 0, 0);
            text-decoration: underline;
            transition: color 0.3s;
        }

        .email-link:hover {
            color: #f0a500;
        }

        .footerlogo {
            border-radius: 8%;
            height: 78px;
            width: 160px;
            margin-top: 5%;
            padding: auto;
        }
    </style>
</head>
<body>
    <div class="navbar">
        <a href="home.html"><img src="images/logo.png" alt="Logo" class="logo"></a>
        <div class="menu">
            <ul>
                <li><a href="home.html">Home</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="services.html">Services</a></li>
                <li><a href="products.html">Products</a></li>
                <li><a href="blog.html">Blog</a></li>
                <li><a href="contact.html">Contact</a></li>
                <li class="dropdown">
                    <a href="javascript:void(0)">More</a>
                    <ul class="dropdown-menu">
                        <li><a href="privacy.html">Privacy Policy</a></li>
                        <li><a href="terms.html">Terms of Service</a></li>
                        <li><a href="faq.html">FAQ</a></li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>
    <div class="productcontainer">
        <div class="title">
            <header>
                <h1>Products</h1>
                <div class="icon-cart">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="black">
                        <path d="M10 18a2 2 0 100 4 2 2 0 000-4zM18 18a2 2 0 100 4 2 2 0 000-4zM6.217 4l.996 2h13.538l-2.146 7H8.145l-.496 2h9.17a1 1 0 110 2H6.217a1 1 0 01-.97-1.243l1.96-7L4 4H2a1 1 0 110-2h3.217a1 1 0 01.97.757z"/>
                    </svg>
                    <span>3</span>
                </div>
            </header>
        </div>
        <div class="listProduct">
            <div class="item">
                <img src="images/product1.png" alt="Product Image">
                <h2 class="product-name">Milk Cream</h2>
                <p class="price">₹50</p>
            </div>
            <div class="item">
                <img src="images/product2.png" alt="Product Image">
                <h2 class="product-name">Milk Bread</h2>
                <p class="price">₹30</p>
            </div>
            <div class="item">
                <img src="images/product3.png" alt="Product Image">
                <h2 class="product-name">Bun</h2>
                <p class="price">₹25</p>
            </div>
        </div>
    </div>
    <footer>
        <div class="footer-container">
            <div class="footer-column">
                <img src="images/footerlogo.png" alt="Logo" class="footerlogo">
                <div class="companyAddress">
                    <h3>Our Address</h3>
                    <p>123 Main Street,<br> Cityville, ST 12345</p>
                </div>
            </div>
            <div class="footer-column">
                <div class="icon-text">
                    <i class="fas fa-phone-alt"></i>
                    <h4>Phone</h4>
                </div>
                <p><a href="tel:+1234567890" class="email-link">+1 (234) 567-890</a></p>
                <div class="icon-text">
                    <i class="fas fa-envelope"></i>
                    <h4>Email</h4>
                </div>
                <p><a href="mailto:info@company.com" class="email-link">info@company.com</a></p>
            </div>
            <div class="footer-column">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="home.html">Home</a></li>
                    <li><a href="about.html">About</a></li>
                    <li><a href="services.html">Services</a></li>
                    <li><a href="products.html">Products</a></li>
                    <li><a href="contact.html">Contact</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Follow Us</h3>
                <div class="social-icons">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-linkedin-in"></i></a>
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2023 Company Name. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
