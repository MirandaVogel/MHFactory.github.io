<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern Website</title>
    <style>
        /* Basic Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        /* Background */
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: #703575;
            color: #333;
        }
        /* Miranda Top Box */
        header {
            background: #4a5587 ;
            color: #fff;
            padding: 1rem 0;
            text-align: center;
            border-top-left-radius: 10px;  /* Rounds the top-left corner */
            border-top-right-radius: 10px; /* Rounds the top-right corner */
        }
        /* Long box bellow Miranda V*/
        nav {
            display: flex;
            justify-content: center;
            background: #fcbd84;
        }
        /*Text in Box 1*/
        .box1 {
            color: #fff;
            padding: 1rem;
            text-decoration: none;
            text-transform: uppercase;
            var randomNumber = getRandomNumber(10, 40);
            borderRadius: randomNumber + 'px';/* Adds rounded corners */
        }
        /*Text in Box 2*/
        .box2 {
            color: #fff;
            padding: 1rem;
            text-decoration: none;
            text-transform: uppercase;
            var randomNumber = getRandomNumber(10, 40);
            borderRadius: randomNumber + 'px';/* Adds rounded corners */
        }
        /*Text in Box 3*/
        .box3 {
            color: #fff;
            padding: 1rem;
            text-decoration: none;
            text-transform: uppercase;
            var randomNumber = getRandomNumber(10, 40);
            borderRadius: randomNumber + 'px';/* Adds rounded corners */
        }
        /*Text in Box 4*/
        .box4 {
            color: #fff;
            padding: 1rem;
            text-decoration: none;
            text-transform: uppercase;
            var randomNumber = getRandomNumber(10, 40);
            borderRadius: randomNumber + 'px';/* Adds rounded corners */
        }
        /* Color for when hover on button */
        .box1:hover, .box2:hover, .box3:hover, .box4:hover   {
            background: #9abae1;
        }

        /*Big box bellow options*/
        .container {
            background: #4a5587;
            max-width: 1200px;
            margin: 0 auto;
            padding: 1rem;
        }

        .hero {
            background: url('https://via.placeholder.com/1200x400') no-repeat center center/cover;
            color: #fff;
            height: 400px;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        .hero h1 {
            font-size: 3rem;
        }

        .hero p {
            font-size: 1.5rem;
        }

        .content {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .card {
            background: #fff;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            flex: 1;
            min-width: 300px;
            padding: 1rem;
            text-align: center;
        }

        .card img {
            max-width: 100%;
            border-radius: 10px;
        }

        footer {
            background: #333;
            color: #fff;
            text-align: center;
            padding: 1rem 0;
            margin-top: 2rem;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1.2rem;
            }

            .content {
                flex-direction: column;
            }
        }
    </style>
</head>

<body>
    <header>
        <h1>Miranda Vogel</h1>
    </header>

    <nav>
        <a href="#" class="box1">Home</a>
        <a href="#" class="box2">About</a>
        <a href="#" class="box3">Services</a>
        <a href="#" class="box4">Contact</a>
    </nav>

    <script>
        /* Function to generate a random number between min and max */
        function getRandomNumber(min, max) {
            return Math.floor(Math.random() * (max - min + 1)) + min;
        }

        /* Apply random border-radius to each corner of each box */
        function applyRandomBorderRadius(selector) {
            var element = document.querySelector(selector);
            if (element) {
                var topLeft = getRandomNumber(10, 40);
                var topRight = getRandomNumber(10, 40);
                var bottomRight = getRandomNumber(10, 40);
                var bottomLeft = getRandomNumber(10, 40);
                element.style.borderRadius = `${topLeft}px ${topRight}px ${bottomRight}px                     ${bottomLeft}px`; 
            }
        }

        /* Apply to each box independently */
        applyRandomBorderRadius('.box1');
        applyRandomBorderRadius('.box2');
        applyRandomBorderRadius('.box3');
        applyRandomBorderRadius('.box4');
    </script>
    
    <section class="hero">
        <div>
            <h1>Your Adventure Awaits</h1>
        </div>
    </section>

    <div class="container">
        <section class="content">
            <div class="card">
                <img src="https://via.placeholder.com/300" alt="Placeholder Image">
                <h2>Destination 1</h2>
                <p>Explore the beautiful scenery and rich culture.</p>
            </div>

            <div class="card">
                <img src="https://via.placeholder.com/300" alt="Placeholder Image">
                <h2>Destination 2</h2>
                <p>Discover the hidden gems of this location.</p>
            </div>

            <div class="card">
                <img src="https://via.placeholder.com/300" alt="Placeholder Image">
                <h2>Destination 3</h2>
                <p>Experience the adventure of a lifetime.</p>
            </div>
        </section>
    </div>

    <footer>
        <p>&copy; 2024 My Website. All rights reserved. Just kidding.</p>
    </footer>
</body>

</html>

