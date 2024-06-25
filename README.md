<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Products</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">

    <style>
        body {
            font-family: 'poppins', sans-serif;
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
            
            max-width:max-content;
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
            width: 25px;
            margin-top: 30px;
        }

        .partnerLogo {
            width: 250px;
        }
        .productDetails{
            margin-left: 0px;
            margin-right: 0px;
            display: flex;
            justify-content: space-around;
            align-items: stretch;
            gap: 0px;
        }

        .listProduct {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    padding: 20px;
}

.listProduct .item {
    background-color: #ffffff;
    padding: 20px;
    border-radius: 10px;
    text-align: center;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease-in-out;
}

.listProduct .item img {
    width: 100%; /* Ensure images fill their containers */
    max-width: 100%; /* Prevent images from exceeding their container width */
    border-radius: 10px;
    margin-bottom: 15px;
}

.listProduct .item h2 {
    font-weight: 500;
    font-size: 18px;
    margin-bottom: 10px;
}

.listProduct .item .price {
    font-size: 16px;
    color: #666666;
}

.listProduct .item:hover {
    transform: translateY(-5px); /* Add hover effect */
    box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.2);
}


.productcontainer {
    text-align: center; /* Center align content within the product container */
}

.product-name {
    margin-bottom: 20px; /* Adjust spacing as needed */
}

.product-name h4 {
    font-weight: bold;
    font-size: 24px; /* Adjust font size as needed */
    color: #000000; /* Black color for the text */
}


        
    </style>
</head>
<body>
    <div class="navbar">
        <div class="icon">
            <img src="images/octinsLogo.png" class="logo" alt="Main Logo">
        </div>
        <div class="menu">
            <ul>
                <li><a href="index.html">Home</a></li>
                <li class="dropdown">
                    <a href="#">About</a>
                    <ul class="dropdown-content">
                        <li><a href="ourCompany.html">Our Company</a></li>
                        <li><a href="vision.html">Vision</a></li>
                        <li><a href="passion.html">Passion</a></li>
                        <li><a href="ourJourney.html">Our Journey</a></li>
                    </ul>
                </li>
                <li><a href="product.html">Products</a></li>
                <li><a href="services.html">Services</a></li>
                <li><a href="contactUs.html">Contact Us</a></li>
            </ul>
        </div>
    </div>

   
        <div class="productcontainer">
            <header>
                <div class="title">PRODUCTS LIST</div>
            </header>
            <div class="productcontainer">
                <header>
                    <div class="title">PRODUCTS LIST</div>
                </header>
                <div class="listProduct">
                    <div class="product-name">
                        <h4>Product name</h4>
                    </div>
                    <div class="item">
                        <img src="images/batteryOperatedUlt.PNG" alt="Product 1">
                    </div>
                    <div class="item">
                        <img src="images/batteryOperatedUlt.PNG" alt="Product 2">
                    </div>
                    <div class="item">
                        <img src="images/batteryOperatedUlt.PNG" alt="Product 3">
                    </div>
                    <div class="item">
                        <img src="images/batteryOperatedUlt.PNG" alt="Product 4">
                    </div>
                </div>
            </div>
            
        </div>
        
        
    </div>
    
    <footer>
        
        <div class="footer-container">
            <div class="footer-column">
                <div class="icon-text">
                    <i class="fas fa-map-marker-alt"></i>
                    <h4>USA</h4>
                </div>
                <p class="companyAddress">
                    Octothorp Integrated Solutions, LLC<br>
                    9060 Brockhamway<br>
                    Alpharetta<br>
                    Georgia<br>
                    30022<br>
                    <a href="mailto:contact@octothorp.com" class="email-link">contact@octothorp.com</a>
                </p>
                
            </div>
            <div class="footer-column">
                <!--<h3>Partners</h3>*
                <img src="images/partnerLogo.png" class="partnerLogo" alt="Partner Logo">-->
                <div class="icon-text">
                    <i class="fas fa-map-marker-alt"></i>
                    <h4>INDIA</h4>
                </div>
                <p class="companyAddress">
                    Octothorp Integrated Solutions<br>
                    1st Floor, Dhwarco Ministar,<br>
                    Plot No 12C/1, 3rd Cross Street,<br>
                    South Phase Industrial Estate,<br>
                    Guindy, Chennai, TN-600032<br>
                    <a href="mailto:Indsales@octins.com" class="email-link">Indsales@octins.com</a>
                </p>
            </div>
            <div class="footer-column">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="index.html">Home</a></li>
                    <li><a href="ourCompany.html">About Us</a></li>
                    <li><a href="product.html">Products</a></li>
                    <li><a href="services.html">Services</a></li>
                </ul>
            </div>
            <div class="footer-column">
                <h3>Contact Us</h3>
                <p>+91 9789063630</p>
                <p><a href="mailto:Indsales@octins.com" class="email-link">Indsales@octins.com</a></p>
                <div class="social-icons">
                    <a href="#" aria-label="Facebook"><img src="images/facebookLogo.png" class="footerlogo" alt="Facebook"></a>
                    <a href="#" aria-label="Twitter"><img src="images/twitterLogo.png" class="footerlogo" alt="Twitter"></a>
                    <a href="https://www.linkedin.com/company/octins/?originalSubdomain=in" aria-label="LinkedIn"><img src="images/linkedInLogo.png" class="footerlogo" alt="LinkedIn"></a>
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            &copy; 2024 Octothorp. All rights reserved.
        </div>
    </footer>
</body>
</html>
