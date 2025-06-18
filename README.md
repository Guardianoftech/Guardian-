<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>rohit Owner - Professional Video Creator</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Raleway:wght@700;800&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #6c63ff;
            --secondary: #ff6584;
            --dark: #1a1a2e;
            --darker: #0f0f1b;
            --light: #f8f9fa;
            --gray: #e2e2e2;
            --transition: all 0.4s ease;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, var(--darker), var(--dark));
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header & Navigation */
        header {
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            background: rgba(26, 26, 46, 0.9);
            backdrop-filter: blur(10px);
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Raleway', sans-serif;
            font-size: 28px;
            font-weight: 800;
            color: var(--primary);
            text-decoration: none;
        }

        .logo span {
            color: var(--secondary);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            font-size: 16px;
            transition: var(--transition);
            position: relative;
        }

        .nav-links a:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--primary);
            left: 0;
            bottom: -5px;
            transition: var(--transition);
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a:hover:after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding-top: 80px;
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            max-width: 650px;
            z-index: 2;
        }

        .hero h1 {
            font-family: 'Raleway', sans-serif;
            font-size: 4rem;
            font-weight: 800;
            line-height: 1.2;
            margin-bottom: 20px;
        }

        .hero h1 span {
            color: var(--primary);
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .cta-button {
            display: inline-block;
            padding: 14px 32px;
            background: var(--primary);
            color: white;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            transition: var(--transition);
            border: 2px solid var(--primary);
            margin-right: 15px;
        }

        .cta-button:hover {
            background: transparent;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(108, 99, 255, 0.3);
        }

        .cta-button.secondary {
            background: transparent;
            border: 2px solid var(--secondary);
        }

        .cta-button.secondary:hover {
            background: var(--secondary);
        }

        .hero-image {
            position: absolute;
            right: 0;
            top: 50%;
            transform: translateY(-50%);
            width: 45%;
            max-width: 600px;
            z-index: 1;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
        }

        .hero-image:before {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            opacity: 0.3;
        }

        .hero-image img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* Section Styling */
        section {
            padding: 100px 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 70px;
        }

        .section-header h2 {
            font-family: 'Raleway', sans-serif;
            font-size: 2.8rem;
            margin-bottom: 15px;
            position: relative;
            display: inline-block;
        }

        .section-header h2:after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background: var(--primary);
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
        }

        .section-header p {
            max-width: 700px;
            margin: 25px auto 0;
            font-size: 1.1rem;
            opacity: 0.8;
        }

        /* Services */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .service-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 40px 30px;
            text-align: center;
            transition: var(--transition);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .service-card:hover {
            transform: translateY(-10px);
            background: rgba(108, 99, 255, 0.1);
            border-color: var(--primary);
        }

        .service-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 25px;
        }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }

        /* Portfolio */
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
        }

        .portfolio-item {
            border-radius: 15px;
            overflow: hidden;
            position: relative;
            height: 300px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .portfolio-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .portfolio-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to top, rgba(108, 99, 255, 0.8), transparent);
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            padding: 25px;
            opacity: 0;
            transition: var(--transition);
        }

        .portfolio-item:hover .portfolio-overlay {
            opacity: 1;
        }

        .portfolio-item:hover img {
            transform: scale(1.1);
        }

        .portfolio-overlay h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }

        /* Social Section */
        .social-section {
            background: rgba(255, 255, 255, 0.03);
            text-align: center;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 40px;
        }

        .social-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 30px;
            width: 300px;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .social-card:hover {
            transform: translateY(-10px);
            background: rgba(108, 99, 255, 0.1);
            border-color: var(--primary);
        }

        .social-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .social-card h3 {
            font-size: 1.4rem;
            margin-bottom: 15px;
        }

        .social-card a {
            display: inline-block;
            padding: 10px 25px;
            background: var(--primary);
            color: white;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            margin-top: 10px;
            transition: var(--transition);
        }

        .social-card a:hover {
            background: var(--secondary);
            transform: scale(1.05);
        }

        /* Footer */
        footer {
            background: var(--darker);
            padding: 50px 0 30px;
            text-align: center;
        }

        .footer-logo {
            font-family: 'Raleway', sans-serif;
            font-size: 2rem;
            font-weight: 800;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            list-style: none;
            margin: 30px 0;
        }

        .footer-links li {
            margin: 0 15px;
        }

        .footer-links a {
            color: var(--gray);
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-links a:hover {
            color: var(--primary);
        }

        .copyright {
            color: var(--gray);
            opacity: 0.7;
            font-size: 0.9rem;
            margin-top: 30px;
        }

        /* Responsive */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 3rem;
            }
            
            .hero-image {
                width: 50%;
            }
        }

        @media (max-width: 768px) {
            .hero {
                text-align: center;
            }
            
            .hero-content {
                margin: 0 auto;
                padding-top: 80px;
            }
            
            .hero-image {
                position: relative;
                width: 80%;
                margin: 50px auto 0;
                transform: none;
                top: auto;
                right: auto;
            }
            
            .social-links {
                flex-direction: column;
                align-items: center;
            }
            
            .nav-links {
                display: none;
            }
        }

        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2.3rem;
            }
            
            .section-header h2 {
                font-size: 2.2rem;
            }
            
            .cta-button {
                display: block;
                margin: 0 auto 15px;
                width: 80%;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav class="navbar">
                <a href="#" class="logo">Tyson<span>Studio</span></a>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#social">Connect</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Crafting <span>Stunning Visual Stories</span> That Captivate Audiences</h1>
                <p>I'm Tyson Owner, a professional video creator specializing in cinematic storytelling, brand films, and engaging content that drives results. With a passion for visual excellence and a keen eye for detail, I transform ideas into compelling visual narratives.</p>
                <div class="hero-buttons">
                    <a href="#portfolio" class="cta-button">View My Work</a>
                    <a href="#contact" class="cta-button secondary">Get In Touch</a>
                </div>
            </div>
        </div>
        <div class="hero-image">
            <img src="https://images.unsplash.com/photo-1574717024453-354056aafa98?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Video Production">
        </div>
    </section>

    <!-- Services Section -->
    <section id="services">
        <div class="container">
            <div class="section-header">
                <h2>My Services</h2>
                <p>I offer a comprehensive range of video production services tailored to your specific needs and goals.</p>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-film"></i>
                    </div>
                    <h3>Commercial Production</h3>
                    <p>Engaging commercials that capture attention and drive conversions for your brand or product.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-video"></i>
                    </div>
                    <h3>Corporate Videos</h3>
                    <p>Professional corporate videos that communicate your brand story and values effectively.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-music"></i>
                    </div>
                    <h3>Music Videos</h3>
                    <p>Creative and visually striking music videos that bring songs to life and amplify their impact.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-photo-video"></i>
                    </div>
                    <h3>Event Coverage</h3>
                    <p>Comprehensive event coverage that captures key moments and creates lasting memories.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-edit"></i>
                    </div>
                    <h3>Post-Production</h3>
                    <p>Expert editing, color grading, and visual effects to polish your footage to perfection.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-drone"></i>
                    </div>
                    <h3>Aerial Cinematography</h3>
                    <p>Breathtaking aerial footage captured with professional drone equipment for unique perspectives.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section id="portfolio" style="background: rgba(255,255,255,0.03);">
        <div class="container">
            <div class="section-header">
                <h2>Featured Projects</h2>
                <p>Explore a selection of my recent video productions that showcase my creative vision and technical expertise.</p>
            </div>
            <div class="portfolio-grid">
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1578575437130-527eed3abbec?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Project 1">
                    <div class="portfolio-overlay">
                        <h3>Brand Campaign</h3>
                        <p>Commercial Series</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1533227268428-f9ed0900fb3b?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Project 2">
                    <div class="portfolio-overlay">
                        <h3>Music Video</h3>
                        <p>Artist: The Midnight</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1580519542036-c47de6196ba5?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Project 3">
                    <div class="portfolio-overlay">
                        <h3>Corporate Profile</h3>
                        <p>Tech Solutions Inc.</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1559703243-099f0e907f45?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Project 4">
                    <div class="portfolio-overlay">
                        <h3>Travel Documentary</h3>
                        <p>Discover Japan</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1545239705-1564e58b9e4a?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Project 5">
                    <div class="portfolio-overlay">
                        <h3>Product Launch</h3>
                        <p>Automotive Industry</p>
                    </div>
                </div>
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1527689638836-411945a2b57a?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Project 6">
                    <div class="portfolio-overlay">
                        <h3>Event Highlights</h3>
                        <p>Tech Conference 2023</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Social Section -->
    <section id="social" class="social-section">
        <div class="container">
            <div class="section-header">
                <h2>Connect With Me</h2>
                <p>Follow my work and stay updated with my latest projects and behind-the-scenes content.</p>
            </div>
            <div class="social-links">
                <div class="social-card">
                    <div class="social-icon">
                        <i class="fab fa-youtube"></i>
                    </div>
                    <h3>YouTube Channel</h3>
                    <p>Subscribe to my YouTube channel for video tutorials, project breakdowns, and creative insights.</p>
                    <a href="https://youtube.com/@TYSON_OWNER" target="_blank">@TYSON_OWNER</a>
                </div>
                <div class="social-card">
                    <div class="social-icon">
                        <i class="fab fa-telegram"></i>
                    </div>
                    <h3>Telegram Channel</h3>
                    <p>Join my Telegram community for exclusive content updates and direct communication.</p>
                    <a href="https://t.me/TYSON_OWNER" target="_blank">@TYSON_OWNER</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <div class="section-header">
                <h2>Get In Touch</h2>
                <p>Have a project in mind? Let's collaborate and create something amazing together.</p>
            </div>
            <div style="max-width: 700px; margin: 0 auto; background: rgba(255,255,255,0.05); padding: 40px; border-radius: 15px; border: 1px solid rgba(255,255,255,0.1);">
                <form>
                    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-bottom: 20px;">
                        <div>
                            <input type="text" placeholder="Your Name" style="width: 100%; padding: 15px; border-radius: 8px; border: none; background: rgba(255,255,255,0.08); color: white; font-family: inherit;">
                        </div>
                        <div>
                            <input type="email" placeholder="Your Email" style="width: 100%; padding: 15px; border-radius: 8px; border: none; background: rgba(255,255,255,0.08); color: white; font-family: inherit;">
                        </div>
                    </div>
                    <div style="margin-bottom: 20px;">
                        <input type="text" placeholder="Subject" style="width: 100%; padding: 15px; border-radius: 8px; border: none; background: rgba(255,255,255,0.08); color: white; font-family: inherit;">
                    </div>
                    <div style="margin-bottom: 20px;">
                        <textarea placeholder="Your Message" rows="5" style="width: 100%; padding: 15px; border-radius: 8px; border: none; background: rgba(255,255,255,0.08); color: white; font-family: inherit;"></textarea>
                    </div>
                    <button type="submit" style="background: var(--primary); color: white; border: none; padding: 15px 40px; border-radius: 50px; font-weight: 600; font-family: inherit; font-size: 1rem; cursor: pointer; transition: var(--transition);">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-logo">Tyson<span>Studio</span></div>
            <p>Professional Video Production & Creative Content</p>
            <ul class="footer-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#social">Connect</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="copyright">
                &copy; 2023 Tyson Owner. All Rights Reserved. Developed by HUNK IT TECH
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Header background change on scroll
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(26, 26, 46, 0.95)';
                header.style.boxShadow = '0 5px 20px rgba(0, 0, 0, 0.2)';
            } else {
                header.style.background = 'rgba(26, 26, 46, 0.9)';
                header.style.boxShadow = '0 5px 20px rgba(0, 0, 0, 0.1)';
            }
        });
    </script>
</body>
</html>
