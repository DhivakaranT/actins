<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body{
            font-family: 'poppins',sans-serif;
            margin: 0;
        }
        .productcontainer{
            width: 900px;
            max-width: 90vw;
            margin: auto;
            text-align: center;
            padding-top: 10px;
        }
        svg{
            width: 30px;
        }
        header{
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 20px 0;
        }
        .header .icon-cart{
            position: relative;
        }
        .header .icon-cart span{
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
        .listProduct .item img{
            width: 90px;
            filter: drop-shadow(0 30px 30px #0009);
        }
        .listProduct{
            display: grid;
            grid-template-columns: repeat(4,1fr);
            gap:20px;
        }
        .listProduct .item{
            background-color: aliceblue;
            padding: 20px;
            border-radius: 20px;
        }
        .listProduct .item h2{
            font-weight: 500;
            font-size: large;
        }
        .listProduct .items .price{
            letter-spacing: 7px;
            font-size: small;
        }
        .listProduct .item button{
            background-color: black;
            color: #fff;
            padding: 5px 10px;
            border-radius: 20px;
            margin-top: 10px;
            border: none;
            cursor: pointer;
        }
        .cartTab{
            width: 400px;
            background-color: black;
            color: #fff;
            position: fixed;
            inset:0 0 0 auto;
            display: grid;
            grid-template-rows  :70px 1fr 70px; 
        }
        .cartTab h1{
            padding:20px;
            margin:0;
            font-weight: 300;
        }
        .cartTab .buyBtn{
            display: grid;
            grid-template-columns: repeat(2, 1fr);
        }
        .cartTab .buyBtn button{
            background-color: orangered;
            border: none;
            font-family: poppins;
            font-weight: 500;
            cursor: pointer;
        }
        .cartTab .listCart .item img{
            width: 100%;
        }
        .cartTab .listCart .item{
            display: grid;
            grid-template-columns: 70px 150px 50px 1fr;
            gap: 10px;
            text-align: center;
            align-items: center;
        }
        .listCart .quantity span{
            display:inline-block;
            width: 25px;
            height: 25px;
            background-color: #fff;
            color: black;
            border-radius: 40px;
            cursor: pointer;
        }
        .listCart .quantity span:nth-child(2){
            background-color: transparent;
            color: #fff;
        }
        .listCart .item{

        }






    </style>
</head>
<body>
    <div class="productcontainer">
        <header>
            <div class="title">PRODUCTS LIST</div>
            <div class="icon-card"></div>
            <svg aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" viewBox="0 0 24 24">
                <path fill-rule="evenodd" d="M4 4a1 1 0 0 1 1-1h1.5a1 1 0 0 1 .979.796L7.939 6H19a1 1 0 0 1 .979 1.204l-1.25 6a1 1 0 0 1-.979.796H9.605l.208 1H17a3 3 0 1 1-2.83 2h-2.34a3 3 0 1 1-4.009-1.76L5.686 5H5a1 1 0 0 1-1-1Z" clip-rule="evenodd"/>
              </svg>
              <span>0</span>
              
        </header>
        <div class="listProduct">
            <div class="item">
                <img src="images/globe.png" alt="">
                <h2> Product Name 1</h2>
                <div class="price">$000</div>
                <button class="addcart">
                    Add To Cart
                </button>
            </div>
        </div>
    </div>
    <div class="cartTab">
        <h1>Shopping cart</h1>
        <div class="listCart">
            <div class="item">
                <div class="image">
                    <img src="" alt="">
                </div>
                <div class="name">
                    NAME
                </div>
                <div class="totalPrice">
                    $000
                </div>
                <div class="quantity">
                    <span class="minus">-</span>
                    <span>1</span>
                    <span class="plus">+</span>
                </div>
            </div>

        </div>
        <div class="buyBtn">
            <button class="close">CLOSE</button>
            <button class="buy">BUY</button>
        </div>
    </div>
    
</body>
</html>
