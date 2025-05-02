<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pythoniacs-Codebook</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #FF5733;
            --secondary: #4CAF50;
            --dark: #333;
            --light: #f8f9fa;
            --accent: #6C63FF;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f5f5f5;
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        section {
            padding: 60px 0;
        }
        
        h1, h2, h3 {
            font-family: 'Montserrat', sans-serif;
            margin-bottom: 20px;
        }
        
        /* Header Styles */
        .hero {
            text-align: center;
            padding: 80px 0;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path fill="rgba(255,255,255,0.3)" d="M0,0 L100,0 L100,100 L0,100 Z" /></svg>');
            opacity: 0.1;
            z-index: 0;
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            color: var(--primary);
            text-shadow: 4px 4px 8px rgba(0, 0, 0, 0.2);
            margin-bottom: 30px;
            animation: fadeIn 1.5s ease-out;
        }
        
        .hero p {
            font-size: 1.4rem;
            max-width: 900px;
            margin: 0 auto 40px;
            animation: slideUp 1.5s ease-out;
        }
        
        /* Section Styles */
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 50px;
            position: relative;
        }
        
        .section-title::after {
            content: "";
            display: block;
            width: 100px;
            height: 4px;
            background: var(--primary);
            margin: 15px auto;
            border-radius: 2px;
        }
        
        .section-subtitle {
            color: var(--secondary);
            font-size: 2rem;
            margin-bottom: 30px;
        }
        
        /* Badges Section */
        .badges-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin: 30px 0;
        }
        
        .badge {
            display: inline-block;
            padding: 8px 12px;
            border-radius: 5px;
            font-size: 0.9rem;
            font-weight: 600;
            color: white;
            text-decoration: none;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        /* About Section */
        .about-box {
            border: 2px solid var(--secondary);
            border-radius: 15px;
            padding: 40px;
            background-color: #e8f5e9;
            box-shadow: 0 6px 10px rgba(0, 0, 0, 0.1);
            max-width: 800px;
            margin: 0 auto;
        }
        
        .feature-list {
            list-style-type: none;
            font-size: 1.3rem;
            margin: 25px 0;
        }
        
        .feature-list li {
            margin-bottom: 15px;
            padding-left: 30px;
            position: relative;
        }
        
        .feature-list li::before {
            content: "💡";
            position: absolute;
            left: 0;
        }
        
        /* Projects Section */
        .projects-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .project-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-title {
            color: var(--primary);
            margin-bottom: 10px;
        }
        
        /* Stats Section */
        .stats-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
        }
        
        .stat-item {
            flex: 1;
            min-width: 250px;
            max-width: 350px;
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s;
        }
        
        .stat-item:hover {
            transform: scale(1.05);
        }
        
        /* Contact Section */
        .contact-links {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-top: 30px;
        }
        
        /* Footer */
        footer {
            text-align: center;
            padding: 40px 0;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            margin-top: 60px;
        }
        
        footer h1 {
            color: var(--primary);
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes slideUp {
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
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .about-box {
                padding: 20px;
            }
            
            .feature-list {
                font-size: 1.1rem;
            }
        }
        
        /* Divider */
        .divider {
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--primary), transparent);
            margin: 40px auto;
            max-width: 800px;
            border: none;
        }
        
        /* Highlight */
        .highlight {
            color: var(--primary);
            font-weight: 700;
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>🌟 Welcome to Pythoniacs-Codebook! 🚀</h1>
            <p>
                At <span class="highlight">Pythoniacs-Codebook</span>, we believe in the power of <span class="highlight">technology, coding, and innovation</span> to transform ideas into reality. Whether you're a seasoned developer or a curious beginner, we're here to inspire, educate, and create! Let's build the future, together! 💡🚀
            </p>
        </div>
    </section>
    
    <!-- Technologies Section -->
    <section class="container">
        <h2 class="section-title">💻 Things I Code With</h2>
        <div class="badges-container">
            <span class="badge" style="background-color: #3776AB;">Python</span>
            <span class="badge" style="background-color: #00599C;">C++</span>
            <span class="badge" style="background-color: #007396;">Java</span>
            <span class="badge" style="background-color: #F7DF1E; color: black;">JavaScript</span>
            <span class="badge" style="background-color: #FF6F00;">TensorFlow</span>
            <span class="badge" style="background-color: #D00000;">Keras</span>
            <span class="badge" style="background-color: #F7931E;">Scikit-learn</span>
            <span class="badge" style="background-color: #150458;">Pandas</span>
            <span class="badge" style="background-color: #013243;">NumPy</span>
            <span class="badge" style="background-color: #3776AB;">Matplotlib</span>
            <span class="badge" style="background-color: #4479A1;">MySQL</span>
            <span class="badge" style="background-color: #005571;">NoSQL</span>
            <span class="badge" style="background-color: #232F3E;">AWS</span>
            <span class="badge" style="background-color: #E34F26;">HTML5</span>
            <span class="badge" style="background-color: #1572B6;">CSS3</span>
            <span class="badge" style="background-color: #7952B3;">Bootstrap</span>
            <span class="badge" style="background-color: #000000;">Next.js</span>
            <span class="badge" style="background-color: #000000;">Flask</span>
            <span class="badge" style="background-color: #F05032;">Git</span>
            <span class="badge" style="background-color: #FF8C00;">Jupyter Notebook</span>
            <span class="badge" style="background-color: #217346;">Excel</span>
            <span class="badge" style="background-color: #007ACC;">VS Code</span>
            <span class="badge" style="background-color: #000000;">PyCharm</span>
            <span class="badge" style="background-color: #1B6AC6;">NetBeans</span>
            <span class="badge" style="background-color: #00979D;">Arduino</span>
            <span class="badge" style="background-color: #00979D;">ESP32 CAM</span>
            <span class="badge" style="background-color: #FF6F00;">YOLO</span>
            <span class="badge" style="background-color: #000000;">SSD</span>
            <span class="badge" style="background-color: #FF6F00;">AI/ML</span>
            <span class="badge" style="background-color: #FF0000;">Deep Learning</span>
            <span class="badge" style="background-color: #4CAF50;">Data Analytics</span>
            <span class="badge" style="background-color: #007396;">Object Detection</span>
            <span class="badge" style="background-color: #000000;">Image Processing</span>
        </div>
    </section>
    
    <hr class="divider">
    
    <!-- About Section -->
    <section class="container">
        <h2 class="section-title">💡 About Us</h2>
        <div class="about-box">
            <ul class="feature-list">
                <li>Simplify complex concepts with <strong>easy-to-follow tutorials</strong> 📚</li>
                <li>Spark creativity through <strong>coding challenges</strong> 💻</li>
                <li>Explore the <strong>latest tech trends</strong> 🌐</li>
                <li>Showcase inspiring <strong>projects</strong> 🚀</li>
            </ul>
            <p style="font-size: 1.2rem; text-align: center; margin-top: 30px; font-weight: bold;">
                Let's build a community that celebrates innovation and empowers everyone to achieve their tech dreams.
            </p>
        </div>
    </section>
    
    <hr class="divider">
    
    <!-- Offerings Section -->
    <section class="container">
        <h2 class="section-title">🚀 What We Offer</h2>
        <div class="about-box">
            <ul class="feature-list">
                <li><strong>In-Depth Tutorials</strong>: Learn step-by-step with examples and projects.</li>
                <li><strong>Coding Challenges</strong>: Test your skills and grow with real-world problems.</li>
                <li><strong>Tech Trends</strong>: Stay updated on the latest advancements in technology.</li>
                <li><strong>Project Showcases</strong>: Discover creative and inspiring projects.</li>
            </ul>
        </div>
    </section>
    
    <hr class="divider">
    
    <!-- Projects Section -->
    <section class="container">
        <h2 class="section-title">🎯 Featured Projects</h2>
        <div class="projects-container">
            <div class="project-card">
                <div class="project-content">
                    <h3 class="project-title">Colorful Spiral 🎨</h3>
                    <p>Interactive Python Turtle Graphics with stunning visuals and music.</p>
                    <a href="https://github.com/C7-CodeWithMe/Colorful-Spiral-Script-" target="_blank" style="color: var(--primary); text-decoration: none; font-weight: bold; display: inline-block; margin-top: 15px;">View Project →</a>
                </div>
            </div>
        </div>
    </section>
    
    <hr class="divider">
    
    <!-- Contact Section -->
    <section class="container">
        <h2 class="section-title">🌐 Connect with Us</h2>
        <div class="badges-container">
            <a href="https://www.youtube.com/channel/UCtgTRDzqbaRtpyNzy1fu1vA" target="_blank" class="badge" style="background-color: #FF0000;">YouTube</a>
            <a href="https://github.com/Pythoniacs-Codebook" target="_blank" class="badge" style="background-color: #181717;">GitHub</a>
            <a href="https://wa.me/message/V33NEXMUPK3CJ1" target="_blank" class="badge" style="background-color: #25D366;">WhatsApp</a>
            <a href="mailto:code2with2me@gmail.com" target="_blank" class="badge" style="background-color: #D14836;">Email</a>
            <a href="https://web.facebook.com/profile.php?id=61566373615325" target="_blank" class="badge" style="background-color: #1877F2;">Facebook</a>
            <a href="https://www.tiktok.com/@pythoniacs_codebook?is_from_webapp=1&sender_device=pc" target="_blank" class="badge" style="background-color: #000000;">TikTok</a>
            <a href="https://web.facebook.com/share/g/1D9uyWSGQp" target="_blank" class="badge" style="background-color: #1877F2;">Facebook Group</a>
        </div>
    </section>
    
    <hr class="divider">
    
    <!-- Fun Facts Section -->
    <section class="container">
        <h2 class="section-title">🎉 Fun Facts</h2>
        <div class="about-box">
            <ul class="feature-list">
                <li>We love breaking down tech barriers for everyone!</li>
                <li>Creativity and problem-solving are at the heart of what we do.</li>
                <li>Together, we can shape the future of technology!</li>
            </ul>
        </div>
    </section>
    
    <hr class="divider">
    
    <!-- Stats Section -->
    <section class="container">
        <h2 class="section-title">📊 GitHub Stats & Activity</h2>
        <div class="stats-container">
            <img src="https://github-readme-stats.vercel.app/api?username=Pythoniacs-Codebook&show_icons=true&theme=radical" alt="GitHub Stats" class="stat-item">
            <img src="https://streak-stats.demolab.com/?user=Pythoniacs-Codebook&theme=radical" alt="GitHub Streak Stats" class="stat-item">
            <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Pythoniacs-Codebook&layout=compact&theme=radical" alt="Top Languages" class="stat-item">
        </div>
        <div style="text-align: center; margin-top: 30px;">
            <a href="https://github.com/Pythoniacs-Codebook" target="_blank" class="badge" style="background-color: #12100E; font-size: 1.1rem; padding: 12px 20px;">
                Explore My Projects
            </a>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <h1>🌟 Pythoniacs-Codebook – Where Ideas Turn Into Reality! 🌟</h1>
    </footer>
</body>
</html>
