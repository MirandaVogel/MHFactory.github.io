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
            background-color: #c2edff;
            color: #333;
        }
        /* Miranda Top Box */
        header {
            background: #4a5587 ;
            color: #fff;
            padding: 1rem 0;
            text-align: center;
        }
        /* Long box bellow Miranda V*/
        nav {
            display: flex;
            justify-content: center;
            background: #fcbd84;
        }

        nav a {
            color: #fff;
            padding: 1rem;
            text-decoration: none;
            text-transform: uppercase;
        }
        /* Color for when hover on button */
        nav a:hover {
            background: #9abae1;
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
        <a href="https://mirandavogel.github.io/MHFactory.github.io/" target="_blank">Home</a>
        <a href="https://mirandavogel.github.io/MHFactory.github.io/about" target="_blank">About</a>
        <a href="https://mirandavogel.github.io/MHFactory.github.io/services" target="_blank">Services</a>
        <a href="https://mirandavogel.github.io/MHFactory.github.io/contact" target="_blank">Contact</a>
    </nav>

    
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
