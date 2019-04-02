<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.0/animate.min.css" />
    <style>
        * {
            margin: 0;
            padding: 0;
        }
        nav {
            width: 100%;
            background-color: black;
            padding-top: 20px;
            padding-bottom: 20px;
            display: flex;
            justify-content: center;
        }
        nav a {
            display: block;
            text-decoration: none;
            color: white;
            margin: 0 15px;
        }
        #about {
            height: 1200px;
            background-color: rgb(255, 174, 0);
        }
        #product {
            height: 1200px;
            background-color: rgb(238, 255, 0);
        }
        #service {
            height: 1200px;
            background-color: rgb(72, 255, 0);
        }
        #contact {
            height: 1200px;
            background-color: rgb(0, 247, 255);
        }
        #gotop {
            display: block;
            width: 50px;
            height: 50px;
            line-height: 60px;
            text-align: center;
            background: #00000052;
            color: white;
            text-decoration: none;
            position: fixed;
            right: 30px;
            bottom: 30px;
            z-index: 999;
        }
    </style>
</head>

<body>

    <nav>
        <a href="#" data-target="#about">About</a>
        <a href="#" data-target="#product">Product</a>
        <a href="#" data-target="#service">Service</a>
        <a href="#" data-target="#contact">Contact</a>
    </nav>
    <div id="about"></div>
    <div id="product"></div>
    <div id="service"></div>
    <div id="contact"></div>
    <a href="#" id="gotop">
        <h1>^</h1>
    </a>

    <script>
        $(document).ready(function () {
            $("nav a").click(function () {
                var target = $(this).attr("data-target");
                var top = $(target).offset().top;
                $("html,body").animate({
                    scrollTop: top
                })
            })
            $("#gotop").click(function () {
                $("html,body").animate({
                    scrollTop: 0
                })
            })
            $("#gotop").hide();
            $(window).scroll(function (e) {
                var scroll = $(window).scrollTop();
                if (scroll >= 1800) {
                    $("#gotop").show().removeClass().addClass("animated bounceInDown");
                } else {
                    $("#gotop").removeClass().addClass("animated bounceOutUp");
                }
            })
        })
    </script>
</body>

</html>
