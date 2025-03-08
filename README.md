<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Mother's Day</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: #ffcccc;
            margin: 0;
            overflow: hidden;
        }
        .dot {
            position: absolute;
            width: 10px;
            height: 10px;
            background-color: red;
            border-radius: 50%;
            animation: moveAlongHeart 4s linear forwards;
        }
        @keyframes moveAlongHeart {
            0% {
                transform: translate(0, 0);
            }
            20% {
                transform: translate(30px, -40px);
            }
            40% {
                transform: translate(60px, 0px);
            }
            60% {
                transform: translate(30px, 40px);
            }
            80% {
                transform: translate(0px, 20px);
            }
            100% {
                transform: translate(0px, 0px);
                opacity: 0;
            }
        }
        .heart {
            position: relative;
            width: 100px;
            height: 100px;
            background-color: red;
            transform: rotate(-45deg);
            display: none;
        }
        .heart::before,
        .heart::after {
            content: "";
            position: absolute;
            width: 100px;
            height: 100px;
            background-color: red;
            border-radius: 50%;
        }
        .heart::before {
            top: -50px;
            left: 0;
        }
        .heart::after {
            left: 50px;
            top: 0;
        }
        @keyframes showHeart {
            to { display: block; }
        }
    </style>
</head>
<body>
    <div class="dot"></div>
    <div class="heart" id="heart"></div>
    <script>
        setTimeout(() => {
            document.querySelector(".dot").style.display = "none";
            document.getElementById("heart").style.display = "block";
        }, 4000);
    </script>
</body>
</html>
