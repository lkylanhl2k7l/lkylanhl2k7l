<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Heart Animation</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #282c34;
            margin: 0;
        }
        .heart {
            position: relative;
            width: 100px;
            height: 100px;
            background-color: red;
            transform: rotate(-45deg);
            animation: sparkle 1.5s infinite;
        }
        .heart:before, .heart:after {
            content: '';
            position: absolute;
            width: 100px;
            height: 100px;
            background-color: red;
            border-radius: 50%;
        }
        .heart:before {
            top: -50px;
            left: 0;
        }
        .heart:after {
            left: 50px;
            top: 0;
        }
        @keyframes sparkle {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.1);
            }
        }
    </style>
</head>
<body>
    <div class="heart"></div>
</body>
</html>
