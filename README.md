<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mohammad Kammar Ahmed - Data Scientist & AI Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #0f0c29 0%, #302b63 50%, #24243e 100%);
            color: #e0e0e0;
            font-family: 'Fira Code', monospace;
            overflow-x: hidden;
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 60px;
            animation: slideInDown 0.8s ease-out;
        }

        h1 {
            font-size: 3.5em;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
            text-shadow: 0 0 30px rgba(102, 126, 234, 0.3);
        }

        .tagline {
            font-size: 1.3em;
            color: #64b5f6;
            margin-bottom: 20px;
            animation: fadeIn 1.2s ease-out;
        }

        .location {
            color: #90caf9;
            margin-bottom: 15px;
            font-size: 1.1em;
        }

        .socials {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 15px;
            flex-wrap: wrap;
        }

        .social-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 10px 15px;
            background: rgba(102, 126, 234, 0.1);
            border: 1px solid #667eea;
            border-radius: 25px;
            color: #90caf9;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            background: rgba(102, 126, 234, 0.3);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(102, 126, 234, 0.2);
        }

        .main-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
            margin-bottom: 80px;
            animation: slideInUp 0.8s ease-out;
        }

        .about-section {
            animation: fadeInLeft 1s ease-out;
        }

        .about-section h2 {
            font-size: 2em;
            color: #667eea;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .about-section p {
            line-height: 1.8;
            margin-bottom: 20px;
            color: #b0bec5;
            font-size: 1.05em;
        }

        .highlight-box {
            background: rgba(102, 126, 234, 0.1);
            border-left: 4px solid #667eea;
            padding: 15px 20px;
            margin: 15px 0;
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        .highlight-box:hover {
            background: rgba(102, 126, 234, 0.2);
            transform: translateX(5px);
        }

        .highlight-box strong {
            color: #667eea;
        }

        /* Character Animation */
        .character-container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 400px;
            animation: fadeInRight 1s ease-out;
        }

        svg {
            filter: drop-shadow(0 10px 30px rgba(102, 126, 234, 0.3));
        }

        @keyframes wave {
            0%, 100% { transform: translateY(0px) rotateZ(0deg); }
            25% { transform: translateY(-10px) rotateZ(5deg); }
            50% { transform: translateY(-20px) rotateZ(0deg); }
            75% { transform: translateY(-10px) rotateZ(-5deg); }
        }

        @keyframes blink {
            0%, 49%, 100% { opacity: 1; }
            50%, 99% { opacity: 0; }
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .hand {
            animation: wave 0.6s infinite;
            transform-origin: 70px 30px;
        }

        .eyes {
            animation: blink 3s infinite;
        }

        .body {
            animation: float 3s ease-in-out infinite;
        }

        /* Skills Section */
        .skills-section {
            margin-bottom: 80px;
            animation: fadeIn 1.2s ease-out;
        }

        .skills-section h2 {
            font-size: 2em;
            color: #667eea;
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }

        .skills-section h2::after {
            content: '';
            display: block;
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, #667eea, #764ba2);
            margin: 15px auto 0;
            border-radius: 2px;
        }

        .skill-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .skill-category {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.1), rgba(118, 75, 162, 0.1));
            border: 1px solid rgba(102, 126, 234, 0.3);
            padding: 30px;
            border-radius: 10px;
            transition: all 0.3s ease;
            animation: scaleIn 0.6s ease-out backwards;
        }

        .skill-category:nth-child(1) { animation-delay: 0.1s; }
        .skill-category:nth-child(2) { animation-delay: 0.2s; }
        .skill-category:nth-child(3) { animation-delay: 0.3s; }
        .skill-category:nth-child(4) { animation-delay: 0.4s; }

        .skill-category:hover {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.2), rgba(118, 75, 162, 0.2));
            transform: translateY(-10px);
            border-color: rgba(102, 126, 234, 0.6);
            box-shadow: 0 20px 40px rgba(102, 126, 234, 0.2);
        }

        .skill-category h3 {
            color: #667eea;
            margin-bottom: 15px;
            font-size: 1.3em;
        }

        .skill-badge {
            display: inline-block;
            background: rgba(102, 126, 234, 0.2);
            color: #90caf9;
            padding: 6px 12px;
            border-radius: 20px;
            margin: 5px;
            font-size: 0.9em;
            border: 1px solid rgba(102, 126, 234, 0.4);
            transition: all 0.3s ease;
        }

        .skill-badge:hover {
            background: rgba(102, 126, 234, 0.4);
            transform: scale(1.1);
        }

        /* Projects Section */
        .projects-section {
            margin-bottom: 80px;
        }

        .projects-section h2 {
            font-size: 2em;
            color: #667eea;
            text-align: center;
            margin-bottom: 50px;
        }

        .projects-section h2::after {
            content: '';
            display: block;
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, #667eea, #764ba2);
            margin: 15px auto 0;
            border-radius: 2px;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .project-card {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.05), rgba(118, 75, 162, 0.05));
            border: 1px solid rgba(102, 126, 234, 0.3);
            padding: 30px;
            border-radius: 10px;
            transition: all 0.3s ease;
            animation: slideInUp 0.6s ease-out backwards;
        }

        .project-card:nth-child(1) { animation-delay: 0.1s; }
        .project-card:nth-child(2) { animation-delay: 0.2s; }
        .project-card:nth-child(3) { animation-delay: 0.3s; }
        .project-card:nth-child(4) { animation-delay: 0.4s; }
        .project-card:nth-child(5) { animation-delay: 0.5s; }

        .project-card:hover {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.15), rgba(118, 75, 162, 0.15));
            transform: translateY(-15px);
            border-color: rgba(102, 126, 234, 0.6);
            box-shadow: 0 30px 60px rgba(102, 126, 234, 0.25);
        }

        .project-icon {
            font-size: 2.5em;
            margin-bottom: 15px;
        }

        .project-card h3 {
            color: #667eea;
            margin-bottom: 10px;
            font-size: 1.3em;
        }

        .project-desc {
            color: #b0bec5;
            line-height: 1.6;
            margin-bottom: 15px;
            font-size: 0.95em;
        }

        .project-link {
            color: #90caf9;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
            display: inline-block;
        }

        .project-link:hover {
            color: #667eea;
            transform: translateX(5px);
        }

        /* Call to Action */
        .cta-section {
            text-align: center;
            padding: 60px 30px;
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.1), rgba(118, 75, 162, 0.1));
            border-radius: 15px;
            animation: fadeIn 1.5s ease-out;
        }

        .cta-section h2 {
            color: #667eea;
            font-size: 2em;
            margin-bottom: 20px;
        }

        .cta-section p {
            color: #b0bec5;
            font-size: 1.1em;
            margin-bottom: 30px;
            line-height: 1.8;
        }

        .cta-button {
            display: inline-block;
            padding: 15px 40px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
            transition: all 0.3s ease;
            margin: 10px;
            border: 2px solid transparent;
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 30px rgba(102, 126, 234, 0.4);
        }

        /* Animations */
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

        @keyframes fadeInLeft {
            from {
                opacity: 0;
                transform: translateX(-50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes fadeInRight {
            from {
                opacity: 0;
                transform: translateX(50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes scaleIn {
            from {
                opacity: 0;
                transform: scale(0.8);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        @media (max-width: 768px) {
            .main-content {
                grid-template-columns: 1fr;
                gap: 40px;
            }

            h1 {
                font-size: 2.2em;
            }

            .skill-grid, .project-grid {
                grid-template-columns: 1fr;
            }

            .character-container {
                height: 300px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <header>
            <h1>🚀 Mohammad Kammar Ahmed</h1>
            <p class="tagline">Data Scientist | ML Engineer | AI Tool Explorer</p>
            <div class="location">📍 Hyderabad, India</div>
            <div class="socials">
                <a href="https://www.linkedin.com/in/mohammad-kammar-ahmed-48b391253/" class="social-link">
                    <span>🔗</span> LinkedIn
                </a>
                <a href="mailto:mdqamarahmed123@gmail.com" class="social-link">
                    <span>✉️</span> Email
                </a>
                <a href="https://github.com/nameisahmedh" class="social-link">
                    <span>🐙</span> GitHub
                </a>
            </div>
        </header>

        <!-- Main Content with Character -->
        <section class="main-content">
            <div class="about-section">
                <h2>👨‍💻 Who Am I?</h2>
                <p>
                    Final-year B.Tech CSE (Data Science) student obsessed with transforming raw data into intelligent systems. I bridge the gap between complex Machine Learning models and user-friendly applications.
                </p>

                <div class="highlight-box">
                    <strong>🔭 Current Focus:</strong> Building scalable AI systems with agentic workflows and mastering production-grade ML pipelines.
                </div>

                <div class="highlight-box">
                    <strong>🧠 My Strength:</strong> End-to-end ML solutions - from data preprocessing with <strong>SMOTE</strong> to deploying React frontends with <strong>LLM integrations</strong>.
                </div>

                <div class="highlight-box">
                    <strong>⚡ The Edge:</strong> I actively experiment with cutting-edge AI tools (Gemini, Perplexity, ClipDrop) and integrate them immediately into production systems.
                </div>

                <div class="highlight-box">
                    <strong>🏆 Leadership:</strong> General Secretary of Codeoholics - driving innovation and technical excellence in the developer community.
                </div>
            </div>

            <!-- Animated Character -->
            <div class="character-container">
                <svg viewBox="0 0 200 400" width="200" height="400">
                    <!-- Body -->
                    <g class="body">
                        <!-- Head -->
                        <circle cx="100" cy="80" r="35" fill="#FFD4A3"/>
                        
                        <!-- Eyes -->
                        <g class="eyes">
                            <circle cx="90" cy="75" r="4" fill="#333"/>
                            <circle cx="110" cy="75" r="4" fill="#333"/>
                        </g>
                        
                        <!-- Smile -->
                        <path d="M 92 85 Q 100 92 108 85" stroke="#333" stroke-width="2" fill="none"/>
                        
                        <!-- Hair -->
                        <path d="M 65 50 Q 100 35 135 50" fill="#1a1a1a"/>
                        
                        <!-- Body -->
                        <rect x="80" y="120" width="40" height="60" rx="5" fill="#667EEA"/>
                        
                        <!-- Arms -->
                        <rect x="45" y="125" width="35" height="15" rx="7" fill="#FFD4A3"/>
                        <rect x="120" y="125" width="35" height="15" rx="7" fill="#FFD4A3"/>
                        
                        <!-- Left Hand -->
                        <g class="hand">
                            <circle cx="40" cy="130" r="10" fill="#FFD4A3"/>
                        </g>
                        
                        <!-- Right Hand (waving) -->
                        <g class="hand" style="transform-origin: 155px 30px;">
                            <circle cx="160" cy="130" r="10" fill="#FFD4A3"/>
                        </g>
                        
                        <!-- Legs -->
                        <rect x="85" y="185" width="12" height="50" rx="6" fill="#2C2C2C"/>
                        <rect x="103" y="185" width="12" height="50" rx="6" fill="#2C2C2C"/>
                        
                        <!-- Shoes -->
                        <ellipse cx="91" cy="240" rx="10" ry="8" fill="#000"/>
                        <ellipse cx="109" cy="240" rx="10" ry="8" fill="#000"/>
                        
                        <!-- Floating symbols -->
                        <g opacity="0.7">
                            <text x="25" y="50" font-size="20" fill="#667EEA">🤖</text>
                            <text x="160" y="80" font-size="20" fill="#764BA2">📊</text>
                            <text x="30" y="150" font-size="18" fill="#90CAF9">⚙️</text>
                            <text x="165" y="160" font-size="18" fill="#90CAF9">💡</text>
                        </g>
                    </g>
                </svg>
            </div>
        </section>

        <!-- Skills Section -->
        <section class="skills-section">
            <h2>🛠️ Tech Arsenal</h2>
            <div class="skill-grid">
                <div class="skill-category">
                    <h3>🤖 Machine Learning</h3>
                    <div>
                        <span class="skill-badge">Scikit-Learn</span>
                        <span class="skill-badge">XGBoost</span>
                        <span class="skill-badge">CatBoost</span>
                        <span class="skill-badge">Random Forest</span>
                        <span class="skill-badge">Neural Networks</span>
                        <span class="skill-badge">SMOTE</span>
                    </div>
                </div>

                <div class="skill-category">
                    <h3>📊 Data Science</h3>
                    <div>
                        <span class="skill-badge">Pandas</span>
                        <span class="skill-badge">NumPy</span>
                        <span class="skill-badge">Matplotlib</span>
                        <span class="skill-badge">Seaborn</span>
                        <span class="skill-badge">Exploratory Analysis</span>
                        <span class="skill-badge">Feature Engineering</span>
                    </div>
                </div>

                <div class="skill-category">
                    <h3>🌐 Frontend Development</h3>
                    <div>
                        <span class="skill-badge">React 19</span>
                        <span class="skill-badge">Vite</span>
                        <span class="skill-badge">TailwindCSS</span>
                        <span class="skill-badge">Framer Motion</span>
                        <span class="skill-badge">JavaScript</span>
                        <span class="skill-badge">Responsive Design</span>
                    </div>
                </div>

                <div class="skill-category">
                    <h3>⚙️ Backend & Tools</h3>
                    <div>
                        <span class="skill-badge">Node.js</span>
                        <span class="skill-badge">Express.js</span>
                        <span class="skill-badge">Flask</span>
                        <span class="skill-badge">MongoDB</span>
                        <span class="skill-badge">LLM APIs</span>
                        <span class="skill-badge">Deployment</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Projects Section -->
        <section class="projects-section">
            <h2>🚀 Featured Projects</h2>
            <div class="project-grid">
                <div class="project-card">
                    <div class="project-icon">🤖</div>
                    <h3>Arix: AI Content Engine</h3>
                    <p class="project-desc">All-in-one platform integrating text generation (Gemini), image creation (ClipDrop), and background removal with React 19 frontend.</p>
                    <a href="https://arix-ai.vercel.app/" class="project-link">View Demo →</a>
                </div>

                <div class="project-card">
                    <div class="project-icon">🩺</div>
                    <h3>Stroke Prediction System</h3>
                    <p class="project-desc">ML pipeline comparing 7 algorithms with SMOTE preprocessing, Chi2 feature selection, and batch CSV prediction capabilities.</p>
                    <a href="https://strokeprediction-1-1ykl.onrender.com/" class="project-link">Explore →</a>
                </div>

                <div class="project-card">
                    <div class="project-icon">📄</div>
                    <h3>Resume Analyzer</h3>
                    <p class="project-desc">Smart ATS tool powered by Perplexity AI. Compares resumes against job descriptions with keyword gap analysis and scoring.</p>
                    <a href="https://arixai-resume-analyzer.vercel.app/" class="project-link">Try Now →</a>
                </div>

                <div class="project-card">
                    <div class="project-icon">🌸</div>
                    <h3>Iris Classification Suite</h3>
                    <p class="project-desc">Interactive ML fundamentals visualization with real-time model switching across 5 algorithms with instant confidence scoring.</p>
                    <a href="https://iris-classification2.onrender.com/" class="project-link">Explore →</a>
                </div>

                <div class="project-card">
                    <div class="project-icon">👥</div>
                    <h3>Staff Management System</h3>
                    <p class="project-desc">Secure role-based system showcasing internal tool logic with task priority levels, overdue detection, and mood tracking.</p>
                    <a href="https://github.com/nameisahmedh/staff-management-system" class="project-link">View Code →</a>
                </div>
            </div>
        </section>

        <!-- Call to Action -->
        <section class="cta-section">
            <h2>Let's Build Something Amazing</h2>
            <p>
                I'm actively seeking <strong>Data Science Internships</strong> and <strong>ML Engineering Opportunities</strong>. Whether you want to discuss scalable ML systems, React optimization, or LLM integration—let's connect!
            </p>
            <a href="https://www.linkedin.com/in/mohammad-kammar-ahmed-48b391253/" class="cta-button">Connect on LinkedIn</a>
            <a href="mailto:mdqamarahmed123@gmail.com" class="cta-button">Send Email</a>
        </section>
    </div>
</body>
</html>
