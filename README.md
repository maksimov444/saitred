<!DOCTYPE html>
<html lang="ru">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Практика | Александр Максимов</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: #000;
            color: #fff;
            font-family: Arial, sans-serif;
            line-height: 1.6;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        /* NAV */

        nav {
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(0, 0, 0, .95);
            border-bottom: 1px solid #222;
            backdrop-filter: blur(10px);
        }

        .container {
            width: 90%;
            max-width: 1150px;
            margin: auto;
        }

        .nav-container {
            min-height: 70px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-weight: bold;
            font-size: 20px;
            letter-spacing: 1px;
        }

        .menu {
            display: flex;
            gap: 25px;
            list-style: none;
        }

        .menu a {
            color: #888;
            font-size: 14px;
            transition: .2s;
        }

        .menu a:hover {
            color: white;
        }

        .back-link {
            color: #888;
            font-size: 14px;
            border: 1px solid #333;
            padding: 8px 14px;
            border-radius: 8px;
            transition: .2s;
        }

        .back-link:hover {
            background: #fff;
            color: #000;
            border-color: #fff;
        }

        /* HEADER */

        header {
            min-height: 80vh;
            display: flex;
            align-items: center;
            border-bottom: 1px solid #222;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: "";
            position: absolute;
            top: -50%;
            right: -20%;
            width: 700px;
            height: 700px;
            background: radial-gradient(circle, rgba(80, 80, 80, .25), transparent 70%);
            pointer-events: none;
        }

        .header-content {
            padding: 100px 0;
            position: relative;
            z-index: 1;
        }

        .small-title {
            color: #777;
            text-transform: uppercase;
            letter-spacing: 4px;
            font-size: 13px;
            margin-bottom: 25px;
        }

        h1 {
            font-size: clamp(45px, 8vw, 95px);
            line-height: .95;
            letter-spacing: -4px;
            margin-bottom: 30px;
        }

        h1 span {
            color: #555;
        }

        .header-description {
            max-width: 700px;
            color: #999;
            font-size: 20px;
        }

        .header-meta {
            margin-top: 50px;
            display: flex;
            flex-wrap: wrap;
            gap: 40px;
        }

        .meta-item .label {
            color: #555;
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 6px;
        }

        .meta-item .value {
            font-size: 18px;
            color: #ddd;
        }

        /* SECTIONS */

        section {
            padding: 100px 0;
            border-bottom: 1px solid #222;
        }

        .section-number {
            color: #555;
            font-size: 13px;
            letter-spacing: 3px;
            margin-bottom: 10px;
        }

        .section-title {
            font-size: 45px;
            margin-bottom: 45px;
            letter-spacing: -1px;
        }

        /* CARDS */

        .cards {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .card {
            padding: 30px;
            background: #090909;
            border: 1px solid #252525;
            border-radius: 15px;
            transition: .25s;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: #555;
        }

        .card h3 {
            font-size: 20px;
            margin-bottom: 12px;
        }

        .card p {
            color: #999;
            font-size: 15px;
        }

        /* ABOUT */

        .about {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 70px;
        }

        .about p {
            color: #aaa;
            font-size: 17px;
            margin-bottom: 20px;
        }

        .about strong {
            color: #fff;
        }

        .info-list {
            list-style: none;
        }

        .info-list li {
            display: flex;
            justify-content: space-between;
            padding: 15px 0;
            border-bottom: 1px solid #1c1c1c;
            font-size: 15px;
        }

        .info-list li span:first-child {
            color: #666;
        }

        .info-list li span:last-child {
            color: #ddd;
            text-align: right;
        }

        /* TIMELINE */

        .timeline {
            position: relative;
            padding-left: 40px;
            border-left: 1px solid #252525;
        }

        .timeline-item {
            position: relative;
            padding-bottom: 45px;
        }

        .timeline-item:last-child {
            padding-bottom: 0;
        }

        .timeline-item::before {
            content: "";
            position: absolute;
            left: -46px;
            top: 6px;
            width: 11px;
            height: 11px;
            border-radius: 50%;
            background: #fff;
            border: 3px solid #000;
        }

        .timeline-item .week {
            color: #666;
            font-size: 13px;
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-bottom: 8px;
        }

        .timeline-item h3 {
            font-size: 22px;
            margin-bottom: 10px;
        }

        .timeline-item p {
            color: #999;
            font-size: 16px;
        }

        /* TASKS */

        .tasks {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .task {
            padding: 30px;
            background: #090909;
            border: 1px solid #252525;
            border-radius: 15px;
        }

        .task .num {
            font-size: 40px;
            color: #2a2a2a;
            font-weight: bold;
            margin-bottom: 10px;
            line-height: 1;
        }

        .task h3 {
            font-size: 20px;
            margin-bottom: 12px;
        }

        .task p {
            color: #999;
            font-size: 15px;
        }

        /* SKILLS */

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .skill {
            padding: 10px 16px;
            border: 1px solid #333;
            border-radius: 8px;
            color: #bbb;
            font-size: 14px;
        }

        /* NOTES */

        .notes {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .note {
            padding: 30px;
            background: #090909;
            border: 1px solid #252525;
            border-radius: 15px;
        }

        .note h3 {
            font-size: 22px;
            margin-bottom: 12px;
        }

        .note p {
            color: #999;
        }

        /* FOOTER */

        footer {
            padding: 50px 0;
            color: #555;
            font-size: 14px;
        }

        footer .container {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 15px;
        }

        /* MOBILE */

        @media (max-width: 800px) {

            .nav-container {
                flex-direction: column;
                padding: 15px 0;
                gap: 15px;
            }

            .menu {
                gap: 12px;
                flex-wrap: wrap;
                justify-content: center;
            }

            .menu a {
                font-size: 12px;
            }

            .about {
                grid-template-columns: 1fr;
                gap: 40px;
            }

            .cards {
                grid-template-columns: 1fr;
            }

            .tasks {
                grid-template-columns: 1fr;
            }

            section {
                padding: 70px 0;
            }

            .section-title {
                font-size: 34px;
            }

            .header-meta {
                gap: 25px;
            }
        }
    </style>
</head>

<body>

    <!-- ================= NAVIGATION ================= -->

    <nav>
        <div class="container nav-container">

            <div class="logo">
                АМ · ПРАКТИКА
            </div>

            <ul class="menu">
                <li><a href="#about">О практике</a></li>
                <li><a href="#place">Место</a></li>
                <li><a href="#timeline">Ход</a></li>
                <li><a href="#tasks">Задачи</a></li>
                <li><a href="#skills">Навыки</a></li>
                <li><a href="#results">Итоги</a></li>
            </ul>

            <a class="back-link" href="index.html">← Назад в резюме</a>

        </div>
    </nav>

    <!-- ================= HEADER ================= -->

    <header>

        <div class="container">

            <div class="header-content">

                <div class="small-title">
                    Отчёт по учебной практике
                </div>

                <h1>
                    Практика в<br>
                    судебном участке
                    <span>№&nbsp;__</span>
                </h1>

                <p class="header-description">
                    Прохождение учебной практики студентом
                    3 курса Люберецкого техникума имени Гагарина
                    Максимовым Александром. Продолжительность —
                    3 недели.
                </p>

                <div class="header-meta">

                    <div class="meta-item">
                        <div class="label">Студент</div>
                        <div class="value">Максимов Александр</div>
                    </div>

                    <div class="meta-item">
                        <div class="label">Учебное заведение</div>
                        <div class="value">Люберецкий техникум им. Гагарина</div>
                    </div>

                    <div class="meta-item">
                        <div class="label">Срок практики</div>
                        <div class="value">3 недели</div>
                    </div>

                    <div class="meta-item">
                        <div class="label">Место</div>
                        <div class="value">Судебный участок</div>
                    </div>

                </div>

            </div>

        </div>

    </header>

    <!-- ================= ABOUT ================= -->

    <section id="about">

        <div class="container">

            <div class="section-number">
                01 — ABOUT
            </div>

            <h2 class="section-title">
                О практике
            </h2>

            <div class="about">

                <div>
                    <p>
                        Учебная практика проходила в течение
                        <strong>3 недель</strong> в судебном участке.
                    </p>

                    <p>
                        Цель практики — закрепление и расширение
                        теоретических знаний, полученных в техникуме,
                        а также получение практических навыков работы
                        с документами, делопроизводством и
                        информационными системами судебного участка.
                    </p>

                    <p>
                        Во время практики я ознакомился со структурой
                        судебного участка, порядком приёма граждан,
                        правилами оформления и хранения судебных
                        документов, а также с основами работы
                        в государственных информационных системах.
                    </p>
                </div>

                <div>
                    <ul class="info-list">
                        <li><span>Студент</span><span>Максимов А.</span></li>
                        <li><span>Специальность</span><span>Информационные технологии</span></li>
                        <li><span>Курс</span><span>3 курс</span></li>
                        <li><span>Место практики</span><span>Судебный участок</span></li>
                        <li><span>Срок</span><span>3 недели</span></li>
                        <li><span>Формат</span><span>Очная практика</span></li>
                    </ul>
                </div>

            </div>

        </div>

    </section>

    <!-- ================= PLACE ================= -->

    <section id="place">

        <div class="container">

            <div class="section-number">
                02 — PLACE
            </div>

            <h2 class="section-title">
                Место практики
            </h2>

            <div class="cards">

                <div class="card">
                    <h3>Судебный участок</h3>
                    <p>
                        Орган мирового правосудия, рассматривающий
                        гражданские, административные и уголовные
                        дела в пределах своей подсудности.
                    </p>
                </div>

                <div class="card">
                    <h3>Структура</h3>
                    <p>
                        Мировой судья, помощник судьи, секретарь
                        судебного заседания, делопроизводитель
                        и специалисты аппарата.
                    </p>
                </div>

                <div class="card">
                    <h3>Направления работы</h3>
                    <p>
                        Приём граждан, подготовка дел к рассмотрению,
                        ведение протоколов, оформление судебных
                        актов и работа с архивом.
                    </p>
                </div>

            </div>

        </div>

    </section>

    <!-- ================= TIMELINE ================= -->

    <section id="timeline">

        <div class="container">

            <div class="section-number">
                03 — TIMELINE
            </div>

            <h2 class="section-title">
                Ход практики
            </h2>

            <div class="timeline">

                <div class="timeline-item">
                    <div class="week">Неделя 1</div>
                    <h3>Ознакомление с участком</h3>
                    <p>
                        Инструктаж по охране труда и внутреннему
                        распорядку. Знакомство со структурой судебного
                        участка, должностными обязанностями сотрудников
                        и основными направлениями деятельности.
                    </p>
                </div>

                <div class="timeline-item">
                    <div class="week">Неделя 2</div>
                    <h3>Работа с документами</h3>
                    <p>
                        Изучение порядка приёма, регистрации и хранения
                        судебных документов. Помощь в подготовке дел
                        к судебным заседаниям, работа с делопроизводством
                        и ознакомление с номенклатурой дел.
                    </p>
                </div>

                <div class="timeline-item">
                    <div class="week">Неделя 3</div>
                    <h3>Информационные системы и итоги</h3>
                    <p>
                        Работа с государственными информационными
                        системами и электронным документооборотом.
                        Обобщение полученных знаний, подготовка отчёта
                        и оформление дневника практики.
                    </p>
                </div>

            </div>

        </div>

    </section>

    <!-- ================= TASKS ================= -->

    <section id="tasks">

        <div class="container">

            <div class="section-number">
                04 — TASKS
            </div>

            <h2 class="section-title">
                Выполненные задачи
            </h2>

            <div class="tasks">

                <div class="task">
                    <div class="num">01</div>
                    <h3>Изучение структуры участка</h3>
                    <p>
                        Ознакомление с полномочиями мирового судьи,
                        обязанностями сотрудников аппарата и порядком
                        организации работы судебного участка.
                    </p>
                </div>

                <div class="task">
                    <div class="num">02</ помог уже опотным работникам маленькими задачами
