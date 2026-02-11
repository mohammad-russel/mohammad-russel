<!-- Tailwind CSS & FontAwesome Dependencies -->
<script src="https://cdn.tailwindcss.com"></script>
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
<script>
    tailwind.config = {
        theme: {
            extend: {
                colors: {
                    slate: { 850: '#151e2e', 900: '#0f172a' },
                    cyan: { 400: '#36BCF7' }
                },
                animation: {
                    'fade-in': 'fadeIn 1s ease-out forwards',
                    'slide-up': 'slideUp 0.8s ease-out forwards',
                },
                keyframes: {
                    fadeIn: { '0%': { opacity: '0' }, '100%': { opacity: '1' } },
                    slideUp: { '0%': { opacity: '0', transform: 'translateY(20px)' }, '100%': { opacity: '1', transform: 'translateY(0)' } }
                }
            }
        }
    }
</script>

<!-- Content Wrapper -->
<div class="bg-slate-900 text-slate-300 font-sans w-full flex flex-col items-center selection:bg-cyan-400 selection:text-slate-900 p-4">

    <main class="w-full max-w-4xl py-12 space-y-16">

        <!-- Hero Section -->
        <section class="text-center space-y-6 animate-fade-in">
            <div class="inline-block p-1 rounded-full bg-gradient-to-r from-cyan-400 to-blue-500 mb-4">
                <div class="bg-slate-900 rounded-full p-1">
                    <img src="https://ui-avatars.com/api/?name=Mohammad+Rasel&background=0D1117&color=36BCF7&size=128" alt="Mohammad Rasel" class="w-32 h-32 rounded-full border-4 border-slate-900 shadow-2xl">
                </div>
            </div>
            
            <h1 class="text-4xl md:text-5xl font-bold text-white tracking-tight">
                Hi, I'm <span class="text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-500">Mohammad Rasel</span>
            </h1>

            <div class="h-12 flex items-center justify-center">
                <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&pause=1000&color=36BCF7&center=true&vCenter=true&width=500&lines=Full+Stack+PHP+Developer;MVP+Builder;System+Automation+Architect" alt="Typing Text" />
            </div>

            <p class="text-xl text-slate-400 italic font-light max-w-2xl mx-auto">
                "Turning complex business logic into automated, scalable systems."
            </p>

            <div class="pt-4">
                <a href="https://raseloriginal.digital" target="_blank" class="inline-flex items-center gap-2 px-6 py-3 bg-cyan-500 hover:bg-cyan-400 text-slate-900 font-bold rounded-full transition-all transform hover:scale-105 shadow-[0_0_20px_rgba(56,188,247,0.3)]">
                    <i class="fas fa-globe"></i> Visit Portfolio
                </a>
            </div>
        </section>

        <!-- About Section -->
        <section class="bg-slate-850 rounded-2xl p-8 border border-slate-700/50 shadow-xl animate-slide-up" style="animation-delay: 0.2s;">
            <div class="flex items-center gap-3 mb-6">
                <span class="text-2xl">🚀</span>
                <h2 class="text-2xl font-bold text-white">About Me</h2>
            </div>
            <div class="space-y-4 text-lg leading-relaxed">
                <p>
                    I am a <strong class="text-cyan-400">Full Stack PHP Developer</strong> and <strong class="text-cyan-400">System Automation Architect</strong> focused on building MVPs that solve real business problems.
                </p>
                <ul class="space-y-3 mt-4">
                    <li class="flex items-start gap-3">
                        <span class="mt-1 text-cyan-400">🔭</span>
                        <span><strong>Currently working on:</strong> A custom <span class="text-slate-100">Inventory & Staff Management System</span>.</span>
                    </li>
                    <li class="flex items-start gap-3">
                        <span class="mt-1 text-green-400">🌱</span>
                        <span><strong>Currently learning:</strong> The <span class="text-slate-100">MERN Stack</span>.</span>
                    </li>
                </ul>
            </div>
        </section>

        <!-- Tech Stack -->
        <section class="space-y-6 animate-slide-up" style="animation-delay: 0.4s;">
            <div class="flex items-center gap-3 mb-2 justify-center">
                <span class="text-2xl">🛠️</span>
                <h2 class="text-2xl font-bold text-white">Tech Stack & Tools</h2>
            </div>
            
            <div class="grid gap-6 md:grid-cols-2">
                <!-- Backend -->
                <div class="bg-slate-850 p-6 rounded-xl border border-slate-700/50">
                    <h3 class="text-sm font-semibold text-slate-400 uppercase tracking-wider mb-4 border-b border-slate-700 pb-2">Core & Backend</h3>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-slate-700/50 text-indigo-300 rounded-lg border border-indigo-500/20 text-sm font-medium flex items-center gap-2"><i class="fab fa-php"></i> PHP</span>
                        <span class="px-3 py-1 bg-slate-700/50 text-blue-300 rounded-lg border border-blue-500/20 text-sm font-medium flex items-center gap-2"><i class="fas fa-database"></i> MySQL</span>
                        <span class="px-3 py-1 bg-slate-700/50 text-yellow-300 rounded-lg border border-yellow-500/20 text-sm font-medium flex items-center gap-2"><i class="fab fa-js"></i> JavaScript</span>
                    </div>
                </div>

                <!-- Frontend -->
                <div class="bg-slate-850 p-6 rounded-xl border border-slate-700/50">
                    <h3 class="text-sm font-semibold text-slate-400 uppercase tracking-wider mb-4 border-b border-slate-700 pb-2">Frontend</h3>
                    <div class="flex flex-wrap gap-2">
                        <span class="px-3 py-1 bg-slate-700/50 text-orange-300 rounded-lg border border-orange-500/20 text-sm font-medium flex items-center gap-2"><i class="fab fa-html5"></i> HTML5</span>
                        <span class="px-3 py-1 bg-slate-700/50 text-blue-300 rounded-lg border border-blue-500/20 text-sm font-medium flex items-center gap-2"><i class="fab fa-css3-alt"></i> CSS3</span>
                        <span class="px-3 py-1 bg-slate-700/50 text-teal-300 rounded-lg border border-teal-500/20 text-sm font-medium flex items-center gap-2"><i class="fas fa-wind"></i> Tailwind</span>
                        <span class="px-3 py-1 bg-slate-700/50 text-blue-200 rounded-lg border border-blue-400/20 text-sm font-medium">jQuery</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- Stats -->
        <section class="space-y-8 animate-slide-up" style="animation-delay: 0.6s;">
            <div class="text-center">
                <div class="flex items-center gap-3 mb-6 justify-center">
                    <span class="text-2xl">📊</span>
                    <h2 class="text-2xl font-bold text-white">GitHub Activity</h2>
                </div>
                
                <div class="grid md:grid-cols-2 gap-4">
                    <img src="https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&theme=tokyonight&hide_border=true&bg_color=151e2e&title_color=36BCF7&icon_color=36BCF7" 
                         alt="GitHub Stats" 
                         class="w-full h-auto rounded-xl shadow-lg">
                    
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_GITHUB_USERNAME&layout=compact&theme=tokyonight&hide_border=true&bg_color=151e2e&title_color=36BCF7" 
                         alt="Top Languages" 
                         class="w-full h-auto rounded-xl shadow-lg">
                </div>
            </div>
        </section>

        <footer class="border-t border-slate-800 pt-8 text-center animate-slide-up" style="animation-delay: 0.8s;">
            <p class="text-slate-500 mb-4">Connect with me</p>
            <div class="flex justify-center gap-4">
                <a href="https://raseloriginal.digital" class="p-3 bg-slate-800 hover:bg-cyan-500 hover:text-slate-900 rounded-full transition-colors duration-300 text-cyan-400">
                    <i class="fas fa-globe text-xl"></i>
                </a>
                <a href="https://github.com/YOUR_GITHUB_USERNAME" class="p-3 bg-slate-800 hover:bg-slate-700 rounded-full transition-colors duration-300 text-white">
                    <i class="fab fa-github text-xl"></i>
                </a>
            </div>
        </footer>

    </main>
</div>
