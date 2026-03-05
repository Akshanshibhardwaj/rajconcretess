<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Raj Concretes Products | Quality Construction Materials</title>
    <style>
        /* --- CSS VARIABLES & RESET --- */
        :root {
            --primary-color: #f39c12; /* Construction Yellow */
            --secondary-color: #2c3e50; /* Dark Blue/Grey */
            --concrete-light: #ecf0f1;
            --concrete-dark: #7f8c8d;
            --text-color: #333;
            --white: #ffffff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--white);
        }

        a { text-decoration: none; color: inherit; }
        ul { list-style: none; }

        /* --- HEADER & NAVIGATION --- */
        header {
            background-color: var(--secondary-color);
            color: var(--white);
            padding: 1rem 5%;
            position: sticky;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            text-transform: uppercase;
            border-left: 5px solid var(--primary-color);
            padding-left: 10px;
        }

        .nav-links {
            display: flex;
            gap: 20px;
        }

        .nav-links a {
            color: var(--white);
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary-color);
        }

        .cta-btn {
            background-color: var(--primary-color);
            color: var(--white);
            padding: 10px 20px;
            border-radius: 5px;
            font-weight: bold;
            transition: background 0.3s;
        }

        .cta-btn:hover {
            background-color: #e67e22;
        }

        /* Mobile Menu Button */
        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* --- HERO SECTION --- */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1518709268805-4e9042af9f23?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');
            background-size: cover;
            background-position: center;
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: var(--white);
            padding: 0 20px;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            max-width: 600px;
        }

        /* --- ABOUT SECTION --- */
        .section {
            padding: 80px 5%;
        }

        .about {
            background-color: var(--white);
            text-align: center;
        }

        .section-title {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--secondary-color);
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 50%;
            height: 4px;
            background-color: var(--primary-color);
            margin: 10px auto 0;
        }

        .about-content {
            max-width: 800px;
            margin: 0 auto;
        }

        /* --- PRODUCTS SECTION --- */
        .products {
            background-color: var(--concrete-light);
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .product-card {
            background: var(--white);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .product-card:hover {
            transform: translateY(-5px);
        }

        .product-img {
            height: 200px;
            background-color: #ddd;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #666;
            font-size: 0.9rem;
        }
        
        /* Using placeholder images for demo */
        .product-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .product-info {
            padding: 20px;
            text-align: center;
        }

        .product-info h3 {
            color: var(--secondary-color);
            margin-bottom: 10px;
        }

        /* --- FEATURES SECTION --- */
        .features {
            background-color: var(--secondary-color);
            color: var(--white);
            text-align: center;
        }

        .features-grid {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 40px;
            margin-top: 40px;
        }

        .feature-item {
            flex: 1 1 300px;
            padding: 20px;
        }

        .feature-icon {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 15px;
        }

        /* --- CONTACT SECTION --- */
        .contact {
            background-color: var(--white);
        }

        .contact-container {
            display: flex;
            flex-wrap: wrap;
            gap: 40px;
            justify-content: center;
        }

        .contact-info, .contact-form {
            flex: 1 1 400px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        .contact-item span {
            margin-left: 15px;
            color: var(--secondary-color);
            font-weight: bold;
        }

        form input, form textarea {
            width: 100%;
            padding: 12px;
            margin-bottom: 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }

        form button {
            background-color: var(--secondary-color);
            color: var(--white);
            padding: 12px 30px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1rem;
        }

        form button:hover {
            background-color: #1a252f;
        }

        /* --- FOOTER --- */
        footer {
            background-color: #222;
            color: #aaa;
            text-align: center;
            padding: 20px;
        }

        /* --- RESPONSIVE --- */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 70px;
                right: 0;
                background-color: var(--secondary-color);
                width: 100%;
                text-align: center;
                padding: 20px 0;
            }

            .nav-links.active {
                display: flex;
            }

            .menu-toggle {
                display: block;
            }

            .hero h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="logo">RAJ CONCRETES</div>
        <div class="menu-toggle" onclick="toggleMenu()">☰</div>
        <nav>
            <ul class="nav-links" id="navLinks">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#products">Products</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="#contact" class="cta-btn">Get Quote</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <h1>Building Strong Foundations</h1>
        <p>Premium quality concrete products for all your construction needs. Durable, reliable, and built to last.</p>
        <a href="#products" class="cta-btn">View Our Products</a>
    </section>

    <!-- About Section -->
    <section id="about" class="section about">
        <h2 class="section-title">About Raj Concretes</h2>
        <div class="about-content">
            <p>At Raj Concretes Products, we are dedicated to providing the highest quality concrete solutions for the construction industry. With years of experience and a commitment to excellence, we supply durable precast products that stand the test of time.</p>
            <br>
            <p>Whether you are building a home, a commercial complex, or infrastructure projects, our products ensure structural integrity and longevity.</p>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products" class="section products">
        <div style="text-align: center;">
            <h2 class="section-title">Our Products</h2>
            <p>High-grade concrete solutions for every project.</p>
        </div>
        
        <div class="product-grid">
            <!-- Product 1 -->
            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1590082725353-2b7248222232?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Concrete Pipes">
                </div>
                <div class="product-info">
                    <h3>Concrete Pipes</h3>
                    <p>High-strength drainage and culvert pipes for efficient water management.</p>
                </div>
            </div>

            <!-- Product 2 -->
            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1589939705384-5185137a7f0f?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Manhole Rings">
                </div>
                <div class="product-info">
                    <h3>Manhole Rings</h3>
                    <p>Standard and heavy-duty rings for sewage and utility access points.</p>
                </div>
            </div>

            <!-- Product 3 -->
            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1518709268805-4e9042af9f23?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Interlocking Blocks">
                </div>
                <div class="product-info">
                    <h3>Interlocking Blocks</h3>
                    <p>Eco-friendly paving blocks for driveways, walkways, and parking lots.</p>
                </div>
            </div>

            <!-- Product 4 -->
            <div class="product-card">
                <div class="product-img">
                    <img src="https://images.unsplash.com/photo-1541888946425-d81bb19240f5?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Ready Mix Concrete">
                </div>
                <div class="product-info">
                    <h3>Ready Mix Concrete</h3>
                    <p>Customized concrete mixes delivered directly to your construction site.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="section features">
        <h2 class="section-title" style="color: white; border-color: white;">Why Choose Us?</h2>
        <div class="features-grid">
            <div class="feature-item">
                <div class="feature-icon">★</div>
                <h3>High Quality</h3>
                <p>We use premium materials to ensure every product meets strict durability standards.</p>
            </div>
            <div class="feature-item">
                <div class="feature-icon">⏱</div>
                <h3>On-Time Delivery</h3>
                <p>We understand the importance of schedules. We deliver when you need us.</p>
            </div>
            <div class="feature-item">
                <div class="feature-icon">♥</div>
                <h3>Customer Support</h3>
                <p>Our team is always ready to assist you with technical advice and orders.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section contact">
        <div style="text-align: center;">
            <h2 class="section-title">Contact Us</h2>
            <p>Get in touch for orders and inquiries.</p>
        </div>

        <div class="contact-container">
            <div class="contact-info">
                <div class="contact-item">
                    <span>📍</span> Address: [Insert Your Address Here]
                </div>
                <div class="contact-item">
                    <span>📞</span> Phone: +91 98765 43210
                </div>
                <div class="contact-item">
                    <span>✉️</span> Email: info@rajconcretes.com
                </div>
                <div class="contact-item">
                    <span>📘</span> Facebook: <a href="https://www.facebook.com/p/raj-concretes-products-61580003442583/" target="_blank" style="color: #3b5998;">Raj Concretes Products</a>
                </div>
            </div>

            <div class="contact-form">
                <form>
                    <input type="text" placeholder="Your Name" required>
                    <input type="email" placeholder="Your Email" required>
                    <input type="tel" placeholder="Phone Number">
                    <textarea rows="5" placeholder="Message / Product Inquiry" required></textarea>
                    <button type="submit">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2023 Raj Concretes Products. All Rights Reserved.</p>
    </footer>

    <script>
        // Simple script to toggle mobile
