<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nikitha Shiva - Senior Data Engineer Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #667eea;
            --secondary-color: #764ba2;
            --accent-color: #f093fb;
            --text-light: #ffffff;
            --text-dark: #333333;
            --bg-dark: #1a1a1a;
            --bg-light: #f8f9fa;
            --card-bg: rgba(255, 255, 255, 0.1);
            --border-radius: 15px;
            --shadow: 0 20px 40px rgba(0,0,0,0.1);
            --gradient-1: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            --gradient-2: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            --gradient-3: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(26, 26, 26, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            transition: all 0.3s ease;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 2rem;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            background: var(--gradient-1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: var(--text-light);
            text-decoration: none;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-links a:hover {
            color: var(--primary-color);
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            background: var(--gradient-1);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--text-light);
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
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000"><polygon fill="rgba(255,255,255,0.05)" points="0,0 1000,300 1000,1000 0,700"/></svg>');
        }

        .hero-content {
            max-width: 800px;
            padding: 0 2rem;
            position: relative;
            z-index: 2;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            font-weight: 800;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            animation: fadeInUp 1s ease-out;
        }

        .hero .subtitle {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease-out 0.2s both;
        }

        .hero .description {
            font-size: 1.2rem;
            margin-bottom: 3rem;
            line-height: 1.8;
            animation: fadeInUp 1s ease-out 0.4s both;
        }

        .cta-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease-out 0.6s both;
        }

        .btn {
            padding: 12px 30px;
            border: none;
            border-radius: var(--border-radius);
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }

        .btn-primary {
            background: rgba(255, 255, 255, 0.2);
            color: var(--text-light);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        .btn-primary:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-2px);
        }

        .btn-secondary {
            background: transparent;
            color: var(--text-light);
            border: 2px solid rgba(255, 255, 255, 0.5);
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateY(-2px);
        }

        /* Stats Section */
        .stats {
            background: var(--bg-dark);
            color: var(--text-light);
            padding: 4rem 0;
        }

        .stats-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            padding: 0 2rem;
        }

        .stat-item {
            text-align: center;
            padding: 2rem;
            background: var(--card-bg);
            border-radius: var(--border-radius);
            backdrop-filter: blur(10px);
            transition: transform 0.3s ease;
        }

        .stat-item:hover {
            transform: translateY(-5px);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            background: var(--gradient-3);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 1rem;
            opacity: 0.8;
        }

        /* About Section */
        .about {
            padding: 6rem 0;
            background: var(--bg-light);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            background: var(--gradient-1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 4rem;
            align-items: center;
        }

        .tech-stack {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1rem;
            margin-top: 2rem;
        }

        .tech-item {
            background: var(--gradient-2);
            color: var(--text-light);
            padding: 1rem;
            border-radius: var(--border-radius);
            text-align: center;
            font-weight: 600;
            transition: transform 0.3s ease;
        }

        .tech-item:hover {
            transform: scale(1.05);
        }

        /* Projects Section */
        .projects {
            padding: 6rem 0;
            background: var(--bg-dark);
            color: var(--text-light);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .project-card {
            background: var(--card-bg);
            backdrop-filter: blur(10px);
            border-radius: var(--border-radius);
            padding: 2rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: var(--gradient-3);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow);
        }

        .project-card:hover::before {
            opacity: 1;
        }

        .project-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            background: var(--gradient-3);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .project-title {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--text-light);
        }

        .project-description {
            margin-bottom: 1.5rem;
            opacity: 0.8;
            line-height: 1.6;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1.5rem;
        }

        .tech-tag {
            background: rgba(255, 255, 255, 0.1);
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .project-links {
            display: flex;
            gap: 1rem;
        }

        .project-link {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .project-link:hover {
            color: var(--accent-color);
            transform: translateY(-1px);
        }

        /* Contact Section */
        .contact {
            padding: 6rem 0;
            background: var(--gradient-1);
            color: var(--text-light);
            text-align: center;
        }

        .contact-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 3rem;
            flex-wrap: wrap;
        }

        .contact-link {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            color: var(--text-light);
            text-decoration: none;
            font-size: 1.2rem;
            transition: all 0.3s ease;
        }

        .contact-link:hover {
            transform: translateY(-2px);
            opacity: 0.8;
        }

        /* Footer */
        footer {
            background: var(--bg-dark);
            color: var(--text-light);
            text-align: center;
            padding: 2rem 0;
            opacity: 0.8;
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

        @keyframes float {
            0%, 100% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-20px);
            }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero .subtitle {
                font-size: 1.2rem;
            }
            
            .about-content {
                grid-template-columns: 1fr;
                gap: 2rem;
            }
            
            .nav-links {
                display: none;
            }
            
            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .stats-container {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Smooth scroll */
        html {
            scroll-behavior: smooth;
        }

        /* Loading animation */
        .loading {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--gradient-1);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            opacity: 1;
            transition: opacity 0.5s ease;
        }

        .loading.hide {
            opacity: 0;
            pointer-events: none;
        }

        .spinner {
            width: 50px;
            height: 50px;
            border: 3px solid rgba(255, 255, 255, 0.3);
            border-top: 3px solid white;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <!-- Loading Screen -->
    <div class="loading" id="loading">
        <div class="spinner"></div>
    </div>

    <!-- Navigation -->
    <nav id="navbar">
        <div class="nav-container">
            <div class="logo">Nikitha Shiva</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Nikitha Shiva</h1>
            <p class="subtitle">Senior Data Engineer | AWS Specialist | 5+ Years Experience</p>
            <p class="description">
                Designing scalable data pipelines processing 500M+ daily records with expertise in 
                AWS, Azure, and cutting-edge ML technologies. Proven track record of delivering 
                90% accurate ML models and 30% cost reductions in production environments.
            </p>
            <div class="cta-buttons">
                <a href="#projects" class="btn btn-primary">
                    <i class="fas fa-rocket"></i> View My Work
                </a>
                <a href="https://www.linkedin.com/in/nikitha-reddy3187" target="_blank" class="btn btn-secondary">
                    <i class="fab fa-linkedin"></i> Connect on LinkedIn
                </a>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <div class="stats-container">
            <div class="stat-item">
                <div class="stat-number">500M+</div>
                <div class="stat-label">Daily Records Processed</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">90%</div>
                <div class="stat-label">ML Model Accuracy</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">30%</div>
                <div class="stat-label">Cost Reduction Achieved</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">60ms</div>
                <div class="stat-label">Latency Reduction</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">5+</div>
                <div class="stat-label">Years Experience</div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <h3>Passionate Data Engineer</h3>
                    <p>
                        With 5+ years of progressive experience in data engineering, I specialize in building 
                        modern, scalable data architectures on AWS and Azure. My expertise spans the entire 
                        data lifecycle - from ingestion and processing to advanced analytics and machine learning.
                    </p>
                    <p>
                        I have successfully delivered enterprise-scale solutions processing over 500 million 
                        records daily, achieved 90% accuracy in ML models, and reduced operational costs by 
                        up to 30% through intelligent automation and optimization.
                    </p>
                    <h4>Current Focus:</h4>
                    <ul>
                        <li>🏗️ Modern Data Lake Architectures</li>
                        <li>🤖 ML/AI Pipeline Development</li>
                        <li>⚡ Real-time Streaming Systems</li>
                        <li>📄 Intelligent Document Processing</li>
                        <li>🛡️ Data Governance & Security</li>
                    </ul>
                </div>
                <div class="tech-stack">
                    <div class="tech-item">AWS</div>
                    <div class="tech-item">Azure</div>
                    <div class="tech-item">Python</div>
                    <div class="tech-item">Apache Spark</div>
                    <div class="tech-item">Kafka</div>
                    <div class="tech-item">Airflow</div>
                    <div class="tech-item">Terraform</div>
                    <div class="tech-item">Docker</div>
                    <div class="tech-item">Snowflake</div>
                    <div class="tech-item">TensorFlow</div>
                    <div class="tech-item">XGBoost</div>
                    <div class="tech-item">Databricks</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section class="projects" id="projects">
        <div class="container">
            <h2 class="section-title">Featured Projects</h2>
            <div class="projects-grid">
                
                <!-- Project 1: AWS Data Lake -->
                <div class="project-card">
                    <div class="project-icon">🏗️</div>
                    <h3 class="project-title">AWS Modern Data Lake Foundation</h3>
                    <p class="project-description">
                        Enterprise-grade lakehouse architecture implementing Bronze→Silver→Gold medallion pattern 
                        with comprehensive Terraform infrastructure, achieving 15% data quality improvement and 
                        30% cost reduction.
                    </p>
                    <div class="project-tech">
                        <span class="tech-tag">AWS</span>
                        <span class="tech-tag">Terraform</span>
                        <span class="tech-tag">Apache Spark</span>
                        <span class="tech-tag">Delta Lake</span>
                        <span class="tech-tag">Python</span>
                    </div>
                    <div class="project-links">
                        <a href="https://github.com/nikitha-shiva/aws-modern-data-lake-foundation" target="_blank" class="project-link">
                            <i class="fab fa-github"></i> View Code
                        </a>
                    </div>
                </div>

                <!-- Project 2: ML Pipeline -->
                <div class="project-card">
                    <div class="project-icon">🤖</div>
                    <h3 class="project-title">Customer Retention ML Pipeline</h3>
                    <p class="project-description">
                        End-to-end ML pipeline achieving 90% accuracy in customer retention predictions with 
                        real-time serving API, automated retraining, and comprehensive drift detection using 
                        XGBoost and advanced feature engineering.
                    </p>
                    <div class="project-tech">
                        <span class="tech-tag">XGBoost</span>
                        <span class="tech-tag">MLflow</span>
                        <span class="tech-tag">FastAPI</span>
                        <span class="tech-tag">Airflow</span>
                        <span class="tech-tag">Redis</span>
                    </div>
                    <div class="project-links">
                        <a href="https://github.com/nikitha-shiva/customer-retention-ml-pipeline" target="_blank" class="project-link">
                            <i class="fab fa-github"></i> View Code
                        </a>
                    </div>
                </div>

                <!-- Project 3: Real-time Streaming -->
                <div class="project-card">
                    <div class="project-icon">🌊</div>
                    <h3 class="project-title">Real-Time Network Monitoring</h3>
                    <p class="project-description">
                        High-throughput streaming platform with Kafka and Spark achieving 30% reliability 
                        improvement and 60ms latency reduction. Features auto-scaling, anomaly detection, 
                        and comprehensive monitoring dashboard.
                    </p>
                    <div class="project-tech">
                        <span class="tech-tag">Apache Kafka</span>
                        <span class="tech-tag">Apache Spark</span>
                        <span class="tech-tag">Docker</span>
                        <span class="tech-tag">Kubernetes</span>
                        <span class="tech-tag">Azure</span>
                    </div>
                    <div class="project-links">
                        <a href="https://github.com/nikitha-shiva/real-time-network-monitoring-kafka" target="_blank" class="project-link">
                            <i class="fab fa-github"></i> View Code
                        </a>
                    </div>
                </div>

                <!-- Project 4: Document Processing -->
                <div class="project-card">
                    <div class="project-icon">📄</div>
                    <h3 class="project-title">Intelligent Document Processing</h3>
                    <p class="project-description">
                        Advanced document processing pipeline handling complex Excel files and PDFs with OCR, 
                        table extraction, and automated schema mapping. Perfect solution for transforming 
                        messy files into trusted, analytics-ready data.
                    </p>
                    <div class="project-tech">
                        <span class="tech-tag">AWS Textract</span>
                        <span class="tech-tag">Python</span>
                        <span class="tech-tag">Pandas</span>
                        <span class="tech-tag">OpenCV</span>
                        <span class="tech-tag">Lambda</span>
                    </div>
                    <div class="project-links">
                        <a href="https://github.com/nikitha-shiva/intelligent-document-processing" target="_blank" class="project-link">
                            <i class="fab fa-github"></i> View Code
                        </a>
                    </div>
                </div>

                <!-- Project 5: Spotify Analytics -->
                <div class="project-card">
                    <div class="project-icon">🎵</div>
                    <h3 class="project-title">Spotify Data Analytics Platform</h3>
                    <p class="project-description">
                        End-to-end ETL system processing 500M+ daily records with Snowflake and AWS, 
                        delivering music recommendation insights with 85% accuracy. Features real-time 
                        processing and comprehensive analytics dashboard.
                    </p>
                    <div class="project-tech">
                        <span class="tech-tag">AWS</span>
                        <span class="tech-tag">Snowflake</span>
                        <span class="tech-tag">Python</span>
                        <span class="tech-tag">AWS Glue</span>
                        <span class="tech-tag">S3</span>
                    </div>
                    <div class="project-links">
                        <a href="https://github.com/nikitha-shiva/spotify-end-end-project" target="_blank" class="project-link">
                            <i class="fab fa-github"></i> View Code
                        </a>
                    </div>
                </div>

                <!-- Project 6: Spotify Data -->
                <div class="project-card">
                    <div class="project-icon">📊</div>
                    <h3 class="project-title">Spotify Data Analysis</h3>
                    <p class="project-description">
                        Comprehensive data analysis and visualization of Spotify streaming patterns, 
                        user behavior analytics, and music trend insights using advanced statistical 
                        methods and machine learning techniques.
                    </p>
                    <div class="project-tech">
                        <span class="tech-tag">Jupyter</span>
                        <span class="tech-tag">Pandas</span>
                        <span class="tech-tag">Matplotlib</span>
                        <span class="tech-tag">Seaborn</span>
                        <span class="tech-tag">Scikit-Learn</span>
                    </div>
                    <div class="project-links">
                        <a href="https://github.com/nikitha-shiva/Spotify_data" target="_blank" class="project-link">
                            <i class="fab fa-github"></i> View Code
                        </a>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="contact-content">
                <h2 class="section-title">Let's Build Something Amazing Together</h2>
                <p>
                    I'm always interested in discussing new opportunities, challenging projects, 
                    and innovative data solutions. Let's connect and explore how we can transform 
                    your data into actionable insights.
                </p>
                <div class="contact-links">
                    <a href="https://www.linkedin.com/in/nikitha-reddy3187" target="_blank" class="contact-link">
                        <i class="fab fa-linkedin"></i> LinkedIn
                    </a>
                    <a href="https://github.com/nikitha-shiva" target="_blank" class="contact-link">
                        <i class="fab fa-github"></i> GitHub
                    </a>
                    <a href="mailto:nikitha@example.com" class="contact-link">
                        <i class="fas fa-envelope"></i> Email
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2024 Nikitha Shiva. Crafted with ❤️ and lots of ☕</p>
        </div>
    </footer>

    <script>
        // Loading screen
        window.addEventListener('load', function() {
            document.getElementById('loading').classList.add('hide');
        });

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

        // Navbar background change on scroll
        window.addEventListener('scroll', function() {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 100) {
                navbar.style.background = 'rgba(26, 26, 26, 0.98)';
            } else {
                navbar.style.background = 'rgba(26, 26, 26, 0.95)';
            }
        });

        // Animate elements on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animation = 'fadeInUp 0.6s ease-out forwards';
                }
            });
        }, observerOptions);

        // Observe all project cards and other elements
        document.addEventListener('DOMContentLoaded', function() {
            document.querySelectorAll('.project-card, .stat-item, .about-content').forEach(el => {
                observer.observe(el);
            });
        });

        // Add typing effect to hero title
        function typeWriter(element, text, speed = 100) {
            let i = 0;
            element.innerHTML = '';
            function type() {
                if (i < text.length) {
                    element.innerHTML += text.charAt(i);
                    i++;
                    setTimeout(type, speed);
                }
            }
            type();
        }

        // Initialize typing effect when page loads
        document.addEventListener('DOMContentLoaded', function() {
            const heroTitle = document.querySelector('.hero h1');
            setTimeout(() => {
                typeWriter(heroTitle, 'Nikitha Shiva', 150);
            }, 1000);
