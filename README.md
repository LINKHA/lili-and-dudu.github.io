<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的个人网站</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#165DFF',
                        secondary: '#7B61FF',
                        accent: '#00B42A',
                        dark: '#1D2129',
                    },
                    fontFamily: {
                        inter: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
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
        }
    </style>
</head>
<body class="font-inter bg-gray-50 text-dark">
    <!-- 导航栏 -->
    <nav class="sticky top-0 z-50 bg-white/90 backdrop-blur-sm shadow-sm transition-custom">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-primary flex items-center">
                <i class="fa fa-code mr-2"></i>
                <span>我的网站</span>
            </a>
            <div class="hidden md:flex space-x-6">
                <a href="#home" class="font-medium hover:text-primary transition-custom">首页</a>
                <a href="#about" class="font-medium hover:text-primary transition-custom">关于我</a>
                <a href="#projects" class="font-medium hover:text-primary transition-custom">项目</a>
                <a href="#contact" class="font-medium hover:text-primary transition-custom">联系</a>
            </div>
            <button class="md:hidden text-dark focus:outline-none" id="menu-toggle">
                <i class="fa fa-bars text-xl"></i>
            </button>
        </div>
        <!-- 移动端菜单 -->
        <div class="md:hidden hidden bg-white shadow-lg absolute w-full" id="mobile-menu">
            <div class="container mx-auto px-4 py-2 flex flex-col space-y-3">
                <a href="#home" class="font-medium py-2 hover:text-primary transition-custom">首页</a>
                <a href="#about" class="font-medium py-2 hover:text-primary transition-custom">关于我</a>
                <a href="#projects" class="font-medium py-2 hover:text-primary transition-custom">项目</a>
                <a href="#contact" class="font-medium py-2 hover:text-primary transition-custom">联系</a>
            </div>
        </div>
    </nav>

    <!-- 首页 -->
    <section id="home" class="min-h-screen flex items-center justify-center bg-gradient-to-br from-primary/5 to-secondary/5">
        <div class="container mx-auto px-4 py-16 md:py-24">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-10 md:mb-0">
                    <h1 class="text-[clamp(2.5rem,5vw,4rem)] font-bold leading-tight text-dark">
                        你好，我是<span class="text-primary">开发者</span>
                    </h1>
                    <p class="text-lg md:text-xl text-gray-600 mt-4 mb-8 max-w-xl">
                        专注于前端开发，热衷于创建美观且功能强大的网站和应用程序。
                    </p>
                    <div class="flex space-x-4">
                        <a href="#projects" class="px-6 py-3 bg-primary text-white rounded-lg shadow-lg hover:bg-primary/90 transition-custom transform hover:-translate-y-1">
                            查看我的项目
                        </a>
                        <a href="#contact" class="px-6 py-3 bg-white text-primary border border-primary rounded-lg hover:bg-gray-50 transition-custom transform hover:-translate-y-1">
                            联系我
                        </a>
                    </div>
                </div>
                <div class="md:w-1/2 flex justify-center">
                    <div class="w-64 h-64 md:w-80 md:h-80 rounded-full bg-gradient-to-br from-primary to-secondary shadow-xl flex items-center justify-center">
                        <div class="w-60 h-60 md:w-76 md:h-76 rounded-full bg-white overflow-hidden shadow-inner">
                            <img src="https://picsum.photos/seed/developer/300/300" alt="开发者照片" class="w-full h-full object-cover">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 关于我 -->
    <section id="about" class="py-16 md:py-24 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl md:text-4xl font-bold text-center mb-16">关于我</h2>
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-2/5 mb-10 md:mb-0">
                    <div class="relative">
                        <div class="w-64 h-64 md:w-80 md:h-80 mx-auto rounded-xl overflow-hidden shadow-xl">
                            <img src="https://picsum.photos/seed/profile/400/400" alt="个人照片" class="w-full h-full object-cover">
                        </div>
                        <div class="absolute -bottom-4 -right-4 w-20 h-20 bg-primary rounded-lg shadow-lg flex items-center justify-center">
                            <span class="text-white font-bold text-2xl">3+</span>
                        </div>
                    </div>
                </div>
                <div class="md:w-3/5 md:pl-16">
                    <h3 class="text-2xl font-bold mb-4">前端开发工程师</h3>
                    <p class="text-gray-600 mb-6">
                        我是一名热爱技术的前端开发工程师，拥有3年多的开发经验。我擅长使用HTML、CSS和JavaScript构建响应式、高性能的网站和Web应用程序。
                    </p>
                    <p class="text-gray-600 mb-6">
                        我热衷于学习新技术，并将其应用到实际项目中。我相信优秀的前端设计不仅要美观，还要具有良好的用户体验和性能。
                    </p>
                    <div class="grid grid-cols-2 gap-4 mb-8">
                        <div class="flex items-center">
                            <i class="fa fa-check-circle text-primary mr-2"></i>
                            <span>HTML5 & CSS3</span>
                        </div>
                        <div class="flex items-center">
                            <i class="fa fa-check-circle text-primary mr-2"></i>
                            <span>JavaScript ES6+</span>
                        </div>
                        <div class="flex items-center">
                            <i class="fa fa-check-circle text-primary mr-2"></i>
                            <span>React.js</span>
                        </div>
                        <div class="flex items-center">
                            <i class="fa fa-check-circle text-primary mr-2"></i>
                            <span>Vue.js</span>
                        </div>
                        <div class="flex items-center">
                            <i class="fa fa-check-circle text-primary mr-2"></i>
                            <span>Tailwind CSS</span>
                        </div>
                        <div class="flex items-center">
                            <i class="fa fa-check-circle text-primary mr-2"></i>
                            <span>响应式设计</span>
                        </div>
                    </div>
                    <div class="flex space-x-4">
                        <a href="#" class="px-4 py-2 bg-gray-100 hover:bg-gray-200 rounded-lg transition-custom">
                            <i class="fa fa-github mr-2"></i> GitHub
                        </a>
                        <a href="#" class="px-4 py-2 bg-gray-100 hover:bg-gray-200 rounded-lg transition-custom">
                            <i class="fa fa-linkedin mr-2"></i> LinkedIn
                        </a>
                        <a href="#" class="px-4 py-2 bg-gray-100 hover:bg-gray-200 rounded-lg transition-custom">
                            <i class="fa fa-twitter mr-2"></i> Twitter
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 项目 -->
    <section id="projects" class="py-16 md:py-24 bg-gray-50">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl md:text-4xl font-bold text-center mb-16">我的项目</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- 项目卡片 1 -->
                <div class="bg-white rounded-xl overflow-hidden shadow-lg hover:shadow-xl transition-custom transform hover:-translate-y-1">
                    <div class="h-48 overflow-hidden">
                        <img src="https://picsum.photos/seed/project1/600/400" alt="项目截图" class="w-full h-full object-cover">
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-center mb-3">
                            <h3 class="text-xl font-bold">响应式网站设计</h3>
                            <span class="px-3 py-1 bg-primary/10 text-primary text-sm rounded-full">HTML/CSS</span>
                        </div>
                        <p class="text-gray-600 mb-4">
                            一个现代化的响应式企业网站，适配各种设备屏幕尺寸，具有流畅的动画效果和交互体验。
                        </p>
                        <div class="flex justify-between items-center">
                            <a href="#" class="text-primary hover:text-primary/80 font-medium">查看详情</a>
                            <div class="flex space-x-2">
                                <a href="#" class="text-gray-400 hover:text-gray-600">
                                    <i class="fa fa-github"></i>
                                </a>
                                <a href="#" class="text-gray-400 hover:text-gray-600">
                                    <i class="fa fa-link"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 项目卡片 2 -->
                <div class="bg-white rounded-xl overflow-hidden shadow-lg hover:shadow-xl transition-custom transform hover:-translate-y-1">
                    <div class="h-48 overflow-hidden">
                        <img src="https://picsum.photos/seed/project2/600/400" alt="项目截图" class="w-full h-full object-cover">
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-center mb-3">
                            <h3 class="text-xl font-bold">React应用开发</h3>
                            <span class="px-3 py-1 bg-primary/10 text-primary text-sm rounded-full">React.js</span>
                        </div>
                        <p class="text-gray-600 mb-4">
                            使用React.js开发的单页应用，集成了状态管理和API调用，提供了流畅的用户体验。
                        </p>
                        <div class="flex justify-between items-center">
                            <a href="#" class="text-primary hover:text-primary/80 font-medium">查看详情</a>
                            <div class="flex space-x-2">
                                <a href="#" class="text-gray-400 hover:text-gray-600">
                                    <i class="fa fa-github"></i>
                                </a>
                                <a href="#" class="text-gray-400 hover:text-gray-600">
                                    <i class="fa fa-link"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 项目卡片 3 -->
                <div class="bg-white rounded-xl overflow-hidden shadow-lg hover:shadow-xl transition-custom transform hover:-translate-y-1">
                    <div class="h-48 overflow-hidden">
                        <img src="https://picsum.photos/seed/project3/600/400" alt="项目截图" class="w-full h-full object-cover">
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-center mb-3">
                            <h3 class="text-xl font-bold">电商网站</h3>
                            <span class="px-3 py-1 bg-primary/10 text-primary text-sm rounded-full">Vue.js</span>
                        </div>
                        <p class="text-gray-600 mb-4">
                            一个完整的电商网站，包含商品展示、购物车、支付流程等功能，采用Vue.js框架开发。
                        </p>
                        <div class="flex justify-between items-center">
                            <a href="#" class="text-primary hover:text-primary/80 font-medium">查看详情</a>
                            <div class="flex space-x-2">
                                <a href="#" class="text-gray-400 hover:text-gray-600">
                                    <i class="fa fa-github"></i>
                                </a>
                                <a href="#" class="text-gray-400 hover:text-gray-600">
                                    <i class="fa fa-link"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 联系 -->
    <section id="contact" class="py-16 md:py-24 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl md:text-4xl font-bold text-center mb-16">联系我</h2>
            <div class="max-w-3xl mx-auto">
                <div class="bg-gray-50 rounded-xl p-8 shadow-lg">
                    <form>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                            <div>
                                <label for="name" class="block text-sm font-medium text-gray-700 mb-1">姓名</label>
                                <input type="text" id="name" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请输入您的姓名">
                            </div>
                            <div>
                                <label for="email" class="block text-sm font-medium text-gray-700 mb-1">邮箱</label>
                                <input type="email" id="email" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请输入您的邮箱">
                            </div>
                        </div>
                        <div class="mb-6">
                            <label for="subject" class="block text-sm font-medium text-gray-700 mb-1">主题</label>
                            <input type="text" id="subject" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请输入主题">
                        </div>
                        <div class="mb-6">
                            <label for="message" class="block text-sm font-medium text-gray-700 mb-1">留言</label>
                            <textarea id="message" rows="5" class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-primary focus:border-primary transition-custom" placeholder="请输入您的留言"></textarea>
                        </div>
                        <button type="submit" class="w-full px-6 py-3 bg-primary text-white rounded-lg shadow-lg hover:bg-primary/90 transition-custom transform hover:-translate-y-1">
                            发送留言
                        </button>
                    </form>
                </div>
                <div class="flex flex-col md:flex-row justify-between mt-12">
                    <div class="flex items-center mb-6 md:mb-0">
                        <div class="w-12 h-12 rounded-full bg-primary/10 flex items-center justify-center mr-4">
                            <i class="fa fa-envelope text-primary"></i>
                        </div>
                        <div>
                            <h4 class="font-medium">邮箱</h4>
                            <p class="text-gray-600">contact@example.com</p>
                        </div>
                    </div>
                    <div class="flex items-center mb-6 md:mb-0">
                        <div class="w-12 h-12 rounded-full bg-primary/10 flex items-center justify-center mr-4">
                            <i class="fa fa-phone text-primary"></i>
                        </div>
                        <div>
                            <h4 class="font-medium">电话</h4>
                            <p class="text-gray-600">+86 123 4567 8910</p>
                        </div>
                    </div>
                    <div class="flex items-center">
                        <div class="w-12 h-12 rounded-full bg-primary/10 flex items-center justify-center mr-4">
                            <i class="fa fa-map-marker text-primary"></i>
                        </div>
                        <div>
                            <h4 class="font-medium">地址</h4>
                            <p class="text-gray-600">北京市海淀区科技园</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer class="bg-dark text-white py-12">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-6 md:mb-0">
                    <a href="#" class="text-2xl font-bold flex items-center">
                        <i class="fa fa-code mr-2"></i>
                        <span>我的网站</span>
                    </a>
                    <p class="text-gray-400 mt-2">
                        专注于前端开发，创建美观且功能强大的网站和应用程序。
                    </p>
                </div>
                <div class="flex space-x-6 mb-6 md:mb-0">
                    <a href="#" class="text-gray-400 hover:text-white transition-custom">
                        <i class="fa fa-github text-xl"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white transition-custom">
                        <i class="fa fa-linkedin text-xl"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white transition-custom">
                        <i class="fa fa-twitter text-xl"></i>
                    </a>
                    <a href="#" class="text-gray-400 hover:text-white transition-custom">
                        <i class="fa fa-instagram text-xl"></i>
                    </a>
                </div>
            </div>
            <div class="border-t border-gray-800 mt-8 pt-8 text-center text-gray-400">
                <p>&copy; 2025 我的个人网站. 保留所有权利.</p>
            </div>
        </div>
    </footer>

    <script>
        // 移动端菜单切换
        const menuToggle = document.getElementById('menu-toggle');
        const mobileMenu = document.getElementById('mobile-menu');

        menuToggle.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // 导航栏滚动效果
        const nav = document.querySelector('nav');
        let lastScrollTop = 0;

        window.addEventListener('scroll', () => {
            const scrollTop = window.pageYOffset || document.documentElement.scrollTop;

            if (scrollTop > 50) {
                nav.classList.add('shadow-md');
                nav.classList.add('py-2');
                nav.classList.remove('py-3');
            } else {
                nav.classList.remove('shadow-md');
                nav.classList.add('py-3');
                nav.classList.remove('py-2');
            }

            lastScrollTop = scrollTop;
        });

        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();

                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);

                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });

                    // 关闭移动端菜单
                    if (!mobileMenu.classList.contains('hidden')) {
                        mobileMenu.classList.add('hidden');
                    }
                }
            });
        });
    </script>
</body>
</html>
