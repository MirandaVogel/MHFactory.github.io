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

        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: #d2f4ff;
            color: #333;
        }

        header {
            background: #9abae1;
            color: #fff;
            padding: 1rem 0;
            text-align: center;
        }

        nav {
            display: flex;
            justify-content: center;
            background: #444;
        }

        nav a {
            color: #fff;
            padding: 1rem;
            text-decoration: none;
            text-transform: uppercase;
        }

        nav a:hover {
            background: #555;
        }

        .container {
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
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Services</a>
        <a href="#">Contact</a>
    </nav>
    <section id="home">
    <h2>Home Section</h2>
    <p>Welcome to the home section.</p>
    
    </section>
    
    <section id="about">
        <h2>About Section</h2>
        <p>Learn more about us here.</p>
    </section>
    
    <section id="services">
        <h2>Services Section</h2>
        <p>Discover our services.</p>
    </section>
    
    <section id="contact">
        <h2>Contact Section</h2>
        <p>Get in touch with us.</p>
    </section>
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
        <p>&copy; 2024 My Website. All rights reserved.</p>
    </footer>
</body>

</html>
