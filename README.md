<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ayush Kamboj - Mobile Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(-45deg, #1a1a2e, #16213e, #0f3460, #533483);
            background-size: 400% 400%;
            animation: gradientShift 15s ease infinite;
            color: #ffffff;
            line-height: 1.6;
            overflow-x: hidden;
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .header {
            text-align: center;
            margin-bottom: 3rem;
            animation: slideInDown 1s ease-out;
        }

        @keyframes slideInDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .name {
            font-size: 3.5rem;
            font-weight: bold;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #FFD700, #FFA500, #FF6B6B);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: pulse 2s ease-in-out infinite alternate;
            text-shadow: 0 0 30px rgba(255, 215, 0, 0.5);
        }

        @keyframes pulse {
            from { transform: scale(1); }
            to { transform: scale(1.05); }
        }

        .subtitle {
            font-size: 1.5rem;
            opacity: 0.9;
            margin-bottom: 2rem;
        }

        .quote {
            font-style: italic;
            font-size: 1.2rem;
            opacity: 0.8;
            animation: fadeIn 2s ease-in 0.5s both;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 0.8; }
        }

        .section {
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(15px);
            border-radius: 20px;
            padding: 2rem;
            margin-bottom: 2rem;
            border: 1px solid rgba(255, 255, 255, 0.3);
            animation: slideInUp 1s ease-out;
            transition: transform 0.3s ease;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }

        .section:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }

        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .section-title {
            font-size: 2rem;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
            margin-top: 1rem;
        }

        .tech-card {
            background: rgba(255, 255, 255, 0.2);
            padding: 1.5rem;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            transition: all 0.3s ease;
            animation: popIn 0.6s ease-out;
            box-shadow: 0 4px 16px rgba(0, 0, 0, 0.2);
        }

        .tech-card:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: scale(1.05);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
        }

        @keyframes popIn {
            0% {
                opacity: 0;
                transform: scale(0.8);
            }
            100% {
                opacity: 1;
                transform: scale(1);
            }
        }

        .tech-title {
            font-size: 1.3rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
            color: #FFE135;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .skill-tag {
            background: rgba(255, 255, 255, 0.25);
            padding: 0.5rem 1rem;
            border-radius: 25px;
            font-size: 0.9rem;
            border: 1px solid rgba(255, 255, 255, 0.4);
            transition: all 0.3s ease;
            animation: skillFloat 3s ease-in-out infinite;
            font-weight: 500;
            text-shadow: 0 1px 2px rgba(0, 0, 0, 0.3);
        }

        .skill-tag:hover {
            background: rgba(255, 255, 255, 0.4);
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        @keyframes skillFloat {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-5px); }
        }

        .interests {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1rem;
        }

        .interest-item {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            background: rgba(255, 255, 255, 0.15);
            padding: 1rem;
            border-radius: 15px;
            transition: all 0.3s ease;
            animation: bounce 2s ease infinite;
        }

        .interest-item:hover {
            background: rgba(255, 255, 255, 0.25);
            transform: scale(1.1);
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }

        .contact-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
            margin-top: 2rem;
        }

        .contact-btn {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            padding: 1rem 2rem;
            background: rgba(255, 255, 255, 0.2);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            border: 2px solid rgba(255, 255, 255, 0.3);
            transition: all 0.3s ease;
            font-weight: bold;
            animation: glow 2s ease-in-out infinite alternate;
        }

        .contact-btn:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4);
        }

        @keyframes glow {
            from {
                box-shadow: 0 0 20px rgba(255, 255, 255, 0.3);
            }
            to {
                box-shadow: 0 0 30px rgba(255, 255, 255, 0.5);
            }
        }

        .floating-icons {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .floating-icon {
            position: absolute;
            font-size: 2rem;
            opacity: 0.1;
            animation: float 6s ease-in-out infinite;
        }

        .floating-icon:nth-child(1) { top: 20%; left: 10%; animation-delay: 0s; }
        .floating-icon:nth-child(2) { top: 60%; right: 10%; animation-delay: 1s; }
        .floating-icon:nth-child(3) { bottom: 20%; left: 20%; animation-delay: 2s; }
        .floating-icon:nth-child(4) { top: 40%; right: 30%; animation-delay: 3s; }
        .floating-icon:nth-child(5) { bottom: 40%; right: 20%; animation-delay: 4s; }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        .typing-text {
            border-right: 3px solid #FFD700;
            animation: typewriter 4s steps(40) 1s both, blink 0.75s step-end infinite;
            white-space: nowrap;
            overflow: hidden;
        }

        @keyframes typewriter {
            from { width: 0; }
            to { width: 100%; }
        }

        @keyframes blink {
            50% { border-color: transparent; }
        }

        @media (max-width: 768px) {
            .name { font-size: 2.5rem; }
            .tech-grid { grid-template-columns: 1fr; }
            .contact-links { gap: 1rem; }
            .contact-btn { padding: 0.8rem 1.5rem; }
        }
    </style>
</head>
<body>
    <div class="floating-icons">
        <div class="floating-icon">📱</div>
        <div class="floating-icon">💻</div>
        <div class="floating-icon">🚀</div>
        <div class="floating-icon">⚡</div>
        <div class="floating-icon">🎯</div>
    </div>

    <div class="container">
        <header class="header">
            <h1 class="name">🚀 Ayush Kamboj</h1>
            <p class="subtitle typing-text">Mobile Development Enthusiast</p>
            <p class="quote">"Crafting exceptional mobile experiences, one line of code at a time"</p>
        </header>

        <section class="section">
            <h2 class="section-title">🎯 Who Am I?</h2>
            <p>A passionate <strong>Flutter</strong> and <strong>Android Native</strong> developer who thrives on turning innovative ideas into reality. I'm on a mission to build mobile applications that not only function flawlessly but also create meaningful impact in users' lives. My journey is fueled by curiosity, collaboration, and the endless pursuit of clean, efficient code.</p>
        </section>

        <section class="section">
            <h2 class="section-title">🛠️ Technical Arsenal</h2>
            <div class="tech-grid">
                <div class="tech-card">
                    <div class="tech-title">🎨 Flutter Ecosystem</div>
                    <div class="skills">
                        <span class="skill-tag">GetX</span>
                        <span class="skill-tag">BLoC</span>
                        <span class="skill-tag">Cubit</span>
                        <span class="skill-tag">Provider</span>
                        <span class="skill-tag">Clean Architecture</span>
                    </div>
                </div>
                <div class="tech-card">
                    <div class="tech-title">📱 Android Native</div>
                    <div class="skills">
                        <span class="skill-tag">Kotlin</span>
                        <span class="skill-tag">Jetpack Compose</span>
                        <span class="skill-tag">Coroutines</span>
                        <span class="skill-tag">MVVM</span>
                        <span class="skill-tag">MVP</span>
                    </div>
                </div>
                <div class="tech-card">
                    <div class="tech-title">🚀 Deployment & Distribution</div>
                    <div class="skills">
                        <span class="skill-tag">App Store</span>
                        <span class="skill-tag">Play Store</span>
                        <span class="skill-tag">CI/CD</span>
                        <span class="skill-tag">Optimization</span>
                    </div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">💡 What Drives Me</h2>
            <div class="interests">
                <div class="interest-item">
                    <span>🔥</span>
                    <span><strong>Open Source Advocate</strong> - Actively seeking meaningful contributions</span>
                </div>
                <div class="interest-item">
                    <span>🌟</span>
                    <span><strong>Continuous Learner</strong> - Always exploring cutting-edge technologies</span>
                </div>
                <div class="interest-item">
                    <span>🤝</span>
                    <span><strong>Collaboration Enthusiast</strong> - Best solutions from diverse minds</span>
                </div>
                <div class="interest-item">
                    <span>🎯</span>
                    <span><strong>Problem Solver</strong> - Creating solutions that make a difference</span>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">📊 Coding Journey</h2>
            <div class="interests">
                <div class="interest-item">
                    <span>💻</span>
                    <span><strong>LeetCode</strong> - Solving algorithmic challenges daily</span>
                </div>
                <div class="interest-item">
                    <span>🏗️</span>
                    <span><strong>Building</strong> - Scalable mobile applications</span>
                </div>
                <div class="interest-item">
                    <span>🔧</span>
                    <span><strong>Optimizing</strong> - Performance across platforms</span>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">🤝 Let's Collaborate!</h2>
            <p>I'm actively looking for:</p>
            <div class="interests">
                <div class="interest-item">
                    <span>🌟</span>
                    <span><strong>Open Source Projects</strong> in Flutter & Android</span>
                </div>
                <div class="interest-item">
                    <span>🚀</span>
                    <span><strong>Innovative Startups</strong> building the next big thing</span>
                </div>
                <div class="interest-item">
                    <span>👥</span>
                    <span><strong>Developer Communities</strong> focused on mobile excellence</span>
                </div>
                <div class="interest-item">
                    <span>📚</span>
                    <span><strong>Mentorship Opportunities</strong> - giving and receiving</span>
                </div>
            </div>
            <p style="margin-top: 1rem; font-style: italic; text-align: center;">
                <em>Got an exciting project or open source initiative? Let's connect and build something amazing together!</em>
            </p>
        </section>

        <section class="section">
            <h2 class="section-title">🌐 Connect With Me</h2>
            <div class="contact-links">
                <a href="https://www.linkedin.com/in/kambojayush/" class="contact-btn" target="_blank">
                    💼 LinkedIn
                </a>
                <a href="https://leetcode.com/u/Ayu5h_001/" class="contact-btn" target="_blank">
                    🧮 LeetCode
                </a>
                <a href="mailto:ayushkamboj46@gmail.com" class="contact-btn">
                    📧 Gmail
                </a>
            </div>
        </section>

        <footer style="text-align: center; margin-top: 3rem; padding: 2rem;">
            <p style="font-size: 1.2rem; font-style: italic; opacity: 0.8;">
                "The best way to predict the future is to create it. Let's build something extraordinary together!"
            </p>
            <p style="margin-top: 1rem; opacity: 0.7;">
                <strong>Pronouns:</strong> He/Him
            </p>
        </footer>
    </div>
</body>
</html>
