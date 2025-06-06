<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>陳小堃 | 前端开发者</title>
    <!-- 引入Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- 引入Font Awesome -->
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <!-- 引入Google字体 -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Tailwind配置 -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#165DFF',
                        secondary: '#36D399',
                        dark: '#1E293B',
                        light: '#F8FAFC',
                        muted: '#94A3B8'
                    },
                    fontFamily: {
                        inter: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    
    <!-- 自定义工具类 -->
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .text-shadow {
                text-shadow: 0 2px 4px rgba(0,0,0,0.1);
            }
            .transition-custom {
                transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            }
            .animate-float {
                animation: float 6s ease-in-out infinite;
            }
            @keyframes float {
                0% { transform: translateY(0px); }
                50% { transform: translateY(-20px); }
                100% { transform: translateY(0px); }
            }
            .bg-gradient-blue {
                background: linear-gradient(135deg, #165DFF 0%, #0E42C0 100%);
            }
        }
    </style>
</head>
<body class="font-inter bg-light text-dark antialiased">
    <!-- 导航栏 -->
    <header id="navbar" class="fixed w-full top-0 z-50 transition-all duration-300 bg-transparent">
        <div class="container mx-auto px-4 py-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-white flex items-center">
                <span class="bg-primary p-1 rounded mr-2">
                    <i class="fa fa-code"></i>
                </span>
                <span class="text-shadow">陳小堃</span>
            </a>
            
            <!-- 桌面导航 -->
            <nav class="hidden md:flex space-x-8">
                <a href="#home" class="text-white hover:text-secondary transition-custom font-medium">首页</a>
                <a href="#about" class="text-white hover:text-secondary transition-custom font-medium">关于我</a>
                <a href="#skills" class="text-white hover:text-secondary transition-custom font-medium">技能</a>
                <a href="#projects" class="text-white hover:text-secondary transition-custom font-medium">项目</a>
                <a href="#contact" class="text-white hover:text-secondary transition-custom font-medium">联系我</a>
            </nav>
            
            <!-- 移动菜单按钮 -->
            <button id="mobile-menu-button" class="md:hidden text-white text-2xl">
                <i class="fa fa-bars"></i>
            </button>
        </div>
        
        <!-- 移动导航 -->
        <div id="mobile-menu" class="md:hidden bg-dark/95 backdrop-blur-md absolute w-full left-0 top-full transform -translate-y-full opacity-0 transition-all duration-300 invisible">
            <div class="container mx-auto px-4 py-4 flex flex-col space-y-4">
                <a href="#home" class="text-white hover:text-secondary transition-custom font-medium py-2 border-b border-gray-700">首页</a>
                <a href="#about" class="text-white hover:text-secondary transition-custom font-medium py-2 border-b border-gray-700">关于我</a>
                <a href="#skills" class="text-white hover:text-secondary transition-custom font-medium py-2 border-b border-gray-700">技能</a>
                <a href="#projects" class="text-white hover:text-secondary transition-custom font-medium py-2 border-b border-gray-700">项目</a>
                <a href="#contact" class="text-white hover:text-secondary transition-custom font-medium py-2">联系我</a>
            </div>
        </div>
    </header>

    <!-- 英雄区域 -->
    <section id="home" class="relative min-h-screen flex items-center justify-center overflow-hidden">
        <!-- 背景渐变 -->
        <div class="absolute inset-0 bg-gradient-blue z-0"></div>
        
        <!-- 装饰元素 -->
        <div class="absolute inset-0 z-0 overflow-hidden">
            <div class="absolute top-1/4 left-1/4 w-32 h-32 bg-secondary/20 rounded-full blur-3xl animate-float"></div>
            <div class="absolute bottom-1/4 right-1/4 w-40 h-40 bg-primary/20 rounded-full blur-3xl animate-float" style="animation-delay: 2s"></div>
        </div>
        
        <div class="container mx-auto px-4 z-10 text-center">
            <div class="max-w-4xl mx-auto">
                <h1 class="text-[clamp(2.5rem,8vw,5rem)] font-bold leading-tight text-white mb-4">
                    <span class="block">你好，我是</span>
                    <span class="text-secondary">陳小堃</span>
                </h1>
                <p class="text-[clamp(1rem,3vw,1.5rem)] text-gray-200 mb-8 max-w-2xl mx-auto">
                    一名充满激情的 <span class="text-secondary font-medium">前端开发者</span>，专注于创造美观且用户友好的数字体验
                </p>
                <div class="flex flex-wrap justify-center gap-4">
                    <a href="#projects" class="px-8 py-3 bg-white text-primary font-semibold rounded-full hover:bg-gray-100 transition-custom shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                        查看我的作品
                    </a>
                    <a href="#contact" class="px-8 py-3 bg-transparent border-2 border-white text-white font-semibold rounded-full hover:bg-white/10 transition-custom shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                        联系我
                    </a>
                </div>
                
                <!-- 社交媒体链接 -->
                <div class="mt-12 flex justify-center space-x-6">
                    <a href="#" class="text-white hover:text-secondary transition-custom text-2xl">
                        <i class="fa fa-github"></i>
                    </a>
                    <a href="#" class="text-white hover:text-secondary transition-custom text-2xl">
                        <i class="fa fa-linkedin"></i>
                    </a>
                    <a href="#" class="text-white hover:text-secondary transition-custom text-2xl">
                        <i class="fa fa-twitter"></i>
                    </a>
                    <a href="#" class="text-white hover:text-secondary transition-custom text-2xl">
                        <i class="fa fa-dribbble"></i>
                    </a>
                </div>
            </div>
        </div>
        
        <!-- 滚动指示器 -->
        <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 text-white animate-bounce">
            <a href="#about" class="flex flex-col items-center">
                <span class="mb-2 text-sm font-medium">向下滚动</span>
                <i class="fa fa-chevron-down"></i>
            </a>
        </div>
    </section>

    <!-- 关于我部分 -->
    <section id="about" class="py-24 bg-light">
        <div class="container mx-auto px-4">
            <div class="max-w-6xl mx-auto">
                <div class="text-center mb-16">
                    <h2 class="text-[clamp(1.5rem,4vw,2.5rem)] font-bold mb-4">关于我</h2>
                    <div class="w-20 h-1 bg-primary mx-auto rounded-full"></div>
                </div>
                
                <div class="grid md:grid-cols-2 gap-12 items-center">
                    <!-- 个人照片 -->
                    <div class="relative">
                        <div class="relative z-10 rounded-2xl overflow-hidden shadow-2xl transform hover:scale-[1.02] transition-custom">
                            <img src="https://picsum.photos/seed/person/600/700" alt="陳小堃" class="w-full h-auto">
                        </div>
                        <div class="absolute -bottom-6 -right-6 w-64 h-64 bg-primary/10 rounded-full -z-10"></div>
                        <div class="absolute -top-6 -left-6 w-32 h-32 bg-secondary/10 rounded-full -z-10"></div>
                    </div>
                    
                    <!-- 关于我内容 -->
                    <div>
                        <h3 class="text-2xl font-semibold mb-4">你好！我是陳小堃，一名前端开发者</h3>
                        <p class="text-gray-600 mb-6 leading-relaxed">
                            拥有3年的Web开发经验。
                        </p>
                        <p class="text-gray-600 mb-8 leading-relaxed">
                            我拥有计算机科目的基础。
                        </p>
                        
                        <!-- 个人信息 -->
                        <div class="grid grid-cols-2 gap-4 mb-8">
                            <div class="flex items-center">
                                <i class="fa fa-calendar text-primary mr-3"></i>
                                <span>2007年8月2日</span>
                            </div>
                            <div class="flex items-center">
                                <i class="fa fa-map-marker text-primary mr-3"></i>
                                <span>铜仁市松桃区</span>
                            </div>
                            <div class="flex items-center">
                                <i class="fa fa-envelope text-primary mr-3"></i>
                                <span>1686828049@qq.com</span>
                            </div>
                            <div class="flex items-center">
                                <i class="fa fa-phone text-primary mr-3"></i>
                                <span>+86 19013885282</span>
                            </div>
                        </div>
                        
                        <a href="#" class="inline-flex items-center px-6 py-3 bg-primary text-white font-semibold rounded-full hover:bg-primary/90 transition-custom shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                            <i class="fa fa-download mr-2"></i> 下载简历
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 技能部分 -->
    <section id="skills" class="py-24 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="max-w-6xl mx-auto">
                <div class="text-center mb-16">
                    <h2 class="text-[clamp(1.5rem,4vw,2.5rem)] font-bold mb-4">我的技能</h2>
                    <div class="w-20 h-1 bg-primary mx-auto rounded-full"></div>
                </div>
                
                <div class="grid md:grid-cols-2 gap-12">
                    <!-- 技术技能 -->
                    <div>
                        <h3 class="text-xl font-semibold mb-6 flex items-center">
                            <i class="fa fa-code text-primary mr-3"></i> 技术技能
                        </h3>
                        
                        <div class="space-y-6">
                            <!-- 技能条1 -->
                            <div>
                                <div class="flex justify-between mb-2">
                                    <span class="font-medium">HTML/CSS</span>
                                    <span>95%</span>
                                </div>
                                <div class="h-2 bg-gray-200 rounded-full overflow-hidden">
                                    <div class="h-full bg-primary rounded-full" style="width: 95%"></div>
                                </div>
                            </div>
                            
                            <!-- 技能条2 -->
                            <div>
                                <div class="flex justify-between mb-2">
                                    <span class="font-medium">JavaScript</span>
                                    <span>90%</span>
                                </div>
                                <div class="h-2 bg-gray-200 rounded-full overflow-hidden">
                                    <div class="h-full bg-primary rounded-full" style="width: 90%"></div>
                                </div>
                            </div>
                            
                            <!-- 技能条3 -->
                            <div>
                                <div class="flex justify-between mb-2">
                                    <span class="font-medium">React</span>
                                    <span>85%</span>
                                </div>
                                <div class="h-2 bg-gray-200 rounded-full overflow-hidden">
                                    <div class="h-full bg-primary rounded-full" style="width: 85%"></div>
                                </div>
                            </div>
                            
                            <!-- 技能条4 -->
                            <div>
                                <div class="flex justify-between mb-2">
                                    <span class="font-medium">Vue.js</span>
                                    <span>80%</span>
                                </div>
                                <div class="h-2 bg-gray-200 rounded-full overflow-hidden">
                                    <div class="h-full bg-primary rounded-full" style="width: 80%"></div>
                                </div>
                            </div>
                            
                            <!-- 技能条5 -->
                            <div>
                                <div class="flex justify-between mb-2">
                                    <span class="font-medium">Node.js</span>
                                    <span>75%</span>
                                </div>
                                <div class="h-2 bg-gray-200 rounded-full overflow-hidden">
                                    <div class="h-full bg-primary rounded-full" style="width: 75%"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- 专业技能 -->
                    <div>
                        <h3 class="text-xl font-semibold mb-6 flex items-center">
                            <i class="fa fa-users text-primary mr-3"></i> 专业技能
                        </h3>
                        
                        <!-- 技能图表 -->
                        <div class="bg-white p-6 rounded-xl shadow-lg h-[300px]">
                            <canvas id="skillChart"></canvas>
                        </div>
                    </div>
                </div>
                
                <!-- 工具和技术 -->
                <div class="mt-16">
                    <h3 class="text-xl font-semibold mb-8 text-center">工具与技术</h3>
                    
                    <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-6 gap-6">
                        <!-- 工具1 -->
                        <div class="bg-white p-6 rounded-xl shadow-lg text-center hover:shadow-xl transition-custom transform hover:-translate-y-1">
                            <div class="text-4xl mb-3 text-primary">
                                <i class="fa fa-github"></i>
                            </div>
                            <h4 class="font-medium">Git</h4>
                        </div>
                        
                        <!-- 工具2 -->
                        <div class="bg-white p-6 rounded-xl shadow-lg text-center hover:shadow-xl transition-custom transform hover:-translate-y-1">
                            <div class="text-4xl mb-3 text-primary">
                                <i class="fa fa-terminal"></i>
                            </div>
                            <h4 class="font-medium">命令行</h4>
                        </div>
                        
                        <!-- 工具3 -->
                        <div class="bg-white p-6 rounded-xl shadow-lg text-center hover:shadow-xl transition-custom transform hover:-translate-y-1">
                            <div class="text-4xl mb-3 text-primary">
                                <i class="fa fa-paint-brush"></i>
                            </div>
                            <h4 class="font-medium">Figma</h4>
                        </div>
                        
                        <!-- 工具4 -->
                        <div class="bg-white p-6 rounded-xl shadow-lg text-center hover:shadow-xl transition-custom transform hover:-translate-y-1">
                            <div class="text-4xl mb-3 text-primary">
                                <i class="fa fa-database"></i>
                            </div>
                            <h4 class="font-medium">MongoDB</h4>
                        </div>
                        
                        <!-- 工具5 -->
                        <div class="bg-white p-6 rounded-xl shadow-lg text-center hover:shadow-xl transition-custom transform hover:-translate-y-1">
                            <div class="text-4xl mb-3 text-primary">
                                <i class="fa fa-cloud"></i>
                            </div>
                            <h4 class="font-medium">AWS</h4>
                        </div>
                        
                        <!-- 工具6 -->
                        <div class="bg-white p-6 rounded-xl shadow-lg text-center hover:shadow-xl transition-custom transform hover:-translate-y-1">
                            <div class="text-4xl mb-3 text-primary">
                                <i class="fa fa-bolt"></i>
                            </div>
                            <h4 class="font-medium">Firebase</h4>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 项目部分 -->
    <section id="projects" class="py-24 bg-light">
        <div class="container mx-auto px-4">
            <div class="max-w-6xl mx-auto">
                <div class="text-center mb-16">
                    <h2 class="text-[clamp(1.5rem,4vw,2.5rem)] font-bold mb-4">我的项目</h2>
                    <div class="w-20 h-1 bg-primary mx-auto rounded-full"></div>
                </div>
                
                <!-- 项目筛选 -->
                <div class="flex flex-wrap justify-center gap-4 mb-12">
                    <button class="px-6 py-2 bg-primary text-white rounded-full font-medium filter-btn active" data-filter="all">全部</button>
                    <button class="px-6 py-2 bg-gray-200 hover:bg-gray-300 rounded-full font-medium filter-btn" data-filter="web">Web应用</button>
                    <button class="px-6 py-2 bg-gray-200 hover:bg-gray-300 rounded-full font-medium filter-btn" data-filter="mobile">移动应用</button>
                    <button class="px-6 py-2 bg-gray-200 hover:bg-gray-300 rounded-full font-medium filter-btn" data-filter="design">UI/UX设计</button>
                </div>
                
                <!-- 项目网格 -->
                <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- 项目1 -->
                    <div class="project-item bg-white rounded-xl overflow-hidden shadow-lg hover:shadow-xl transition-custom transform hover:-translate-y-2" data-category="web">
                        <div class="relative overflow-hidden">
                            <img src="https://picsum.photos/seed/project1/600/400" alt="电子商务网站" class="w-full h-64 object-cover transition-transform duration-500 hover:scale-110">
                            <div class="absolute inset-0 bg-primary/70 flex items-center justify-center opacity-0 hover:opacity-100 transition-custom">
                                <a href="#" class="text-white text-2xl mx-3 hover:text-secondary transition-custom">
                                    <i class="fa fa-link"></i>
                                </a>
                                <a href="#" class="text-white text-2xl mx-3 hover:text-secondary transition-custom">
                                    <i class="fa fa-github"></i>
                                </a>
                            </div>
                        </div>
                        <div class="p-6">
                            <span class="inline-block px-3 py-1 bg-primary/10 text-primary text-sm rounded-full mb-3">Web应用</span>
                            <h3 class="text-xl font-semibold mb-2">电子商务平台</h3>
                            <p class="text-gray-600 mb-4">一个功能齐全的电子商务平台，集成了支付系统和产品管理功能。</p>
                            <div class="flex flex-wrap gap-2">
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">React</span>
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">Node.js</span>
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">MongoDB</span>
                            </div>
                        </div>
                    </div>
                    
                    <!-- 项目2 -->
                    <div class="project-item bg-white rounded-xl overflow-hidden shadow-lg hover:shadow-xl transition-custom transform hover:-translate-y-2" data-category="mobile">
                        <div class="relative overflow-hidden">
                            <img src="https://picsum.photos/seed/project2/600/400" alt="健身应用" class="w-full h-64 object-cover transition-transform duration-500 hover:scale-110">
                            <div class="absolute inset-0 bg-primary/70 flex items-center justify-center opacity-0 hover:opacity-100 transition-custom">
                                <a href="#" class="text-white text-2xl mx-3 hover:text-secondary transition-custom">
                                    <i class="fa fa-link"></i>
                                </a>
                                <a href="#" class="text-white text-2xl mx-3 hover:text-secondary transition-custom">
                                    <i class="fa fa-github"></i>
                                </a>
                            </div>
                        </div>
                        <div class="p-6">
                            <span class="inline-block px-3 py-1 bg-primary/10 text-primary text-sm rounded-full mb-3">移动应用</span>
                            <h3 class="text-xl font-semibold mb-2">健身追踪器</h3>
                            <p class="text-gray-600 mb-4">一款用于跟踪锻炼、营养和健身目标的移动应用，具有实时数据分析功能。</p>
                            <div class="flex flex-wrap gap-2">
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">React Native</span>
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">Firebase</span>
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">Chart.js</span>
                            </div>
                        </div>
                    </div>
                    
                    <!-- 项目3 -->
                    <div class="project-item bg-white rounded-xl overflow-hidden shadow-lg hover:shadow-xl transition-custom transform hover:-translate-y-2" data-category="design">
                        <div class="relative overflow-hidden">
                            <img src="https://picsum.photos/seed/project3/600/400" alt="仪表盘UI" class="w-full h-64 object-cover transition-transform duration-500 hover:scale-110">
                            <div class="absolute inset-0 bg-primary/70 flex items-center justify-center opacity-0 hover:opacity-100 transition-custom">
                                <a href="#" class="text-white text-2xl mx-3 hover:text-secondary transition-custom">
                                    <i class="fa fa-link"></i>
                                </a>
                                <a href="#" class="text-white text-2xl mx-3 hover:text-secondary transition-custom">
                                    <i class="fa fa-github"></i>
                                </a>
                            </div>
                        </div>
                        <div class="p-6">
                            <span class="inline-block px-3 py-1 bg-primary/10 text-primary text-sm rounded-full mb-3">UI/UX设计</span>
                            <h3 class="text-xl font-semibold mb-2">分析仪表盘</h3>
                            <p class="text-gray-600 mb-4">一个现代分析仪表盘设计，包含交互式图表和数据可视化组件。</p>
                            <div class="flex flex-wrap gap-2">
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">Figma</span>
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">UI/UX</span>
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">原型设计</span>
                            </div>
                        </div>
                    </div>
                    
                    <!-- 项目4 -->
                    <div class="project-item bg-white rounded-xl overflow-hidden shadow-lg hover:shadow-xl transition-custom transform hover:-translate-y-2" data-category="web">
                        <div class="relative overflow-hidden">
                            <img src="https://picsum.photos/seed/project4/600/400" alt="博客平台" class="w-full h-64 object-cover transition-transform duration-500 hover:scale-110">
                            <div class="absolute inset-0 bg-primary/70 flex items-center justify-center opacity-0 hover:opacity-100 transition-custom">
                                <a href="#" class="text-white text-2xl mx-3 hover:text-secondary transition-custom">
                                    <i class="fa fa-link"></i>
                                </a>
                                <a href="#" class="text-white text-2xl mx-3 hover:text-secondary transition-custom">
                                    <i class="fa fa-github"></i>
                                </a>
                            </div>
                        </div>
                        <div class="p-6">
                            <span class="inline-block px-3 py-1 bg-primary/10 text-primary text-sm rounded-full mb-3">Web应用</span>
                            <h3 class="text-xl font-semibold mb-2">博客平台</h3>
                            <p class="text-gray-600 mb-4">一个支持Markdown和SEO优化的博客内容管理系统。</p>
                            <div class="flex flex-wrap gap-2">
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">Next.js</span>
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">Sanity.io</span>
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">Tailwind CSS</span>
                            </div>
                        </div>
                    </div>
                    
                    <!-- 项目5 -->
                    <div class="project-item bg-white rounded-xl overflow-hidden shadow-lg hover:shadow-xl transition-custom transform hover:-translate-y-2" data-category="mobile">
                        <div class="relative overflow-hidden">
                            <img src="https://picsum.photos/seed/project5/600/400" alt="旅行应用" class="w-full h-64 object-cover transition-transform duration-500 hover:scale-110">
                            <div class="absolute inset-0 bg-primary/70 flex items-center justify-center opacity-0 hover:opacity-100 transition-custom">
                                <a href="#" class="text-white text-2xl mx-3 hover:text-secondary transition-custom">
                                    <i class="fa fa-link"></i>
                                </a>
                                <a href="#" class="text-white text-2xl mx-3 hover:text-secondary transition-custom">
                                    <i class="fa fa-github"></i>
                                </a>
                            </div>
                        </div>
                        <div class="p-6">
                            <span class="inline-block px-3 py-1 bg-primary/10 text-primary text-sm rounded-full mb-3">移动应用</span>
                            <h3 class="text-xl font-semibold mb-2">旅行伴侣</h3>
                            <p class="text-gray-600 mb-4">一款用于发现目的地、预订住宿和跟踪旅行行程的移动应用。</p>
                            <div class="flex flex-wrap gap-2">
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">Flutter</span>
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">Google Maps</span>
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">REST API</span>
                            </div>
                        </div>
                    </div>
                    
                    <!-- 项目6 -->
                    <div class="project-item bg-white rounded-xl overflow-hidden shadow-lg hover:shadow-xl transition-custom transform hover:-translate-y-2" data-category="design">
                        <div class="relative overflow-hidden">
                            <img src="https://picsum.photos/seed/project6/600/400" alt="支付UI" class="w-full h-64 object-cover transition-transform duration-500 hover:scale-110">
                            <div class="absolute inset-0 bg-primary/70 flex items-center justify-center opacity-0 hover:opacity-100 transition-custom">
                                <a href="#" class="text-white text-2xl mx-3 hover:text-secondary transition-custom">
                                    <i class="fa fa-link"></i>
                                </a>
                                <a href="#" class="text-white text-2xl mx-3 hover:text-secondary transition-custom">
                                    <i class="fa fa-github"></i>
                                </a>
                            </div>
                        </div>
                        <div class="p-6">
                            <span class="inline-block px-3 py-1 bg-primary/10 text-primary text-sm rounded-full mb-3">UI/UX设计</span>
                            <h3 class="text-xl font-semibold mb-2">支付流程</h3>
                            <p class="text-gray-600 mb-4">一个无缝的支付流程设计，支持多种支付方式和安全的结账过程。</p>
                            <div class="flex flex-wrap gap-2">
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">Figma</span>
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">支付网关</span>
                                <span class="px-2 py-1 bg-gray-100 text-gray-700 text-xs rounded">用户测试</span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- 查看更多按钮 -->
                <div class="text-center mt-12">
                    <a href="#" class="inline-flex items-center px-8 py-3 bg-primary text-white font-semibold rounded-full hover:bg-primary/90 transition-custom shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                        查看所有项目
                        <i class="fa fa-arrow-right ml-2"></i>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- 联系部分 -->
    <section id="contact" class="py-24 bg-gray-50">
        <div class="container mx-auto px-4">
            <div class="max-w-6xl mx-auto">
                <div class="text-center mb-16">
                    <h2 class="text-[clamp(1.5rem,4vw,2.5rem)] font-bold mb-4">联系我</h2>
                    <div class="w-20 h-1 bg-primary mx-auto rounded-full"></div>
                </div>
                
                <div class="grid md:grid-cols-2 gap-12">
                    <!-- 联系表单 -->
                    <div class="bg-white p-8 rounded-xl shadow-lg">
                        <h3 class="text-xl font-semibold mb-6">给我发送消息</h3>
                        <form>
                            <div class="mb-6">
                                <label for="name" class="block text-sm font-medium text-gray-700 mb-2">您的姓名</label>
                                <input type="text" id="name" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="陳小堃">
                            </div>
                            
                            <div class="mb-6">
                                <label for="email" class="block text-sm font-medium text-gray-700 mb-2">您的邮箱</label>
                                <input type="email" id="email" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="zhangsan@example.com">
                            </div>
                            
                            <div class="mb-6">
                                <label for="subject" class="block text-sm font-medium text-gray-700 mb-2">主题</label>
                                <input type="text" id="subject" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="项目咨询">
                            </div>
                            
                            <div class="mb-6">
                                <label for="message" class="block text-sm font-medium text-gray-700 mb-2">您的消息</label>
                                <textarea id="message" rows="5" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请告诉我关于您的项目..."></textarea>
                            </div>
                            
                            <button type="submit" class="w-full py-3 bg-primary text-white font-semibold rounded-lg hover:bg-primary/90 transition-custom shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                                发送消息
                            </button>
                        </form>
                    </div>
                    
                    <!-- 联系信息 -->
                    <div>
                        <h3 class="text-xl font-semibold mb-6">联系方式</h3>
                        
                        <div class="space-y-6">
                            <!-- 联系项目1 -->
                            <div class="flex items-start">
                                <div class="bg-primary/10 p-3 rounded-full mr-4">
                                    <i class="fa fa-map-marker text-primary text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-medium mb-1">地址</h4>
                                    <p class="text-gray-600">贵州省铜仁市松桃区</p>
                                </div>
                            </div>
                            
                            <!-- 联系项目2 -->
                            <div class="flex items-start">
                                <div class="bg-primary/10 p-3 rounded-full mr-4">
                                    <i class="fa fa-envelope text-primary text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-medium mb-1">邮箱</h4>
                                    <p class="text-gray-600">1686828049@qq.com</p>
                                </div>
                            </div>
                            
                            <!-- 联系项目3 -->
                            <div class="flex items-start">
                                <div class="bg-primary/10 p-3 rounded-full mr-4">
                                    <i class="fa fa-phone text-primary text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-medium mb-1">电话</h4>
				     <p>ks：陳小堃</p>
     <p>QQ：3481255411</p>
     <p>微信：CMK20070802H</p>
	
   <p><a href="https://www.anymp4.com/zh-TW/iphone-unlocker/">苹果开锁工具</a></p>

   <p><a href="https://www.aichunjing.com/win11/">win系统软件下载</a></p>
	   	   
   <p><a href="https://hp30243681.jzfkw.net/">咨询</a></p>
	    <p>谢谢访问</p>
                                    <p class="text-gray-600">+86 19013885282</p>
                                </div>
                            </div>
                            
                            <!-- 联系项目4 -->
                            <div class="flex items-start">
                                <div class="bg-primary/10 p-3 rounded-full mr-4">
                                    <i class="fa fa-clock-o text-primary text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-medium mb-1">工作时间</h4>
                                    <p class="text-gray-600">周一至周五: 9:00 AM - 6:00 PM</p>
                                    <p class="text-gray-600">周六: 10:00 AM - 4:00 PM</p>
                                </div>
                            </div>
                        </div>
                        
                        <!-- 社交媒体链接 -->
                        <div class="mt-12">
                            <h4 class="font-medium mb-4">关注我</h4>
                            <div class="flex space-x-4">
                                <a href="#" class="w-10 h-10 rounded-full bg-gray-200 flex items-center justify-center text-gray-700 hover:bg-primary hover:text-white transition-custom">
                                    <i class="fa fa-github"></i>
                                </a>
                                <a href="#" class="w-10 h-10 rounded-full bg-gray-200 flex items-center justify-center text-gray-700 hover:bg-primary hover:text-white transition-custom">
                                    <i class="fa fa-linkedin"></i>
                                </a>
                                <a href="#" class="w-10 h-10 rounded-full bg-gray-200 flex items-center justify-center text-gray-700 hover:bg-primary hover:text-white transition-custom">
                                    <i class="fa fa-twitter"></i>
                                </a>
                                <a href="#" class="w-10 h-10 rounded-full bg-gray-200 flex items-center justify-center text-gray-700 hover:bg-primary hover:text-white transition-custom">
                                    <i class="fa fa-dribbble"></i>
                                </a>
                                <a href="#" class="w-10 h-10 rounded-full bg-gray-200 flex items-center justify-center text-gray-700 hover:bg-primary hover:text-white transition-custom">
                                    <i class="fa fa-instagram"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer class="bg-dark text-white py-12">
        <div class="container mx-auto px-4">
            <div class="max-w-6xl mx-auto">
                <div class="grid md:grid-cols-4 gap-8">
                    <!-- 关于小部件 -->
                    <div>
                        <h3 class="text-xl font-bold mb-4 flex items-center">
                            <span class="bg-primary p-1 rounded mr-2">
                                <i class="fa fa-code"></i>
                            </span>
                           陳小堃
                        </h3>
                        <p class="text-gray-400 mb-6">
                            一名充满激情的前端开发者，致力于创造美观且用户友好的数字体验。
                        </p>
                        <div class="flex space-x-4">
                            <a href="#" class="text-gray-400 hover:text-white transition-custom">
                                <i class="fa fa-github"></i>
                            </a>
                            <a href="#" class="text-gray-400 hover:text-white transition-custom">
                                <i class="fa fa-linkedin"></i>
                            </a>
                            <a href="#" class="text-gray-400 hover:text-white transition-custom">
                                <i class="fa fa-twitter"></i>
                            </a>
                            <a href="#" class="text-gray-400 hover:text-white transition-custom">
                                <i class="fa fa-dribbble"></i>
                            </a>
                        </div>
                    </div>
                    
                    <!-- 快速链接 -->
                    <div>
                        <h4 class="text-lg font-semibold mb-4">快速链接</h4>
                        <ul class="space-y-2">
                            <li><a href="#home" class="text-gray-400 hover:text-white transition-custom">首页</a></li>
                            <li><a href="#about" class="text-gray-400 hover:text-white transition-custom">关于我</a></li>
                            <li><a href="#skills" class="text-gray-400 hover:text-white transition-custom">技能</a></li>
                            <li><a href="#projects" class="text-gray-400 hover:text-white transition-custom">项目</a></li>
                            <li><a href="#contact" class="text-gray-400 hover:text-white transition-custom">联系我</a></li>
                        </ul>
                    </div>
                    
                    <!-- 服务 -->
                    <div>
                        <h4 class="text-lg font-semibold mb-4">服务</h4>
                        <ul class="space-y-2">
                            <li><a href="#" class="text-gray-400 hover:text-white transition-custom">Web开发</a></li>
                            <li><a href="#" class="text-gray-400 hover:text-white transition-custom">移动应用开发</a></li>
                            <li><a href="#" class="text-gray-400 hover:text-white transition-custom">UI/UX设计</a></li>
                            <li><a href="#" class="text-gray-400 hover:text-white transition-custom">电子商务解决方案</a></li>
                            <li><a href="#" class="text-gray-400 hover:text-white transition-custom">咨询服务</a></li>
                        </ul>
                    </div>
                    
                    <!-- 订阅 -->
                    <div>
                        <h4 class="text-lg font-semibold mb-4">订阅</h4>
                        <p class="text-gray-400 mb-4">
                            订阅我的通讯，获取最新更新和技巧。
                        </p>
                        <form class="flex">
                            <input type="email" placeholder="您的邮箱" class="px-4 py-2 rounded-l-lg w-full focus:outline-none text-dark">
                            <button type="submit" class="bg-primary px-4 py-2 rounded-r-lg hover:bg-primary/90 transition-custom">
                                <i class="fa fa-paper-plane"></i>
                            </button>
                        </form>
                    </div>
                </div>
                
                <div class="border-t border-gray-800 mt-12 pt-8 text-center">
                    <p class="text-gray-400">
                        &copy; 2023 陳小堃. 保留所有权利.
                    </p>
                </div>
            </div>
        </div>
    </footer>

    <!-- 返回顶部按钮 -->
    <button id="back-to-top" class="fixed bottom-8 right-8 bg-primary text-white w-12 h-12 rounded-full flex items-center justify-center shadow-lg opacity-0 invisible transition-all duration-300 hover:bg-primary/90">
        <i class="fa fa-chevron-up"></i>
    </button>

    <!-- JavaScript -->
    <script>
        // 导航栏滚动效果
        const navbar = document.getElementById('navbar');
        const backToTop = document.getElementById('back-to-top');
        
        window.addEventListener('scroll', function() {
            if (window.scrollY > 50) {
                navbar.classList.add('bg-dark/95', 'backdrop-blur-md', 'shadow-lg');
                navbar.classList.remove('bg-transparent');
                backToTop.classList.remove('opacity-0', 'invisible');
                backToTop.classList.add('opacity-100', 'visible');
            } else {
                navbar.classList.remove('bg-dark/95', 'backdrop-blur-md', 'shadow-lg');
                navbar.classList.add('bg-transparent');
                backToTop.classList.add('opacity-0', 'invisible');
                backToTop.classList.remove('opacity-100', 'visible');
            }
        });
        
        // 移动菜单切换
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');
        
        mobileMenuButton.addEventListener('click', function() {
            if (mobileMenu.classList.contains('opacity-0')) {
                mobileMenu.classList.remove('opacity-0', '-translate-y-full', 'invisible');
                mobileMenu.classList.add('opacity-100', 'translate-y-0', 'visible');
                mobileMenuButton.innerHTML = '<i class="fa fa-times"></i>';
            } else {
                mobileMenu.classList.add('opacity-0', '-translate-y-full', 'invisible');
                mobileMenu.classList.remove('opacity-100', 'translate-y-0', 'visible');
                mobileMenuButton.innerHTML = '<i class="fa fa-bars"></i>';
            }
        });
        
        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // 如果移动菜单是打开的，关闭它
                    if (!mobileMenu.classList.contains('opacity-0')) {
                        mobileMenu.classList.add('opacity-0', '-translate-y-full', 'invisible');
                        mobileMenu.classList.remove('opacity-100', 'translate-y-0', 'visible');
                        mobileMenuButton.innerHTML = '<i class="fa fa-bars"></i>';
                    }
                }
            });
        });
        
        // 返回顶部按钮
        backToTop.addEventListener('click', function() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
        
        // 项目筛选
        const filterButtons = document.querySelectorAll('.filter-btn');
        const projectItems = document.querySelectorAll('.project-item');
        
        filterButtons.forEach(button => {
            button.addEventListener('click', function() {
                // 从所有按钮中移除活动类
                filterButtons.forEach(btn => {
                    btn.classList.remove('bg-primary', 'text-white');
                    btn.classList.add('bg-gray-200', 'hover:bg-gray-300');
                });
                
                // 给点击的按钮添加活动类
                this.classList.remove('bg-gray-200', 'hover:bg-gray-300');
                this.classList.add('bg-primary', 'text-white');
                
                const filterValue = this.getAttribute('data-filter');
                
                // 筛选项目
                projectItems.forEach(item => {
                    if (filterValue === 'all' || item.getAttribute('data-category') === filterValue) {
                        item.style.display = 'block';
                    } else {
                        item.style.display = 'none';
                    }
                });
            });
        });
        
        // 初始化技能图表
        window.addEventListener('load', function() {
            const ctx = document.getElementById('skillChart').getContext('2d');
            const skillChart = new Chart(ctx, {
                type: 'radar',
                data: {
                    labels: ['沟通能力', '团队协作', '问题解决', '创造力', '时间管理', '领导力'],
                    datasets: [{
                        label: '专业技能',
                        data: [90, 85, 80, 75, 85, 70],
                        backgroundColor: 'rgba(22, 93, 255, 0.2)',
                        borderColor: 'rgba(22, 93, 255, 1)',
                        pointBackgroundColor: 'rgba(22, 93, 255, 1)',
                        pointBorderColor: '#fff',
                        pointHoverBackgroundColor: '#fff',
                        pointHoverBorderColor: 'rgba(22, 93, 255, 1)'
                    }]
                },
                options: {
                    scales: {
                        r: {
                            angleLines: {
                                display: true
                            },
                            suggestedMin: 0,
                            suggestedMax: 100
                        }
                    }
                }
            });
        });
        
        // 滚动动画
        const observerOptions = {
            root: null,
            rootMargin: '0px',
            threshold: 0.1
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate-fade-in');
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);
        
        // 为元素添加动画类
        document.querySelectorAll('.project-item, .skill-bar').forEach(item => {
            item.classList.add('opacity-0', 'translate-y-8', 'transition-all', 'duration-700');
            observer.observe(item);
        });
    </script>
</body>
</html>
