file:///C:/Users/User/Downloads/Максимов/index.html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Astra Linux - Российская операционная система</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary-color: #0b3d91;
            --secondary-color: #e63946;
            --light-color: #f8f9fa;
            --dark-color: #212529;
            --gray-color: #6c757d;
        }

        body {
            color: var(--dark-color);
            background-color: #f5f7fa;
            line-height: 1.6;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background-color: var(--primary-color);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo i {
            font-size: 2.2rem;
            color: var(--secondary-color);
        }

        .logo h1 {
            font-size: 1.8rem;
            font-weight: 700;
        }

        .logo span {
            color: var(--secondary-color);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 2rem;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            font-size: 1.1rem;
        }

        nav ul li a:hover {
            color: #ffcc00;
        }

        .mobile-menu-btn {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero section */
        .hero {
            background: linear-gradient(rgba(11, 61, 145, 0.9), rgba(11, 61, 145, 0.8)), url('https://images.unsplash.com/photo-1550745165-9bc0b252726f?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 6rem 0;
            text-align: center;
        }

        .hero h2 {
            font-size: 3rem;
            margin-bottom: 1rem;
            font-weight: 700;
        }

        .hero p {
            font-size: 1.3rem;
            max-width: 800px;
            margin: 0 auto 2rem;
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary-color);
            color: white;
            padding: 0.8rem 2rem;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background-color: #c1121f;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        /* Features section */
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--primary-color);
            font-size: 2.2rem;
            position: relative;
        }

        .section-title:after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background-color: var(--secondary-color);
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
        }

        section {
            padding: 5rem 0;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .feature-card {
            background-color: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s, box-shadow 0.3s;
            text-align: center;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }

        .feature-card i {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 1.5rem;
        }

        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary-color);
        }

        /* Editions section */
        .editions {
            background-color: var(--light-color);
        }

        .editions-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .edition-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }

        .edition-card:hover {
            transform: translateY(-10px);
        }

        .edition-header {
            background-color: var(--primary-color);
            color: white;
            padding: 1.5rem;
            text-align: center;
        }

        .edition-header h3 {
            font-size: 1.5rem;
        }

        .edition-body {
            padding: 2rem;
        }

        .edition-body ul {
            list-style-type: none;
        }

        .edition-body ul li {
            padding: 0.5rem 0;
            border-bottom: 1px solid #eee;
        }

        .edition-body ul li:last-child {
            border-bottom: none;
        }

        .edition-body ul li i {
            color: var(--secondary-color);
            margin-right: 10px;
        }

        /* About section */
        .about-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
            align-items: center;
        }

        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--primary-color);
        }

        .about-image {
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* Footer */
        footer {
            background-color: var(--primary-color);
            color: white;
            padding: 3rem 0 1.5rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
            color: #ffcc00;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 0.8rem;
        }

        .footer-column ul li a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-column ul li a:hover {
            color: #ffcc00;
        }

        .copyright {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            color: #aaa;
        }

        /* Responsive */
        @media (max-width: 992px) {
            .hero h2 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
        }

        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
                gap: 1rem;
            }
            
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0.5rem 1rem;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
        }

        @media (max-width: 576px) {
            .hero {
                padding: 4rem 0;
            }
            
            section {
                padding: 3rem 0;
            }
            
            .feature-card, .edition-card {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">
                <i class="fab fa-linux"></i>
                <h1>Astra <span>Linux</span></h1>
            </div>
            <div class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Главная</a></li>
                    <li><a href="#features">Особенности</a></li>
                    <li><a href="#editions">Редакции</a></li>
                    <li><a href="#about">О системе</a></li>
                    <li><a href="#download" class="btn">Скачать</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h2>Российская операционная система</h2>
            <p>Astra Linux — защищённая операционная система, разработанная для выполнения задач любой степени сложности в интересах государства и бизнеса, с повышенными требованиями к информационной безопасности.</p>
            <a href="#download" class="btn">Скачать Astra Linux</a>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features">
        <div class="container">
            <h2 class="section-title">Ключевые особенности</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <i class="fas fa-shield-alt"></i>
                    <h3>Безопасность</h3>
                    <p>Сертифицированная ОС для работы с информацией, составляющей государственную тайну. Встроенные механизмы защиты информации.</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-cogs"></i>
                    <h3>Стабильность</h3>
                    <p>Длительный цикл поддержки, регулярные обновления и высокая надёжность системы в работе.</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-certificate"></i>
                    <h3>Сертификация</h3>
                    <p>Соответствие требованиям регуляторов. Сертификаты ФСТЭК, Минобороны и ФСБ России.</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-users-cog"></i>
                    <h3>Универсальность</h3>
                    <p>Поддержка широкого спектра аппаратных платформ и приложений. Работа как на серверах, так и на рабочих станциях.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Editions Section -->
    <section class="editions" id="editions">
        <div class="container">
            <h2 class="section-title">Редакции Astra Linux</h2>
            <div class="editions-container">
                <div class="edition-card">
                    <div class="edition-header">
                        <h3>Common Edition</h3>
                    </div>
                    <div class="edition-body">
                        <ul>
                            <li><i class="fas fa-check"></i> Для широкого круга пользователей</li>
                            <li><i class="fas fa-check"></i> Базовые средства защиты</li>
                            <li><i class="fas fa-check"></i> Поддержка офисных приложений</li>
                            <li><i class="fas fa-check"></i> Графическая среда Fly</li>
                            <li><i class="fas fa-check"></i> Совместимость с популярным ПО</li>
                        </ul>
                    </div>
                </div>
                <div class="edition-card">
                    <div class="edition-header">
                        <h3>Special Edition</h3>
                    </div>
                    <div class="edition-body">
                        <ul>
                            <li><i class="fas fa-check"></i> Для работы с гостайной</li>
                            <li><i class="fas fa-check"></i> Межсетевые экраны и криптография</li>
                            <li><i class="fas fa-check"></i> Контроль целостности и доступов</li>
                            <li><i class="fas fa-check"></i> Средства аудита безопасности</li>
                            <li><i class="fas fa-check"></i> Сертификация ФСТЭК и ФСБ</li>
                        </ul>
                    </div>
                </div>
                <div class="edition-card">
                    <div class="edition-header">
                        <h3>Server Edition</h3>
                    </div>
                    <div class="edition-body">
                        <ul>
                            <li><i class="fas fa-check"></i> Для развёртывания серверов</li>
                            <li><i class="fas fa-check"></i> Поддержка виртуализации</li>
                            <li><i class="fas fa-check"></i> Средства резервного копирования</li>
                            <li><i class="fas fa-check"></i> Мониторинг и управление</li>
                            <li><i class="fas fa-check"></i> Высокая отказоустойчивость</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <h2 class="section-title">О системе Astra Linux</h2>
            <div class="about-content">
                <div class="about-text">
                    <h3>Надёжность и безопасность</h3>
                    <p>Astra Linux — это российская операционная система, разработанная компанией "РусБИТех-Астра". Система создавалась с учётом требований российских регуляторов и специальных служб к защите информации.</p>
                    <p>ОС обладает сертификатами соответствия требованиям по безопасности информации ФСТЭК России, Минобороны России и ФСБ России, что позволяет использовать её для обработки информации, составляющей государственную тайну.</p>
                    <p>Система активно внедряется в государственных учреждениях, силовых структурах и корпоративном секторе как основа для создания защищённой ИТ-инфраструктуры.</p>
                    <a href="#download" class="btn">Узнать больше</a>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1558494949-ef010cbdcc31?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80" alt="Astra Linux интерфейс">
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Astra Linux</h3>
                    <p>Российская операционная система для государственных структур и корпоративного сектора с повышенными требованиями к информационной безопасности.</p>
                </div>
                <div class="footer-column">
                    <h3>Редакции</h3>
                    <ul>
                        <li><a href="#">Common Edition</a></li>
                        <li><a href="#">Special Edition</a></li>
                        <li><a href="#">Server Edition</a></li>
                        <li><a href="#">Для встраиваемых систем</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Ресурсы</h3>
                    <ul>
                        <li><a href="#">Документация</a></li>
                        <li><a href="#">Форум поддержки</a></li>
                        <li><a href="#">Блог</a></li>
                        <li><a href="#">Партнёры</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Контакты</h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> Россия, Москва</li>
                        <li><i class="fas fa-globe"></i> www.astra-linux.com</li>
                        <li><i class="fas fa-envelope"></i> info@astra-linux.com</li>
                        <li><i class="fas fa-phone"></i> +7 (495) 123-45-67</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Astra Linux. Все права защищены. Разработано компанией "РусБИТех-Астра".</p>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Mobile menu toggle
        const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
        const nav = document.querySelector('nav ul');
        
        mobileMenuBtn.addEventListener('click', () => {
            nav.style.display = nav.style.display === 'flex' ? 'none' : 'flex';
        });

        // Handle window resize
        window.addEventListener('resize', () => {
            if(window.innerWidth > 768) {
                nav.style.display = 'flex';
            } else {
                nav.style.display = 'none';
            }
        });

        // Initialize mobile menu display
        if(window.innerWidth <= 768) {
            nav.style.display = 'none';
            mobileMenuBtn.style.display = 'block';
        }
    </script>
</body>
</html>
