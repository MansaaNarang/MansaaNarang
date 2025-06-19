<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mansaa Narang - Frontend Developer</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: white;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .header {
            text-align: center;
            padding: 60px 0;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            margin-bottom: 40px;
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            animation: shimmer 3s infinite;
        }
        
        @keyframes shimmer {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }
        
        .header h1 {
            font-size: 3.5rem;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: gradient 3s ease-in-out infinite;
        }
        
        @keyframes gradient {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }
        
        .header h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            opacity: 0.9;
        }
        
        .profile-views {
            display: inline-block;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            padding: 10px 20px;
            border-radius: 25px;
            margin: 20px 0;
            font-weight: 500;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }
        
        .section {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 30px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
        .section h2 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: #4ecdc4;
            text-align: center;
        }
        
        .about-me {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .info-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid #4ecdc4;
            transition: transform 0.3s ease;
        }
        
        .info-card:hover {
            transform: translateX(10px);
        }
        
        .info-card h4 {
            color: #ff6b6b;
            margin-bottom: 10px;
            font-size: 1.2rem;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .skill-item {
            background: linear-gradient(45deg, #667eea, #764ba2);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            transition: transform 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .skill-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s;
        }
        
        .skill-item:hover::before {
            left: 100%;
        }
        
        .skill-item:hover {
            transform: translateY(-5px) scale(1.05);
        }
        
        .skill-item img {
            width: 40px;
            height: 40px;
            margin-bottom: 10px;
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .project-card {
            background: linear-gradient(135deg, #667eea, #764ba2);
            padding: 25px;
            border-radius: 15px;
            transition: transform 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, #ff6b6b, #4ecdc4, #45b7d1);
        }
        
        .project-card:hover {
            transform: translateY(-10px);
        }
        
        .project-card h4 {
            color: #4ecdc4;
            margin-bottom: 10px;
            font-size: 1.3rem;
        }
        
        .project-card p {
            opacity: 0.9;
            line-height: 1.6;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
        .social-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 12px 20px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            text-decoration: none;
            border-radius: 25px;
            transition: all 0.3s ease;
            font-weight: 500;
        }
        
        .social-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .stat-card {
            text-align: center;
            padding: 20px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            transition: transform 0.3s ease;
        }
        
        .stat-card:hover {
            transform: scale(1.05);
        }
        
        .stat-card img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
        }
        
        .trophy-container {
            text-align: center;
            margin-top: 30px;
        }
        
        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .floating-element {
            position: absolute;
            width: 20px;
            height: 20px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }
        
        .floating-element:nth-child(1) { top: 20%; left: 10%; animation-delay: 0s; }
        .floating-element:nth-child(2) { top: 60%; left: 20%; animation-delay: 2s; }
        .floating-element:nth-child(3) { top: 40%; left: 80%; animation-delay: 4s; }
        .floating-element:nth-child(4) { top: 80%; left: 70%; animation-delay: 1s; }
        .floating-element:nth-child(5) { top: 30%; left: 90%; animation-delay: 3s; }
        
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.5rem;
            }
            
            .container {
                padding: 10px;
            }
            
            .social-links {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="floating-elements">
        <div class="floating-element"></div>
        <div class="floating-element"></div>
        <div class="floating-element"></div>
        <div class="floating-element"></div>
        <div class="floating-element"></div>
    </div>

    <div class="container">
        <div class="header">
            <h1>Hi 👋, I'm Mansaa Narang</h1>
            <h3>A Frontend Developer from India</h3>
            <div class="profile-views">
                <img src="https://komarev.com/ghpvc/?username=mansaanarang&label=Profile%20views&color=0e75b6&style=flat" alt="Profile views" />
            </div>
            <div style="margin-top: 20px;">
                <img src="https://github-profile-trophy.vercel.app/?username=mansaanarang&theme=darkhub&no-frame=true&margin-w=4&row=1" alt="GitHub Trophies" />
            </div>
        </div>

        <div class="section">
            <h2>🚀 About Me</h2>
            <div class="about-me">
                <div class="info-card">
                    <h4>🔭 Currently Working On</h4>
                    <p>E-commerce Website - Building modern, responsive web applications</p>
                </div>
                <div class="info-card">
                    <h4>🌱 Learning & Growing</h4>
                    <p>Completed SMARTINTERNZ project assignments</p>
                </div>
                <div class="info-card">
                    <h4>👯 Collaboration</h4>
                    <p>United Transit Services (UTS) - Team collaboration project</p>
                </div>
                <div class="info-card">
                    <h4>🤝 Personal Project</h4>
                    <p>Art Gallery Website - Showcasing creative web development</p>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🛠️ Languages and Tools</h2>
            <div class="skills-grid">
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="C++" />
                    <div>C++</div>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="CSS3" />
                    <div>CSS3</div>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="JavaScript" />
                    <div>JavaScript</div>
                </div>
                <div class="skill-item">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="MySQL" />
                    <div>MySQL</div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>📊 GitHub Statistics</h2>
            <div class="stats-container">
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api/top-langs?username=mansaanarang&show_icons=true&locale=en&layout=compact&theme=tokyonight" alt="Top Languages" />
                </div>
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api?username=mansaanarang&show_icons=true&locale=en&theme=tokyonight" alt="GitHub Stats" />
                </div>
            </div>
            <div class="stat-card" style="margin-top: 20px;">
                <img src="https://github-readme-streak-stats.herokuapp.com/?user=mansaanarang&theme=tokyonight" alt="GitHub Streak" />
            </div>
        </div>

        <div class="section">
            <h2>🌐 Connect With Me</h2>
            <div class="social-links">
                <a href="https://codepen.io/mansaa-narang" target="_blank" class="social-link">
                    <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/codepen.svg" alt="CodePen" height="20" width="20" />
                    CodePen
                </a>
                <a href="https://www.linkedin.com/in/mansaa-narang-067118277/" target="_blank" class="social-link">
                    <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="LinkedIn" height="20" width="20" />
                    LinkedIn
                </a>
                <a href="https://leetcode.com/u/mansaa_narang/" target="_blank" class="social-link">
                    <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/leet-code.svg" alt="LeetCode" height="20" width="20" />
                    LeetCode
                </a>
                <a href="https://www.geeksforgeeks.org/user/mansaanarang/" target="_blank" class="social-link">
                    <img src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/geeks-for-geeks.svg" alt="GeeksforGeeks" height="20" width="20" />
                    GeeksforGeeks
                </a>
                <a href="mailto:mansaanarang08@gmail.com" class="social-link">
                    📧 Email
                </a>
                <a href="https://drive.google.com/file/d/1Cs1mQd_6AaXMU80rNtkJdcPloGlw3TDB/view?usp=sharing" target="_blank" class="social-link">
                    📄 Resume
                </a>
            </div>
        </div>
    </div>
</body>
</html>
