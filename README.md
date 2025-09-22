<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>سيرة ذاتية </title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@9/swiper-bundle.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700&display=swap');
        
        body {
            font-family: 'Tajawal', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #e9ecef 100%);
        }
        
        .card-hover {
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        
        .card-hover:hover {
            transform: translateY(-10px) scale(1.03);
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
        }
        
        .icon-container {
            position: relative;
            overflow: hidden;
        }
        
        .icon-container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent 30%, rgba(255,255,255,0.3) 50%, transparent 70%);
            transform: translateX(-100%);
            transition: transform 0.6s;
        }
        
        .card-hover:hover .icon-container::before {
            transform: translateX(100%);
        }
        
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.8);
            backdrop-filter: blur(5px);
            animation: fadeIn 0.3s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .modal-content {
            animation: slideIn 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            background: white;
            border-radius: 20px;
            overflow: hidden;
            max-width: 90%;
            max-height: 90vh;
            margin: 2% auto;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
        }
        
        @keyframes slideIn {
            from { transform: translateY(-50px) scale(0.9); opacity: 0; }
            to { transform: translateY(0) scale(1); opacity: 1; }
        }
        
        .skill-bar {
            transition: width 2s ease-in-out;
        }
        
        .timeline-item {
            position: relative;
            padding-right: 40px;
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            right: 15px;
            top: 0;
            bottom: 0;
            width: 2px;
            background: linear-gradient(to bottom, #667eea, #764ba2);
        }
        
        .timeline-dot {
            position: absolute;
            right: 11px;
            top: 5px;
            width: 12px;
            height: 12px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 50%;
            box-shadow: 0 0 0 4px white, 0 0 0 6px #667eea;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .project-card {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            transition: all 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }
        
        .certificate-card {
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);
            transition: all 0.3s ease;
        }
        
        .certificate-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }
        
        .swiper {
            width: 100%;
            height: 300px;
        }
        
        .swiper-slide {
            text-align: center;
            font-size: 18px;
            background: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 15px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .profile-image {
            border: 4px solid white;
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        .icon-glow {
            transition: all 0.3s ease;
        }
        
        .card-hover:hover .icon-glow {
            filter: drop-shadow(0 0 15px rgba(102, 126, 234, 0.8));
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="bg-gradient-to-r from-purple-600 to-indigo-700 text-white py-12 px-4 shadow-xl">
        <div class="container mx-auto flex flex-col md:flex-row items-center justify-between">
            <div class="text-center md:text-right mb-8 md:mb-0">
                <h1 class="text-4xl md:text-5xl font-bold mb-2">امام السيد علي حفني </h1>
                <p class="text-xl md:text-2xl opacity-90">مطور برمجيات </p>
                <div class="mt-6 flex justify-center md:justify-end space-x-4">
                    <a href="#" class="text-white hover:text-purple-200 transition transform hover:scale-110">
                        <i class="fab fa-linkedin text-2xl"></i>
                    </a>
                    <a href="#" class="text-white hover:text-purple-200 transition transform hover:scale-110">
                        <i class="fab fa-github text-2xl"></i>
                    </a>
                    <a href="#" class="text-white hover:text-purple-200 transition transform hover:scale-110">
                        <i class="fab fa-twitter text-2xl"></i>
                    </a>
                </div>
            </div>
            <div class="relative">
                <img src="https://z-cdn-media.chatglm.cn/files/caebf657-aa76-42bf-a0c2-ade441092e51_b40697d7-9be5-4497-8bb4-6dc0a2e98e74.jpg?auth_key=1790067210-50931f4fe124463ca1d5cc2a086526de-0-471e542621864d680ad0c7c836e34f4c" 
                     alt="صورة شخصية" 
                     class="w-48 h-48 rounded-full profile-image">
                <div class="absolute -bottom-2 -left-2 bg-yellow-400 text-gray-800 px-3 py-1 rounded-full text-sm font-semibold animate-pulse">
                    متاح للعمل بدوام كامل / عن بعد
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content - Icon Cards Grid -->
    <main class="container mx-auto px-4 py-16">
        <h2 class="text-4xl font-bold text-center mb-16 gradient-text">أقسام السيرة الذاتية</h2>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- About Card -->
            <div class="card-hover bg-white rounded-2xl shadow-lg overflow-hidden cursor-pointer" onclick="openModal('aboutModal')">
                <div class="icon-container bg-gradient-to-br from-purple-500 to-indigo-600 h-32 flex items-center justify-center">
                    <i class="fas fa-user-circle text-white text-5xl icon-glow"></i>
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold text-gray-800 mb-2">نبذة عني</h3>
                    <p class="text-gray-600">تعرف على خبرتي وإنجازاتي</p>
                </div>
            </div>

            <!-- Skills Card -->
            <div class="card-hover bg-white rounded-2xl shadow-lg overflow-hidden cursor-pointer" onclick="openModal('skillsModal')">
                <div class="icon-container bg-gradient-to-br from-blue-500 to-cyan-600 h-32 flex items-center justify-center">
                    <i class="fas fa-tools text-white text-5xl icon-glow"></i>
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold text-gray-800 mb-2">المهارات</h3>
                    <p class="text-gray-600">المهارات التقنية والبرمجية</p>
                </div>
            </div>

            <!-- Experience Card -->
            <div class="card-hover bg-white rounded-2xl shadow-lg overflow-hidden cursor-pointer" onclick="openModal('experienceModal')">
                <div class="icon-container bg-gradient-to-br from-green-500 to-teal-600 h-32 flex items-center justify-center">
                    <i class="fas fa-briefcase text-white text-5xl icon-glow"></i>
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold text-gray-800 mb-2">الخبرات</h3>
                    <p class="text-gray-600">خبرات العمل والمشاريع</p>
                </div>
            </div>

            <!-- Projects Card -->
            <div class="card-hover bg-white rounded-2xl shadow-lg overflow-hidden cursor-pointer" onclick="openModal('projectsModal')">
                <div class="icon-container bg-gradient-to-br from-orange-500 to-red-600 h-32 flex items-center justify-center">
                    <i class="fas fa-flask text-white text-5xl icon-glow"></i>
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold text-gray-800 mb-2">المشاريع</h3>
                    <p class="text-gray-600">المشاريع العلمية والتطبيقية</p>
                </div>
            </div>

            <!-- Certificates Card -->
            <div class="card-hover bg-white rounded-2xl shadow-lg overflow-hidden cursor-pointer" onclick="openModal('certificatesModal')">
                <div class="icon-container bg-gradient-to-br from-yellow-500 to-amber-600 h-32 flex items-center justify-center">
                    <i class="fas fa-certificate text-white text-5xl icon-glow"></i>
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold text-gray-800 mb-2">الشهادات</h3>
                    <p class="text-gray-600">الشهادات الاحترافية</p>
                </div>
            </div>

            <!-- Contact Card -->
            <div class="card-hover bg-white rounded-2xl shadow-lg overflow-hidden cursor-pointer" onclick="openModal('contactModal')">
                <div class="icon-container bg-gradient-to-br from-pink-500 to-rose-600 h-32 flex items-center justify-center">
                    <i class="fas fa-envelope text-white text-5xl icon-glow"></i>
                </div>
                <div class="p-6">
                    <h3 class="text-2xl font-bold text-gray-800 mb-2">تواصل معي</h3>
                    <p class="text-gray-600">اتصل بي مباشرة</p>
                </div>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-8 mt-16">
        <div class="container mx-auto px-4 text-center">
            <p>&copy; 2023 جميع الحقوق محفوظة</p>
        </div>
    </footer>
    <!-- Modals -->
    <!-- About Modal -->
    <div id="aboutModal" class="modal">
        <div class="modal-content">
            <div class="bg-gradient-to-r from-purple-600 to-indigo-700 text-white p-6 flex justify-between items-center">
                <h2 class="text-3xl font-bold">نبذة عني</h2>
                <span class="text-4xl cursor-pointer hover:text-gray-300" onclick="closeModal('aboutModal')">&times;</span>
            </div>
            <div class="p-8 overflow-y-auto" style="max-height: 70vh;">
                <div class="flex flex-col md:flex-row gap-8">
                    <img src="https://z-cdn-media.chatglm.cn/files/caebf657-aa76-42bf-a0c2-ade441092e51_b40697d7-9be5-4497-8bb4-6dc0a2e98e74.jpg?auth_key=1790067210-50931f4fe124463ca1d5cc2a086526de-0-471e542621864d680ad0c7c836e34f4c" 
                         alt="صورة شخصية" 
                         class="w-48 h-48 rounded-full mx-auto md:mx-0 shadow-lg">
                    <div>
                        <p class="text-gray-700 text-lg leading-relaxed mb-4">
                            
                           أنا مطور برمجيات شغوف بالتقنيات الحديثة وأملك خبرة في التعلم الالي والتعلم العميق  ومطور مواقع ويب .
                           أركز على تقديم حلول مبتكرة وسهلة الاستخدام تلبي احتياجات العملاء وتحسن تجربة المستخدم
                        </p>
                        <p class="text-gray-700 text-lg leading-relaxed">
                            أؤمن بأن الجودة والتطوير المستمر هو مفتاح النجاح في عالم التكنولوجيا، ولذلك أحرص على متابعة أحدث التقنيات
                            والمعايير العالمية في تطوير البرمجيات.
                        </p>
                        <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mt-8">
                            <div class="text-center bg-purple-50 p-4 rounded-lg">
                                <i class="fas fa-code text-3xl text-purple-600 mb-2"></i>
                                <p class="text-gray-700 font-semibold"></p>
                                <p class="text-gray-600">خبرة</p>
                            </div>
                            <div class="text-center bg-blue-50 p-4 rounded-lg">
                                <i class="fas fa-project-diagram text-3xl text-blue-600 mb-2"></i>
                                <p class="text-gray-700 font-semibold">4+</p>
                                <p class="text-gray-600">مشروع مكتمل</p>
                            </div>
                            <div class="text-center bg-green-50 p-4 rounded-lg">
                                <i class="fas fa-users text-3xl text-green-600 mb-2"></i>
                                <p class="text-gray-700 font-semibold">5+</p>
                                <p class="text-gray-600">عميل راضٍ</p>
                            </div>
                            <div class="text-center bg-yellow-50 p-4 rounded-lg">
                                <i class="fas fa-award text-3xl text-yellow-600 mb-2"></i>
                                <p class="text-gray-700 font-semibold">4+</p>
                                <p class="text-gray-600">شهادة احترافية</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Skills Modal -->
    <div id="skillsModal" class="modal">
        <div class="modal-content">
            <div class="bg-gradient-to-r from-blue-500 to-cyan-600 text-white p-6 flex justify-between items-center">
                <h2 class="text-3xl font-bold">المهارات</h2>
                <span class="text-4xl cursor-pointer hover:text-gray-300" onclick="closeModal('skillsModal')">&times;</span>
            </div>
            <div class="p-8 overflow-y-auto" style="max-height: 70vh;">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div class="bg-gray-50 p-6 rounded-xl shadow-md">
                        <h3 class="text-xl font-bold mb-4 text-blue-600">
                            <i class="fas fa-laptop-code mr-2"></i>البرمجة
                        </h3>
                        <div class="space-y-4">
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="text-gray-700">JavaScript</span>
                                    <span class="text-blue-600 font-semibold">80%</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-3">
                                    <div class="skill-bar bg-blue-600 h-3 rounded-full" style="width: 0%" data-width="95%"></div>
                                </div>
                            </div>
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="text-gray-700">Python</span>
                                    <span class="text-blue-600 font-semibold">97%</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-3">
                                    <div class="skill-bar bg-blue-600 h-3 rounded-full" style="width: 0%" data-width="85%"></div>
                                </div>
                            </div>
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="text-gray-700">Java</span>
                                    <span class="text-blue-600 font-semibold">80%</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-3">
                                    <div class="skill-bar bg-blue-600 h-3 rounded-full" style="width: 0%" data-width="80%"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="bg-gray-50 p-6 rounded-xl shadow-md">
                        <h3 class="text-xl font-bold mb-4 text-blue-600">
                            <i class="fas fa-palette mr-2"></i>تصميم الويب
                        </h3>
                        <div class="space-y-4">
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="text-gray-700">React/Vue.js</span>
                                    <span class="text-blue-600 font-semibold">90%</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-3">
                                    <div class="skill-bar bg-blue-600 h-3 rounded-full" style="width: 0%" data-width="90%"></div>
                                </div>
                            </div>
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="text-gray-700">HTML/CSS</span>
                                    <span class="text-blue-600 font-semibold">95%</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-3">
                                    <div class="skill-bar bg-blue-600 h-3 rounded-full" style="width: 0%" data-width="95%"></div>
                                </div>
                            </div>
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="text-gray-700">Tailwind CSS</span>
                                    <span class="text-blue-600 font-semibold">85%</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-3">
                                    <div class="skill-bar bg-blue-600 h-3 rounded-full" style="width: 0%" data-width="85%"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="bg-gray-50 p-6 rounded-xl shadow-md">
                        <h3 class="text-xl font-bold mb-4 text-blue-600">
                            <i class="fas fa-database mr-2"></i>قواعد البيانات
                        </h3>
                        <div class="space-y-4">
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="text-gray-700">MySQL</span>
                                    <span class="text-blue-600 font-semibold">85%</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-3">
                                    <div class="skill-bar bg-blue-600 h-3 rounded-full" style="width: 0%" data-width="85%"></div>
                                </div>
                            </div>
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="text-gray-700">MongoDB</span>
                                    <span class="text-blue-600 font-semibold">80%</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-3">
                                    <div class="skill-bar bg-blue-600 h-3 rounded-full" style="width: 0%" data-width="80%"></div>
                                </div>
                            </div>
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="text-gray-700">Redis</span>
                                    <span class="text-blue-600 font-semibold">75%</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-3">
                                    <div class="skill-bar bg-blue-600 h-3 rounded-full" style="width: 0%" data-width="75%"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="bg-gray-50 p-6 rounded-xl shadow-md">
                        <h3 class="text-xl font-bold mb-4 text-blue-600">
                            <i class="fas fa-cogs mr-2"></i>الأدوات والمنصات
                        </h3>
                        <div class="space-y-4">
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="text-gray-700">GitHub</span>
                                    <span class="text-blue-600 font-semibold">90%</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-3">
                                    <div class="skill-bar bg-blue-600 h-3 rounded-full" style="width: 0%" data-width="90%"></div>
                                </div>
                            </div>
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="text-gray-700">Docker</span>
                                    <span class="text-blue-600 font-semibold">80%</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-3">
                                    <div class="skill-bar bg-blue-600 h-3 rounded-full" style="width: 0%" data-width="80%"></div>
                                </div>
                            </div>
                            <div>
                                <div class="flex justify-between mb-1">
                                    <span class="text-gray-700">AWS</span>
                                    <span class="text-blue-600 font-semibold">75%</span>
                                </div>
                                <div class="w-full bg-gray-200 rounded-full h-3">
                                    <div class="skill-bar bg-blue-600 h-3 rounded-full" style="width: 0%" data-width="75%"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Experience Modal -->
    <div id="experienceModal" class="modal">
        <div class="modal-content">
            <div class="bg-gradient-to-r from-green-500 to-teal-600 text-white p-6 flex justify-between items-center">
                <h2 class="text-3xl font-bold">الخبرات العملية</h2>
                <span class="text-4xl cursor-pointer hover:text-gray-300" onclick="closeModal('experienceModal')">&times;</span>
            </div>
            <div class="p-8 overflow-y-auto" style="max-height: 70vh;">
                <div class="space-y-6">
                    <div class="bg-white rounded-xl shadow-md p-6 relative border-l-4 border-green-500">
                        <div class="timeline-dot"></div>
                        <div class="timeline-item">
                            <h3 class="text-xl font-bold text-gray-800">مطور رئيسي</h3>
                            <p class="text-green-600 font-semibold">شركة التقنية المتقدمة</p>
                            <p class="text-gray-600 mb-2">2021 - حتى الآن</p>
                            <ul class="text-gray-700 space-y-2">
                                <li><i class="fas fa-check-circle text-green-600 mr-2"></i>قيادة فريق من 5 مطورين في تطوير تطبيقات الويب</li>
                                <li><i class="fas fa-check-circle text-green-600 mr-2"></i>تطوير وتصميم واجهات مستخدم تفاعلية</li>
                                <li><i class="fas fa-check-circle text-green-600 mr-2"></i>تحسين أداء التطبيقات بنسبة 40%</li>
                            </ul>
                        </div>
                    </div>
                    <div class="bg-white rounded-xl shadow-md p-6 relative border-l-4 border-blue-500">
                        <div class="timeline-dot"></div>
                        <div class="timeline-item">
                            <h3 class="text-xl font-bold text-gray-800">مطور واجهات مستخدم</h3>
                            <p class="text-blue-600 font-semibold">وكالة الإبداع الرقمي</p>
                            <p class="text-gray-600 mb-2">2019 - 2021</p>
                            <ul class="text-gray-700 space-y-2">
                                <li><i class="fas fa-check-circle text-blue-600 mr-2"></i>تصميم وتطوير أكثر من 20 موقعًا تجاريًا</li>
                                <li><i class="fas fa-check-circle text-blue-600 mr-2"></i>تعاون مع فرق التصميم لتحويل التصاميم إلى كود</li>
                                <li><i class="fas fa-check-circle text-blue-600 mr-2"></i>ضمان التوافق عبر جميع المتصفحات والأجهزة</li>
                            </ul>
                        </div>
                    </div>
                    <div class="bg-white rounded-xl shadow-md p-6 relative border-l-4 border-purple-500">
                        <div class="timeline-dot"></div>
                        <div class="timeline-item">
                            <h3 class="text-xl font-bold text-gray-800">مطور مبتدئ</h3>
                            <p class="text-purple-600 font-semibold">شركة البرمجيات العربية</p>
                            <p class="text-gray-600 mb-2">2017 - 2019</p>
                            <ul class="text-gray-700 space-y-2">
                                <li><i class="fas fa-check-circle text-purple-600 mr-2"></i>المشاركة في تطوير تطبيقات الويب</li>
                                <li><i class="fas fa-check-circle text-purple-600 mr-2"></i>صيانة وتحديث المواقع الحالية</li>
                                <li><i class="fas fa-check-circle text-purple-600 mr-2"></i>تعلم أفضل الممارسات في تطوير البرمجيات</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Projects Modal -->
    <div id="projectsModal" class="modal">
        <div class="modal-content">
            <div class="bg-gradient-to-r from-orange-500 to-red-600 text-white p-6 flex justify-between items-center">
                <h2 class="text-3xl font-bold">المشاريع العلمية</h2>
                <span class="text-4xl cursor-pointer hover:text-gray-300" onclick="closeModal('projectsModal')">&times;</span>
            </div>
            <div class="p-8 overflow-y-auto" style="max-height: 70vh;">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div class="project-card rounded-xl p-6 cursor-pointer" onclick="showProjectDetail('project1')">
                        <div class="mb-4">
                            <img src="https://picsum.photos/seed/project1/400/200" alt="مشروع 1" class="w-full h-48 object-cover rounded-lg">
                        </div>
                        <h3 class="text-xl font-bold text-gray-800 mb-2">منصة التعلم الإلكتروني</h3>
                        <p class="text-gray-700 mb-4">منصة متكاملة للتعلم الإلكتروني</p>
                        <div class="flex flex-wrap gap-2">
                            <span class="bg-orange-600 text-white px-3 py-1 rounded-full text-sm">React</span>
                            <span class="bg-orange-600 text-white px-3 py-1 rounded-full text-sm">Node.js</span>
                            <span class="bg-orange-600 text-white px-3 py-1 rounded-full text-sm">MongoDB</span>
                        </div>
                    </div>
                    <div class="project-card rounded-xl p-6 cursor-pointer" onclick="showProjectDetail('project2')">
                        <div class="mb-4">
                            <img src="https://picsum.photos/seed/project2/400/200" alt="مشروع 2" class="w-full h-48 object-cover rounded-lg">
                        </div>
                        <h3 class="text-xl font-bold text-gray-800 mb-2">تطبيق إدارة المشاريع</h3>
                        <p class="text-gray-700 mb-4">تطبيق ويب لإدارة المشاريع</p>
                        <div class="flex flex-wrap gap-2">
                            <span class="bg-orange-600 text-white px-3 py-1 rounded-full text-sm">Vue.js</span>
                            <span class="bg-orange-600 text-white px-3 py-1 rounded-full text-sm">Firebase</span>
                            <span class="bg-orange-600 text-white px-3 py-1 rounded-full text-sm">Tailwind</span>
                        </div>
                    </div>
                    <div class="project-card rounded-xl p-6 cursor-pointer" onclick="showProjectDetail('project3')">
                        <div class="mb-4">
                            <img src="https://picsum.photos/seed/project3/400/200" alt="مشروع 3" class="w-full h-48 object-cover rounded-lg">
                        </div>
                        <h3 class="text-xl font-bold text-gray-800 mb-2">نظام التجارة الإلكترونية</h3>
                        <p class="text-gray-700 mb-4">منصة متكاملة للتجارة الإلكترونية</p>
                        <div class="flex flex-wrap gap-2">
                            <span class="bg-orange-600 text-white px-3 py-1 rounded-full text-sm">Next.js</span>
                            <span class="bg-orange-600 text-white px-3 py-1 rounded-full text-sm">Django</span>
                            <span class="bg-orange-600 text-white px-3 py-1 rounded-full text-sm">PostgreSQL</span>
                        </div>
                    </div>
                    <div class="project-card rounded-xl p-6 cursor-pointer" onclick="showProjectDetail('project4')">
                        <div class="mb-4">
                            <img src="https://picsum.photos/seed/project4/400/200" alt="مشروع 4" class="w-full h-48 object-cover rounded-lg">
                        </div>
                        <h3 class="text-xl font-bold text-gray-800 mb-2">تطبيق المواعيد الطبية</h3>
                        <p class="text-gray-700 mb-4">تطبيق لتسهيل预约 المواعيد الطبية</p>
                        <div class="flex flex-wrap gap-2">
                            <span class="bg-orange-600 text-white px-3 py-1 rounded-full text-sm">React Native</span>
                            <span class="bg-orange-600 text-white px-3 py-1 rounded-full text-sm">Express</span>
                            <span class="bg-orange-600 text-white px-3 py-1 rounded-full text-sm">MySQL</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Certificates Modal -->
    <div id="certificatesModal" class="modal">
        <div class="modal-content">
            <div class="bg-gradient-to-r from-yellow-500 to-amber-600 text-white p-6 flex justify-between items-center">
                <h2 class="text-3xl font-bold">الشهادات الاحترافية</h2>
                <span class="text-4xl cursor-pointer hover:text-gray-300" onclick="closeModal('certificatesModal')">&times;</span>
            </div>
            <div class="p-8 overflow-y-auto" style="max-height: 70vh;">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div class="certificate-card rounded-xl p-6 cursor-pointer" onclick="showCertificateDetail('cert1')">
                        <div class="text-center mb-4">
                            <i class="fas fa-award text-5xl text-yellow-600"></i>
                        </div>
                        <h3 class="text-xl font-bold text-gray-800 mb-2">Google Cloud Architect</h3>
                        <p class="text-gray-700 mb-4">شهادة احترافية في تصميم البنية التحتية السحابية</p>
                        <p class="text-gray-600 text-sm">تاريخ الحصول: 2023</p>
                    </div>
                    <div class="certificate-card rounded-xl p-6 cursor-pointer" onclick="showCertificateDetail('cert2')">
                        <div class="text-center mb-4">
                            <i class="fas fa-award text-5xl text-yellow-600"></i>
                        </div>
                        <h3 class="text-xl font-bold text-gray-800 mb-2">AWS Certified Developer</h3>
                        <p class="text-gray-700 mb-4">شهادة مطور AWS المتقدم</p>
                        <p class="text-gray-600 text-sm">تاريخ الحصول: 2022</p>
                    </div>
                    <div class="certificate-card rounded-xl p-6 cursor-pointer" onclick="showCertificateDetail('cert3')">
                        <div class="text-center mb-4">
                            <i class="fas fa-award text-5xl text-yellow-600"></i>
                        </div>
                        <h3 class="text-xl font-bold text-gray-800 mb-2">React Professional</h3>
                        <p class="text-gray-700 mb-4">شهادة احترافية في React.js</p>
                        <p class="text-gray-600 text-sm">تاريخ الحصول: 2022</p>
                    </div>
                    <div class="certificate-card rounded-xl p-6 cursor-pointer" onclick="showCertificateDetail('cert4')">
                        <div class="text-center mb-4">
                            <i class="fas fa-award text-5xl text-yellow-600"></i>
                        </div>
                        <h3 class="text-xl font-bold text-gray-800 mb-2">MongoDB Certified Developer</h3>
                        <p class="text-gray-700 mb-4">شهادة مطور MongoDB</p>
                        <p class="text-gray-600 text-sm">تاريخ الحصول: 2021</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Contact Modal -->
    <div id="contactModal" class="modal">
        <div class="modal-content">
            <div class="bg-gradient-to-r from-pink-500 to-rose-600 text-white p-6 flex justify-between items-center">
                <h2 class="text-3xl font-bold">تواصل معي</h2>
                <span class="text-4xl cursor-pointer hover:text-gray-300" onclick="closeModal('contactModal')">&times;</span>
            </div>
            <div class="p-8">
                <form class="space-y-6 max-w-2xl mx-auto">
                    <div>
                        <label class="block text-gray-700 font-semibold mb-2">الاسم</label>
                        <input type="text" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:border-pink-500 transition" placeholder="أدخل اسمك">
                    </div>
                    <div>
                        <label class="block text-gray-700 font-semibold mb-2">البريد الإلكتروني</label>
                        <input type="email" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:border-pink-500 transition" placeholder="أدخل بريدك الإلكتروني">
                    </div>
                    <div>
                        <label class="block text-gray-700 font-semibold mb-2">الرسالة</label>
                        <textarea class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:border-pink-500 transition" rows="4" placeholder="اكتب رسالتك هنا"></textarea>
                    </div>
                    <button type="submit" class="w-full bg-gradient-to-r from-pink-500 to-rose-600 text-white py-3 rounded-lg font-semibold hover:opacity-90 transition duration-300 transform hover:scale-105">
                        إرسال الرسالة
                    </button>
                </form>
                <div class="mt-8 text-center">
                    <h3 class="text-xl font-bold mb-4">طرق أخرى للتواصل</h3>
                    <div class="flex justify-center space-x-6">
                        <a href="#" class="text-gray-600 hover:text-pink-500 transition transform hover:scale-110">
                            <i class="fab fa-linkedin text-3xl"></i>
                        </a>
                        <a href="#" class="text-gray-600 hover:text-pink-500 transition transform hover:scale-110">
                            <i class="fab fa-github text-3xl"></i>
                        </a>
                        <a href="#" class="text-gray-600 hover:text-pink-500 transition transform hover:scale-110">
                            <i class="fab fa-twitter text-3xl"></i>
                        </a>
                        <a href="#" class="text-gray-600 hover:text-pink-500 transition transform hover:scale-110">
                            <i class="fas fa-envelope text-3xl"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Project Detail Modal -->
    <div id="projectDetailModal" class="modal">
        <div class="modal-content">
            <div class="bg-gradient-to-r from-orange-500 to-red-600 text-white p-6 flex justify-between items-center">
                <h2 id="projectDetailTitle" class="text-3xl font-bold">تفاصيل المشروع</h2>
                <span class="text-4xl cursor-pointer hover:text-gray-300" onclick="closeModal('projectDetailModal')">&times;</span>
            </div>
            <div class="p-8 overflow-y-auto" style="max-height: 70vh;">
                <div id="projectDetailContent">
                    <!-- Content will be dynamically inserted here -->
                </div>
            </div>
        </div>
    </div>

    <!-- Certificate Detail Modal -->
    <div id="certificateDetailModal" class="modal">
        <div class="modal-content">
            <div class="bg-gradient-to-r from-yellow-500 to-amber-600 text-white p-6 flex justify-between items-center">
                <h2 id="certificateDetailTitle" class="text-3xl font-bold">تفاصيل الشهادة</h2>
                <span class="text-4xl cursor-pointer hover:text-gray-300" onclick="closeModal('certificateDetailModal')">&times;</span>
            </div>
            <div class="p-8 overflow-y-auto" style="max-height: 70vh;">
                <div id="certificateDetailContent">
                    <!-- Content will be dynamically inserted here -->
                </div>
            </div>
        </div>
    </div>

    <script>
        // Modal functions
        function openModal(modalId) {
            document.getElementById(modalId).style.display = 'block';
            // Animate skill bars when skills modal is opened
            if (modalId === 'skillsModal') {
                setTimeout(() => {
                    const skillBars = document.querySelectorAll('#skillsModal .skill-bar');
                    skillBars.forEach(bar => {
                        const width = bar.getAttribute('data-width');
                        bar.style.width = width;
                    });
                }, 300);
            }
        }

        function closeModal(modalId) {
            document.getElementById(modalId).style.display = 'none';
        }

        // Close modal when clicking outside
        window.onclick = function(event) {
            if (event.target.classList.contains('modal')) {
                event.target.style.display = 'none';
            }
        }

        // Project details data
        const projectDetails = {
            project1: {
                title: "منصة التعلم الإلكتروني",
                image: "https://picsum.photos/seed/project1/800/400",
                description: "منصة تعليمية متكاملة تدعم الفيديو التفاعلي، الاختبارات، والشهادات الإلكترونية.",
                features: [
                    "دعم الفيديو التفاعلي مع إمكانية التشغيل البطيء",
                    "نظام اختبارات متقدم مع تصحيح تلقائي",
                    "إصدار شهادات رقمية قابلة للتحقق",
                    "لوحة تحكم للمدرسين والمتدربين",
                    "دعم متعدد اللغات"
                ],
                tech: ["React", "Node.js", "MongoDB", "WebRTC", "AWS"]
            },
            project2: {
                title: "تطبيق إدارة المشاريع",
                image: "https://picsum.photos/seed/project2/800/400",
                description: "تطبيق ويب متقدم لإدارة المشاريع مع ميزات تتبع المهام والتحقق من التقدم.",
                features: [
                    "لوحة Kanban تفاعلية",
                    "تتبع المهام والتحقق من التقدم",
                    "إشعارات فورية للمستخدمين",
                    "تقارير أداء مفصلة",
                    "دعم المشاريع المتعددة"
                ],
                tech: ["Vue.js", "Firebase", "Tailwind CSS", "Chart.js", "Pusher"]
            },
            project3: {
                title: "نظام التجارة الإلكترونية",
                image: "https://picsum.photos/seed/project3/800/400",
                description: "منصة تجارة إلكترونية متكاملة مع دعم متاجر متعددة وإدارة المخزون.",
                features: [
                    "دعم متاجر متعددة البائعين",
                    "نظام دفعات آمنة متعدد البوابات",
                    "إدارة المخزون تلقائية",
                    "تحليلات مبيعات متقدمة",
                    "دعم اللغات المتعددة"
                ],
                tech: ["Next.js", "Django", "PostgreSQL", "Stripe", "Redis"]
            },
            project4: {
                title: "تطبيق المواعيد الطبية",
                image: "https://picsum.photos/seed/project4/800/400",
                description: "تطبيق لتسهيل预约 المواعيد الطبية مع إدارة الأطباء والمستشفيات.",
                features: [
                    "جدول مواعيد تفاعلي",
                    "إشعارات للمواعيد القادمة",
                    "تقييم الأطباء والمستشفيات",
                    "تاريخ طبي تفاعلي",
                    "دعم الفيديو الطبي"
                ],
                tech: ["React Native", "Express", "MySQL", "Socket.io", "Twilio"]
            }
        };

        // Certificate details data
        const certificateDetails = {
            cert1: {
                title: "Google Cloud Architect",
                image: "https://picsum.photos/seed/cert1/400/300",
                description: "شهادة احترافية في تصميم البنية التحتية السحابية على منصة Google Cloud.",
                details: "تغطي هذه الشهادة تصميم البنى التحتية السحابية الآمنة والموثوقة والقابلة للتوسع باستخدام خدمات Google Cloud Platform.",
                issuer: "Google Cloud",
                date: "أبريل 2023"
            },
            cert2: {
                title: "AWS Certified Developer",
                image: "https://picsum.photos/seed/cert2/400/300",
                description: "شهادة مطور AWS المتقدم لتطوير التطبيقات السحابية.",
                details: "تأكد هذه الشهادة القدرة على تطوير وتوزيع التطبيقات الآمنة والفعالة على منصة AWS.",
                issuer: "Amazon Web Services",
                date: "يونيو 2022"
            },
            cert3: {
                title: "React Professional",
                image: "https://picsum.photos/seed/cert3/400/300",
                description: "شهادة احترافية في تطوير تطبيقات الويب باستخدام React.js.",
                details: "تغطي الشهادة مفاهيم React المتقدمة بما في ذلك Hooks, Context API, وأفضل الممارسات.",
                issuer: "React Developer Certification",
                date: "سبتمبر 2022"
            },
            cert4: {
                title: "MongoDB Certified Developer",
                image: "https://picsum.photos/seed/cert4/400/300",
                description: "شهادة مطور MongoDB لقاعدة البيانات غير العلائقية.",
                details: "تأكد هذه الشهادة القدرة على تصميم وتطوير تطبيقات باستخدام MongoDB.",
                issuer: "MongoDB University",
                date: "مارس 2021"
            }
        };

        // Show project detail
        function showProjectDetail(projectId) {
            const project = projectDetails[projectId];
            const modal = document.getElementById('projectDetailModal');
            const title = document.getElementById('projectDetailTitle');
            const content = document.getElementById('projectDetailContent');
            
            title.textContent = project.title;
            content.innerHTML = `
                <img src="${project.image}" alt="${project.title}" class="w-full h-64 object-cover rounded-lg mb-6">
                <p class="text-gray-700 mb-6">${project.description}</p>
                <h3 class="text-xl font-semibold mb-3">الميزات الرئيسية:</h3>
                <ul class="list-disc list-inside text-gray-700 mb-6 space-y-2">
                    ${project.features.map(feature => `<li>${feature}</li>`).join('')}
                </ul>
                <h3 class="text-xl font-semibold mb-3">التقنيات المستخدمة:</h3>
                <div class="flex flex-wrap gap-2 mb-6">
                    ${project.tech.map(tech => `<span class="bg-orange-600 text-white px-3 py-1 rounded-full">${tech}</span>`).join('')}
                </div>
            `;
            
            modal.style.display = 'block';
        }

        // Show certificate detail
        function showCertificateDetail(certId) {
            const cert = certificateDetails[certId];
            const modal = document.getElementById('certificateDetailModal');
            const title = document.getElementById('certificateDetailTitle');
            const content = document.getElementById('certificateDetailContent');
            
            title.textContent = cert.title;
            content.innerHTML = `
                <img src="${cert.image}" alt="${cert.title}" class="w-full h-48 object-cover rounded-lg mb-6">
                <p class="text-gray-700 mb-4">${cert.description}</p>
                <p class="text-gray-600 mb-2"><strong>الجهة المانحة:</strong> ${cert.issuer}</p>
                <p class="text-gray-600 mb-4"><strong>تاريخ الحصول:</strong> ${cert.date}</p>
                <p class="text-gray-700">${cert.details}</p>
            `;
            
            modal.style.display = 'block';
        }

        // Form submission
        document.querySelector('form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Create success message
            const successDiv = document.createElement('div');
            successDiv.className = 'bg-green-100 border border-green-400 text-green-700 px-4 py-3 rounded-lg mt-4 text-center';
            successDiv.innerHTML = '<i class="fas fa-check-circle mr-2"></i>تم إرسال رسالتك بنجاح! سأتواصل معك قريباً.';
            
            // Insert success message
            this.appendChild(successDiv);
            
            // Reset form
            this.reset();
            
            // Remove success message after 5 seconds
            setTimeout(() => {
                successDiv.remove();
            }, 5000);
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Add parallax effect to header
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const parallax = document.querySelector('header');
            parallax.style.transform = `translateY(${scrolled * 0.3}px)`;
        });
    </script>
</body>
</html>
