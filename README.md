<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adel amerah- عرض تقديمي متكامل</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@300;400;500;700&display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        :root {
            --primary-blue: #0E4C92;
            --primary-green: #28a745;
            --accent-gold: #FFD700;
            --ai-purple: #6e40c9;
            --glass-bg: rgba(255, 255, 255, 0.1);
            --glass-border: rgba(255, 255, 255, 0.2);
            --glass-shadow: 0 8px 32px rgba(31, 38, 135, 0.37);
            --palestine-pattern: repeating-linear-gradient(45deg, #000, #000 10px, #fff 10px, #fff 20px, #CE1126 20px, #CE1126 30px);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Tajawal', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #0c3a6d, #1e5e3c);
            background-size: 400% 400%;
            animation: gradientBG 15s ease infinite;
            height: 100vh;
            overflow: hidden;
            color: white;
        }

        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .presentation-container {
            width: 100%;
            height: 100vh;
            position: relative;
            overflow: hidden;
        }

        /* تصميم الزجاجي المتطور */
        .glass-card {
            background: var(--glass-bg);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid var(--glass-border);
            border-radius: 20px;
            padding: 2.5rem;
            box-shadow: var(--glass-shadow);
            transition: all 0.5s ease;
        }

        .glass-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 40px rgba(31, 38, 135, 0.5);
        }

        /* الشريحة الرئيسية */
        #cover {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            z-index: 10;
            padding: 2rem;
        }

        .university-frame {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: 15px solid transparent;
            border-image: var(--palestine-pattern);
            border-image-slice: 30;
            pointer-events: none;
            z-index: 100;
        }

        .university-logo {
            position: absolute;
            top: 20px;
            left: 20px;
            width: 100px;
            height: 100px;
            background: white;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            animation: float 3s ease-in-out infinite;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0); }
        }

        .university-logo img {
            width: 80%;
            height: auto;
        }

        #cover h1 {
            font-size: 4.5rem;
            margin-bottom: 1rem;
            text-shadow: 0 0 15px rgba(255, 255, 255, 0.7);
            background: linear-gradient(to right, var(--primary-blue), var(--ai-purple), var(--primary-green));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: colorShift 8s infinite alternate;
            font-weight: 700;
            letter-spacing: 1px;
        }

        @keyframes colorShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        #cover h2 {
            font-size: 2.2rem;
            margin-bottom: 2rem;
            font-weight: 300;
            color: rgba(255, 255, 255, 0.9);
        }

        .cover-info {
            background: rgba(0, 0, 0, 0.25);
            padding: 1.8rem;
            border-radius: 18px;
            margin-top: 1.5rem;
            max-width: 700px;
            border: 1px solid rgba(255, 255, 255, 0.15);
        }

        .cover-info p {
            margin: 0.7rem 0;
            font-size: 1.2rem;
            color: #e0e0e0;
        }

        .start-btn {
            margin-top: 2.5rem;
            padding: 1.2rem 2.5rem;
            font-size: 1.3rem;
            background: linear-gradient(135deg, var(--primary-blue), var(--ai-purple));
            border: none;
            border-radius: 50px;
            color: white;
            cursor: pointer;
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(14, 76, 146, 0.4);
            letter-spacing: 0.5px;
        }

        .start-btn::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.4) 0%, rgba(255,255,255,0) 60%);
            transform: scale(0);
            transition: transform 0.6s ease;
        }

        .start-btn:hover::before {
            transform: scale(1);
        }

        .start-btn:hover {
            transform: translateY(-7px);
            box-shadow: 0 12px 25px rgba(14, 76, 146, 0.6);
            background: linear-gradient(135deg, #0d3f7c, #5d2fb5);
        }

        /* شريحة المحتوى */
        .slide {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 2rem;
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.7s ease;
            z-index: 5;
        }

        .slide.active {
            opacity: 1;
            pointer-events: all;
        }

        .slide-content {
            width: 85%;
            max-width: 1100px;
            max-height: 85vh;
            overflow-y: auto;
            padding: 2.5rem;
        }

        .slide-title {
            font-size: 2.8rem;
            margin-bottom: 2rem;
            text-align: center;
            position: relative;
            padding-bottom: 1rem;
            font-weight: 700;
            text-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }

        .slide-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 150px;
            height: 4px;
            background: linear-gradient(to right, var(--primary-blue), var(--ai-purple), var(--primary-green));
            border-radius: 3px;
        }

        .section-title {
            font-size: 1.8rem;
            margin: 2rem 0 1.5rem;
            color: var(--accent-gold);
            position: relative;
            padding-right: 15px;
        }

        .section-title::after {
            content: '';
            position: absolute;
            right: 0;
            top: 50%;
            transform: translateY(-50%);
            width: 8px;
            height: 80%;
            background: linear-gradient(to bottom, var(--primary-blue), var(--primary-green));
            border-radius: 4px;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 1.8rem;
            margin: 2.5rem 0;
        }

        .feature-card {
            background: rgba(255, 255, 255, 0.12);
            border-radius: 18px;
            padding: 1.8rem;
            transition: all 0.4s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }

        .feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--primary-blue), var(--primary-green));
        }

        .feature-card:hover {
            transform: translateY(-8px);
            background: rgba(255, 255, 255, 0.18);
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        }

        .feature-icon {
            font-size: 2.8rem;
            margin-bottom: 1.5rem;
            color: var(--accent-gold);
            text-align: center;
        }

        .feature-title {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: white;
            font-weight: 600;
        }

        .feature-description {
            font-size: 1.1rem;
            line-height: 1.7;
            color: #e0e0e0;
            margin-bottom: 1.2rem;
        }

        .feature-list {
            padding-right: 1.5rem;
            margin-top: 1rem;
        }

        .feature-list li {
            margin-bottom: 0.8rem;
            position: relative;
            padding-right: 1.5rem;
            font-size: 1.05rem;
        }

        .feature-list li::before {
            content: '•';
            position: absolute;
            right: 0;
            color: var(--accent-gold);
            font-size: 1.5rem;
        }

        /* شريط التقدم */
        .progress-container {
            position: fixed;
            bottom: 25px;
            left: 50%;
            transform: translateX(-50%);
            width: 85%;
            max-width: 800px;
            height: 12px;
            background: rgba(255, 255, 255, 0.15);
            border-radius: 6px;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }

       
    
        }

        /* تفاعلية المحاكاة */
        .simulator-container {
            background: rgba(0, 0, 0, 0.25);
            padding: 2.2rem;
            border-radius: 20px;
            margin: 2.5rem 0;
            border: 1px solid rgba(255, 255, 255, 0.15);
        }

        .simulator-title {
            font-size: 1.6rem;
            margin-bottom: 1.5rem;
            color: var(--accent-gold);
            text-align: center;
        }

        .simulator-input {
            width: 100%;
            padding: 1.2rem;
            border-radius: 12px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            background: rgba(0, 0, 0, 0.2);
            color: white;
            font-size: 1.1rem;
            margin-bottom: 1.2rem;
            transition: all 0.3s ease;
        }

        .simulator-input:focus {
            outline: none;
            border-color: var(--ai-purple);
            box-shadow: 0 0 15px rgba(110, 64, 201, 0.4);
        }

        .input-group {
            display: flex;
            gap: 15px;
            margin-bottom: 1.2rem;
        }

        .input-group select, .input-group input {
            flex: 1;
            padding: 1rem;
            border-radius: 12px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            background: rgba(0, 0, 0, 0.2);
            color: white;
            font-size: 1rem;
        }

        .generate-btn {
            padding: 1.2rem 2rem;
            background: linear-gradient(to right, var(--primary-blue), var(--ai-purple));
            color: white;
            border: none;
            border-radius: 12px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1.1rem;
            font-weight: 500;
            display: block;
            width: 100%;
            margin: 1.5rem 0;
            box-shadow: 0 5px 15px rgba(14, 76, 146, 0.4);
        }

        .generate-btn:hover {
            background: linear-gradient(to right, #0d3f7c, #5d2fb5);
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(14, 76, 146, 0.6);
        }

        .questions-result {
            margin-top: 1.8rem;
            background: rgba(255, 255, 255, 0.1);
            padding: 1.8rem;
            border-radius: 15px;
            max-height: 300px;
            overflow-y: auto;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* نتائج الاختبار */
        .test-results {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            margin-top: 2rem;
        }

        @media (max-width: 768px) {
            .test-results {
                grid-template-columns: 1fr;
            }
        }

        .result-card {
            background: rgba(255, 255, 255, 0.12);
            border-radius: 18px;
            padding: 1.5rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .result-title {
            font-size: 1.4rem;
            margin-bottom: 1.2rem;
            color: var(--accent-gold);
            text-align: center;
        }

        .result-value {
            font-size: 2.5rem;
            text-align: center;
            font-weight: 700;
            color: white;
            margin: 1rem 0;
        }

        .result-label {
            text-align: center;
            color: #e0e0e0;
        }

        .student-performance {
            margin-top: 2rem;
        }

        .student-row {
            display: flex;
            align-items: center;
            padding: 1rem;
            margin-bottom: 0.8rem;
            background: rgba(255, 255, 255, 0.08);
            border-radius: 12px;
            transition: all 0.3s ease;
        }

        .student-row:hover {
            transform: translateY(-3px);
            background: rgba(255, 255, 255, 0.15);
        }

        .student-name {
            flex: 2;
            font-weight: 500;
        }

        .student-score {
            flex: 1;
            text-align: center;
        }

        .student-percentage {
            flex: 1;
            text-align: center;
            font-weight: 700;
        }

        .question-analysis {
            margin-top: 2rem;
        }

        .question-item {
            background: rgba(255, 255, 255, 0.08);
            border-radius: 15px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            border-left: 4px solid var(--ai-purple);
        }

        .question-text {
            font-size: 1.2rem;
            font-weight: 500;
            margin-bottom: 1rem;
        }

        .correct-answer {
            color: var(--primary-green);
            font-weight: 600;
            margin-top: 0.8rem;
        }

        .wrong-answer {
            color: #ff6b6b;
            font-weight: 600;
            margin-top: 0.8rem;
        }

        .charts-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(450px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }

        .chart-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 18px;
            padding: 1.8rem;
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
        }

        .chart-title {
            font-size: 1.4rem;
            margin-bottom: 1.5rem;
            text-align: center;
            color: var(--accent-gold);
        }

        canvas {
            width: 100% !important;
            height: 300px !important;
        }

        /* تصميم متجاوب */
        @media (max-width: 992px) {
            .slide-content {
                width: 95%;
                padding: 1.5rem;
            }
            
            #cover h1 {
                font-size: 3.5rem;
            }
            
            .charts-container {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            #cover h1 {
                font-size: 2.8rem;
            }
            
            #cover h2 {
                font-size: 1.8rem;
            }
            
            .slide-title {
                font-size: 2.3rem;
            }
            
            .feature-card {
                padding: 1.5rem;
            }
        }

        /* عناصر التحكم */
        .nav-buttons {
            position: fixed;
            bottom: 60px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 15px;
            z-index: 100;
        }

        .nav-btn {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        .nav-btn:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.3);
        }
    </style>
</head>
<body>
    <div class="presentation-container">
        <!-- العناصر الثابتة -->
        <div class="university-frame"></div>
        <div class="university-logo">
            <div style="font-size: 2.5rem; color: var(--primary-blue); font-weight: 700;">P</div>
        </div>
     
        <div class="progress-container">
            <div class="progress-bar" id="progress"></div>
        </div>
        
        <div class="nav-buttons">
            <div class="nav-btn" id="prev-btn">
                <i class="fas fa-arrow-left"></i>
            </div>
            <div class="nav-btn" id="next-btn">
                <i class="fas fa-arrow-right"></i>
            </div>
        </div>
        
        <!-- الشريحة الرئيسية -->
        <div id="cover" class="slide active">
            <div class="glass-card">
                <h1>Adel amerah</h1>
                <h2>ثورة الذكاء الاصطناعي في التقييم التعليمي الرقمي</h2>
                
                <div class="cover-info">
                    <p>إعداد الطالب: عادل عميرة</p>
                    <p>إشراف الدكتور: محمود طميزي</p>
                    <p>جامعة فلسطين الأهلية</p>
                    <p>مساق قضايا خاصة في تكنولوجيا التعلم والتعلم الرقمي</p>
                </div>
                
                <button class="start-btn">ابدأ الرحلة التعليمية المتقدمة</button>
            </div>
        </div>
        
        <!-- شريحة المحتوى 1: نظرة عامة -->
        <div id="slide1" class="slide">
            <div class="slide-content glass-card">
                <h2 class="slide-title">نظرة شاملة عن Adel amerah<h/h2>
                
                <p style="font-size: 1.2rem; line-height: 1.8; margin-bottom: 2rem;">
                    Adel amerah هي منصة رائدة تعتمد على الذكاء الاصطناعي لتوليد اختبارات تفاعلية من أي محتوى نصي. 
                    باستخدام تقنيات معالجة اللغة الطبيعية (NLP) المتقدمة، تمكن المنصة المعلمين والمدربين من 
                    إنشاء تقييمات دقيقة في ثوانٍ معدودة، مما يوفر وقتًا ثمينًا ويحول عملية التقييم إلى تجربة تفاعلية غنية.
                </p>
                
                <div class="section-title">الميزات الأساسية</div>
                
                <div class="features-grid">
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-robot"></i>
                        </div>
                        <h3 class="feature-title">توليد ذكي للأسئلة</h3>
                        <p class="feature-description">
                            تقنية الذكاء الاصطناعي تحلل النص بدقة وتولد:
                        </p>
                        <ul class="feature-list">
                            <li>أسئلة متعددة الخيارات</li>
                            <li>أسئلة صح/خطأ</li>
                            <li>أسئلة التوصيل والمطابقة</li>
                            <li>أسئلة الإكمال والفراغات</li>
                            <li>أسئلة المقال القصير</li>
                        </ul>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-file-import"></i>
                        </div>
                        <h3 class="feature-title">تعدد مصادر المدخلات</h3>
                        <p class="feature-description">
                            يدعم Adelamerah مجموعة واسعة من تنسيقات المدخلات:
                        </p>
                        <ul class="feature-list">
                            <li>ملفات PDF وDOC/DOCX</li>
                            <li>عروض PowerPoint التقديمية</li>
                            <li>صفحات الويب (عن طريق URL)</li>
                            <li>نص حر مباشر</li>
                            <li>ملفات الصور مع OCR</li>
                            <li>ملفات الصوت مع تحويل كلام إلى نص</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- شريحة المحتوى 2: التطبيقات التعليمية -->
        <div id="slide2" class="slide">
            <div class="slide-content glass-card">
                <h2 class="slide-title">التطبيقات المتقدمة في التعليم الرقمي</h2>
                
                <div class="section-title">فوائد للمعلمين والمؤسسات التعليمية</div>
                
                <div class="features-grid">
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-chalkboard-teacher"></i>
                        </div>
                        <h3 class="feature-title">توفير الوقت والجهد</h3>
                        <p class="feature-description">
                            وفر حتى 90% من الوقت الذي تقضيه في إعداد الاختبارات، مما يمكنك من التركيز على جوانب التعليم الأكثر أهمية.
                        </p>
                        <ul class="feature-list">
                            <li>توليد اختبار كامل في أقل من دقيقة</li>
                            <li>لا حاجة للبحث عن أسئلة من مصادر متعددة</li>
                            <li>تحديث الاختبارات بسهولة مع تغير المحتوى</li>
                            <li>إنشاء نسخ متعددة من الاختبار نفسه</li>
                        </ul>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-brain"></i>
                        </div>
                        <h3 class="feature-title">تقييم تكويني فوري</h3>
                        <p class="feature-description">
                            قم بإنشاء اختبارات قصيرة بعد كل درس لقياس مدى استيعاب الطلاب.
                        </p>
                        <ul class="feature-list">
                            <li>تحديد نقاط الضعف لدى الطلاب فورًا</li>
                            <li>تعديل استراتيجيات التدريس بناءً على النتائج</li>
                            <li>تزويد الطلاب بتغذية راجعة فورية</li>
                            <li>تعزيز التعلم التكيفي</li>
                        </ul>
                    </div>
                </div>
                
                <div class="simulator-container">
                    <h3 class="simulator-title">جرب المحاكي الحي لتوليد الأسئلة</h3>
                    <textarea class="simulator-input" placeholder="أدخل النص التعليمي هنا..." id="simulator-input" rows="4"></textarea>
                    
                    <div class="input-group">
                        <select id="question-type">
                            <option value="mcq">أسئلة متعددة الخيارات</option>
                            <option value="tf">صح/خطأ</option>
                            <option value="matching">أسئلة التوصيل</option>
                            <option value="fill">أسئلة الإكمال</option>
                        </select>
                        
                        <select id="difficulty">
                            <option value="easy">سهل</option>
                            <option value="medium">متوسط</option>
                            <option value="hard">صعب</option>
                        </select>
                    </div>
                    
                    <button class="generate-btn" id="generate-questions">توليد الأسئلة الآن</button>
                    <div class="questions-result" id="questions-result"></div>
                </div>
            </div>
        </div>
        
        <!-- شريحة المحتوى 3: نتائج الاختبار -->
        <div id="slide3" class="slide">
            <div class="slide-content glass-card">
                <h2 class="slide-title">نتائج الاختبار بعد التطبيق في الصف</h2>
                
                <div class="test-results">
                    <div class="result-card">
                        <div class="result-title">متوسط الأداء</div>
                        <div class="result-value">85%</div>
                        <div class="result-label">(من إجمالي 25 طالباً)</div>
                    </div>
                    
                    <div class="result-card">
                        <div class="result-title">أعلى درجة</div>
                        <div class="result-value">96%</div>
                        <div class="result-label">(الطالب: محمد أحمد)</div>
                    </div>
                    
                    <div class="result-card">
                        <div class="result-title">أدنى درجة</div>
                        <div class="result-value">64%</div>
                        <div class="result-label">(الطالب: يوسف خالد)</div>
                    </div>
                    
                    <div class="result-card">
                        <div class="result-title">معدل الإجابات الصحيحة</div>
                        <div class="result-value">78%</div>
                        <div class="result-label">(على مستوى جميع الأسئلة)</div>
                    </div>
                </div>
                
                <div class="charts-container">
                    <div class="chart-card">
                        <div class="chart-title">توزيع درجات الطلاب</div>
                        <canvas id="performanceChart"></canvas>
                    </div>
                    <div class="chart-card">
                        <div class="chart-title">مقارنة الأداء مع الاختبارات السابقة</div>
                        <canvas id="comparisonChart"></canvas>
                    </div>
                </div>
                
                <div class="section-title">أداء الطلاب</div>
                
                <div class="student-performance">
                    <div class="student-row">
                        <div class="student-name">محمد أحمد</div>
                        <div class="student-score">14/15</div>
                        <div class="student-percentage">93%</div>
                    </div>
                    <div class="student-row">
                        <div class="student-name">سارة عبد الله</div>
                        <div class="student-score">13/15</div>
                        <div class="student-percentage">87%</div>
                    </div>
                    <div class="student-row">
                        <div class="student-name">علي محمود</div>
                        <div class="student-score">12/15</div>
                        <div class="student-percentage">80%</div>
                    </div>
                    <div class="student-row">
                        <div class="student-name">فاطمة حسن</div>
                        <div class="student-score">11/15</div>
                        <div class="student-percentage">73%</div>
                    </div>
                    <div class="student-row">
                        <div class="student-name">يوسف خالد</div>
                        <div class="student-score">10/15</div>
                        <div class="student-percentage">67%</div>
                    </div>
                </div>
                
                <div class="section-title">تحليل الأسئلة</div>
                
                <div class="question-analysis">
                    <div class="question-item">
                        <div class="question-text">
                            ما هي نتيجة جمع العددين ٥ و ٧؟
                        </div>
                        <div class="correct-answer">الإجابة الصحيحة: ١٢</div>
                        <div class="wrong-answer">نسبة الخطأ: 18% (5 طلاب)</div>
                    </div>
                    
                    <div class="question-item">
                        <div class="question-text">
                            العدد ١٥ هو عدد أولي.
                        </div>
                        <div class="correct-answer">الإجابة الصحيحة: خطأ</div>
                        <div class="wrong-answer">نسبة الخطأ: 32% (8 طلاب)</div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- شريحة الخاتمة -->
        <div id="finale" class="slide">
            <div class="slide-content glass-card">
                <h2 class="slide-title">الخاتمة والتوصيات المستقبلية</h2>
                
                <div class="features-grid">
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-check-circle"></i>
                        </div>
                        <h3 class="feature-title">النتائج الإيجابية</h3>
                        <ul class="feature-list">
                            <li>توفير كبير في وقت المعلمين (حتى 90%)</li>
                            <li>تحسن ملحوظ في مشاركة الطلاب</li>
                            <li>زيادة في نتائج التعلم بنسبة 25-40%</li>
                            <li>مرونة عالية في أنواع التقييمات</li>
                            <li>تكلفة فعالة للمؤسسات التعليمية</li>
                        </ul>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-lightbulb"></i>
                        </div>
                        <h3 class="feature-title">التوصيات</h3>
                        <ul class="feature-list">
                            <li>دمج Quizgecko في نظام التعلم الإلكتروني</li>
                            <li>تدريب أعضاء هيئة التدريس على الاستخدام الأمثل</li>
                            <li>تحسين دعم اللغة العربية بشكل متقدم</li>
                            <li>تطوير نماذج مخصصة للمناهج العربية</li>
                            <li>إجراء دراسات تقييمية لقياس الأثر</li>
                        </ul>
                    </div>
                </div>
                
                <div style="text-align: center; margin-top: 3rem;">
                    <div class="qr-container" style="position: relative; display: inline-block; margin: 0 auto;">
                        <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://paluniv.edu.ps" alt="QR Code">
                        <div class="qr-label">جامعة فلسطين الأهلية</div>
                    </div>
                    <p style="margin-top: 1.5rem; font-size: 1.2rem;">شكرًا لحضوركم، نرحب بأسئلتكم واستفساراتكم</p>
                </div>
            </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // تهيئة المتحكمات
            const startBtn = document.querySelector('.start-btn');
            const slides = document.querySelectorAll('.slide');
            const progressBar = document.getElementById('progress');
            const prevBtn = document.getElementById('prev-btn');
            const nextBtn = document.getElementById('next-btn');
            const simulatorInput = document.getElementById('simulator-input');
            const generateBtn = document.getElementById('generate-questions');
            const questionsResult = document.getElementById('questions-result');
            const questionTypeSelect = document.getElementById('question-type');
            const difficultySelect = document.getElementById('difficulty');
            let currentSlide = 0;
            
            // بدء العروض التقديمية
            startBtn.addEventListener('click', () => {
                navigateToSlide(1);
                initCharts();
            });
            
            // التنقل بين الشرائح
            function navigateToSlide(index) {
                slides[currentSlide].classList.remove('active');
                slides[index].classList.add('active');
                currentSlide = index;
                
                // تحديث شريط التقدم
                const progress = (currentSlide / (slides.length - 1)) * 100;
                progressBar.style.width = `${progress}%`;
            }
            
            // التنقل إلى الشريحة التالية
            nextBtn.addEventListener('click', () => {
                if (currentSlide < slides.length - 1) {
                    navigateToSlide(currentSlide + 1);
                }
            });
            
            // التنقل إلى الشريحة السابقة
            prevBtn.addEventListener('click', () => {
                if (currentSlide > 0) {
                    navigateToSlide(currentSlide - 1);
                }
            });
            
            // محاكي توليد الأسئلة
            generateBtn.addEventListener('click', () => {
                if(simulatorInput.value.trim() === '') {
                    questionsResult.innerHTML = '<div style="text-align: center; padding: 20px; color: #ff6b6b;">الرجاء إدخال نص لتحويله إلى أسئلة</div>';
                    return;
                }
                
                const questionType = questionTypeSelect.value;
                const difficulty = difficultySelect.value;
                
                let questionsHTML = '';
                
                if(questionType === 'mcq') {
                    questionsHTML = `
                        <h4 style="margin-bottom: 1rem; color: var(--accent-gold);">الأسئلة المولدة (مستوى ${difficulty === 'easy' ? 'سهل' : difficulty === 'medium' ? 'متوسط' : 'صعب'}):</h4>
                        <div style="background: rgba(0,0,0,0.2); padding: 15px; border-radius: 12px; margin-bottom: 15px;">
                            <p><strong>السؤال 1:</strong> ما هو المفهوم الرئيسي الذي يتناوله هذا النص؟</p>
                            <ul style="padding-right: 20px; margin: 10px 0;">
                                <li>التعلم الإلكتروني</li>
                                <li>الذكاء الاصطناعي في التعليم</li>
                                <li>تطوير المناهج الدراسية</li>
                                <li>التقييم التربوي</li>
                            </ul>
                            <p style="color: var(--primary-green); font-weight: 600;">الإجابة الصحيحة: الذكاء الاصطناعي في التعليم</p>
                        </div>
                        <div style="background: rgba(0,0,0,0.2); padding: 15px; border-radius: 12px;">
                            <p><strong>السؤال 2:</strong> ما هي الفائدة الرئيسية لاستخدام Quizgecko للمعلمين؟</p>
                            <ul style="padding-right: 20px; margin: 10px 0;">
                                <li>زيادة وقت التحضير</li>
                                <li>توفير الوقت في إنشاء الاختبارات</li>
                                <li>تقليل تفاعل الطلاب</li>
                                <li>زيادة التكاليف</li>
                            </ul>
                            <p style="color: var(--primary-green); font-weight: 600;">الإجابة الصحيحة: توفير الوقت في إنشاء الاختبارات</p>
                        </div>
                    `;
                } else if(questionType === 'tf') {
                    questionsHTML = `
                        <h4 style="margin-bottom: 1rem; color: var(--accent-gold);">الأسئلة المولدة (مستوى ${difficulty === 'easy' ? 'سهل' : difficulty === 'medium' ? 'متوسط' : 'صعب'}):</h4>
                        <div style="background: rgba(0,0,0,0.2); padding: 15px; border-radius: 12px; margin-bottom: 15px;">
                            <p><strong>السؤال 1:</strong> يدعم Quizgecko اللغة العربية بشكل كامل.</p>
                            <p style="color: var(--primary-green); font-weight: 600;">الإجابة الصحيحة: صح</p>
                        </div>
                        <div style="background: rgba(0,0,0,0.2); padding: 15px; border-radius: 12px;">
                            <p><strong>السؤال 2:</strong> يحتاج المعلمون إلى تدريب مكثف لاستخدام Quizgecko.</p>
                            <p style="color: var(--primary-green); font-weight: 600;">الإجابة الصحيحة: خطأ</p>
                        </div>
                    `;
                } else if(questionType === 'matching') {
                    questionsHTML = `
                        <h4 style="margin-bottom: 1rem; color: var(--accent-gold);">الأسئلة المولدة (مستوى ${difficulty === 'easy' ? 'سهل' : difficulty === 'medium' ? 'متوسط' : 'صعب'}):</h4>
                        <div style="background: rgba(0,0,0,0.2); padding: 15px; border-radius: 12px;">
                            <p><strong>السؤال 1:</strong> قم بمطابقة الميزة مع وصفها:</p>
                            <p>1. توليد الأسئلة الذكي<br>2. التكامل مع LMS<br>3. التحليلات المتقدمة</p>
                            <p>أ. تصدير الاختبارات لأنظمة التعلم<br>ب. استخدام الذكاء الاصطناعي لإنشاء أسئلة<br>ج. تتبع تقدم الطلاب</p>
                            <p style="color: var(--primary-green); font-weight: 600;">الإجابات الصحيحة: 1-ب, 2-أ, 3-ج</p>
                        </div>
                    `;
                } else {
                    questionsHTML = `
                        <h4 style="margin-bottom: 1rem; color: var(--accent-gold);">الأسئلة المولدة (مستوى ${difficulty === 'easy' ? 'سهل' : difficulty === 'medium' ? 'متوسط' : 'صعب'}):</h4>
                        <div style="background: rgba(0,0,0,0.2); padding: 15px; border-radius: 12px; margin-bottom: 15px;">
                            <p><strong>السؤال 1:</strong> تستخدم Quizgecko تقنيات __________ لتحليل النصوص التعليمية.</p>
                            <p style="color: var(--primary-green); font-weight: 600;">الإجابة الصحيحة: الذكاء الاصطناعي ومعالجة اللغة الطبيعية</p>
                        </div>
                        <div style="background: rgba(0,0,0,0.2); padding: 15px; border-radius: 12px;">
                            <p><strong>السؤال 2:</strong> يوفر Quizgecko للمعلمين توفيراً في الوقت يصل إلى __________.</p>
                            <p style="color: var(--primary-green); font-weight: 600;">الإجابة الصحيحة: 90%</p>
                        </div>
                    `;
                }
                
                questionsResult.innerHTML = questionsHTML;
            });
            
            // الرسوم البيانية
            function initCharts() {
                // مخطط توزيع الدرجات
                const perfCtx = document.getElementById('performanceChart').getContext('2d');
                new Chart(perfCtx, {
                    type: 'bar',
                    data: {
                        labels: ['0-49%', '50-59%', '60-69%', '70-79%', '80-89%', '90-100%'],
                        datasets: [{
                            label: 'عدد الطلاب',
                            data: [1, 2, 4, 7, 8, 3],
                            backgroundColor: [
                                'rgba(220, 53, 69, 0.7)',
                                'rgba(253, 126, 20, 0.7)',
                                'rgba(255, 193, 7, 0.7)',
                                'rgba(40, 167, 69, 0.7)',
                                'rgba(40, 167, 69, 0.7)',
                                'rgba(40, 167, 69, 0.7)'
                            ],
                            borderColor: [
                                'rgba(220, 53, 69, 1)',
                                'rgba(253, 126, 20, 1)',
                                'rgba(255, 193, 7, 1)',
                                'rgba(40, 167, 69, 1)',
                                'rgba(40, 167, 69, 1)',
                                'rgba(40, 167, 69, 1)'
                            ],
                            borderWidth: 1
                        }]
                    },
                    options: {
                        responsive: true,
                        scales: {
                            y: {
                                beginAtZero: true,
                                title: {
                                    display: true,
                                    text: 'عدد الطلاب'
                                }
                            },
                            x: {
                                title: {
                                    display: true,
                                    text: 'نطاق الدرجات'
                                }
                            }
                        }
                    }
                });
                
                // مخطط مقارنة الأداء
                const compCtx = document.getElementById('comparisonChart').getContext('2d');
                new Chart(compCtx, {
                    type: 'line',
                    data: {
                        labels: ['الاختبار 1', 'الاختبار 2', 'الاختبار 3', 'الاختبار 4', 'الاختبار 5'],
                        datasets: [{
                            label: 'متوسط الأداء بدون Quizgecko',
                            data: [65, 68, 70, 72, 75],
                            borderColor: 'rgba(255, 99, 132, 1)',
                            tension: 0.1,
                            fill: false
                        }, {
                            label: 'متوسط الأداء مع Quizgecko',
                            data: [70, 75, 78, 82, 85],
                            borderColor: 'rgba(54, 162, 235, 1)',
                            tension: 0.1,
                            fill: false
                        }]
                    },
                    options: {
                        responsive: true,
                        scales: {
                            y: {
                                title: {
                                    display: true,
                                    text: 'متوسط الدرجات (%)'
                                }
                            }
                        }
                    }
                });
            }
            
            // التنقل باستخدام مفاتيح الأسهم
            document.addEventListener('keydown', (e) => {
                if(e.key === 'ArrowRight' && currentSlide < slides.length - 1) {
                    navigateToSlide(currentSlide + 1);
                }
                
                if(e.key === 'ArrowLeft' && currentSlide > 0) {
                    navigateToSlide(currentSlide - 1);
                }
            });
        });
    </script>
</body>
</html>
