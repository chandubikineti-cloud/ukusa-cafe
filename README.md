<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ukusa Cafe - Jubilee Hills</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #8B4513 0%, #D2691E 100%);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .logo {
            font-size: 2rem;
            font-weight: bold;
            text-decoration: none;
            color: white;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #FFD700;
        }

        /* Hero Section */
        .hero {
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><rect fill="%23f8d7a8" width="1200" height="600"/><circle fill="%23D2691E" cx="200" cy="150" r="80"/><circle fill="%238B4513" cx="1000" cy="200" r="60"/><rect fill="%23A0522D" x="800" y="300" width="150" height="80" rx="10"/></svg>') center/cover;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 80px;
            position: relative;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0,0,0,0.4);
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            padding: 0 2rem;
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.5);
        }

        .cta-button {
            display: inline-block;
            background: #D2691E;
            color: white;
            padding: 1rem 2rem;
            text-decoration: none;
            border-radius: 50px;
            font-size: 1.2rem;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        .cta-button:hover {
            background: #B8860B;
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0,0,0,0.3);
        }

        /* Sections */
        section {
            padding: 5rem 0;
            max-width: 1200px;
            margin: 0 auto;
            padding-left: 2rem;
            padding-right: 2rem;
        }

        h2 {
            text-align: center;
            font-size: 3rem;
            margin-bottom: 3rem;
            color: #8B4513;
        }

        /* About */
        .about {
            background: #FFF8DC;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-text p {
            font-size: 1.2rem;
            margin-bottom: 1.5rem;
            text-align: justify;
        }

        .about-image {
            text-align: center;
        }

        .about-image img {
            max-width: 100%;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        /* Menu */
        .menu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .menu-item {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            text-align: center;
            transition: transform 0.3s;
        }

        .menu-item:hover {
            transform: translateY(-10px);
        }

        .menu-item h3 {
            color: #8B4513;
            margin-bottom: 1rem;
        }

        .price {
            font-size: 1.5rem;
            font-weight: bold;
            color: #D2691E;
            margin: 1rem 0;
        }

        /* Location */
        .location {
            background: #f4f4f4;
            text-align: center;
        }

        .location-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .map-placeholder {
            background: #e0e0e0;
            height: 300px;
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            color: #666;
        }

        /* Contact */
        .contact {
            background: #8B4513;
            color: white;
        }

        .contact-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
            text-align: center;
        }

        .contact-item h3 {
            margin-bottom: 1rem;
            color: #FFD700;
        }

        /* Footer */
        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .about-content,
            .location-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            section {
                padding: 3rem 1rem;
            }
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .fade-in {
            animation: fadeInUp 0.8s ease-out;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <a href="#home" class="logo">🍵 Ukusa Cafe</a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#menu">Menu</a></li>
                <li><a href="#location">Location</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1 class="fade-in">Welcome to Ukusa Cafe</h1>
            <p class="fade-in">Experience the perfect blend of UK & USA flavors in the heart of Jubilee Hills</p>
            <a href="#menu" class="cta-button fade-in">View Our Menu</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <h2>About Ukusa</h2>
        <div class="about-content">
            <div class="about-text">
                <p>Ukusa Cafe brings you the best of both worlds - authentic British teas and classic American coffees, all in one cozy spot in Jubilee Hills. Our fusion menu combines traditional recipes with modern twists.</p>
                <p>From our signature English Breakfast Tea paired with American-style pancakes to our robust Filter Coffee with scones, every visit is a culinary journey across the Atlantic.</p>
            </div>
            <div class="about-image">
                <img src="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 400 300'><rect fill='%23f8d7a8' width='400' height='300' rx='20'/><circle fill='%23D2691E' cx='100' cy='80' r='40'/><circle fill='%238B4513' cx='300' cy='100' r='30'/><rect fill='%23A0522D' x='150' y='180' width='100' height='60' rx='10'/><text x='200' y='250' font-family='Arial' font-size='20' fill='%23333' text-anchor='middle'>Cafe Interior</text></svg>" alt="Ukusa Cafe Interior">
            </div>
        </div>
    </section>

    <!-- Menu Section -->
    <section id="menu" class="menu-section">
        <h2>Our Menu</h2>
        <div class="menu-grid">
            <div class="menu-item">
                <h3>English Breakfast Tea</h3>
                <p>Classic full-leaf black tea with milk & sugar</p>
                <div class="price">₹120</div>
            </div>
            <div class="menu-item">
                <h3>Americano</h3>
                <p>Strong espresso with hot water</p>
                <div class="price">₹150</div>
            </div>
            <div class="menu-item">
                <h3>UK-USA Pancakes</h3>
                <p>Fluffy pancakes with clotted cream & maple syrup</p>
                <div class="price">₹280</div>
            </div>
            <div class="menu-item">
                <h3>Filter Coffee</h3>
                <p>South Indian style with American roast</p>
                <div class="price">₹140</div>
            </div>
            <div class="menu-item">
                <h3>Scones & Jam</h3>
                <p>Freshly baked scones with strawberry jam</p>
                <div class="price">₹220</div>
            </div>
            <div class="menu-item">
                <h3>Apple Pie</h3>
                <p>Classic American dessert with vanilla ice cream</p>
                <div class="price">₹250</div>
            </div>
        </div>
    </section>

    <!-- Location Section -->
    <section id="location" class="location">
        <h2>Visit Us</h2>
        <div class="location-content">
            <div>
                <h3>Jubilee Hills, Hyderabad</h3>
                <p><strong>Address:</strong><br>
                Road No. 36, Jubilee Hills,<br>
                Hyderabad, Telangana 500033</p>
                <p><strong>Hours:</strong><br>
                Mon-Sat: 7AM - 11PM<br>
                Sunday: 8AM - 10PM</p>
                <p><strong>Phone:</strong> +91 98765 43210</p>
            </div>
            <div class="map-placeholder">
                🗺️ Map coming soon!<br>
                Road No. 36, Jubilee Hills
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <h2>Get In Touch</h2>
        <div class="contact-content">
            <div class="contact-item">
                <h3>📧 Email</h3>
                <p>hello@ukusacafe.com</p>
            </div>
            <div class="contact-item">
                <h3>📱 WhatsApp</h3>
                <p>+91 98765 43210</p>
            </div>
            <div class="contact-item">
                <h3>📍 Instagram</h3>
                <p>@ukusacafe_hyd</p>
            </div>
            <div class="contact-item">
                <h3>⭐ Reviews</h3>
                <p>4.8/5 on Google</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Ukusa Cafe - Jubilee Hills. All rights reserved. | Made with ☕ in Hyderabad</p>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Add fade-in animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.menu-item, .about-content > *').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>
