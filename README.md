<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aurexis Labs - Next-Gen Innovation | Aarush Agrawal</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@100..900&family=Space+Grotesk:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css"/>
    <style>
        :root {
            --primary: #7c3aed;
            --primary-dark: #6d28d9;
            --secondary: #06b6d4;
            --accent: #f59e0b;
            --gradient-1: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
            --gradient-2: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%);
            --gradient-3: linear-gradient(135deg, #ff9a9e 0%, #fecfef 50%, #fecfef 100%);
            --dark: #0f0f23;
            --dark-2: #1a1a2e;
            --glass: rgba(255, 255, 255, 0.05);
            --glass-border: rgba(255, 255, 255, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            scroll-padding-top: 100px;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: var(--dark);
            color: white;
            overflow-x: hidden;
            position: relative;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 12px;
        }

        ::-webkit-scrollbar-track {
            background: var(--dark-2);
        }

        ::-webkit-scrollbar-thumb {
            background: linear-gradient(var(--gradient-1));
            border-radius: 6px;
        }

        /* Animated Background */
        .bg-animation {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -2;
            overflow: hidden;
        }

        .bg-animation::before {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 80%, rgba(120, 119, 198, 0.3) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(255, 119, 198, 0.3) 0%, transparent 50%),
                radial-gradient(circle at 40% 40%, rgba(120, 219, 255, 0.3) 0%, transparent 50%);
            animation: bgShift 20s ease-in-out infinite;
        }

        @keyframes bgShift {
            0%, 100% { transform: scale(1) rotate(0deg); }
            50% { transform: scale(1.1) rotate(180deg); }
        }

        /* Floating Elements */
        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .float-el {
            position: absolute;
            background: var(--glass);
            backdrop-filter: blur(20px);
            border: 1px solid var(--glass-border);
            border-radius: 50%;
            animation: float 25s infinite linear;
        }

        @keyframes float {
            0% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { transform: translateY(-100vh) rotate(360deg); opacity: 0; }
        }

        /* Navbar */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 10000;
            padding: 1rem 0;
            backdrop-filter: blur(30px);
            background: rgba(15, 15, 35, 0.95);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .nav-container {
            max-width: 1600px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 5%;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 1rem;
            font-family: 'Space Grotesk', sans-serif;
            font-size: 2rem;
            font-weight: 700;
            background: var(--gradient-1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-decoration: none;
            position: relative;
        }

        .logo img {
            height: 60px;
            width: 60px;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(124, 58, 237, 0.5);
            transition: all 0.4s ease;
        }

        .logo:hover img {
            transform: scale(1.1) rotate(5deg);
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 3rem;
            align-items: center;
        }

        .nav-link {
            color: rgba(255, 255, 255, 0.9);
            text-decoration: none;
            font-weight: 500;
            position: relative;
            transition: all 0.3s ease;
            padding: 0.5rem 0;
        }

        .nav-link::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--gradient-1);
            transition: width 0.4s ease;
        }

        .nav-link:hover::before {
            width: 100%;
        }

        .nav-link:hover {
            color: white;
            text-shadow: 0 0 20px rgba(124, 58, 237, 0.5);
        }

        .menu-toggle {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 4px;
        }

        .menu-toggle span {
            width: 30px;
            height: 3px;
            background: white;
            transition: 0.3s;
            border-radius: 2px;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
        }

        .hero-container {
            max-width: 1600px;
            margin: 0 auto;
            padding: 0 5%;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 6rem;
            align-items: center;
        }

        .hero-content h1 {
            font-family: 'Space Grotesk', sans-serif;
            font-size: clamp(4rem, 8vw, 7rem);
            font-weight: 800;
            line-height: 0.9;
            margin-bottom: 2rem;
            background: linear-gradient(135deg, #ffffff 0%, #e0e7ff 50%, #c7d2fe 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero-content .subtitle {
            font-size: 1.5rem;
            color: rgba(255, 255, 255, 0.85);
            margin-bottom: 3rem;
            font-weight: 400;
            max-width: 500px;
        }

        .hero-buttons {
            display: flex;
            gap: 1.5rem;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1.2rem 2.5rem;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.75rem;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .btn-primary {
            background: var(--gradient-1);
            color: white;
            box-shadow: 0 20px 60px rgba(124, 58, 237, 0.4);
        }

        .btn-primary:hover {
            transform: translateY(-8px) scale(1.05);
            box-shadow: 0 30px 80px rgba(124, 58, 237, 0.6);
        }

        .btn-secondary {
            background: var(--glass);
            backdrop-filter: blur(20px);
            border: 2px solid var(--glass-border);
            color: white;
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: translateY(-4px);
        }

        .hero-mockup {
            position: relative;
            justify-self: end;
        }

        .main-mockup {
            width: 100%;
            max-width: 600px;
            border-radius: 40px;
            box-shadow: 
                0 50px 100px rgba(0, 0, 0, 0.5),
                0 0 100px rgba(124, 58, 237, 0.3);
            transform: perspective(1000px) rotateY(-10deg) rotateX(5deg);
            transition: all 0.6s ease;
        }

        .main-mockup:hover {
            transform: perspective(1000px) rotateY(0deg) rotateX(0deg) scale(1.05);
        }

        /* Stats */
        .stats {
            padding: 8rem 5%;
            background: rgba(255, 255, 255, 0.02);
            backdrop-filter: blur(20px);
            position: relative;
        }

        .stats-grid {
            max-width: 1600px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 4rem;
        }

        .stat-card {
            text-align: center;
            padding: 3rem 2rem;
        }

        .stat-number {
            font-family: 'Space Grotesk', sans-serif;
            font-size: clamp(3rem, 6vw, 5rem);
            font-weight: 800;
            background: var(--gradient-1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1rem;
        }

        /* About */
        .about {
            padding: 10rem 5%;
        }

        .section-header {
            text-align: center;
            margin-bottom: 6rem;
        }

        .section-title {
            font-family: 'Space Grotesk', sans-serif;
            font-size: clamp(3rem, 5vw, 4.5rem);
            font-weight: 800;
            background: var(--gradient-1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1.5rem;
        }

        .about-grid {
            max-width: 1600px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 6rem;
            align-items: center;
        }

        .founder-bio h3 {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            background: linear-gradient(135deg, #ffffff 0%, #e0e7ff 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .social-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 1.5rem;
            margin-top: 3rem;
        }

        .social-card {
            background: var(--glass);
            backdrop-filter: blur(20px);
            border: 1px solid var(--glass-border);
            padding: 2rem;
            border-radius: 24px;
            text-align: center;
            transition: all 0.4s ease;
            cursor: pointer;
        }

        .social-card:hover {
            transform: translateY(-15px) scale(1.05);
            background: rgba(255, 255, 255, 0.1);
            box-shadow: 0 30px 80px rgba(0, 0, 0, 0.4);
        }

        .social-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            display: block;
        }

        /* Services */
        .services {
            padding: 10rem 5%;
            background: var(--dark-2);
        }

        .services-grid {
            max-width: 1600px;
            margin: 0 auto 6rem;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 3rem;
        }

        .service-card {
            background: var(--glass);
            backdrop-filter: blur(30px);
            border: 1px solid var(--glass-border);
            padding: 4rem 3rem;
            border-radius: 32px;
            position: relative;
            overflow: hidden;
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: var(--gradient-1);
        }

        .service-card:hover {
            transform: translateY(-20px) scale(1.02);
            box-shadow: 0 50px 100px rgba(0, 0, 0, 0.5);
            border-color: var(--primary);
        }

        .service-icon {
            width: 100px;
            height: 100px;
            background: var(--gradient-1);
            border-radius: 24px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            margin: 0 auto 2rem;
            box-shadow: 0 20px 40px rgba(124, 58, 237, 0.3);
        }

        /* Portfolio Slider */
        .portfolio {
            padding: 10rem 5%;
            background: linear-gradient(135deg, var(--dark) 0%, var(--dark-2) 100%);
        }

        .swiper {
            padding-bottom: 4rem;
        }

        .portfolio-slide {
            background: var(--glass);
            backdrop-filter: blur(20px);
            border-radius: 24px;
            padding: 3rem;
            height: 400px;
            cursor: grab;
        }

        .swiper-pagination-bullet {
            background: var(--primary);
        }

        /* Contact */
        .contact {
            padding: 10rem 5% 6rem;
            position: relative;
        }

        .contact-grid {
            max-width: 1600px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 6rem;
        }

        .contact-form {
            background: var(--glass);
            backdrop-filter: blur(30px);
            border: 1px solid var(--glass-border);
            padding: 4rem;
            border-radius: 32px;
        }

        .form-group {
            margin-bottom: 2rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1.5rem;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid var(--glass-border);
            border-radius: 20px;
            color: white;
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 4px rgba(124, 58, 237, 0.2);
            background: rgba(255, 255, 255, 0.1);
        }

        /* Footer */
        .footer {
            background: var(--dark-2);
            padding: 4rem 5% 2rem;
            text-align: center;
        }

        /* Mobile */
        @media (max-width: 768px) {
            .menu-toggle {
                display: flex;
            }

            .nav-menu {
                display: none;
            }

            .hero-container,
            .about-grid,
            .contact-grid {
                grid-template-columns: 1fr;
                gap: 3rem;
                text-align: center;
            }

            .hero-buttons {
                justify-content: center;
            }
        }

        /* Animations */
        .fade-in-up {
            opacity: 0;
            transform: translateY(60px);
            transition: all 1s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .fade-in-up.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .scale-in {
            opacity: 0;
            transform: scale(0.8);
            transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .scale-in.visible {
            opacity: 1;
            transform: scale(1);
        }
    </style>
</head>
<body>
    <!-- Animated Background -->
    <div class="bg-animation"></div>
    <div class="floating-elements" id="floatingElements"></div>

    <!-- Navbar -->
    <nav class="navbar">
        <div class="nav-container">
            <a href="#home" class="logo">
                <img src="https://i.postimg.cc/ZnvffBCg/1dcdb7f7-de7b-48ae-920e-9869e990031b-7C361840-19A8-47AC-B944-81763F2E43D9.jpg" alt="Aurexis Labs">
                Aurexis Labs
            </a>
            <ul class="nav-menu">
                <li><a href="#home" class="nav-link">Home</a></li>
                <li><a href="#about" class="nav-link">About</a></li>
                <li><a href="#services" class="nav-link">Services</a></li>
                <li><a href="#portfolio" class="nav-link">Portfolio</a></li>
                <li><a href="#contact" class="nav-link">Contact</a></li>
            </ul>
            <div class="menu-toggle">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>
    </nav>

    <!-- Hero -->
    <section id="home" class="hero">
        <div class="hero-container">
            <div class="fade-in-up">
                <h1>Next-Gen <span style="background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1, #f9ca24); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; animation: rainbow 3s ease-in-out infinite;">Innovation</span><br>Engineered by Aurexis Labs</h1>
                <p class="subtitle">Founded by <strong>Aarush Agrawal</strong> | Transforming visionary ideas into world-class digital realities with cutting-edge technology</p>
                <div class="hero-buttons">
                    <a href="#contact" class="btn btn-primary">
                        <i class="fas fa-rocket"></i>
                        Start Project
                    </a>
                    <a href="#services" class="btn btn-secondary">
                        <i class="fas fa-play"></i>
                        View Services
                    </a>
                </div>
            </div>
            <div class="hero-mockup scale-in">
                <img src="https://i.postimg.cc/ZnvffBCg/1dcdb7f7-de7b-48ae-920e-9869e990031b-7C361840-19A8-47AC-B944-81763F2E43D9.jpg" alt="Aurexis Labs" class="main-mockup">
            </div>
        </div>
    </section>

    <!-- Stats -->
    <section class="stats">
        <div class="stats-grid">
            <div class="stat-card fade-in-up">
                <div class="stat-number">500+</div>
                <div>Projects Delivered</div>
            </div>
            <div class="stat-card fade-in-up">
                <div class="stat-number">98%</div>
                <div>Client Satisfaction</div>
            </div>
            <div class="stat-card fade-in-up">
                <div class="stat-number">24/7</div>
                <div>Support Available</div>
            </div>
            <div class="stat-card fade-in-up">
                <div class="stat-number">100%</div>
                <div>On-Time Delivery</div>
            </div>
        </div>
    </section>

    <!-- About -->
    <section id="about" class="about">
        <div class="section-header fade-in-up">
            <h2 class="section-title">Meet the Mastermind</h2>
            <p>Aarush Agrawal - Founder & Visionary Leader of Aurexis Labs</p>
        </div>
        <div class="about-grid">
            <div class="founder-bio fade-in-up">
                <h3>Aarush Agrawal</h3>
                <p><strong>The Architect of Digital Excellence</strong></p>
                <p>Aarush Agrawal founded Aurexis Labs with a singular vision: to push the boundaries of what's possible in digital innovation. A tech prodigy and strategic thinker, Aarush combines deep technical expertise with entrepreneurial brilliance to deliver transformative solutions.</p>
                <div class="social-grid">
                    <a href="mailto:aarushagrawal240411@gmail.com" class="social-card" title="Email Aarush">
                        <i class="fas fa-envelope social-icon"></i>
                        <strong>Email</strong>
                        <div>aarushagrawal240411@gmail.com</div>
                    </a>
                    <a href="https://instagram.com/aurexislabs" target="_blank" class="social-card" title="Instagram">
                        <i class="fab fa-instagram social-icon"></i>
                        <strong>Instagram</strong>
                        <div>@aurexislabs</div>
                    </a>
                </div>
            </div>
            <div class="scale-in">
                <img src="https://i.postimg.cc/ZnvffBCg/1dcdb7f7-de7b-48ae-920e-9869e990031b-7C361840-19A8-47AC-B944-81763F2E43D9.jpg" alt="Aarush Agrawal" style="width: 100%; border-radius: 32px; box-shadow: 0 50px 100px rgba(0,0,0,0.5);">
            </div>
        </div>
    </section>

    <!-- Services -->
    <section id="services" class="services">
        <div class="section-header fade-in-up">
            <h2 class="section-title">Elite Services</h2>
            <p>World-class solutions powered by cutting-edge technology</p>
        </div>
        <div class="services-grid">
            <div class="service-card fade-in-up">
                <div class="service-icon"><i class="fas fa-rocket"></i></div>
                <h3>Web Mastery</h3>
                <p>Next-gen websites with blazing performance, pixel-perfect design, and enterprise-grade scalability.</p>
            </div>
            <div class="service-card fade-in-up">
                <div class="service-icon" style="background: linear-gradient(135deg, #06b6d4 0%, #0891b2 100%);"><i class="fas fa-mobile-alt"></i></div>
                <h3>Mobile Innovation</h3>
                <p>Native & cross-platform apps that dominate app stores with exceptional UX and performance.</p>
            </div>
            <div class="service-card fade-in-up">
                <div class="service-icon" style="background: linear-gradient(135deg, #10b981 0%, #059669 100%);"><i class="fas fa-brain"></i></div>
                <h3>AI Revolution</h3>
                <p>Custom AI/ML solutions, computer vision, NLP, and predictive analytics for business transformation.</p>
            </div>
            <div class="service-card fade-in-up">
                <div class="service-icon" style="background: linear-gradient(135deg, #f59e0b 0%, #d97706 100%);"><i class="fas fa-shield-alt"></i></div>
                <h3>Cyber Fortress</h3>
                <p>Impenetrable security architecture, penetration testing, and compliance for digital assets.</p>
            </div>
        </div>
    </section>

    <!-- Portfolio -->
    <section id="portfolio" class="portfolio">
        <div class="section-header fade-in-up">
            <h2 class="section-title">Featured Works</h2>
            <p>Our latest masterpieces that redefine excellence</p>
        </div>
        <div class="swiper portfolio-swiper">
            <div class="swiper-wrapper">
                <div class="swiper-slide portfolio-slide fade-in-up">
                    <h3>Enterprise Dashboard</h3>
                    <p>Real-time analytics platform for Fortune 500 company</p>
                    <div style="margin-top: 2rem; color: var(--accent);">+300% Performance Boost</div>
                </div>
                <div class="swiper-slide portfolio-slide fade-in-up">
                    <h3>E-Commerce Platform</h3>
                    <p>Scalable marketplace with AI recommendations</p>
                    <div style="margin-top: 2rem; color: var(--accent);">10x Conversion Rate</div>
                </div>
                <div class="swiper-slide portfolio-slide fade-in-up">
                    <h3>Mobile Banking App</h3>
                    <p>Secure fintech solution with biometric auth</p>
                    <div style="margin-top: 2rem; color: var(--accent);">99.99% Uptime</div>
                </div>
            </div>
            <div class="swiper-pagination"></div>
        </div>
    </section>

    <!-- Contact -->
    <section id="contact" class="contact">
        <div class="section-header fade-in-up">
            <h2 class="section-title">Launch Your Vision</h2>
            <p>Ready to build something extraordinary? Let's talk.</p>
        </div>
        <div class="contact-grid">
            <div class="fade-in-up">
                <h3>📧 Get In Touch</h3>
                <div style="margin: 2rem 0; font-size: 1.2rem;">
                    <div style="margin-bottom: 1.5rem;">
                        <i class="fas fa-envelope" style="color: var(--accent); margin-right: 1rem;"></i>
                        aarushagrawal240411@gmail.com
                    </div>
                    <div style="margin-bottom: 1.5rem;">
                        <i class="fab fa-instagram" style="color: var(--accent); margin-right: 1rem;"></i>
                        @aurexislabs
                    </div>
                </div>
            </div>
            <form action="https://formspree.io/f/xjgepqwn" method="POST" class="contact-form fade-in-up">
                <div class="form-group">
                    <input type="text" name="name" placeholder="Your Name" required>
                </div>
                <div class="form-group">
                    <input type="email" name="email" placeholder="Your Email" required>
                </div>
                <div class="form-group">
                    <input type="text" name="subject" placeholder="Project Type" required>
                </div>
                <div class="form-group">
                    <textarea name="message" rows="6" placeholder="Tell us about your vision..." required></textarea>
                </div>
                <button type="submit" class="btn btn-primary" style="width: 100%; justify-content: center;">
                    <i class="fas fa-paper-plane"></i>
                    Launch Project
                </button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div style="max-width: 1600px; margin: 0 auto;">
            <div style="display: flex; justify-content: center; gap: 3rem; margin-bottom: 2rem; flex-wrap: wrap;">
                <a href="#home" style="color: rgba(255,255,255,0.7); text-decoration: none;">Home</a>
                <a href="#about" style="color: rgba(255,255,255,0.7); text-decoration: none;">About</a>
                <a href="#services" style="color: rgba(255,255,255,0.7); text-decoration: none;">Services</a>
                <a href="#contact" style="color: rgba(255,255,255,0.7); text-decoration: none;">Contact</a>
            </div>
            <p style="opacity: 0.7;">© 2024 Aurexis Labs. Founded by <strong>Aarush Agrawal</strong>. All rights reserved. 🚀</p>
        </div>
    </footer>

    <!-- Scripts -->
    <script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
    <script>
        // Navbar scroll
        window.addEventListener('scroll', () => {
            document.querySelector('.navbar').style.background = window.scrollY > 50 
                ? 'rgba(15, 15, 35, 0.98)' 
                : 'rgba(15, 15, 35, 0.95)';
        });

        // Floating elements
        function createFloaters() {
            const container = document.getElementById('floatingElements');
            for(let i = 0; i < 20; i++) {
                const el = document.createElement('div');
                el.className = 'float-el';
                el.style.left = Math.random() * 100 + '%';
                el.style.width = (Math.random() * 60 + 20) + 'px';
                el.style.height = el.style.width;
                el.style.animationDuration = (Math.random() * 15 + 10) + 's';
                el.style.animationDelay = Math.random() * 5 + 's';
                container.appendChild(el);
            }
        }
        createFloaters();

        // Intersection Observer
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if(entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.fade-in-up, .scale-in').forEach(el => observer.observe(el));

        // Swiper
        new Swiper('.portfolio-swiper', {
            slidesPerView: 1,
            spaceBetween: 30,
            pagination: {
                el: '.swiper-pagination',
                clickable: true,
            },
            breakpoints: {
                768: { slidesPerView: 2 },
                1024: { slidesPerView: 3 }
            },
            autoplay: { delay: 3000 },
            loop: true,
        });

        // Form handling
        document.querySelector('form').addEventListener('submit', function() {
            const btn = this.querySelector('button');
            btn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Launching...';
            btn.disabled = true;
        });

        // Rainbow animation
        const style = document.createElement('style');
        style.textContent = `
            @keyframes rainbow {
                0%, 100% { filter: hue-rotate(0deg); }
                50% { filter: hue-rotate(180deg); }
            }
        `;
        document.head.appendChild(style);

        // Mouse trail
        document.addEventListener('mousemove', (e) => {
            const trail = document.createElement('div');
            trail.style.cssText = `
                position: fixed;
                width: 6px; height: 6px;
                background: var(--gradient-1);
                border-radius: 50%;
                pointer-events: none;
                left: ${e.clientX}px;
                top: ${e.clientY}px;
                z-index: 9999;
                animation: trail 0.6s ease-out forwards;
            `;
            document.body.appendChild(trail);
            setTimeout(() => trail.remove(), 600);
        });

        const trailStyle = document.createElement('style');
        trailStyle.textContent = `
            @keyframes trail {
                to { transform: scale(0) translateY(-30px); opacity: 0; }
            }
        `;
        document.head.appendChild(trailStyle);

        // Typing effect
        const subtitle = document.querySelector('.subtitle');
        if(subtitle) {
            const text = subtitle.textContent;
            subtitle.textContent = '';
            let i = 0;
            function type() {
                if(i < text.length) {
                    subtitle.textContent += text[i];
                    i++;
                    setTimeout(type, 30);
                }
            }
            setTimeout(type, 1000);
        }
    </script>
</body>
</html>
