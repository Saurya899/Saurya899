<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Saurabh Kumar | PHP & Laravel Full Stack Developer</title>
    <!-- Google Fonts & Font Awesome -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&family=Fira+Code:wght@400;500;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #f6f9fc 0%, #eef2f8 100%);
            font-family: 'Inter', sans-serif;
            color: #0a0c10;
            line-height: 1.5;
            padding: 2rem 1.5rem;
        }

        .container {
            max-width: 1300px;
            margin: 0 auto;
            width: 100%;
        }

        /* Header Card */
        .hero-card {
            background: rgba(255, 255, 255, 0.96);
            backdrop-filter: blur(2px);
            border-radius: 2.5rem;
            box-shadow: 0 25px 45px -12px rgba(0, 0, 0, 0.2);
            padding: 2rem 2rem 1.8rem;
            margin-bottom: 2rem;
            border: 1px solid rgba(255,255,255,0.6);
            text-align: center;
        }

        h1 {
            font-size: 3rem;
            font-weight: 800;
            background: linear-gradient(120deg, #1e293b, #2d4a6e, #0f2b3d);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            letter-spacing: -0.02em;
            margin-bottom: 0.75rem;
        }

        .subhead {
            font-size: 1.3rem;
            font-weight: 600;
            color: #2563eb;
            background: #eef2ff;
            display: inline-block;
            padding: 0.4rem 1.5rem;
            border-radius: 60px;
            margin-bottom: 1.2rem;
        }

        .typing-wrapper {
            background: #f1f5f9;
            border-radius: 48px;
            padding: 0.5rem 1rem;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            font-family: 'Fira Code', monospace;
            font-size: 1rem;
            color: #0f3b5c;
            margin-top: 0.5rem;
        }

        /* Social Icons Row */
        .social-row {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 1.8rem 0 0.5rem;
            flex-wrap: wrap;
        }
        .social-icon {
            background: white;
            padding: 0.7rem 1.8rem;
            border-radius: 60px;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 12px;
            transition: 0.25s ease;
            box-shadow: 0 5px 12px rgba(0,0,0,0.05);
            border: 1px solid #e2e8f0;
            color: #1f2a44;
            font-size: 0.95rem;
            text-decoration: none;
        }
        .social-icon i {
            font-size: 1.3rem;
        }
        .social-icon:hover {
            transform: translateY(-4px);
            box-shadow: 0 15px 25px -10px rgba(0,0,0,0.15);
            border-color: #a5c9ff;
        }
        .instagram:hover { color: #d62976; border-color: #d62976; background: #fff0f5; }
        .linkedin:hover { color: #0077b5; border-color: #0077b5; background: #f0f9ff; }
        .email:hover { color: #ea4335; border-color: #ea4335; background: #fff0ee; }

        /* Section card styles */
        .section-card {
            background: #ffffffdd;
            backdrop-filter: blur(4px);
            border-radius: 2rem;
            padding: 1.8rem 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 10px 25px -5px rgba(0,0,0,0.05);
            border: 1px solid rgba(255,255,255,0.7);
            transition: transform 0.1s ease;
        }
        .section-title {
            font-size: 1.7rem;
            font-weight: 700;
            margin-bottom: 1.3rem;
            display: flex;
            align-items: center;
            gap: 12px;
            color: #0f2b3d;
            border-left: 5px solid #3b82f6;
            padding-left: 1rem;
        }
        .section-title i {
            color: #3b82f6;
            font-size: 1.7rem;
        }

        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
            gap: 1rem;
        }
        .about-chip {
            background: #f8fafc;
            border-radius: 1.2rem;
            padding: 0.9rem 1.2rem;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 1rem;
            border: 1px solid #eef2ff;
            transition: 0.1s;
        }
        .about-chip i {
            font-size: 1.3rem;
            width: 28px;
            color: #2563eb;
        }

        /* Tech stack badges modern */
        .tech-badge {
            display: inline-flex;
            align-items: center;
            background: white;
            padding: 0.5rem 1rem;
            margin: 0.4rem;
            border-radius: 60px;
            font-size: 0.85rem;
            font-weight: 600;
            gap: 10px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
            border: 1px solid #e0e7ff;
            transition: all 0.2s;
        }
        .tech-badge:hover {
            transform: scale(1.02);
            background: #fefefe;
            border-color: #b1c5f0;
        }
        .stack-wrapper {
            display: flex;
            flex-wrap: wrap;
            margin-top: 0.8rem;
        }

        /* stats row */
        .stats-row {
            display: flex;
            flex-wrap: wrap;
            gap: 1.8rem;
            justify-content: center;
            margin-bottom: 2rem;
        }
        .stat-card {
            flex: 1;
            min-width: 260px;
            background: #ffffffcc;
            backdrop-filter: blur(8px);
            border-radius: 1.8rem;
            padding: 1.2rem;
            text-align: center;
            transition: all 0.2s;
            border: 1px solid #eef2ff;
        }
        .stat-card img {
            max-width: 100%;
            border-radius: 20px;
            box-shadow: 0 6px 14px rgba(0,0,0,0.05);
        }
        .stat-label {
            font-weight: 700;
            margin-top: 0.7rem;
            color: #1e293b;
            font-size: 0.9rem;
        }

        .visitor-badge {
            display: flex;
            justify-content: center;
            margin: 1.5rem 0 0.5rem;
        }
        .visitor-count {
            background: #eef2ff;
            border-radius: 60px;
            padding: 0.5rem 1.4rem;
            font-family: monospace;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
        }

        footer {
            text-align: center;
            margin-top: 2rem;
            font-size: 0.8rem;
            color: #4b5563;
            padding-top: 1rem;
            border-top: 1px solid #cfdfed;
        }
        @media (max-width: 720px) {
            body { padding: 1rem; }
            h1 { font-size: 2rem; }
            .hero-card { padding: 1.2rem; }
            .section-card { padding: 1.2rem; }
        }
        a {
            text-decoration: none;
        }
        .highlight {
            background: linear-gradient(120deg, #e0f2fe, #ffffff);
        }
    </style>
</head>
<body>
<div class="container">
    <!-- Hero Section with Typing SVG simulation (static but stylish) -->
    <div class="hero-card">
        <h1>👋 Hi, I'm Saurabh Kumar</h1>
        <div class="subhead">
            🚀 PHP & Laravel Full Stack Developer | Web Developer | Tech Enthusiast
        </div>
        <div class="typing-wrapper">
            <i class="fas fa-code"></i>
            <span id="dynamic-text"></span>
            <i class="fas fa-cursor" style="opacity:0.8;"></i>
        </div>
        <!-- Socials from original readme -->
        <div class="social-row">
            <a href="https://instagram.com/rockingstarsaurabh" target="_blank" class="social-icon instagram">
                <i class="fab fa-instagram"></i> Instagram
            </a>
            <a href="https://linkedin.com/in/saurabh-kumar-378810272" target="_blank" class="social-icon linkedin">
                <i class="fab fa-linkedin-in"></i> LinkedIn
            </a>
            <a href="mailto:saurabhkumarssp@gmail.com" class="social-icon email">
                <i class="fas fa-envelope"></i> Email
            </a>
        </div>
    </div>

    <!-- About Me Section with Icons -->
    <div class="section-card">
        <div class="section-title">
            <i class="fas fa-user-astronaut"></i> 
            <span>👨‍💻 About Me</span>
        </div>
        <div class="about-grid">
            <div class="about-chip"><i class="fas fa-laptop-code"></i> 💻 Passionate Full Stack Web Developer</div>
            <div class="about-chip"><i class="fas fa-seedling"></i> 🌱 Continuously learning new web technologies</div>
            <div class="about-chip"><i class="fas fa-fire"></i> 🔥 Strong knowledge of PHP and Laravel Framework</div>
            <div class="about-chip"><i class="fas fa-database"></i> 🎯 Building responsive & database-driven apps</div>
            <div class="about-chip"><i class="fas fa-layer-group"></i> 📚 MVC, CRUD, Auth, REST APIs</div>
            <div class="about-chip"><i class="fas fa-paintbrush"></i> 🎨 Clean, responsive & user-friendly interfaces</div>
            <div class="about-chip"><i class="fas fa-tachometer-alt"></i> ⚡ Simple, maintainable & efficient code</div>
        </div>
    </div>

    <!-- Tech Stack - beautifully styled with original badges transformation -->
    <div class="section-card">
        <div class="section-title">
            <i class="fas fa-microchip"></i>
            <span>💻 Tech Stack & Tools</span>
        </div>
        <div class="stack-wrapper">
            <!-- mapping all tech from readme with custom icons -->
            <span class="tech-badge"><i class="fab fa-cuttlefish"></i> C</span>
            <span class="tech-badge"><i class="fab fa-html5"></i> HTML5</span>
            <span class="tech-badge"><i class="fab fa-js"></i> JavaScript</span>
            <span class="tech-badge"><i class="fab fa-php"></i> PHP</span>
            <span class="tech-badge"><i class="fas fa-cloud-upload-alt"></i> Netlify</span>
            <span class="tech-badge"><i class="fab fa-bootstrap"></i> Bootstrap</span>
            <span class="tech-badge"><i class="fas fa-server"></i> Apache</span>
            <span class="tech-badge"><i class="fas fa-database"></i> MySQL</span>
            <span class="tech-badge"><i class="fas fa-database"></i> SQLite</span>
            <span class="tech-badge"><i class="fab fa-canva"></i> Canva</span>
            <span class="tech-badge"><i class="fab fa-github-alt"></i> GitHub Actions</span>
            <span class="tech-badge"><i class="fab fa-github"></i> GitHub</span>
            <span class="tech-badge"><i class="fab fa-git-alt"></i> Git</span>
            <span class="tech-badge"><i class="fas fa-flask"></i> Postman</span>
            <span class="tech-badge"><i class="fas fa-chart-line"></i> Laravel (Expertise)</span>
            <span class="tech-badge"><i class="fas fa-mobile-alt"></i> Responsive Design</span>
        </div>
        <!-- additional note: original stack included laravel, core php -->
        <div style="margin-top: 0.8rem; font-size:0.85rem; color:#2c5282;"><i class="fas fa-crown"></i> Core PHP · Laravel · REST APIs · MVC Pattern</div>
    </div>

    <!-- GitHub Stats: Using actual stats from your profile (original links) -->
    <div class="section-card">
        <div class="section-title">
            <i class="fab fa-github"></i>
            <span>📊 GitHub Analytics</span>
        </div>
        <div class="stats-row">
            <div class="stat-card">
                <div class="stat-label">📈 GitHub Stats</div>
                <img src="https://github-readme-stats.shion.dev/api?username=Saurya899&theme=dark&hide_border=false&include_all_commits=false&count_private=false" alt="GitHub Stats" loading="lazy">
            </div>
            <div class="stat-card">
                <div class="stat-label">🔥 Streak Stats</div>
                <img src="https://streak-stats.demolab.com/?user=Saurya899&theme=dark&hide_border=false" alt="GitHub Streak" loading="lazy">
            </div>
            <div class="stat-card">
                <div class="stat-label">📚 Top Languages</div>
                <img src="https://github-readme-stats.shion.dev/api/top-langs/?username=Saurya899&theme=dark&hide_border=false&include_all_commits=false&count_private=false&layout=compact" alt="Top Languages" loading="lazy">
            </div>
        </div>
    </div>

    <!-- visitor counter and footer -->
    <div class="visitor-badge">
        <div class="visitor-count">
            <i class="fas fa-eye"></i> 
            <span>Profile views:</span> 
            <img src="https://komarev.com/ghpvc/?username=Saurya899&icon=0&color=0&style=flat" alt="visitor counter" style="display: inline-block; width: auto; height: 20px; margin-left: 6px;">
        </div>
    </div>

    <footer>
        <p>⚡ Built with modern design | PHP • Laravel • Full Stack Enthusiast | © Saurabh Kumar</p>
        <p style="margin-top: 6px;"><i class="fas fa-code-branch"></i> Proudly created with GPRM & custom elegance</p>
    </footer>
</div>

<!-- small script for dynamic typing effect to replicate readme-typing-svg but interactive -->
<script>
    (function() {
        const phrases = [
            "PHP Developer",
            "Laravel Developer",
            "Core PHP Expert",
            "HTML / CSS / JavaScript",
            "Building Modern Web Apps"
        ];
        let idx = 0;
        let charIndex = 0;
        let isDeleting = false;
        const dynamicSpan = document.getElementById("dynamic-text");
        if (!dynamicSpan) return;
        
        function typeEffect() {
            const currentPhrase = phrases[idx];
            if (isDeleting) {
                dynamicSpan.textContent = currentPhrase.substring(0, charIndex - 1);
                charIndex--;
                if (charIndex === 0) {
                    isDeleting = false;
                    idx = (idx + 1) % phrases.length;
                    setTimeout(typeEffect, 400);
                } else {
                    setTimeout(typeEffect, 60);
                }
            } else {
                dynamicSpan.textContent = currentPhrase.substring(0, charIndex + 1);
                charIndex++;
                if (charIndex === currentPhrase.length) {
                    isDeleting = true;
                    setTimeout(typeEffect, 1800);
                } else {
                    setTimeout(typeEffect, 100);
                }
            }
        }
        typeEffect();
    })();
</script>
</body>
</html>
