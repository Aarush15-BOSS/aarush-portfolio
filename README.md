<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aurexis Labs - Innovation Redefined</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* Navigation */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            z-index: 1000;
            padding: 1rem 0;
            transition: all 0.3s ease;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
        }

        .nav-container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 5%;
        }

        .logo {
            height: 50px;
            width: auto;
            transition: transform 0.3s ease;
        }

        .logo:hover {
            transform: scale(1.05);
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2.5rem;
        }

        .nav-link {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            font-size: 1rem;
            position: relative;
            transition: color 0.3s ease;
        }

        .nav-link:hover {
            color: #6366f1;
        }

        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: linear-gradient(90deg, #6366f1, #8b5cf6);
            transition: width 0.3s ease;
        }

        .nav-link:hover::after {
            width: 100%;
        }

        .cta-button {
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            box-shadow: 0 10px 30px rgba(99, 102, 241, 0.4);
        }

        .cta-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 15px 40px rgba(99, 102, 241, 0.6);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000"><defs><radialGradient id="a" cx="50%" cy="50%"><stop offset="0%" stop-color="%236366f1" stop-opacity="0.1"/><stop offset="100%" stop-color="%238b5cf6" stop-opacity="0"/></radialGradient></defs><circle cx="200" cy="200" r="100" fill="url(%23a)"><animate attributeName="r" values="100;150;100" dur="3s" repeatCount="indefinite"/></circle><circle cx="800" cy="300" r="80" fill="url(%23a)"><animate attributeName="r" values="80;120;80" dur="4s" repeatCount="indefinite"/></circle></svg>');
            animation: float 20s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        .hero-content {
            max-width: 900px;
            padding: 0 2rem;
            position: relative;
            z-index: 2;
        }

        .hero h1 {
            font-size: clamp(3rem, 8vw, 6rem);
            font-weight: 800;
            background: linear-gradient(135deg, #ffffff 0%, #e2e8f0 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease-out;
        }

        .hero p {
            font-size: 1.5rem;
            color: #cbd5e1;
            margin-bottom: 3rem;
            animation: fadeInUp 1s ease-out 0.2s both;
        }

        .hero-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease-out 0.4s both;
        }

        /* About Section */
        .about {
            padding: 120px 0;
            background: #f8fafc;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 5%;
        }

        .section-header {
            text-align: center;
            margin-bottom: 5rem;
        }

        .section-header h2 {
            font-size: 3.5rem;
            font-weight: 800;
            background: linear-gradient(135deg, #1e293b 0%, #334155 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 1rem;
        }

        .section-header p {
            font-size: 1.25rem;
            color: #64748b;
            max-width: 600px;
            margin: 0 auto;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 5rem;
            align-items: center;
        }

        .about-text h3 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            color: #1e293b;
        }

        .founder {
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            font-size: 3rem;
            font-weight: 800;
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Services */
        .services {
            padding: 120px 0;
            background: #0f0f23;
            color: white;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2.5rem;
        }

        .service-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(20px);
            padding: 3rem 2.5rem;
            border-radius: 24px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #6366f1, #8b5cf6, #ec4899);
        }

        .service-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 30px 60px rgba(99, 102, 241, 0.3);
        }

        .service-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #6366f1, #8b5cf6);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 2rem;
            font-size: 2rem;
        }

        /* Contact */
        .contact {
            padding: 120px 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 5rem;
            align-items: center;
        }

        .contact-info h3 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
            padding: 1rem;
            background: rgba(255,255,255,0.1);
            border-radius: 16px;
        }

        .contact-form {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(20px);
            padding: 3rem;
            border-radius: 24px;
            border: 1px solid rgba(255,255,255,0.2);
        }

        .form-group {
            margin-bottom: 2rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem 1.5rem;
            border: none;
            border-radius: 12px;
            background: rgba(255,255,255,0.9);
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            background: white;
            box-shadow: 0 0 0 3px rgba(99,102,241,0.3);
        }

        /* Footer */
        .footer {
            background: #0f0f23;
            color: #cbd5e1;
            padding: 3rem 0 1.5rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h4 {
            color: white;
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }

        .social-links {
            display: flex;
            gap: 1rem;
        }

        .social-link {
            width: 45px;
            height: 45px;
            background: linear-gradient(135deg, #6366f1, #8b5cf6);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(99,102,241,0.4);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid #334155;
            color: #64748b;
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

        /* Responsive */
        @media (max-width: 768px) {
            .nav-menu {
                display: none;
            }

            .hero h1 {
                font-size: 3rem;
            }

            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
                gap: 3rem;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .stats {
                grid-template-columns: 1fr;
            }
        }

        /* Scroll animations */
        .reveal {
            opacity: 0;
            transform: translateY(50px);
            transition: all 0.8s ease;
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar" id="navbar">
        <div class="nav-container">
            <img src="https://i.postimg.cc/ZnvffBCg/1dcdb7f7-de7b-48ae-920e-9869e990031b-7C361840-19A8-47AC-B944-81763F2E43D9.jpg" alt="Aurexis Labs Logo" class="logo">
            <ul class="nav-menu">
                <li><a href="#home" class="nav-link">Home</a></li>
                <li><a href="#about" class="nav-link">About</a></li>
                <li><a href="#services" class="nav-link">Services</a></li>
                <li><a href="#contact" class="nav-link">Contact</a></li>
            </ul>
            <a href="#contact" class="cta-button">Get Started</a>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Future-Ready Innovation</h1>
            <p>Aurexis Labs crafts cutting-edge solutions that redefine possibilities. Founded by <span class="founder">Aarush Agrawal</span>, we're building tomorrow's technology today.</p>
            <div class="hero-buttons">
                <a href="#services" class="cta-button">Explore Services</a>
                <a href="#contact" class="cta-button" style="background: transparent; border: 2px solid white;">Contact Us</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about reveal">
        <div class="container">
            <div class="section-header">
                <h2>About Aurexis Labs</h2>
                <p>Where visionary ideas meet cutting-edge technology. We're not just building products – we're shaping the future.</p>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Founded by <span class="founder">Aarush Agrawal</span></h3>
                    <p>Aurexis Labs was born from a passion for innovation and excellence. Under the leadership of founder Aarush Agrawal, we combine creativity with technical mastery to deliver transformative solutions that drive real impact.</p>
                    <p>Our mission is simple: solve complex problems with elegant technology. From AI-powered applications to scalable web platforms, we build what the future demands.</p>
                    <div class="stats">
                        <div class="stat">
                            <div class="stat-number">100+</div>
                            <div>Projects Delivered</div>
                        </div>
                        <div class="stat">
                            <div class="stat-number">50+</div>
                            <div>Happy Clients</div>
                        </div>
                        <div class="stat">
                            <div class="stat-number">24/7</div>
                            <div>Support</div>
                        </div>
                    </div>
                </div>
                <div style="position: relative;">
                    <img src="https://i.postimg.cc/ZnvffBCg/1dcdb7f7-de7b-48ae-920e-9869e990031b-7C361840-19A8-47AC-B944-81763F2E43D9.jpg" alt="Aurexis Labs" style="width: 100%; border-radius: 24px; box-shadow: 0 30px 60px rgba(0,0,0,0.2);">
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="services">
        <div class="container">
            <div class="section-header">
                <h2>What We Do</h2>
                <p>Comprehensive solutions powered by the latest technologies</p>
            </div>
            <div class="services-grid">
                <div class="service-card reveal">
                    <div class="service-icon">
                        <i class="fas fa-robot"></i>
                    </div>
                    <h3>AI & Machine Learning</h3>
                    <p>Intelligent systems that learn, adapt, and deliver results beyond human capability.</p>
                </div>
                <div class="service-card reveal">
                    <div class="service-icon">
                        <i class="fas fa-code"></i>
                    </div>
                    <h3>Web Development</h3>
                    <p>Lightning-fast, scalable web applications built with modern frameworks and best practices.</p>
                </div>
                <div class="service-card reveal">
                    <div class="service-icon">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3>Mobile Apps</h3>
                    <p>Native and cross-platform mobile experiences that engage users across all devices.</p>
                </div>
                <div class="service-card reveal">
                    <div class="service-icon">
                        <i class="fas fa-cloud"></i>
                    </div>
                    <h3>Cloud Solutions</h3>
                    <p>Scalable, secure cloud infrastructure designed for growth and reliability.</p>
                </div>
                <div class="service-card reveal">
                    <div class="service-icon">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3>Cybersecurity</h3>
                    <p>Enterprise-grade security solutions protecting your digital assets 24/7.</p>
                </div>
                <div class="service-card reveal">
                    <div class="service-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>Analytics & BI</h3>
                    <p>Transform raw data into actionable insights with advanced analytics platforms.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-header">
                <h2>Ready to Transform Your Vision?</h2>
                <p>Let's create something extraordinary together</p>
            </div>
            <div class="contact-content">
                <div class="contact-info reveal">
                    <h3>Get In Touch</h3>
                    <div class="contact-item">
                        <i class="fas fa-envelope" style="font-size: 1.5rem; color: #6366f1;"></i>
                        <div>
                            <div style="font-weight: 600; margin-bottom: 0.25rem;">Email</div>
                            <a href="mailto:aarushagrawal240411@gmail.com" style="color: white; text-decoration: none;">aarushagrawal240411@gmail.com</a>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fab fa-instagram" style="font-size: 1.5rem; color: #e4405f;"></i>
                        <div>
                            <div style="font-weight: 600; margin-bottom: 0.25rem;">Instagram</div>
                            <a href="https://instagram.com/aurexislabs" target="_blank" style="color: white; text-decoration: none;">@aurexislabs</a>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt" style="font-size: 1.5rem; color: #f59e0b;"></i>
                        <div>
                            <div style="font-weight: 600; margin-bottom: 0.25rem;">Location</div>
                            <div>Building the Future, Worldwide</div>
                        </div>
                    </div>
                    <div style="margin-top: 2rem;">
                        <h4>Follow Our Journey</h4>
                        <div class="social-links">
                            <a href="https://instagram.com/aurexislabs" target="_blank" class="social-link">
                                <i class="fab fa-instagram"></i>
                            </a>
                            <a href="mailto:aarushagrawal240411@gmail.com" class="social-link">
                                <i class="fas fa-envelope"></i>
                            </a>
                            <a href="#" class="social-link">
                                <i class="fab fa-linkedin"></i>
                            </a>
                            <a href="#" class="social-link">
                                <i class="fab fa-twitter"></i>
                            </a>
                        </div>
                    </div>
                </div>
                <form class="contact-form reveal">
                    <div class="form-group">
                        <input type="text" placeholder="Your Name" required>
                    </div>
                    <div class="form-group">
                        <input type="email" placeholder="Your Email" required>
                    </div>
                    <div class="form-group">
                        <input type="text" placeholder="Subject" required>
                    </div>
                    <div class="form-group">
                        <textarea rows="5" placeholder="Tell us about your project..." required></textarea>
                    </div>
                    <button type="submit" class="cta-button" style="width: 100%; font-size: 1.1rem;">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <img src="https://i.postimg.cc/ZnvffBCg/1dcdb7f7-de7b-48ae-920e-9869e990031b-7C361840-19A8-47AC-B944-81763F2E43D9.jpg" alt="Aurexis Labs" style="height: 40px; margin-bottom: 1rem;">
                    <p style="max-width: 300px; margin-bottom: 1rem;">Aurexis Labs. Redefining innovation through technology. Founded by Aarush Agrawal.</p>
                    <div class="social-links">
                        <a href="https://instagram.com/aurexislabs" target="_blank" class="social-link">
                            <i class="fab fa-instagram"></i>
                        </a>
                    </div>
                </div>
                <div class="footer-section">
                    <h4>Quick Links</h4>
                    <ul style="list-style: none;">
                        <li><a href="#home" style="color: #cbd5e1; text-decoration: none;">Home</a></li>
                        <li><a href="#about" style="color: #cbd5e1; text-decoration: none;">About</a></li>
                        <li><a href="#services" style="color: #cbd5e1; text-decoration: none;">Services</a></li>
                        <li><a href="#contact" style="color: #cbd5e1; text-decoration: none;">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h4>Services</h4>
                    <ul style="list-style: none;">
                        <li><a href="#" style="color: #cbd5e1; text-decoration: none;">AI & ML</a></li>
                        <li><a href="#" style="color: #cbd5e1; text-decoration: none;">Web Development</a></li>
                        <li><a href="#" style="color: #cbd5e1; text-decoration: none;">Mobile Apps</a></li>
                        <li><a href="#" style="color: #cbd5e1; text-decoration: none;">Cloud Solutions</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h4>Company</h4>
                    <p>Founded by <strong>Aarush Agrawal</strong></p>
                    <p><strong>aarushagrawal240411@gmail.com</strong></p>
                    <p style="margin-top: 1rem; font-size: 0.9rem; opacity: 0.8;">© 2024 Aurexis Labs. All rights reserved.</p>
                </div>
            </div>
            <div class="footer-bottom">
                <p>Made with ❤️ by Aurexis Labs | Designed for the Future</p>
            </div>
        </div>
    </footer>

    <script>
        // Navbar scroll effect
        window.addEventListener('scroll', () => {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 100) {
                navbar.style.background = 'rgba(255, 255, 255, 0.98)';
                navbar.style.boxShadow = '0 5px 30px rgba(0,0,0,0.15)';
            } else {
                navbar.style.background = 'rgba(255, 255, 255, 0.95)';
                navbar.style.boxShadow = '0 2px 20px rgba(0,0,0,0.1)';
            }
        });

        // Smooth scrolling
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

        // Scroll reveal animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.reveal').forEach(el => {
            observer.observe(el);
        });

        // Hero text typing effect
        const heroText = "Future-Ready Innovation";
        let i = 0;
        const heroH1 = document.querySelector('.hero h1');
        function typeWriter() {
            if (i < heroText.length) {
                heroH1.textContent = heroText.slice(0, i + 1);
                i++;
                setTimeout(typeWriter, 100);
            }
        }
        setTimeout(typeWriter, 500);

        // Form submission
        document.querySelector('.contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! We\'ll get back to you soon. 🚀');
            this.reset();
        });

        // Particle animation for hero
        function createParticle() {
            const particle = document.createElement('div');
            particle.style.cssText = `
                position: absolute;
                width: 4px;
                height: 4px;
                background: linear-gradient(45deg, #6366f1, #8b5cf6);
                border-radius: 50%;
                pointer-events: none;
                left: ${Math.random() * 100}vw;
                top: 100vh;
                animation: floatUp 6s linear infinite;
                z-index: 1;
            `;
            particle.innerHTML = '•';
            document.querySelector('.hero').appendChild(particle);

            setTimeout(() => {
                particle.remove();
            }, 6000);
        }

        function createParticleAnimation() {
            setInterval(createParticle, 300);
        }

        const style = document.createElement('style');
        style.textContent = `
            @keyframes floatUp {
                to {
                    transform: translateY(-100vh) rotate(360deg);
                    opacity: 0;
                }
            }
        `;
        document.head.appendChild(style);

        setTimeout(createParticleAnimation, 1000);

        // Stats counter animation
        function animateStats() {
            const stats = document.querySelectorAll('.stat-number');
            stats.forEach(stat => {
                const target = parseInt(stat.textContent);
                let current = 0;
                const increment = target / 100;
                const timer = setInterval(() => {
                    current += increment;
                    if (current >= target) {
                        stat.textContent = target;
                        clearInterval(timer);
                    } else {
                        stat.textContent = Math.floor(current);
                    }
                }, 20);
            });
        }

        const statsObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    animateStats();
                    statsObserver.unobserve(entry.target);
                }
            });
        });

        document.querySelector('.stats')?.parentElement && statsObserver.observe(document.querySelector('.stats')?.parentElement);
    </script>
</body>
</html>
