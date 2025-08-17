<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Why You Matter - Therapeutic Guide</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
            min-height: 100vh;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .hero-section {
            text-align: center;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(15px);
            border-radius: 30px;
            padding: 60px 40px;
            margin-bottom: 30px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.15);
            border: 3px solid rgba(255, 255, 255, 0.3);
            position: relative;
            overflow: hidden;
        }

        .hero-section::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(102, 126, 234, 0.1) 0%, transparent 70%);
            animation: pulse 4s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 0.7; }
            50% { transform: scale(1.1); opacity: 0.3; }
        }

        .hero-title {
            font-size: 4em;
            font-weight: 800;
            background: linear-gradient(45deg, #667eea, #764ba2, #f093fb);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 20px;
            text-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            position: relative;
            z-index: 2;
        }

        .hero-subtitle {
            font-size: 1.4em;
            color: #666;
            margin-bottom: 30px;
            position: relative;
            z-index: 2;
        }

        .hero-emoji {
            font-size: 3em;
            margin-bottom: 20px;
            display: block;
            position: relative;
            z-index: 2;
        }

        .nav-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .nav-card {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            cursor: pointer;
            transition: all 0.4s ease;
            border: 2px solid rgba(255, 255, 255, 0.3);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            position: relative;
            overflow: hidden;
        }

        .nav-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(45deg, #667eea, #764ba2, #f093fb);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }

        .nav-card:hover::before {
            transform: scaleX(1);
        }

        .nav-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.2);
            border-color: rgba(102, 126, 234, 0.5);
        }

        .nav-card-emoji {
            font-size: 3em;
            margin-bottom: 15px;
            display: block;
        }

        .nav-card-title {
            font-size: 1.8em;
            font-weight: 700;
            margin-bottom: 10px;
            color: #333;
        }

        .nav-card-desc {
            color: #666;
            font-size: 1em;
        }

        .section {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(15px);
            border-radius: 25px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
            border: 2px solid rgba(255, 255, 255, 0.3);
            display: none;
        }

        .section.active {
            display: block;
            animation: fadeInUp 0.6s ease;
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .section-header {
            text-align: center;
            margin-bottom: 40px;
        }

        .section-title {
            font-size: 2.5em;
            font-weight: 700;
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 15px;
        }

        .section-subtitle {
            font-size: 1.2em;
            color: #666;
        }

        .content-grid {
            display: grid;
            gap: 25px;
            margin-bottom: 30px;
        }

        .content-card {
            background: linear-gradient(135deg, #f8f9ff, #fff);
            border-radius: 20px;
            padding: 30px;
            border: 2px solid #e1e8ff;
            transition: all 0.3s ease;
            position: relative;
        }

        .content-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(102, 126, 234, 0.15);
            border-color: #667eea;
        }

        .card-header {
            display: flex;
            align-items: center;
            margin-bottom: 20px;
        }

        .card-emoji {
            font-size: 2.5em;
            margin-right: 15px;
        }

        .card-title {
            font-size: 1.6em;
            font-weight: 600;
            color: #333;
        }

        .highlight-box {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 25px;
            border-radius: 15px;
            margin: 20px 0;
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.3);
        }

        .highlight-title {
            font-size: 1.4em;
            font-weight: 600;
            margin-bottom: 10px;
        }

        .exercise-box {
            background: linear-gradient(135deg, #f093fb, #f5576c);
            color: white;
            padding: 25px;
            border-radius: 15px;
            margin: 20px 0;
            box-shadow: 0 10px 25px rgba(240, 147, 251, 0.3);
        }

        .technique-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .technique-card {
            background: white;
            padding: 20px;
            border-radius: 15px;
            border-left: 5px solid #667eea;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
        }

        .technique-card:hover {
            transform: translateX(5px);
            box-shadow: 0 8px 25px rgba(102, 126, 234, 0.15);
        }

        .table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }

        .table th,
        .table td {
            padding: 15px;
            text-align: left;
            border-bottom: 1px solid #e1e8ff;
        }

        .table th {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            font-weight: 600;
        }

        .table tr:hover {
            background-color: #f8f9ff;
        }

        .back-btn {
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            padding: 15px 30px;
            border: none;
            border-radius: 50px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.3);
            margin-bottom: 20px;
        }

        .back-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(102, 126, 234, 0.4);
        }

        .progress-indicator {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin: 20px 0;
        }

        .progress-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: #ddd;
            transition: all 0.3s ease;
        }

        .progress-dot.active {
            background: linear-gradient(45deg, #667eea, #764ba2);
            transform: scale(1.2);
        }

        .floating-hearts {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .heart {
            position: absolute;
            font-size: 20px;
            color: rgba(240, 147, 251, 0.3);
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); opacity: 0.3; }
            50% { transform: translateY(-20px) rotate(180deg); opacity: 0.7; }
        }

        .crisis-alert {
            background: linear-gradient(135deg, #ff6b6b, #ee5a24);
            color: white;
            padding: 20px;
            border-radius: 15px;
            margin: 20px 0;
            box-shadow: 0 10px 25px rgba(255, 107, 107, 0.3);
            border-left: 5px solid #ff3838;
        }

        @media (max-width: 768px) {
            .hero-title { font-size: 2.5em; }
            .nav-cards { grid-template-columns: 1fr; }
            .container { padding: 10px; }
            .hero-section { padding: 40px 20px; }
            .section { padding: 25px; }
        }
    </style>
</head>
<body>
    <div class="floating-hearts">
        <div class="heart" style="left: 10%; animation-delay: 0s;">💙</div>
        <div class="heart" style="left: 20%; animation-delay: 1s;">💜</div>
        <div class="heart" style="left: 30%; animation-delay: 2s;">💚</div>
        <div class="heart" style="left: 40%; animation-delay: 3s;">💛</div>
        <div class="heart" style="left: 50%; animation-delay: 4s;">🧡</div>
        <div class="heart" style="left: 60%; animation-delay: 5s;">💙</div>
        <div class="heart" style="left: 70%; animation-delay: 6s;">💜</div>
        <div class="heart" style="left: 80%; animation-delay: 1.5s;">💚</div>
        <div class="heart" style="left: 90%; animation-delay: 2.5s;">💛</div>
    </div>

    <div class="container">
        <!-- Home Page -->
        <div id="home" class="section active">
            <div class="hero-section">
                <span class="hero-emoji">🌟</span>
                <h1 class="hero-title">Why You Matter</h1>
                <p class="hero-subtitle">A Comprehensive Therapeutic Guide to Understanding Your Inherent Worth</p>
                <div class="progress-indicator">
                    <div class="progress-dot active"></div>
                    <div class="progress-dot"></div>
                    <div class="progress-dot"></div>
                    <div class="progress-dot"></div>
                    <div class="progress-dot"></div>
                    <div class="progress-dot"></div>
            </div>

        <!-- Progress Tracking Section -->
        <div id="progress" class="section">
            <button class="back-btn" onclick="showSection('home')">← Back to Home</button>
            <div class="section-header">
                <h2 class="section-title">📈 Progress Tracking</h2>
                <p class="section-subtitle">Markers of growth and maintaining improvement</p>
            </div>

            <div class="content-grid">
                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">🌱</span>
                        <h3 class="card-title">Signs of Improving Self-Worth</h3>
                    </div>
                    <div class="technique-grid">
                        <div class="technique-card">
                            <strong>Cognitive</strong><br>
                            Decreased negative self-talk
                        </div>
                        <div class="technique-card">
                            <strong>Social</strong><br>
                            Accepting compliments gracefully
                        </div>
                        <div class="technique-card">
                            <strong>Behavioral</strong><br>
                            Setting healthy boundaries
                        </div>
                        <div class="technique-card">
                            <strong>Emotional</strong><br>
                            Better emotional regulation
                        </div>
                        <div class="technique-card">
                            <strong>Self-Care</strong><br>
                            Increased nurturing behaviors
                        </div>
                        <div class="technique-card">
                            <strong>Growth</strong><br>
                            Willingness to try new things
                        </div>
                    </div>
                </div>

                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">📅</span>
                        <h3 class="card-title">Weekly Progress Plan</h3>
                    </div>
                    
                    <div class="exercise-box">
                        <div class="highlight-title">Week 1-2: Foundation Building</div>
                        <ul>
                            <li>Daily self-compassion check-ins</li>
                            <li>Challenge one negative thought per day</li>
                            <li>Begin gratitude journaling</li>
                        </ul>
                    </div>

                    <div class="highlight-box">
                        <div class="highlight-title">Week 3-4: Strengths Focus</div>
                        <ul>
                            <li>Complete character strengths assessment</li>
                            <li>Ask trusted people what they value about you</li>
                            <li>Practice accepting compliments</li>
                        </ul>
                    </div>

                    <div class="exercise-box">
                        <div class="highlight-title">Week 5-6: Values & Meaning</div>
                        <ul>
                            <li>Clarify top 5 personal values</li>
                            <li>Identify current ways you live these values</li>
                            <li>Set one small values-based weekly goal</li>
                        </ul>
                    </div>

                    <div class="highlight-box">
                        <div class="highlight-title">Week 7-8: Integration</div>
                        <ul>
                            <li>Create personal worth reminder cards</li>
                            <li>Develop self-compassion rituals</li>
                            <li>Plan for maintaining progress</li>
                        </ul>
                    </div>
                </div>

                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">🎯</span>
                        <h3 class="card-title">Maintaining Progress</h3>
                    </div>
                    <div class="technique-grid">
                        <div class="technique-card">
                            <strong>Daily Practice</strong><br>
                            Regular self-compassion moments
                        </div>
                        <div class="technique-card">
                            <strong>Values Check</strong><br>
                            Ongoing values clarification
                        </div>
                        <div class="technique-card">
                            <strong>Connection</strong><br>
                            Community and relationships
                        </div>
                        <div class="technique-card">
                            <strong>Support</strong><br>
                            Professional help as needed
                        </div>
                        <div class="technique-card">
                            <strong>Celebration</strong><br>
                            Acknowledging growth
                        </div>
                        <div class="technique-card">
                            <strong>Patience</strong><br>
                            Gentle with the process
                        </div>
                    </div>
                </div>
            </div>

            <div class="highlight-box" style="text-align: center; margin-top: 30px;">
                <h3>🌟 Remember: The journey to understanding "why you matter" is ongoing.</h3>
                <p style="font-size: 1.2em; margin-top: 10px;">Be patient with yourself and celebrate each step forward, no matter how small. You are worthy of love, care, and all the good things life has to offer. 💜</p>
            </div>
        </div>
    </div>

    <script>
        function showSection(sectionId) {
            // Hide all sections
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                section.classList.remove('active');
            });
            
            // Show selected section
            document.getElementById(sectionId).classList.add('active');
            
            // Update progress dots
            updateProgressDots(sectionId);
            
            // Scroll to top
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function updateProgressDots(sectionId) {
            const dots = document.querySelectorAll('.progress-dot');
            dots.forEach(dot => dot.classList.remove('active'));
            
            const sectionMap = {
                'home': 0,
                'concepts': 1,
                'interventions': 2,
                'exercises': 3,
                'crisis': 4,
                'resources': 5,
                'progress': 5
            };
            
            const index = sectionMap[sectionId] || 0;
            if (dots[index]) {
                dots[index].classList.add('active');
            }
        }

        // Add some interactive sparkle effects
        function createSparkle() {
            const sparkle = document.createElement('div');
            sparkle.innerHTML = '✨';
            sparkle.style.position = 'fixed';
            sparkle.style.left = Math.random() * window.innerWidth + 'px';
            sparkle.style.top = Math.random() * window.innerHeight + 'px';
            sparkle.style.fontSize = '20px';
            sparkle.style.pointerEvents = 'none';
            sparkle.style.zIndex = '1000';
            sparkle.style.animation = 'sparkleFloat 3s ease-out forwards';
            
            document.body.appendChild(sparkle);
            
            setTimeout(() => {
                sparkle.remove();
            }, 3000);
        }

        // Add sparkle animation
        const sparkleStyle = document.createElement('style');
        sparkleStyle.textContent = `
            @keyframes sparkleFloat {
                0% { opacity: 1; transform: translateY(0px) scale(1); }
                100% { opacity: 0; transform: translateY(-100px) scale(0); }
            }
        `;
        document.head.appendChild(sparkleStyle);

        // Create sparkles periodically
        setInterval(createSparkle, 5000);

        // Add click sparkles to nav cards
        document.querySelectorAll('.nav-card').forEach(card => {
            card.addEventListener('click', function(e) {
                for (let i = 0; i < 3; i++) {
                    setTimeout(() => createSparkle(), i * 200);
                }
            });
        });
    </script>
</body>
</html>
            </div>

            <div class="nav-cards">
                <div class="nav-card" onclick="showSection('concepts')">
                    <span class="nav-card-emoji">🧠</span>
                    <h3 class="nav-card-title">Core Concepts</h3>
                    <p class="nav-card-desc">Understanding inherent worth and common barriers to self-value</p>
                </div>

                <div class="nav-card" onclick="showSection('interventions')">
                    <span class="nav-card-emoji">🛠️</span>
                    <h3 class="nav-card-title">Therapeutic Tools</h3>
                    <p class="nav-card-desc">Evidence-based interventions and healing techniques</p>
                </div>

                <div class="nav-card" onclick="showSection('exercises')">
                    <span class="nav-card-emoji">📝</span>
                    <h3 class="nav-card-title">Practical Exercises</h3>
                    <p class="nav-card-desc">Interactive activities and session-ready materials</p>
                </div>

                <div class="nav-card" onclick="showSection('crisis')">
                    <span class="nav-card-emoji">🚨</span>
                    <h3 class="nav-card-title">Crisis Support</h3>
                    <p class="nav-card-desc">Emergency interventions and safety resources</p>
                </div>

                <div class="nav-card" onclick="showSection('resources')">
                    <span class="nav-card-emoji">📚</span>
                    <h3 class="nav-card-title">Resources</h3>
                    <p class="nav-card-desc">Books, apps, and continued learning materials</p>
                </div>

                <div class="nav-card" onclick="showSection('progress')">
                    <span class="nav-card-emoji">📈</span>
                    <h3 class="nav-card-title">Progress Tracking</h3>
                    <p class="nav-card-desc">Markers of growth and maintaining improvement</p>
                </div>
            </div>
        </div>

        <!-- Core Concepts Section -->
        <div id="concepts" class="section">
            <button class="back-btn" onclick="showSection('home')">← Back to Home</button>
            <div class="section-header">
                <h2 class="section-title">🧠 Core Therapeutic Concepts</h2>
                <p class="section-subtitle">Foundation principles for understanding self-worth</p>
            </div>

            <div class="content-grid">
                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">✨</span>
                        <h3 class="card-title">Understanding Inherent Worth</h3>
                    </div>
                    <div class="highlight-box">
                        <div class="highlight-title">Fundamental Principle</div>
                        <p>Every person has inherent worth that exists independent of achievements, relationships, or external validation. This worth is not earned or lost—it simply <strong>is</strong>.</p>
                    </div>
                    <h4>🎯 Key Therapeutic Messages:</h4>
                    <ul style="margin: 15px 0; padding-left: 20px;">
                        <li>Your value doesn't depend on productivity or success</li>
                        <li>You matter because you exist, not because of what you do</li>
                        <li>Your worth remains constant through struggles and setbacks</li>
                        <li>You deserve care, respect, and compassion—especially from yourself</li>
                    </ul>
                </div>

                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">🚧</span>
                        <h3 class="card-title">Common Barriers to Self-Worth</h3>
                    </div>
                    
                    <h4>💭 Cognitive Distortions:</h4>
                    <div class="technique-grid">
                        <div class="technique-card">
                            <strong>All-or-Nothing</strong><br>
                            "I'm either perfect or worthless"
                        </div>
                        <div class="technique-card">
                            <strong>Mental Filter</strong><br>
                            Focusing only on negatives
                        </div>
                        <div class="technique-card">
                            <strong>Personalization</strong><br>
                            Taking blame for external events
                        </div>
                        <div class="technique-card">
                            <strong>Should Statements</strong><br>
                            Harsh unrealistic expectations
                        </div>
                    </div>

                    <h4>🌱 Origins of Low Self-Worth:</h4>
                    <ul style="margin: 15px 0; padding-left: 20px;">
                        <li>Childhood criticism or neglect experiences</li>
                        <li>Traumatic events or ongoing stress</li>
                        <li>Comparison culture (especially social media)</li>
                        <li>Perfectionism and fear of failure</li>
                        <li>Societal messages about success and value</li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- Therapeutic Interventions Section -->
        <div id="interventions" class="section">
            <button class="back-btn" onclick="showSection('home')">← Back to Home</button>
            <div class="section-header">
                <h2 class="section-title">🛠️ Therapeutic Interventions</h2>
                <p class="section-subtitle">Evidence-based tools for building self-worth</p>
            </div>

            <div class="content-grid">
                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">🎯</span>
                        <h3 class="card-title">Values Clarification</h3>
                    </div>
                    <div class="exercise-box">
                        <div class="highlight-title">Core Values Exercise</div>
                        <p><strong>Guide clients to identify:</strong></p>
                        <ul style="margin-top: 10px;">
                            <li>What principles guide your decisions?</li>
                            <li>When do you feel most authentic and alive?</li>
                            <li>What legacy do you want to leave?</li>
                            <li>How do you want to treat others?</li>
                        </ul>
                    </div>
                    <p><strong>Therapeutic Benefit:</strong> Values provide stable self-worth foundation independent of external circumstances.</p>
                </div>

                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">💝</span>
                        <h3 class="card-title">Self-Compassion Development</h3>
                    </div>
                    <p><strong>Three Components (Kristin Neff):</strong></p>
                    
                    <div class="technique-grid">
                        <div class="technique-card">
                            <strong>🤗 Self-Kindness</strong><br>
                            Treating yourself like a good friend
                        </div>
                        <div class="technique-card">
                            <strong>🌍 Common Humanity</strong><br>
                            Struggle is part of human experience
                        </div>
                        <div class="technique-card">
                            <strong>🧘 Mindfulness</strong><br>
                            Balanced awareness without judgment
                        </div>
                    </div>

                    <div class="highlight-box">
                        <div class="highlight-title">Self-Compassion Questions</div>
                        <ul>
                            <li>"What would I say to a dear friend in this situation?"</li>
                            <li>"How can I acknowledge this pain while being kind?"</li>
                            <li>"What do I need right now to feel supported?"</li>
                        </ul>
                    </div>
                </div>

                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">🔄</span>
                        <h3 class="card-title">Cognitive Restructuring</h3>
                    </div>
                    
                    <table class="table">
                        <thead>
                            <tr>
                                <th>❌ Negative Thought</th>
                                <th>✅ Balanced Alternative</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>"I'm worthless"</td>
                                <td>"I'm struggling right now, but that doesn't define my worth"</td>
                            </tr>
                            <tr>
                                <td>"Nobody cares about me"</td>
                                <td>"Some relationships are challenging, but there are people who value me"</td>
                            </tr>
                            <tr>
                                <td>"I always mess up"</td>
                                <td>"I make mistakes sometimes, like everyone does"</td>
                            </tr>
                            <tr>
                                <td>"I'm a burden"</td>
                                <td>"I deserve support, and it's okay to need help"</td>
                            </tr>
                        </tbody>
                    </table>

                    <div class="exercise-box">
                        <div class="highlight-title">The Best Friend Test</div>
                        <ul>
                            <li>Would you say this to your best friend?</li>
                            <li>If not, why are you saying it to yourself?</li>
                            <li>How would you comfort someone you care about?</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>

        <!-- Exercises Section -->
        <div id="exercises" class="section">
            <button class="back-btn" onclick="showSection('home')">← Back to Home</button>
            <div class="section-header">
                <h2 class="section-title">📝 Practical Exercises</h2>
                <p class="section-subtitle">Session-ready activities and homework assignments</p>
            </div>

            <div class="content-grid">
                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">💌</span>
                        <h3 class="card-title">The Self-Worth Letter</h3>
                    </div>
                    <div class="exercise-box">
                        <div class="highlight-title">Instructions</div>
                        <p>Write a letter to yourself from the perspective of someone who loves you unconditionally. Include:</p>
                        <ul style="margin-top: 10px;">
                            <li>Reasons why you matter</li>
                            <li>Appreciation for your struggles and growth</li>
                            <li>Reminders of your inherent worth</li>
                            <li>Encouragement for difficult times</li>
                        </ul>
                    </div>
                </div>

                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">🎯</span>
                        <h3 class="card-title">Values-Based Goal Setting</h3>
                    </div>
                    <p>Replace achievement-based goals with values-aligned intentions:</p>
                    <div class="technique-grid">
                        <div class="technique-card">
                            <strong>Instead of:</strong> "I need to make everyone happy"<br>
                            <strong>Try:</strong> "I want to practice kindness"
                        </div>
                        <div class="technique-card">
                            <strong>Instead of:</strong> "I need to be perfect"<br>
                            <strong>Try:</strong> "I want to be authentic"
                        </div>
                        <div class="technique-card">
                            <strong>Instead of:</strong> "I need to be the best"<br>
                            <strong>Try:</strong> "I want to contribute meaningfully"
                        </div>
                    </div>
                </div>

                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">🌊</span>
                        <h3 class="card-title">The Ripple Effect Map</h3>
                    </div>
                    <div class="highlight-box">
                        <div class="highlight-title">Create a Visual Map</div>
                        <p>Show how your existence has positively impacted others:</p>
                        <ul style="margin-top: 10px;">
                            <li><strong>Direct relationships:</strong> Family, friends, colleagues</li>
                            <li><strong>Indirect influences:</strong> Strangers helped, communities joined</li>
                            <li><strong>Future potential:</strong> How your continued presence matters</li>
                        </ul>
                    </div>
                </div>

                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">🏆</span>
                        <h3 class="card-title">Daily Wins Practice</h3>
                    </div>
                    <div class="exercise-box">
                        <div class="highlight-title">Daily Recognition</div>
                        <p>Identify three things you did well each day:</p>
                        <ul style="margin-top: 10px;">
                            <li>Include efforts, not just outcomes</li>
                            <li>Notice acts of kindness</li>
                            <li>Celebrate moments of courage</li>
                            <li>Acknowledge steps forward</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>

        <!-- Crisis Support Section -->
        <div id="crisis" class="section">
            <button class="back-btn" onclick="showSection('home')">← Back to Home</button>
            <div class="section-header">
                <h2 class="section-title">🚨 Crisis Support</h2>
                <p class="section-subtitle">Emergency interventions and immediate support resources</p>
            </div>

            <div class="crisis-alert">
                <h3>⚠️ When Self-Worth is Critically Low</h3>
                <ul style="margin-top: 10px;">
                    <li>Assess for self-harm or suicidal ideation</li>
                    <li>Provide immediate safety planning</li>
                    <li>Connect with support systems</li>
                    <li>Consider medication evaluation</li>
                    <li>Increase session frequency temporarily</li>
                </ul>
            </div>

            <div class="content-grid">
                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">🆘</span>
                        <h3 class="card-title">Emergency Affirmations</h3>
                    </div>
                    <div class="technique-grid">
                        <div class="technique-card">
                            "I am enough, exactly as I am right now"
                        </div>
                        <div class="technique-card">
                            "This pain is temporary; my worth is permanent"
                        </div>
                        <div class="technique-card">
                            "I deserve to be here and take up space"
                        </div>
                        <div class="technique-card">
                            "Someone's life is better because I exist"
                        </div>
                    </div>
                </div>

                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">📞</span>
                        <h3 class="card-title">Crisis Resources</h3>
                    </div>
                    <div class="highlight-box">
                        <div class="highlight-title">Immediate Support</div>
                        <ul>
                            <li><strong>National Suicide Prevention Lifeline:</strong> 988</li>
                            <li><strong>Crisis Text Line:</strong> Text HOME to 741741</li>
                            <li><strong>NAMI:</strong> National Alliance on Mental Illness</li>
                            <li><strong>Local emergency services:</strong> 911</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>

        <!-- Resources Section -->
        <div id="resources" class="section">
            <button class="back-btn" onclick="showSection('home')">← Back to Home</button>
            <div class="section-header">
                <h2 class="section-title">📚 Additional Resources</h2>
                <p class="section-subtitle">Books, apps, and tools for continued growth</p>
            </div>

            <div class="content-grid">
                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">📖</span>
                        <h3 class="card-title">Recommended Reading</h3>
                    </div>
                    <div class="technique-grid">
                        <div class="technique-card">
                            <strong>"Self-Compassion"</strong><br>
                            by Kristin Neff
                        </div>
                        <div class="technique-card">
                            <strong>"The Gifts of Imperfection"</strong><br>
                            by Brené Brown
                        </div>
                        <div class="technique-card">
                            <strong>"Mind Over Mood"</strong><br>
                            by Dennis Greenberger
                        </div>
                        <div class="technique-card">
                            <strong>"Man's Search for Meaning"</strong><br>
                            by Viktor Frankl
                        </div>
                    </div>
                </div>

                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">📱</span>
                        <h3 class="card-title">Helpful Apps & Tools</h3>
                    </div>
                    <div class="technique-grid">
                        <div class="technique-card">
                            <strong>Insight Timer</strong><br>
                            Meditation & self-compassion
                        </div>
                        <div class="technique-card">
                            <strong>Headspace</strong><br>
                            Mindfulness practices
                        </div>
                        <div class="technique-card">
                            <strong>Sanvello</strong><br>
                            Mood & thought tracking
                        </div>
                        <div class="technique-card">
                            <strong>Ten Percent Happier</strong><br>
                            Meditation & wellness
                        </div>
                    </div>
                </div>

                <div class="content-card">
                    <div class="card-header">
                        <span class="card-emoji">🎓</span>
                        <h3 class="card-title">Therapeutic Approaches</h3>
                    </div>
                    <h4>🧠 Integration with Evidence-Based Therapies:</h4>
                    <div class="technique-grid">
                        <div class="technique-card">
                            <strong>CBT</strong><br>
                            Challenge thoughts, behavioral experiments
                        </div>
                        <div class="technique-card">
                            <strong>ACT</strong><br>
                            Values-based action, psychological flexibility
                        </div>
                        <div class="technique-card">
                            <strong>DBT</strong><br>
                            Distress tolerance, emotion regulation
                        </div>
                        <div class="technique-card">
                            <strong>Trauma-Informed</strong><br>
                            Safety, stabilization, growth
                        </div>
                    </div>
                </div>
            </div>

            