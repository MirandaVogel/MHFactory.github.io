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
            background: linear-gradient(#703575, #e667a0);
            color: #333;
        }
        /* Miranda Top Box */
        header {
            background: #4a5587 ;
            color: #fff;
            padding: 1rem 0;
            text-align: center;
            border-top-left-radius: 10px;
            border-top-right-radius: 10px;
        }
        /* Long box below Miranda V */
        nav {
            display: flex;
            justify-content: center;
            background: #fcbd84;
        }

        /* Common styles for all boxes */
        .box1, .box2, .box3, .box4 {
            color: #fff;
            padding: 1rem;
            text-decoration: none;
            text-transform: uppercase;
            display: inline-block;
            background-color: #4a5587;
            margin: 5px;
            border-radius: 10px;
        }

        /* Hover effect */
        .box1:hover, .box2:hover, .box3:hover, .box4:hover {
            background: #9abae1;
        }
        
        /*Big box below options*/
        .container {
            background: #4a5587;
            max-width: 1400px;
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
            justify-content: center; /* This will center the cards in the available space */
        }

        .card {
            background: #fff;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            flex: 1 1 calc(33.333% - 1rem); /* Each card takes up about one-third of the row */
            max-width: 300px; /* Maximum width for each card */
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
                align-items: center; /* Center the cards when stacked vertically */
                
            }
            .card {
                flex: 1 1 100%; /* Make each card take up the full width on smaller screens */
                max-width: 90%; /* Ensure some padding around the cards */
            }
        }
        @media (min-width: 769px) and (max-width: 1024px) {
            .card {
                flex: 1 1 calc(50% - 1rem); /* Make each card take up half the width on medium screens */
            }
        }
    </style>
</head>

<body>
    <header>
        <h1>Miranda Vogel</h1>
    </header>

    <nav>
        <a href="#Research" class="box1">Research</a>
        <a href="#About" class="box2">About</a>
        <a href="#Services" class="box3">Services</a>
        <a href="#Contact" class="box4">Contact</a>
    </nav>

    <section class="hero">
        <div>
            <h1>Welcome to My Website</h1>
        </div>
    </section>

    <div class="container">
        <section class="content">
            <div class="card">
                <img src="https://via.placeholder.com/300" alt="Placeholder Image">
                <h2 id="Research">Research Box</h2>
                <p>Description of research goes here.</p>
            </div>

            <div class="card">
                <img src="https://via.placeholder.com/300" alt="Placeholder Image">
                <h2 id="About">About Box</h2>
                <p>Description of about goes here.</p>
            </div>

            <div class="card">
                <img src="https://via.placeholder.com/300" alt="Placeholder Image">
                <h2 id="Services">Services Box</h2>
                <p>Description of services goes here.</p>
            </div>
        </section>
    </div>

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
                element.style.borderRadius = `${topLeft}px ${topRight}px ${bottomRight}px ${bottomLeft}px`;
            }
        }

        /* Apply to each box independently */
        applyRandomBorderRadius('.box1');
        applyRandomBorderRadius('.box2');
        applyRandomBorderRadius('.box3');
        applyRandomBorderRadius('.box4');
    </script>
    <script>
        // Easing function for smooth start fast and slow end
        function easeInOutQuad(t) {
            return t < 0.5 ? 2 * t * t : -1 + (4 - 2 * t) * t;
        }

        // Custom smooth scrolling function
        function customSmoothScroll(targetElement, duration) {
            var targetPosition = targetElement.getBoundingClientRect().top + window.pageYOffset;
            var startPosition = window.pageYOffset;
            var startTime = null;

            function animation(currentTime) {
                if (startTime === null) startTime = currentTime;
                var timeElapsed = currentTime - startTime;
                var run = easeInOutQuad(timeElapsed / duration) * (targetPosition - startPosition) + startPosition;
                window.scrollTo(0, run);
                if (timeElapsed < duration) {
                    requestAnimationFrame(animation);
                }
            }

            requestAnimationFrame(animation);
        }

        document.querySelectorAll('nav a').forEach(link => {
            link.addEventListener('click', function(event) {
                event.preventDefault(); // Prevent default anchor behavior
                var targetElement = document.querySelector(this.getAttribute('href'));
                customSmoothScroll(targetElement, 1000); // Scroll with 1 second duration
            });
        });
    </script>
    
    <div style="height: 200px;"></div>

    <footer>
        <p>&copy; 2024 My Website. All rights reserved. Just kidding.</p>
    </footer>
</body>

</html>
