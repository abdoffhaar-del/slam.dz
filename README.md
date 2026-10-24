

<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>موسوعة السلم والسلام المعاصرة</title>
    <!-- Google Fonts & FontAwesome -->
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --bg-main: #0f172a;
            --bg-card: rgba(30, 41, 59, 0.7);
            --bg-card-hover: rgba(51, 65, 85, 0.8);
            --primary: #38bdf8;
            --primary-glow: rgba(56, 189, 248, 0.25);
            --secondary: #2dd4bf;
            --accent: #f59e0b;
            --success: #22c55e;
            --danger: #ef4444;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --border-color: rgba(255, 255, 255, 0.1);
            --radius-lg: 24px;
            --radius-md: 16px;
            --radius-sm: 12px;
            --shadow: 0 20px 40px -15px rgba(0,0,0,0.5);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Tajawal', sans-serif;
            scroll-behavior: smooth;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            background-color: var(--bg-main);
            color: var(--text-main);
            line-height: 1.8;
            background-image: 
                radial-gradient(circle at 15% 15%, rgba(56, 189, 248, 0.12) 0%, transparent 40%),
                radial-gradient(circle at 85% 85%, rgba(45, 212, 191, 0.12) 0%, transparent 40%);
            background-attachment: fixed;
            min-height: 100vh;
        }

        /* Modern Glassmorphic Header */
        header {
            position: sticky;
            top: 0;
            background: rgba(15, 23, 42, 0.85);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-bottom: 1px solid var(--border-color);
            z-index: 1000;
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.2rem 2rem;
            position: relative;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 900;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo i {
            color: var(--primary);
            -webkit-text-fill-color: initial;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 1.8rem;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-muted);
            font-weight: 700;
            font-size: 0.95rem;
            transition: all 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--primary);
            text-shadow: 0 0 10px var(--primary-glow);
        }

        /* Three Dots Menu Container */
        .more-menu-container {
            position: relative;
        }

        .three-dots-btn {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid var(--border-color);
            color: var(--text-main);
            width: 42px;
            height: 42px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            font-size: 1.2rem;
            transition: all 0.3s ease;
        }

        .three-dots-btn:hover, .three-dots-btn.active {
            background: rgba(56, 189, 248, 0.2);
            border-color: var(--primary);
            color: var(--primary);
        }

        .dropdown-menu {
            position: absolute;
            left: 0;
            top: 52px;
            width: 260px;
            background: rgba(15, 23, 42, 0.95);
            border: 1px solid var(--border-color);
            border-radius: var(--radius-md);
            backdrop-filter: blur(20px);
            box-shadow: var(--shadow);
            padding: 0.8rem;
            display: none;
            flex-direction: column;
            gap: 6px;
            z-index: 1001;
        }

        .dropdown-menu.show {
            display: flex;
            animation: fadeIn 0.25s ease-out forwards;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .dropdown-item {
            padding: 0.75rem 1rem;
            color: var(--text-main);
            text-decoration: none;
            font-size: 0.95rem;
            font-weight: 700;
            border-radius: var(--radius-sm);
            display: flex;
            align-items: center;
            gap: 12px;
            transition: all 0.2s ease;
            cursor: pointer;
        }

        .dropdown-item i {
            color: var(--primary);
            width: 20px;
            text-align: center;
        }

        .dropdown-item:hover {
            background: rgba(56, 189, 248, 0.15);
            color: var(--primary);
        }

        .dropdown-divider {
            height: 1px;
            background: var(--border-color);
            margin: 4px 0;
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 5rem 1.5rem 3.5rem;
            max-width: 900px;
            margin: 0 auto;
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 6px 16px;
            background: rgba(56, 189, 248, 0.1);
            border: 1px solid rgba(56, 189, 248, 0.3);
            border-radius: 30px;
            color: var(--primary);
            font-size: 0.85rem;
            font-weight: 700;
            margin-bottom: 1.5rem;
        }

        .hero h1 {
            font-size: 3rem;
            font-weight: 900;
            line-height: 1.25;
            margin-bottom: 1.2rem;
            background: linear-gradient(180deg, #ffffff 0%, #94a3b8 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            font-size: 1.2rem;
            color: var(--text-muted);
            line-height: 1.8;
        }

        /* Main Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1.5rem 4rem;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            font-weight: 900;
            margin-bottom: 2.5rem;
            color: var(--text-main);
            position: relative;
        }

        .section-title span {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: var(--radius-lg);
            padding: 2rem;
            backdrop-filter: blur(12px);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            box-shadow: var(--shadow);
        }

        .card:hover {
            transform: translateY(-6px);
            border-color: rgba(56, 189, 248, 0.4);
            box-shadow: 0 20px 40px -10px var(--primary-glow);
            background: var(--bg-card-hover);
        }

        .card-icon {
            width: 56px;
            height: 56px;
            border-radius: var(--radius-sm);
            background: linear-gradient(135deg, rgba(56, 189, 248, 0.1), rgba(45, 212, 191, 0.1));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.6rem;
            color: var(--primary);
            margin-bottom: 1.2rem;
            border: 1px solid var(--border-color);
        }

        .card h3 {
            font-size: 1.35rem;
            font-weight: 700;
            margin-bottom: 0.8rem;
            color: #fff;
        }

        .card p {
            color: var(--text-muted);
            font-size: 0.98rem;
            line-height: 1.7;
        }

        /* Designers Grid Section */
        .designer-card {
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .designer-avatar {
            width: 85px;
            height: 85px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.2rem;
            color: #0f172a;
            margin: 0 auto 1.2rem;
            box-shadow: 0 0 25px var(--primary-glow);
        }

        .designer-card h3 {
            font-size: 1.4rem;
            color: var(--text-main);
            margin-bottom: 0.4rem;
        }

        .designer-role {
            display: inline-block;
            padding: 4px 12px;
            background: rgba(45, 212, 191, 0.15);
            border: 1px solid rgba(45, 212, 191, 0.3);
            color: var(--secondary);
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 700;
            margin-bottom: 0.8rem;
        }

        /* Poem Cards */
        .poem-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-right: 4px solid var(--primary);
            padding: 1.8rem;
            margin-bottom: 1.2rem;
            border-radius: var(--radius-md);
            backdrop-filter: blur(12px);
            transition: all 0.3s ease;
        }

        .poem-card:hover {
            transform: translateX(-5px);
            border-color: var(--primary);
        }

        .poem-text {
            font-size: 1.2rem;
            font-weight: 700;
            color: var(--text-main);
            margin-bottom: 0.6rem;
        }

        .poem-author {
            color: var(--secondary);
            font-weight: 700;
            font-size: 0.95rem;
        }

        /* Modern Quiz Section */
        .quiz-wrapper {
            max-width: 680px;
            margin: 3rem auto 0;
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: var(--radius-lg);
            padding: 2.5rem;
            box-shadow: var(--shadow);
            backdrop-filter: blur(16px);
            position: relative;
            overflow: hidden;
        }

        .quiz-wrapper::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
        }

        .quiz-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid var(--border-color);
        }

        .quiz-step {
            font-size: 0.9rem;
            color: var(--text-muted);
            font-weight: 700;
        }

        .quiz-score-badge {
            background: rgba(34, 197, 94, 0.15);
            border: 1px solid rgba(34, 197, 94, 0.3);
            color: var(--success);
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 700;
        }

        .quiz-question {
            font-size: 1.3rem;
            font-weight: 700;
            color: #fff;
            margin-bottom: 1.8rem;
            line-height: 1.6;
        }

        .quiz-options {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .quiz-option {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid var(--border-color);
            padding: 1.1rem 1.4rem;
            border-radius: var(--radius-md);
            cursor: pointer;
            font-weight: 700;
            font-size: 1rem;
            color: var(--text-main);
            transition: all 0.25s ease;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .quiz-option:hover {
            background: rgba(56, 189, 248, 0.08);
            border-color: var(--primary);
            transform: translateX(-4px);
        }

        .quiz-option.correct {
            background: rgba(34, 197, 94, 0.2) !important;
            border-color: var(--success) !important;
            color: #fff !important;
            box-shadow: 0 0 20px rgba(34, 197, 94, 0.3);
        }

        .quiz-option.correct::after {
            content: '✓';
            color: var(--success);
            font-weight: 900;
            font-size: 1.2rem;
        }

        .quiz-option.wrong {
            background: rgba(239, 68, 68, 0.2) !important;
            border-color: var(--danger) !important;
            color: #fff !important;
        }

        .quiz-option.wrong::after {
            content: '✕';
            color: var(--danger);
            font-weight: 900;
            font-size: 1.2rem;
        }

        .quiz-option.disabled {
            pointer-events: none;
            opacity: 0.7;
        }

        .quiz-feedback {
            margin-top: 1.5rem;
            padding: 1rem;
            border-radius: var(--radius-sm);
            text-align: center;
            font-weight: 700;
            font-size: 1rem;
            display: none;
        }

        .quiz-feedback.show {
            display: block;
        }

        /* Wall Section */
        .wall-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: var(--radius-lg);
            padding: 2rem;
            backdrop-filter: blur(12px);
        }

        .wall-input {
            display: flex;
            gap: 12px;
            margin-bottom: 1.5rem;
            flex-wrap: wrap;
        }

        .wall-input input {
            flex: 1;
            min-width: 220px;
            padding: 0.9rem 1.2rem;
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid var(--border-color);
            border-radius: var(--radius-sm);
            color: #fff;
            outline: none;
            font-size: 0.95rem;
            transition: border-color 0.3s;
        }

        .wall-input input:focus {
            border-color: var(--primary);
        }

        .wall-input button {
            padding: 0.9rem 1.8rem;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: #0f172a;
            border: none;
            border-radius: var(--radius-sm);
            cursor: pointer;
            font-weight: 900;
            transition: all 0.3s ease;
        }

        .wall-input button:hover {
            opacity: 0.9;
            transform: translateY(-2px);
            box-shadow: 0 10px 20px var(--primary-glow);
        }

        .messages-list {
            display: flex;
            flex-direction: column;
            gap: 10px;
            max-height: 250px;
            overflow-y: auto;
        }

        .message-item {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid var(--border-color);
            padding: 1rem 1.2rem;
            border-radius: var(--radius-sm);
            border-right: 3px solid var(--secondary);
            color: var(--text-main);
            font-size: 0.95rem;
        }

        /* Modal Popup */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(15, 23, 42, 0.85);
            backdrop-filter: blur(10px);
            display: none;
            align-items: center;
            justify-content: center;
            z-index: 2000;
            padding: 1.5rem;
        }

        .modal-overlay.show {
            display: flex;
        }

        .modal-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            border-radius: var(--radius-lg);
            padding: 2rem;
            max-width: 500px;
            width: 100%;
            box-shadow: var(--shadow);
            position: relative;
        }

        .modal-close {
            position: absolute;
            top: 15px;
            left: 15px;
            background: transparent;
            border: none;
            color: var(--text-muted);
            font-size: 1.2rem;
            cursor: pointer;
        }

        .modal-close:hover {
            color: var(--danger);
        }

        footer {
            border-top: 1px solid var(--border-color);
            background: rgba(15, 23, 42, 0.9);
            text-align: center;
            padding: 2rem;
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .nav-links { display: none; }
            .hero h1 { font-size: 2.1rem; }
            .hero p { font-size: 1rem; }
            .quiz-wrapper { padding: 1.5rem; }
            .quiz-question { font-size: 1.15rem; }
        }
    </style>
</head>
<body>

    <!-- Modern Header -->
    <header>
        <nav>
            <div class="logo"><i class="fa-solid fa-dove"></i> موسوعة السلام</div>
            <ul class="nav-links">
                <li><a href="#designers">المصممون</a></li>
                <li><a href="#definition">المفهوم</a></li>
                <li><a href="#poets">الشعراء</a></li>
                <li><a href="#organizations">المنظمات</a></li>
                <li><a href="#nobel">نوبل</a></li>
                <li><a href="#quiz">التحدي</a></li>
                <li><a href="#wall">الحائط</a></li>
            </ul>

            <!-- Three Dots Button & Menu -->
            <div class="more-menu-container">
                <button class="three-dots-btn" id="threeDotsBtn" title="القائمة الإضافية">
                    <i class="fa-solid fa-ellipsis-vertical"></i>
                </button>
                <div class="dropdown-menu" id="dropdownMenu">
                    <a href="#designers" class="dropdown-item" onclick="closeDropdown()">
                        <i class="fa-solid fa-users-gear"></i> فريق المصممين
                    </a>
                    <a href="javascript:void(0)" class="dropdown-item" onclick="showModal('statistics')">
                        <i class="fa-solid fa-chart-pie"></i> إحصائيات السلام
                    </a>
                    <a href="javascript:void(0)" class="dropdown-item" onclick="showModal('sources')">
                        <i class="fa-solid fa-book-bookmark"></i> المصادر والمراجع
                    </a>
                    <div class="dropdown-divider"></div>
                    <a href="javascript:void(0)" class="dropdown-item" onclick="toggleDarkMode()">
                        <i class="fa-solid fa-moon"></i> الوضع الليلي الفائق
                    </a>
                    <a href="javascript:void(0)" class="dropdown-item" onclick="showModal('share')">
                        <i class="fa-solid fa-share-nodes"></i> مشاركة الموسوعة
                    </a>
                </div>
            </div>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-badge"><i class="fa-solid fa-sparkles"></i> المنصة المعاصرة للتثقيف</div>
        <h1>موسوعة السلم والسلام المعاصرة</h1>
        <p>منصة تفاعلية تجسد عمق السلام الإنساني، رؤى الشعراء، المنظمات العالمية، وحائزي نوبل بإبداع فريق العمل مع التحدي التثقيفي!</p>
    </section>

    <!-- Main Content -->
    <div class="container">

        <!-- 0. Designers Section -->
        <section id="designers" style="margin-bottom: 5rem;">
            <h2 class="section-title">فريق <span>المصممين والمبدعين</span></h2>
            <div class="grid">
                <div class="card designer-card">
                    <div class="designer-avatar"><i class="fa-solid fa-user-astronaut"></i></div>
                    <h3>عبدالله</h3>
                    <span class="designer-role">مطور ومصمم واجهات</span>
                    <p>المشرف على الهندسة التفاعلية وبناء الهيكل البرمجي للموسوعة.</p>
                </div>
                <div class="card designer-card">
                    <div class="designer-avatar"><i class="fa-solid fa-palette"></i></div>
                    <h3>زرقط</h3>
                    <span class="designer-role">مصمم تجربة المستخدم</span>
                    <p>المسؤول عن الهوية البصرية والألوان الجمالية المعاصرة للموقع.</p>
                </div>
                <div class="card designer-card">
                    <div class="designer-avatar"><i class="fa-solid fa-code"></i></div>
                    <h3>آدم</h3>
                    <span class="designer-role">مطور المحتوى والتحديات</span>
                    <p>مبتكر بنك الأسئلة التثقيفي وإعداد المادة العلمية للأقسام.</p>
                </div>
                <div class="card designer-card">
                    <div class="designer-avatar"><i class="fa-solid fa-wand-magic-sparkles"></i></div>
                    <h3>طارق</h3>
                    <span class="designer-role">مهندس المؤثرات والتفاعل</span>
                    <p>المصمم للمؤثرات الحركية وتحسين التفاعل والسلاسة للهواتف.</p>
                </div>
            </div>
        </section>

        <!-- 1. Deep Concept Section -->
        <section id="definition" style="margin-bottom: 5rem;">
            <h2 class="section-title">مفهوم <span>السلم والسلام</span></h2>
            <div class="grid">
                <div class="card">
                    <div class="card-icon"><i class="fa-solid fa-heart-pulse"></i></div>
                    <h3>تعريف السلم (Inner Peace)</h3>
                    <p>السلم هو النهج الأخلاقي والسلوكي الداخلي للمجتمعات، ويمثل حالة التوافق والوئام وغياب العنف في العلاقات بين الأفراد والجماعات.</p>
                </div>
                <div class="card">
                    <div class="card-icon"><i class="fa-solid fa-globe"></i></div>
                    <h3>تعريف السلام (Global Peace)</h3>
                    <p>السلام هو الحالة العامة والمناخ السياسي والاجتماعي الشامل الخالي من الحروب والنزاعات، والذي يتيح للبشرية الاستقرار والتطور.</p>
                </div>
                <div class="card">
                    <div class="card-icon"><i class="fa-solid fa-link"></i></div>
                    <h3>السلم في السلام</h3>
                    <p>لا يمكن تحقيق سلام عالمي دائم دون وجود "سلم داخلي مجتمعي" يتأسس على العدل، الديمقراطية، وحماية حقوق الإنسان وتقبل الاختلاف.</p>
                </div>
                <div class="card">
                    <div class="card-icon"><i class="fa-solid fa-shield-halved"></i></div>
                    <h3>أهمية السلام لتقدم الشعوب</h3>
                    <p>يضمن السلام حماية النفس البشرية، الحفاظ على الموارد والبيئة، ازدهار الاقتصاد، وبناء المنظومات التعليمية والصحية للأجيال القادمة.</p>
                </div>
            </div>
        </section>

        <!-- 2. Poets Section -->
        <section id="poets" style="margin-bottom: 5rem;">
            <h2 class="section-title">شعراء غنّوا <span>للسلام</span></h2>
            <div class="poem-card">
                <div class="poem-text">"سَأَحْلُمُ كَيْفَ يَشَاءُ الفَضَاءُ... وَأَبْنِي مِنَ الحُلْمِ جَسْراً لِلسَّلاَمْ"</div>
                <div class="poem-author">- محمود درويش</div>
            </div>
            <div class="poem-card">
                <div class="poem-text">"إذا الشّعْبُ يَوْماً أرَادَ الحَيَاةَ... فَلا بُدَّ أنْ يَسْتَجِيبَ القَدَر"</div>
                <div class="poem-author">- أبو القاسم الشابي</div>
            </div>
            <div class="poem-card">
                <div class="poem-text">"الحب والسلام هما اللغة الوحيدة التي يستطيع كل إنسان فهمها بدون ترجمة."</div>
                <div class="poem-author">- جبران خليل جبران</div>
            </div>
            <div class="poem-card">
                <div class="poem-text">"يا بلاداً نَشَرَت في العالَمِ الحَبَّ والسَّلامْ... أنتِ مَهْدٌ لِلأَمَانِي والنِّظَامْ"</div>
                <div class="poem-author">- نزار قباني</div>
            </div>
        </section>

        <!-- 3. Organizations Section -->
        <section id="organizations" style="margin-bottom: 5rem;">
            <h2 class="section-title">المنظمات <span>الداعية للسلام</span></h2>
            <div class="grid">
                <div class="card">
                    <div class="card-icon"><i class="fa-solid fa-building-columns"></i></div>
                    <h3>الأمم المتحدة (UN)</h3>
                    <p>أنشئت عام 1945 عقب الحرب العالمية الثانية لحفظ الأمن والسلم الدوليين وتطوير العلاقات الودية بين الأمم.</p>
                </div>
                <div class="card">
                    <div class="card-icon"><i class="fa-solid fa-graduation-cap"></i></div>
                    <h3>منظمة اليونسكو (UNESCO)</h3>
                    <p>تعمل على بناء السلام في عقول البشر من خلال التربية والتعليم والعلوم والثقافة وحماية التراث العالمي.</p>
                </div>
                <div class="card">
                    <div class="card-icon"><i class="fa-solid fa-child-reaching"></i></div>
                    <h3>منظمة اليونيسيف (UNICEF)</h3>
                    <p>منظمة الأمم المتحدة للطفولة، تعمل على حماية حقوق الأطفال في مناطق النزاع وتوفير الرعاية والتعليم لهم.</p>
                </div>
                <div class="card">
                    <div class="card-icon"><i class="fa-solid fa-dove"></i></div>
                    <h3>منظمة العفو الدولية (Amnesty)</h3>
                    <p>حركة عالمية مستقلة تدافع عن حقوق الإنسان وتحارب الظلم والانتهاكات وتعزز عدالة السلام.</p>
                </div>
            </div>
        </section>

        <!-- 4. Nobel Laureates -->
        <section id="nobel" style="margin-bottom: 5rem;">
            <h2 class="section-title">حائزو <span>جائزة نوبل للسلام</span></h2>
            <div class="grid">
                <div class="card">
                    <h3>نيلسون مانديلا (1993)</h3>
                    <p>قاد النضال ضد نظام الفصل العنصري في جنوب إفريقيا وأصبح رمزاً عالمياً للتسامح والمصالحة الوطنية.</p>
                </div>
                <div class="card">
                    <h3>الأم تيريزا (1979)</h3>
                    <p>خصصت حياتها بالكامل لخدمة المشردين والفقراء والمرضى ورسخت قيم الرحمة الإنسانية.</p>
                </div>
                <div class="card">
                    <h3>مارتن لوثر كينغ (1964)</h3>
                    <p>قائد حركة الحقوق المدنية في الولايات المتحدة الذي اعتمد أسلوب المقاومة السلمية واللاعنف.</p>
                </div>
                <div class="card">
                    <h3>ملالا يوسفزي (2014)</h3>
                    <p>أصغر حائزة على جائزة نوبل للسلام لنضالها السلمي من أجل حق الفتيات في التعليم برغم المخاطر.</p>
                </div>
                <div class="card">
                    <h3>المَهاتما غاندي (أب السلام)</h3>
                    <p>مؤسس فلسفة "اللاعنف" (Ahimsa) والتظاهر السلمي التي ألهمت حركات الحرية والسلام في العالم.</p>
                </div>
            </div>
        </section>

        <!-- 5. Single Modern Quiz Challenge -->
        <section id="quiz" style="margin-bottom: 5rem;">
            <h2 class="section-title">التحدي <span>الثقافي للسلام</span></h2>
            <div class="quiz-wrapper">
                <div class="quiz-header">
                    <span class="quiz-step" id="quizStep">السؤال 1 من 5</span>
                    <span class="quiz-score-badge" id="quizScore">النقاط: 0</span>
                </div>
                <div class="quiz-question" id="quizQuestion">جاري تحميل السؤال...</div>
                <div class="quiz-options" id="quizOptions"></div>
                <div class="quiz-feedback" id="quizFeedback"></div>
            </div>
        </section>

        <!-- 6. Message Wall -->
        <section id="wall">
            <h2 class="section-title">حائط <span>أمنيات السلام</span></h2>
            <div class="wall-card">
                <div class="wall-input">
                    <input type="text" id="userMsg" placeholder="اكتب أمنيتك أو رسالتك للسلام العالمي...">
                    <button onclick="addMessage()">نشر الرسالة 🕊️</button>
                </div>
                <div class="messages-list" id="messagesList">
                    <div class="message-item">أتمنى أن ينتهي كل صراع ونعيش جميعاً بأمان وسلام.</div>
                    <div class="message-item">السلام يبدأ من الكلمة والابتسامة وحسن المعاملة.</div>
                </div>
            </div>
        </section>

    </div>

    <!-- Modal Popup Structure -->
    <div class="modal-overlay" id="modalOverlay">
        <div class="modal-card">
            <button class="modal-close" onclick="closeModal()"><i class="fa-solid fa-xmark"></i></button>
            <h3 id="modalTitle" style="color:var(--primary); margin-bottom: 1rem;">عنوان النافذة</h3>
            <div id="modalBody" style="color:var(--text-muted); font-size:0.95rem; line-height:1.7;">محتوى النافذة...</div>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <p>موسوعة ودليل السلم والسلام التفاعلي المعاصر © 2026 - إخراج وتصميم الفريق المبدع 🕊️</p>
    </footer>

    <!-- JavaScript Engine -->
    <script>
        /* --- DROPDOWN & THREE DOTS MENU LOGIC --- */
        const threeDotsBtn = document.getElementById('threeDotsBtn');
        const dropdownMenu = document.getElementById('dropdownMenu');

        threeDotsBtn.addEventListener('click', (e) => {
            e.stopPropagation();
            threeDotsBtn.classList.toggle('active');
            dropdownMenu.classList.toggle('show');
        });

        document.addEventListener('click', (e) => {
            if (!dropdownMenu.contains(e.target) && !threeDotsBtn.contains(e.target)) {
                closeDropdown();
            }
        });

        function closeDropdown() {
            threeDotsBtn.classList.remove('active');
            dropdownMenu.classList.remove('show');
        }

        /* --- MODAL POPUP LOGIC --- */
        function showModal(type) {
            closeDropdown();
            const overlay = document.getElementById('modalOverlay');
            const title = document.getElementById('modalTitle');
            const body = document.getElementById('modalBody');

            if (type === 'statistics') {
                title.innerText = '📊 إحصائيات ونشاط الموسوعة';
                body.innerHTML = `
                    <p style="margin-bottom:10px;">• إجمالي الشخصيات والمفكرين: 12 شخصية ملهمة.</p>
                    <p style="margin-bottom:10px;">• عدد المنظمات الدولية المغطاة: 4 منظمات رئيسية.</p>
                    <p style="margin-bottom:10px;">• التحديات والأسئلة التثقيفية: متجددة باستمرار.</p>
                    <p>• نسبة التفاعل اليومي مع حائط الأمنيات: عالية جداً.</p>
                `;
            } else if (type === 'sources') {
                title.innerText = '📚 المصادر والمراجع المعتمدة';
                body.innerHTML = `
                    <p style="margin-bottom:10px;">1. أرشيف منظمة الأمم المتحدة واليونسكو لحفظ السلام.</p>
                    <p style="margin-bottom:10px;">2. السجلات الرسمية لجائزة نوبل للسلام (Nobel Prize Official).</p>
                    <p>3. دواوين ومؤلفات الأدباء (محمود درويش، جبران خليل جبران، نزار قباني).</p>
                `;
            } else if (type === 'share') {
                title.innerText = '🔗 مشاركة الموسوعة مع الأصدقاء';
                body.innerHTML = `
                    <p style="margin-bottom:15px;">يمكنك نسخ رابط الموسوعة المباشر وشاركه فوراً مع أصدقائك لتصل الفائدة للجميع!</p>
                    <button onclick="copyShareLink()" style="width:100%; padding:0.8rem; background:var(--primary); border:none; border-radius:8px; font-weight:bold; cursor:pointer; color:#0f172a;">نسخ الرابط المباشر 📋</button>
                `;
            }

            overlay.classList.add('show');
        }

        function closeModal() {
            document.getElementById('modalOverlay').classList.remove('show');
        }

        function copyShareLink() {
            navigator.clipboard.writeText(window.location.href);
            alert('تم نسخ رابط الموسوعة بنجاح! يمكنك إرساله لأصدقائك الآن 🎉');
            closeModal();
        }

        function toggleDarkMode() {
            closeDropdown();
            alert('أنت تسخدم بالفعل نمط الداكن المعاصر والفريد واللافت للعينين! 🌙');
        }

        /* --- MODERN SINGLE QUIZ ENGINE --- */
        const quizData = [
            {
                q: "ما هي المنظمة العالمية المسؤولة عن حفظ الأمن والسلام الدوليين؟",
                options: ["منظمة الصحة العالمية", "الأمم المتحدة", "منظمة اليونسكو"],
                correct: 1
            },
            {
                q: "ماذا يرمز غصن الزيتون وحمامة السلام؟",
                options: ["رمز القوة والشجاعة", "رمز السلام والوئام", "رمز التجارة والعمل"],
                correct: 1
            },
            {
                q: "من هو القائد العالمي الشهير بلقب (أب السلام واللاعنف)؟",
                options: ["المهاتما غاندي", "نيلسون مانديلا", "مارتن لوثر كينغ"],
                correct: 0
            },
            {
                q: "من هي أصغر شخصية حازت على جائزة نوبل للسلام في التاريخ؟",
                options: ["الأم تيريزا", "ملالا يوسفزي", "شيرين عبادي"],
                correct: 1
            },
            {
                q: "ما هي المنظمة الدولية المختصة بحماية وبناء السلام عبر التربية والتعليم والعلوم؟",
                options: ["اليونسكو (UNESCO)", "اليونيسيف (UNICEF)", "منظمة العفو الدولية"],
                correct: 0
            }
        ];

        let currentIdx = 0;
        let scoreCount = 0;
        let canAnswer = true;

        function loadQuiz() {
            canAnswer = true;
            const current = quizData[currentIdx];
            document.getElementById('quizStep').innerText = `السؤال ${currentIdx + 1} من ${quizData.length}`;
            document.getElementById('quizQuestion').innerText = current.q;
            
            const optionsDiv = document.getElementById('quizOptions');
            const feedbackDiv = document.getElementById('quizFeedback');
            optionsDiv.innerHTML = '';
            feedbackDiv.className = 'quiz-feedback';

            current.options.forEach((opt, idx) => {
                const btn = document.createElement('div');
                btn.className = 'quiz-option';
                btn.innerText = opt;
                btn.onclick = () => handleAnswer(idx, btn);
                optionsDiv.appendChild(btn);
            });
        }

        function handleAnswer(selectedIdx, selectedBtn) {
            if (!canAnswer) return;
            canAnswer = false;

            const current = quizData[currentIdx];
            const options = document.querySelectorAll('.quiz-option');
            const feedbackDiv = document.getElementById('quizFeedback');

            options.forEach(opt => opt.classList.add('disabled'));

            if (selectedIdx === current.correct) {
                selectedBtn.classList.add('correct');
                scoreCount += 10;
                document.getElementById('quizScore').innerText = `النقاط: ${scoreCount}`;
                feedbackDiv.innerText = "إجابة صحيحة ممتازة! 🎯";
                feedbackDiv.style.background = "rgba(34, 197, 94, 0.15)";
                feedbackDiv.style.color = "var(--success)";
                feedbackDiv.classList.add('show');
            } else {
                selectedBtn.classList.add('wrong');
                options[current.correct].classList.add('correct');
                feedbackDiv.innerText = "إجابة خاطئة! الإجابة الصحيحة ظهرت بالأخضر 💡";
                feedbackDiv.style.background = "rgba(239, 68, 68, 0.15)";
                feedbackDiv.style.color = "var(--danger)";
                feedbackDiv.classList.add('show');
            }

            setTimeout(() => {
                currentIdx = (currentIdx + 1) % quizData.length;
                loadQuiz();
            }, 2000);
        }

        // Initialize quiz on load
        loadQuiz();

        /* --- WALL MESSAGES --- */
        function addMessage() {
            const input = document.getElementById('userMsg');
            const text = input.value.trim();
            if(text) {
                const list = document.getElementById('messagesList');
                const item = document.createElement('div');
                item.className = 'message-item';
                item.innerText = text;
                list.prepend(item);
                input.value = '';
            }
        }
    </script>
</body>
</html>
