<!-- FontAwesome Dependencies -->
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">

<style>
    /* Reset & Base Styles */
    * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
    }

    body {
        font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    }

    /* Theme Variables */
    :root {
        --bg-dark: #0f172a;
        --bg-card: #151e2e;
        --text-main: #cbd5e1;
        --text-white: #ffffff;
        --text-muted: #64748b;
        --accent-cyan: #36BCF7;
        --accent-blue: #3b82f6;
        --border-color: rgba(51, 65, 85, 0.5);
    }

    /* Main Wrapper */
    .profile-wrapper {
        background-color: var(--bg-dark);
        color: var(--text-main);
        min-height: 100vh;
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 1rem;
    }

    .container {
        width: 100%;
        max-width: 56rem; /* approx 4xl */
        padding: 3rem 0;
        display: flex;
        flex-direction: column;
        gap: 4rem; /* space-y-16 */
    }

    /* Animations */
    @keyframes fadeIn {
        from { opacity: 0; }
        to { opacity: 1; }
    }

    @keyframes slideUp {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }

    .animate-fade-in {
        animation: fadeIn 1s ease-out forwards;
    }

    .animate-slide-up {
        opacity: 0; /* start hidden */
        animation: slideUp 0.8s ease-out forwards;
    }

    .delay-200 { animation-delay: 0.2s; }
    .delay-400 { animation-delay: 0.4s; }
    .delay-600 { animation-delay: 0.6s; }
    .delay-800 { animation-delay: 0.8s; }

    /* Hero Section */
    .hero-section {
        text-align: center;
        display: flex;
        flex-direction: column;
        gap: 1.5rem;
    }

    .profile-img-container {
        display: inline-block;
        padding: 0.25rem;
        border-radius: 50%;
        background: linear-gradient(to right, var(--accent-cyan), var(--accent-blue));
        margin-bottom: 1rem;
    }

    .profile-img-inner {
        background-color: var(--bg-dark);
        border-radius: 50%;
        padding: 0.25rem;
    }

    .profile-avatar {
        width: 8rem;
        height: 8rem;
        border-radius: 50%;
        border: 4px solid var(--bg-dark);
        box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
    }

    .hero-title {
        font-size: 2.25rem;
        font-weight: 700;
        color: var(--text-white);
        letter-spacing: -0.025em;
    }

    @media (min-width: 768px) {
        .hero-title { font-size: 3rem; }
    }

    .gradient-text {
        background: linear-gradient(to right, var(--accent-cyan), var(--accent-blue));
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }

    .typing-wrapper {
        height: 3rem;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .hero-quote {
        font-size: 1.25rem;
        color: #94a3b8;
        font-style: italic;
        font-weight: 300;
        max-width: 42rem;
        margin: 0 auto;
    }

    .btn-portfolio {
        display: inline-flex;
        align-items: center;
        gap: 0.5rem;
        padding: 0.75rem 1.5rem;
        background-color: #0ea5e9; /* slightly darker cyan for contrast */
        color: var(--bg-dark);
        font-weight: 700;
        border-radius: 9999px;
        text-decoration: none;
        transition: transform 0.2s, background-color 0.2s;
        box-shadow: 0 0 20px rgba(56, 188, 247, 0.3);
    }

    .btn-portfolio:hover {
        background-color: var(--accent-cyan);
        transform: scale(1.05);
    }

    /* Card/Section Styles */
    .card-section {
        background-color: var(--bg-card);
        border-radius: 1rem;
        padding: 2rem;
        border: 1px solid var(--border-color);
        box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
    }

    .section-header {
        display: flex;
        align-items: center;
        gap: 0.75rem;
        margin-bottom: 1.5rem;
    }
    
    .section-header.center {
        justify-content: center;
    }

    .section-title {
        font-size: 1.5rem;
        font-weight: 700;
        color: var(--text-white);
    }

    .text-icon { font-size: 1.5rem; }

    /* List Styles */
    .about-list {
        list-style: none;
        display: flex;
        flex-direction: column;
        gap: 0.75rem;
        margin-top: 1rem;
    }

    .about-item {
        display: flex;
        align-items: flex-start;
        gap: 0.75rem;
    }

    .highlight-cyan { color: var(--accent-cyan); }
    .highlight-green { color: #4ade80; }
    .highlight-yellow { color: #facc15; }
    .highlight-white { color: #f1f5f9; }

    /* Grid Layouts */
    .grid-2 {
        display: grid;
        grid-template-columns: 1fr;
        gap: 1.5rem;
    }

    @media (min-width: 768px) {
        .grid-2 { grid-template-columns: 1fr 1fr; }
    }

    /* Tech Stack Badges */
    .tech-card {
        background-color: var(--bg-card);
        padding: 1.5rem;
        border-radius: 0.75rem;
        border: 1px solid var(--border-color);
    }

    .tech-header {
        font-size: 0.875rem;
        font-weight: 600;
        color: var(--text-muted);
        text-transform: uppercase;
        letter-spacing: 0.05em;
        margin-bottom: 1rem;
        border-bottom: 1px solid rgba(51, 65, 85, 1);
        padding-bottom: 0.5rem;
    }

    .badge-container {
        display: flex;
        flex-wrap: wrap;
        gap: 0.5rem;
    }

    .badge {
        padding: 0.25rem 0.75rem;
        border-radius: 0.5rem;
        font-size: 0.875rem;
        font-weight: 500;
        display: flex;
        align-items: center;
        gap: 0.5rem;
        background-color: rgba(51, 65, 85, 0.5); /* fallback */
    }

    /* Specific Badge Colors mimicking the Tailwind versions */
    .badge-indigo { background: rgba(55, 48, 163, 0.5); color: #a5b4fc; border: 1px solid rgba(99, 102, 241, 0.2); }
    .badge-blue { background: rgba(30, 58, 138, 0.5); color: #93c5fd; border: 1px solid rgba(59, 130, 246, 0.2); }
    .badge-yellow { background: rgba(113, 63, 18, 0.5); color: #fde047; border: 1px solid rgba(234, 179, 8, 0.2); }
    .badge-orange { background: rgba(124, 45, 18, 0.5); color: #fdba74; border: 1px solid rgba(249, 115, 22, 0.2); }
    .badge-teal { background: rgba(19, 78, 74, 0.5); color: #5eead4; border: 1px solid rgba(20, 184, 166, 0.2); }
    .badge-red { background: rgba(127, 29, 29, 0.5); color: #fca5a5; border: 1px solid rgba(239, 68, 68, 0.2); }
    .badge-purple { background: rgba(88, 28, 135, 0.5); color: #d8b4fe; border: 1px solid rgba(168, 85, 247, 0.2); }

    /* Stats Images */
    .stats-img {
        width: 100%;
        height: auto;
        border-radius: 0.75rem;
        box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
    }

    /* Footer */
    .footer {
        border-top: 1px solid #1e293b;
        padding-top: 2rem;
        text-align: center;
        width: 100%;
    }

    .footer p {
        color: var(--text-muted);
        margin-bottom: 1rem;
    }

    .social-links {
        display: flex;
        justify-content: center;
        gap: 1rem;
    }

    .social-btn {
        padding: 0.75rem;
        background-color: #1e293b;
        color: var(--text-white);
        border-radius: 9999px;
        transition: background-color 0.3s;
        display: flex;
        align-items: center;
        justify-content: center;
        text-decoration: none;
    }

    .social-btn.cyan { color: var(--accent-cyan); }
    .social-btn:hover { background-color: var(--accent-cyan); color: var(--bg-dark); }
    .social-btn.cyan:hover { background-color: var(--accent-cyan); color: var(--bg-dark); }

</style>

<!-- Content Wrapper -->
<div class="profile-wrapper">

    <main class="container">

        <!-- Hero Section -->
        <section class="hero-section animate-fade-in">
            <div>
                <div class="profile-img-container">
                    <div class="profile-img-inner">
                        <img src="https://ui-avatars.com/api/?name=Mohammad+Rasel&background=0D1117&color=36BCF7&size=128" alt="Mohammad Rasel" class="profile-avatar">
                    </div>
                </div>
            </div>
            
            <h1 class="hero-title">
                Hi, I'm <span class="gradient-text">Mohammad Rasel</span>
            </h1>

            <div class="typing-wrapper">
                <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&pause=1000&color=36BCF7&center=true&vCenter=true&width=500&lines=Full+Stack+PHP+Developer;MVP+Builder;System+Automation+Architect" alt="Typing Text" />
            </div>

            <p class="hero-quote">
                "Turning complex business logic into automated, scalable systems."
            </p>

            <div style="padding-top: 1rem;">
                <a href="https://raseloriginal.digital" target="_blank" class="btn-portfolio">
                    <i class="fas fa-globe"></i> Visit Portfolio
                </a>
            </div>
        </section>

        <!-- About Section -->
        <section class="card-section animate-slide-up delay-200">
            <div class="section-header">
                <span class="text-icon">🚀</span>
                <h2 class="section-title">About Me</h2>
            </div>
            <div style="font-size: 1.125rem; line-height: 1.75;">
                <p>
                    I am a <strong class="highlight-cyan">Full Stack PHP Developer</strong> and <strong class="highlight-cyan">System Automation Architect</strong> focused on building MVPs that solve real business problems.
                </p>
                <ul class="about-list">
                    <li class="about-item">
                        <span class="highlight-cyan" style="margin-top: 0.25rem;">🔭</span>
                        <span><strong>Currently working on:</strong> A custom <span class="highlight-white">Inventory & Staff Management System</span>.</span>
                    </li>
                    <li class="about-item">
                        <span class="highlight-green" style="margin-top: 0.25rem;">🌱</span>
                        <span><strong>Currently learning:</strong> The <span class="highlight-white">MERN Stack</span>.</span>
                    </li>
                </ul>
            </div>
        </section>

        <!-- Tech Stack -->
        <section class="animate-slide-up delay-400">
            <div class="section-header center">
                <span class="text-icon">🛠️</span>
                <h2 class="section-title">Tech Stack & Tools</h2>
            </div>
            
            <div class="grid-2">
                <!-- Backend -->
                <div class="tech-card">
                    <h3 class="tech-header">Core & Backend</h3>
                    <div class="badge-container">
                        <span class="badge badge-indigo"><i class="fab fa-php"></i> PHP</span>
                        <span class="badge badge-blue"><i class="fas fa-database"></i> MySQL</span>
                        <span class="badge badge-yellow"><i class="fab fa-js"></i> JavaScript</span>
                    </div>
                </div>

                <!-- Frontend -->
                <div class="tech-card">
                    <h3 class="tech-header">Frontend</h3>
                    <div class="badge-container">
                        <span class="badge badge-orange"><i class="fab fa-html5"></i> HTML5</span>
                        <span class="badge badge-blue"><i class="fab fa-css3-alt"></i> CSS3</span>
                        <span class="badge badge-teal"><i class="fas fa-wind"></i> Tailwind</span>
                        <span class="badge badge-blue">jQuery</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Stats -->
        <section class="animate-slide-up delay-600" style="display: flex; flex-direction: column; gap: 2rem;">
            <div style="text-align: center;">
                <div class="section-header center">
                    <span class="text-icon">📊</span>
                    <h2 class="section-title">GitHub Activity</h2>
                </div>
                
                <div class="grid-2">
                    <img src="https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&theme=tokyonight&hide_border=true&bg_color=151e2e&title_color=36BCF7&icon_color=36BCF7" 
                         alt="GitHub Stats" 
                         class="stats-img">
                    
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_GITHUB_USERNAME&layout=compact&theme=tokyonight&hide_border=true&bg_color=151e2e&title_color=36BCF7" 
                         alt="Top Languages" 
                         class="stats-img">
                </div>
            </div>
        </section>

        <footer class="footer animate-slide-up delay-800">
            <p>Connect with me</p>
            <div class="social-links">
                <a href="https://raseloriginal.digital" class="social-btn cyan">
                    <i class="fas fa-globe" style="font-size: 1.25rem;"></i>
                </a>
                <a href="https://github.com/YOUR_GITHUB_USERNAME" class="social-btn">
                    <i class="fab fa-github" style="font-size: 1.25rem;"></i>
                </a>
            </div>
        </footer>

    </main>
</div>
