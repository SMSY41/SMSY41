<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shafi Yamin - Data Analyst Portfolio</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap');

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 50%, #7e22ce 100%);
            color: #333;
            overflow-x: hidden;
        }

        /* Animated Background Shapes */
        .bg-shapes {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            overflow: hidden;
        }

        .shape {
            position: absolute;
            opacity: 0.1;
            animation: floatShape 20s infinite ease-in-out;
        }

        .shape-1 {
            top: 10%;
            left: 10%;
            width: 200px;
            height: 200px;
            background: linear-gradient(45deg, #4ade80, #22d3ee);
            border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
            animation-delay: 0s;
        }

        .shape-2 {
            top: 60%;
            right: 15%;
            width: 150px;
            height: 150px;
            background: linear-gradient(45deg, #f59e0b, #ef4444);
            border-radius: 70% 30% 30% 70% / 70% 70% 30% 30%;
            animation-delay: 3s;
        }

        .shape-3 {
            bottom: 20%;
            left: 20%;
            width: 180px;
            height: 180px;
            background: linear-gradient(45deg, #8b5cf6, #ec4899);
            border-radius: 50% 50% 30% 70% / 50% 30% 70% 50%;
            animation-delay: 6s;
        }

        @keyframes floatShape {
            0%, 100% { transform: translate(0, 0) rotate(0deg); }
            33% { transform: translate(50px, -50px) rotate(120deg); }
            66% { transform: translate(-30px, 30px) rotate(240deg); }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
            position: relative;
            z-index: 1;
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 100px 20px;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 30px;
            margin-bottom: 60px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 6px;
            background: linear-gradient(90deg, #4ade80, #22d3ee, #8b5cf6, #ec4899);
            background-size: 400% 100%;
            animation: gradientSlide 8s linear infinite;
        }

        @keyframes gradientSlide {
            0% { background-position: 0% 50%; }
            100% { background-position: 400% 50%; }
        }

        .profile-image {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            margin: 0 auto 30px;
            background: linear-gradient(135deg, #4ade80, #22d3ee);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 80px;
            box-shadow: 0 10px 30px rgba(74, 222, 128, 0.4);
            animation: profilePulse 3s ease-in-out infinite;
        }

        @keyframes profilePulse {
            0%, 100% { transform: scale(1); box-shadow: 0 10px 30px rgba(74, 222, 128, 0.4); }
            50% { transform: scale(1.05); box-shadow: 0 15px 40px rgba(74, 222, 128, 0.6); }
        }

        .hero h1 {
            font-size: 4em;
            font-weight: 700;
            background: linear-gradient(135deg, #1e3c72, #2a5298, #7e22ce);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 20px;
            animation: fadeInDown 1s ease-out;
        }

        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .hero .subtitle {
            font-size: 1.8em;
            color: #64748b;
            margin-bottom: 30px;
            font-weight: 300;
            animation: fadeInUp 1s ease-out 0.3s both;
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .hero .tagline {
            font-size: 1.2em;
            color: #94a3b8;
            max-width: 700px;
            margin: 0 auto;
            line-height: 1.8;
            animation: fadeInUp 1s ease-out 0.6s both;
        }

        /* Section Styling */
        .section {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 30px;
            padding: 60px 40px;
            margin-bottom: 60px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .section:hover {
            transform: translateY(-10px);
            box-shadow: 0 30px 80px rgba(0, 0, 0, 0.3);
        }

        .section-header {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title {
            font-size: 3em;
            font-weight: 700;
            background: linear-gradient(135deg, #1e3c72, #7e22ce);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 15px;
            position: relative;
            display: inline-block;
        }

        .section-subtitle {
            font-size: 1.2em;
            color: #94a3b8;
        }

        /* Skills Grid - Modern Cards */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .skill-card {
            background: linear-gradient(135deg, #f8fafc, #f1f5f9);
            border-radius: 20px;
            padding: 40px 30px;
            text-align: center;
            transition: all 0.3s;
            border: 2px solid transparent;
            position: relative;
            overflow: hidden;
        }

        .skill-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            border-radius: 20px;
            padding: 2px;
            background: linear-gradient(135deg, #4ade80, #22d3ee, #8b5cf6);
            -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
            -webkit-mask-composite: xor;
            mask-composite: exclude;
            opacity: 0;
            transition: opacity 0.3s;
        }

        .skill-card:hover::before {
            opacity: 1;
        }

        .skill-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
        }

        .skill-category {
            font-size: 1.5em;
            font-weight: 600;
            color: #1e3c72;
            margin-bottom: 20px;
        }

        .skill-items {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            justify-content: center;
        }

        .skill-badge {
            background: linear-gradient(135deg, #4ade80, #22d3ee);
            color: white;
            padding: 10px 20px;
            border-radius: 25px;
            font-size: 0.95em;
            font-weight: 500;
            box-shadow: 0 4px 15px rgba(74, 222, 128, 0.3);
            transition: all 0.3s;
        }

        .skill-badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(74, 222, 128, 0.5);
        }

        .skill-card:nth-child(2) .skill-badge {
            background: linear-gradient(135deg, #8b5cf6, #ec4899);
            box-shadow: 0 4px 15px rgba(139, 92, 246, 0.3);
        }

        .skill-card:nth-child(2) .skill-badge:hover {
            box-shadow: 0 6px 20px rgba(139, 92, 246, 0.5);
        }

        /* Services - Timeline Style */
        .services-timeline {
            position: relative;
            padding: 20px 0;
        }

        .service-item {
            display: flex;
            gap: 30px;
            margin-bottom: 40px;
            align-items: flex-start;
        }

        .service-icon {
            min-width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #4ade80, #22d3ee);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5em;
            box-shadow: 0 10px 30px rgba(74, 222, 128, 0.3);
            transition: all 0.3s;
        }

        .service-item:nth-child(2) .service-icon {
            background: linear-gradient(135deg, #f59e0b, #ef4444);
            box-shadow: 0 10px 30px rgba(245, 158, 11, 0.3);
        }

        .service-item:nth-child(3) .service-icon {
            background: linear-gradient(135deg, #8b5cf6, #ec4899);
            box-shadow: 0 10px 30px rgba(139, 92, 246, 0.3);
        }

        .service-icon:hover {
            transform: rotate(5deg) scale(1.1);
        }

        .service-content {
            flex: 1;
        }

        .service-title {
            font-size: 1.8em;
            font-weight: 600;
            color: #1e3c72;
            margin-bottom: 15px;
        }

        .service-description {
            color: #64748b;
            line-height: 1.8;
            font-size: 1.1em;
        }

        .service-list {
            list-style: none;
            margin-top: 15px;
        }

        .service-list li {
            padding: 8px 0 8px 30px;
            position: relative;
            color: #64748b;
        }

        .service-list li::before {
            content: "✓";
            position: absolute;
            left: 0;
            color: #4ade80;
            font-weight: bold;
            font-size: 1.2em;
        }

        /* Stats - Modern Counter */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 30px;
        }

        .stat-card {
            background: linear-gradient(135deg, #4ade80, #22d3ee);
            border-radius: 20px;
            padding: 40px 20px;
            text-align: center;
            color: white;
            box-shadow: 0 10px 30px rgba(74, 222, 128, 0.3);
            transition: all 0.3s;
        }

        .stat-card:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 15px 40px rgba(74, 222, 128, 0.5);
        }

        .stat-card:nth-child(2) {
            background: linear-gradient(135deg, #f59e0b, #ef4444);
            box-shadow: 0 10px 30px rgba(245, 158, 11, 0.3);
        }

        .stat-card:nth-child(2):hover {
            box-shadow: 0 15px 40px rgba(245, 158, 11, 0.5);
        }

        .stat-card:nth-child(3) {
            background: linear-gradient(135deg, #8b5cf6, #ec4899);
            box-shadow: 0 10px 30px rgba(139, 92, 246, 0.3);
        }

        .stat-card:nth-child(3):hover {
            box-shadow: 0 15px 40px rgba(139, 92, 246, 0.5);
        }

        .stat-card:nth-child(4) {
            background: linear-gradient(135deg, #06b6d4, #3b82f6);
            box-shadow: 0 10px 30px rgba(6, 182, 212, 0.3);
        }

        .stat-card:nth-child(4):hover {
            box-shadow: 0 15px 40px rgba(6, 182, 212, 0.5);
        }

        .stat-number {
            font-size: 3.5em;
            font-weight: 700;
            margin-bottom: 10px;
        }

        .stat-label {
            font-size: 1.2em;
            font-weight: 300;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Contact Buttons */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }

        .contact-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            padding: 20px 30px;
            background: linear-gradient(135deg, #1e3c72, #2a5298);
            color: white;
            text-decoration: none;
            border-radius: 15px;
            font-size: 1.2em;
            font-weight: 600;
            transition: all 0.3s;
            box-shadow: 0 5px 20px rgba(30, 60, 114, 0.3);
        }

        .contact-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(30, 60, 114, 0.5);
        }

        .contact-btn.linkedin {
            background: linear-gradient(135deg, #0077b5, #00a0dc);
        }

        .contact-btn.youtube {
            background: linear-gradient(135deg, #ff0000, #ff4444);
        }

        .contact-btn.telegram {
            background: linear-gradient(135deg, #0088cc, #00aced);
        }

        .contact-btn.email {
            background: linear-gradient(135deg, #ea4335, #fbbc05);
        }

        .contact-icon {
            font-size: 1.5em;
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 40px 20px;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 30px;
            margin-top: 60px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.2);
        }

        .footer-quote {
            font-size: 1.5em;
            font-style: italic;
            background: linear-gradient(135deg, #1e3c72, #7e22ce);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            font-weight: 600;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5em;
            }

            .hero .subtitle {
                font-size: 1.3em;
            }

            .section-title {
                font-size: 2em;
            }

            .service-item {
                flex-direction: column;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Scroll Animation */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Background Shapes -->
    <div class="bg-shapes">
        <div class="shape shape-1"></div>
        <div class="shape shape-2"></div>
        <div class="shape shape-3"></div>
    </div>

    <div class="container">
        <!-- Hero Section -->
        <div class="hero">
            <div class="profile-image">👨‍💻</div>
            <h1>Shafi Yamin</h1>
            <p class="subtitle">Data Analyst | Python Developer | BI Specialist</p>
            <p class="tagline">
                Transforming complex data into actionable insights through advanced analytics, 
                machine learning, and elegant visualizations. Passionate about solving real-world 
                problems with data-driven solutions.
            </p>
        </div>

        <!-- Skills Section -->
        <div class="section fade-in">
            <div class="section-header">
                <h2 class="section-title">Technical Arsenal</h2>
                <p class="section-subtitle">Tools and technologies I work with daily</p>
            </div>
            <div class="skills-grid">
                <div class="skill-card">
                    <div class="skill-category">📊 Data Analysis</div>
                    <div class="skill-items">
                        <span class="skill-badge">Python</span>
                        <span class="skill-badge">NumPy</span>
                        <span class="skill-badge">Pandas</span>
                        <span class="skill-badge">Scikit-learn</span>
                        <span class="skill-badge">SQL</span>
                    </div>
                </div>
                <div class="skill-card">
                    <div class="skill-category">📈 Visualization & BI</div>
                    <div class="skill-items">
                        <span class="skill-badge">Power BI</span>
                        <span class="skill-badge">Excel</span>
                    </div>
                </div>
                <div class="skill-card">
                    <div class="skill-category">💻 Development</div>
                    <div class="skill-items">
                        <span class="skill-badge">C++</span>
                        <span class="skill-badge">Kotlin</span>
                        <span class="skill-badge">Arduino</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Services Section -->
        <div class="section fade-in">
            <div class="section-header">
                <h2 class="section-title">What I Offer</h2>
                <p class="section-subtitle">Comprehensive data solutions for your business</p>
            </div>
            <div class="services-timeline">
                <div class="service-item">
                    <div class="service-icon">📊</div>
                    <div class="service-content">
                        <h3 class="service-title">Data Analytics & Insights</h3>
                        <p class="service-description">
                            Transform raw data into meaningful insights through comprehensive analysis
                        </p>
                        <ul class="service-list">
                            <li>Interactive Dashboard Development</li>
                            <li>Statistical Analysis & Reporting</li>
                            <li>Business Intelligence Solutions</li>
                        </ul>
                    </div>
                </div>
                <div class="service-item">
                    <div class="service-icon">🤖</div>
                    <div class="service-content">
                        <h3 class="service-title">Machine Learning Solutions</h3>
                        <p class="service-description">
                            Build predictive models and intelligent systems for automated decision-making
                        </p>
                        <ul class="service-list">
                            <li>Predictive Modeling & Forecasting</li>
                            <li>Pattern Recognition & Classification</li>
                            <li>Algorithm Development & Optimization</li>
                        </ul>
                    </div>
                </div>
                <div class="service-item">
                    <div class="service-icon">💾</div>
                    <div class="service-content">
                        <h3 class="service-title">Database & ETL</h3>
                        <p class="service-description">
                            Design and optimize data infrastructure for efficient data management
                        </p>
                        <ul class="service-list">
                            <li>Database Design & Optimization</li>
                            <li>ETL Pipeline Development</li>
                            <li>Data Warehousing Solutions</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>

        <!-- Stats Section -->
        <div class="section fade-in">
            <div class="section-header">
                <h2 class="section-title">GitHub Activity</h2>
                <p class="section-subtitle">Numbers that speak for themselves</p>
            </div>
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-number">50+</div>
                    <div class="stat-label">Projects</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">1000+</div>
                    <div class="stat-label">Commits</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">25+</div>
                    <div class="stat-label">Repositories</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">100+</div>
                    <div class="stat-label">Stars</div>
                </div>
            </div>
        </div>

        <!-- Contact Section -->
        <div class="section fade-in">
            <div class="section-header">
                <h2 class="section-title">Let's Connect</h2>
                <p class="section-subtitle">Reach out for collaborations or just a friendly chat</p>
            </div>
            <div class="contact-grid">
                <a href="#" class="contact-btn linkedin">
                    <span class="contact-icon">💼</span>
                    <span>LinkedIn</span>
                </a>
                <a href="#" class="contact-btn youtube">
                    <span class="contact-icon">▶️</span>
                    <span>YouTube</span>
                </a>
                <a href="#" class="contact-btn telegram">
                    <span class="contact-icon">✈️</span>
                    <span>Telegram</span>
                </a>
                <a href="#" class="contact-btn email">
                    <span class="contact-icon">📧</span>
                    <span>Email</span>
                </a>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p class="footer-quote">
                "In God we trust, all others must bring data." - W. Edwards Deming
            </p>
        </div>
    </div>

    <script>
        // Intersection Observer for Scroll Animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(element => {
            observer.observe(element);
        });

        // Smooth scroll for anchor links
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
    </script>
</body>
</html>
