# RestaurantTemplete

<html>
    <head>
        <title>Restaurant Website</title>
        <link rel="stylesheet" href="style.css">
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" integrity="sha512-Fo3rlrZj/k7ujTnHg4CGR2D7kSs0v4LLanw2qksYuRlEzO+tcaEPQogQ0KaoGN26/zrn20ImR1DfuLWnOo7aBA==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    </head>
    <body>
        <div class="top">
            <div class="logo">A M H</div>
            <div class="nav">
                <a href="#">Home</a>
                <a href="#">Menu</a>
                <a href="#">About</a>
                <a href="#">Location</a>
                <a href="#">Contact</a>
            </div>
            <div class="search">
                <i class="fa-solid fa-search"></i>
                <i class="fa-solid fa-bars"></i>
            </div>
        </div>

        <div class="heading">
            <div class="left">
                <p>Are You Hungry?</p>
                <h1>Don't Wait</h1>
                <p>Let start to order food now</p>

                <button>Check out Menu</button>
            </div>

            <div class="right" id="food"></div>

            <div class="SocialMedia">
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-instagram"></i>
                <i class="fa-brands fa-whatsapp"></i>
            </div>
        </div>

        <div class="bottom">
            <div class="menu">
                <div id="food1"></div>
                <div id="food2"></div>
            </div>
        </div>


        <script src="javascript.js"></script>
    </body>
</html>


*{
    padding:0;
    margin:0;
}
body{
    width: 99%;
    height: 97%;
    background-image: url('Background2.png');
    background-size:cover;
}
.top{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    height: 80px;
    align-items:center;
    padding:0px 40px;
}
.logo{
    font-size: 30px;
    color:orange;
}
.nav{
    position: relative;
    left:-180px;
}
a{
    padding:5px 15px;
    color:orange;
    font-size: 20px;
    text-decoration:none;
}
a:hover{
    color:white;
    text-decoration: underline;
    text-underline-position:under;
}
.search{
    font-size: 25px;
}
.search i{
    padding:5px 20px;
}
/************heading**************/
.heading{
    display: flex;
    justify-content: space-evenly;
    padding-top:65px;
    align-items:center;
}
.right{
    width: 440px;
    height: 440px;
    background-image: url('food.jpg');
    background-size:cover;
    border-radius: 400px;
    display: flex;
    justify-content: center;
    align-items:center;
}
.right::before{
    width: 430px;
    height: 430px;
    border:2px solid white;
    content: '';
    position: absolute;
    border-radius: 430px;
    padding:10px;
}

/**********left************/
.left p:nth-child(1){
    color: white;
    font-size: 30px;
    letter-spacing: 1px;
    font-style: italic;
}
.left h1{
    font-size: 90px;
    color:white;
}
.left p:nth-child(3){
    color: orange;
    font-size: 30px;
    font-style: italic;
}
.left button{
    width: 150px;
    height: 30px;
    font-size: 15px;
    border-radius: 20px;
    border:2px solid white;
    background-color:transparent;
    color:white;
    margin:20px 0px;
}
/*********SocialMedia***************/
.SocialMedia{
    position: absolute;
    right: 0;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    flex-direction: column;
    width: 40px;
    height: 200px;
    background-color:white;
    font-size: 25px;

}
.SocialMedia i:hover {
    color:orange;
}


/***************bottom***************/
#food1,#food2{
    background-size:cover;
    width: 100px;
    height: 100px;
    border-radius: 100px;
    margin:0px 20px;
}
#food1{
    background-image: url('food1.png');
}
#food2{
    background-image: url('food.jpg');
}
.menu{
    display: flex;
    margin:0px 100px;
}




let food1s = document.getElementById('food1');
let food2s = document.getElementById('food2');
let foods = document.getElementById('food');

food1s.addEventListener('click',()=>{
    foods.style.backgroundImage="url('food1.png')";
})

food2s.addEventListener('click',()=>{
    foods.style.backgroundImage="url('food.jpg')";
})
