<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <meta name="description" content="بطاقة أعمال يوسف غريب - مهندس IT، مبرمج، فني صيانة هواتف ومشاريع أردوينو">
    <title>يوسف غريب | Yossef Gharib - البطاقة الاحترافية</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;500;600;700;800&family=Poppins:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <!-- Font Awesome 6 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            /* Dark theme (default) */
            --bg-gradient: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #0f172a 100%);
            --card-bg: rgba(15, 23, 42, 0.65);
            --card-border: rgba(255, 255, 255, 0.12);
            --text-primary: #f8fafc;
            --text-secondary: #cbd5e1;
            --accent: #f97316;
            --accent-glow: rgba(249, 115, 22, 0.4);
            --btn-bg: rgba(255, 255, 255, 0.05);
            --btn-hover: rgba(255, 255, 255, 0.12);
            --field-bg: rgba(255, 255, 255, 0.06);
            --field-hover: rgba(249, 115, 22, 0.15);
            --shadow-sm: 0 8px 20px rgba(0, 0, 0, 0.3);
            --shadow-md: 0 20px 35px -10px rgba(0, 0, 0, 0.4);
            --transition: all 0.25s cubic-bezier(0.2, 0.9, 0.4, 1.1);
        }

        body.light {
            --bg-gradient: linear-gradient(135deg, #f1f5f9 0%, #e2e8f0 100%);
            --card-bg: rgba(255, 255, 255, 0.85);
            --card-border: rgba(0, 0, 0, 0.08);
            --text-primary: #0f172a;
            --text-secondary: #334155;
            --accent: #ea580c;
            --accent-glow: rgba(234, 88, 12, 0.2);
            --btn-bg: rgba(0, 0, 0, 0.04);
            --btn-hover: rgba(0, 0, 0, 0.08);
            --field-bg: rgba(0, 0, 0, 0.03);
            --field-hover: rgba(234, 88, 12, 0.1);
            --shadow-sm: 0 8px 20px rgba(0, 0, 0, 0.08);
            --shadow-md: 0 20px 35px -10px rgba(0, 0, 0, 0.15);
        }

        body {
            font-family: 'Cairo', 'Poppins', sans-serif;
            background: var(--bg-gradient);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 1.5rem;
            transition: var(--transition);
        }

        /* بطاقة احترافية زجاجية */
        .card {
            max-width: 680px;
            width: 100%;
            background: var(--card-bg);
            backdrop-filter: blur(16px);
            border-radius: 2rem;
            border: 1px solid var(--card-border);
            box-shadow: var(--shadow-md);
            padding: 2rem 1.8rem;
            transition: var(--transition);
        }

        /* أزرار التحكم */
        .controls {
            display: flex;
            justify-content: flex-end;
            gap: 0.75rem;
            margin-bottom: 1.5rem;
        }

        .icon-btn {
            background: var(--btn-bg);
            border: 1px solid var(--card-border);
            border-radius: 40px;
            padding: 0.5rem 1rem;
            cursor: pointer;
            font-size: 0.85rem;
            font-weight: 600;
            color: var(--text-primary);
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            font-family: inherit;
            backdrop-filter: blur(4px);
            transition: var(--transition);
        }

        .icon-btn:hover {
            background: var(--btn-hover);
            transform: translateY(-2px);
            border-color: var(--accent);
        }

        /* البروفايل */
        .profile {
            text-align: center;
            margin-bottom: 1.5rem;
        }

        .avatar {
            width: 130px;
            height: 130px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--accent);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2), 0 0 0 4px rgba(249, 115, 22, 0.2);
            margin-bottom: 1rem;
            transition: var(--transition);
            cursor: pointer;
        }

        .avatar:hover {
            transform: scale(1.02);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3), 0 0 0 6px rgba(249, 115, 22, 0.3);
        }

        h1 {
            font-size: 2rem;
            font-weight: 800;
            color: var(--text-primary);
            letter-spacing: -0.3px;
            margin-bottom: 0.25rem;
        }

        .badge {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background: var(--accent-glow);
            backdrop-filter: blur(4px);
            padding: 0.3rem 1.2rem;
            border-radius: 60px;
            font-size: 0.85rem;
            font-weight: 600;
            color: var(--accent);
            border: 1px solid rgba(249, 115, 22, 0.3);
            margin-top: 0.5rem;
        }

        .badge i {
            font-size: 0.9rem;
        }

        /* مجالات العمل (بطاقات مصغرة احترافية) */
        .fields {
            margin: 2rem 0;
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            justify-content: center;
        }

        .field-item {
            background: var(--field-bg);
            backdrop-filter: blur(4px);
            border: 1px solid var(--card-border);
            border-radius: 60px;
            padding: 0.6rem 1.3rem;
            font-size: 0.85rem;
            font-weight: 600;
            color: var(--text-primary);
            display: inline-flex;
            align-items: center;
            gap: 0.6rem;
            transition: var(--transition);
            cursor: default;
        }

        .field-item i {
            font-size: 1.1rem;
            color: var(--accent);
        }

        .field-item:hover {
            background: var(--field-hover);
            transform: translateY(-3px);
            border-color: var(--accent);
        }

        /* أزرار الروابط الاجتماعية */
        .links {
            display: flex;
            flex-direction: column;
            gap: 0.9rem;
            margin-top: 0.5rem;
        }

        .btn {
            display: flex;
            align-items: center;
            justify-content: flex-start;
            gap: 1rem;
            background: var(--btn-bg);
            backdrop-filter: blur(4px);
            padding: 0.85rem 1.5rem;
            border-radius: 60px;
            text-decoration: none;
            color: var(--text-primary);
            font-weight: 700;
            font-size: 1rem;
            transition: var(--transition);
            border: 1px solid var(--card-border);
            position: relative;
            overflow: hidden;
        }

        .btn i {
            font-size: 1.5rem;
            width: 32px;
            text-align: center;
            transition: var(--transition);
        }

        .btn span {
            flex: 1;
        }

        /* تأثيرات خاصة بكل منصة */
        .btn-instagram:hover { background: linear-gradient(45deg, #f09433, #d62976, #962fbf); color: white; border-color: transparent; }
        .btn-telegram:hover { background: #0088cc; color: white; border-color: transparent; }
        .btn-facebook:hover { background: #1877f2; color: white; border-color: transparent; }
        .btn-whatsapp:hover { background: #25d366; color: white; border-color: transparent; }
        .btn-tiktok:hover { background: #010101; color: #00f2ea; border-color: #00f2ea; }
        .btn-phone:hover { background: #34b7f1; color: white; border-color: transparent; }

        .btn:hover {
            transform: translateY(-3px);
            gap: 1.2rem;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        }

        .btn:hover i {
            transform: scale(1.05);
        }

        .footer {
            text-align: center;
            margin-top: 2rem;
            font-size: 0.7rem;
            color: var(--text-secondary);
            opacity: 0.8;
        }

        /* مودال تكبير الصورة */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.9);
            z-index: 1000;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            backdrop-filter: blur(5px);
        }

        .modal-content {
            max-width: 90vw;
            max-height: 90vh;
            position: relative;
            border-radius: 1rem;
            overflow: hidden;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
            animation: zoomIn 0.2s ease;
        }

        .modal-content img {
            width: auto;
            height: auto;
            max-width: 100%;
            max-height: 85vh;
            object-fit: contain;
            display: block;
            border-radius: 1rem;
            border: 3px solid var(--accent);
        }

        .close-modal {
            position: absolute;
            top: 20px;
            right: 30px;
            color: #fff;
            font-size: 40px;
            font-weight: bold;
            transition: 0.2s;
            cursor: pointer;
            z-index: 1001;
            background: rgba(0,0,0,0.5);
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            backdrop-filter: blur(4px);
        }

        .close-modal:hover {
            color: var(--accent);
            transform: scale(1.1);
            background: rgba(0,0,0,0.7);
        }

        @keyframes zoomIn {
            from {
                transform: scale(0.9);
                opacity: 0;
            }
            to {
                transform: scale(1);
                opacity: 1;
            }
        }

        /* استجابة للجوال */
        @media (max-width: 480px) {
            body { padding: 1rem; }
            .card { padding: 1.5rem; }
            .avatar { width: 100px; height: 100px; }
            h1 { font-size: 1.6rem; }
            .field-item { font-size: 0.7rem; padding: 0.4rem 1rem; }
            .btn { padding: 0.7rem 1rem; font-size: 0.85rem; }
            .btn i { font-size: 1.3rem; width: 28px; }
            .close-modal { top: 15px; right: 15px; width: 35px; height: 35px; font-size: 28px; }
        }

        /* تخصيص شريط التمرير */
        ::-webkit-scrollbar {
            width: 6px;
        }
        ::-webkit-scrollbar-track {
            background: var(--card-bg);
        }
        ::-webkit-scrollbar-thumb {
            background: var(--accent);
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <div class="card">
        <div class="controls">
            <button id="themeToggle" class="icon-btn"><i class="fas fa-moon"></i> <span data-key="theme">داكن</span></button>
            <button id="langToggle" class="icon-btn"><i class="fas fa-globe"></i> <span data-key="langBtn">English</span></button>
        </div>

        <div class="profile">
            <!-- صورة احترافية مع إمكانية النقر للتكبير -->
            <img class="avatar" id="avatarImg" src="https://ui-avatars.com/api/?background=F97316&color=fff&bold=true&size=130&length=2&name=Y+G" alt="Yossef Gharib">
            <h1 id="name">يوسف غريب قميح</h1>
            <div class="badge" id="badge">
                <i class="fas fa-bolt"></i> <span id="bio">IT Engineer | Programmer</span>
            </div>
        </div>

        <!-- مجالات العمل -->
        <div class="fields" id="fieldsContainer"></div>

        <!-- روابط التواصل -->
        <div class="links">
            <a href="https://www.instagram.com/yossef.gharib.komuh?igsh=MWhpOThnajVlM3cwNQ%3D%3D&utm_source=qr" target="_blank" rel="noopener noreferrer" class="btn btn-instagram">
                <i class="fab fa-instagram"></i> <span data-key="instagram">Instagram</span> <i class="fas fa-external-link-alt" style="font-size: 0.8rem; opacity: 0.7;"></i>
            </a>
            <a href="https://t.me/yossefgharibkomuh" target="_blank" rel="noopener noreferrer" class="btn btn-telegram">
                <i class="fab fa-telegram-plane"></i> <span data-key="telegram">Telegram</span> <i class="fas fa-external-link-alt" style="font-size: 0.8rem; opacity: 0.7;"></i>
            </a>
            <a href="https://www.facebook.com/share/17fpug8st8/?mibextid=wwXIfr" target="_blank" rel="noopener noreferrer" class="btn btn-facebook">
                <i class="fab fa-facebook-f"></i> <span data-key="facebook">Facebook</span> <i class="fas fa-external-link-alt" style="font-size: 0.8rem; opacity: 0.7;"></i>
            </a>
            <a href="https://wa.me/201101234892" target="_blank" rel="noopener noreferrer" class="btn btn-whatsapp">
                <i class="fab fa-whatsapp"></i> <span data-key="whatsapp">WhatsApp</span> <i class="fas fa-external-link-alt" style="font-size: 0.8rem; opacity: 0.7;"></i>
            </a>
            <a href="https://www.tiktok.com/@yossefgharib?_r=1&_t=ZS-978QJXVLedN" target="_blank" rel="noopener noreferrer" class="btn btn-tiktok">
                <i class="fab fa-tiktok"></i> <span data-key="tiktok">TikTok</span> <i class="fas fa-external-link-alt" style="font-size: 0.8rem; opacity: 0.7;"></i>
            </a>
            <a href="tel:+201101234892" class="btn btn-phone">
                <i class="fas fa-phone-alt"></i> <span data-key="phone1">📞 01101234892</span>
            </a>
            <a href="tel:+201212200662" class="btn btn-phone">
                <i class="fas fa-mobile-alt"></i> <span data-key="phone2">📱 01212200662</span>
            </a>
        </div>
        <div class="footer">
            <i class="fas fa-hand-pointer"></i> <span data-key="footer">اضغط على أي زر للتواصل</span>
        </div>
    </div>

    <!-- مودال تكبير الصورة -->
    <div id="imageModal" class="modal">
        <div class="close-modal" id="closeModalBtn">&times;</div>
        <div class="modal-content">
            <img id="modalImg" src="" alt="صورة مكبرة">
        </div>
    </div>

    <script>
        // بيانات المجالات (احترافية مع أيقونات واضحة)
        const fieldsData = {
            ar: [
                { icon: "fas fa-microchip", name: "مهندس IT" },
                { icon: "fas fa-code", name: "مبرمج (Python / Web)" },
                { icon: "fas fa-mobile-alt", name: "صيانة هواتف متقدمة" },
                { icon: "fas fa-robot", name: "مشاريع أردوينو و IoT" }
            ],
            en: [
                { icon: "fas fa-microchip", name: "IT Engineer" },
                { icon: "fas fa-code", name: "Programmer (Python / Web)" },
                { icon: "fas fa-mobile-alt", name: "Advanced Mobile Repair" },
                { icon: "fas fa-robot", name: "Arduino & IoT Projects" }
            ]
        };

        // الترجمات الكاملة
        const translations = {
            ar: {
                theme: "داكن",
                langBtn: "English",
                name: "م.يوسف غريب قميح",
                bio: "IT Engineer | مبرمج | تقني محترف",
                instagram: "انستجرام",
                telegram: "تيليجرام",
                facebook: "فيسبوك",
                whatsapp: "واتساب",
                tiktok: "تيك توك",
                phone1: "📞 01101234892",
                phone2: "📱 01212200662",
                footer: "اضغط على أي زر للتواصل"
            },
            en: {
                theme: "Dark",
                langBtn: "العربية",
                name: "Eg.Yossef Gharib Komuh",
                bio: "IT Engineer | Programmer | Tech Expert",
                instagram: "Instagram",
                telegram: "Telegram",
                facebook: "Facebook",
                whatsapp: "WhatsApp",
                tiktok: "TikTok",
                phone1: "📞 01101234892",
                phone2: "📱 01212200662",
                footer: "Tap any button to connect"
            }
        };

        let currentLang = 'ar';
        let currentTheme = 'dark';

        // عناصر المودال
        const modal = document.getElementById('imageModal');
        const modalImg = document.getElementById('modalImg');
        const avatar = document.getElementById('avatarImg');
        const closeModalBtn = document.getElementById('closeModalBtn');

        // فتح المودال عند النقر على الصورة
        avatar.addEventListener('click', function() {
            modal.style.display = 'flex';
            modalImg.src = avatar.src; // استخدام نفس مصدر الصورة
            // منع تمرير الصفحة الخلفية
            document.body.style.overflow = 'hidden';
        });

        // إغلاق المودال عند النقر على X أو خارج الصورة
        function closeModal() {
            modal.style.display = 'none';
            document.body.style.overflow = '';
        }

        closeModalBtn.addEventListener('click', closeModal);
        modal.addEventListener('click', function(e) {
            // إذا تم النقر على الخلفية (المودال نفسه وليس على المحتوى الداخلي)
            if (e.target === modal) {
                closeModal();
            }
        });

        // إغلاق المودال عند الضغط على زر Escape
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape' && modal.style.display === 'flex') {
                closeModal();
            }
        });

        function renderFields(lang) {
            const container = document.getElementById('fieldsContainer');
            if (!container) return;
            const fields = fieldsData[lang];
            container.innerHTML = '';
            fields.forEach(field => {
                const div = document.createElement('div');
                div.className = 'field-item';
                div.innerHTML = `<i class="${field.icon}"></i> <span>${field.name}</span>`;
                container.appendChild(div);
            });
        }

        function updateThemeText() {
            const themeSpan = document.querySelector('#themeToggle span');
            if (!themeSpan) return;
            if (currentTheme === 'light') {
                themeSpan.innerText = (currentLang === 'ar' ? 'فاتح' : 'Light');
            } else {
                themeSpan.innerText = (currentLang === 'ar' ? 'داكن' : 'Dark');
            }
        }

        function setLanguage(lang) {
            currentLang = lang;
            const t = translations[lang];
            // تحديث كل العناصر التي تحمل data-key
            document.querySelectorAll('[data-key]').forEach(el => {
                const key = el.getAttribute('data-key');
                if (t[key]) el.innerText = t[key];
            });
            // تحديث الاسم والوصف
            document.getElementById('name').innerText = t.name;
            document.getElementById('bio').innerText = t.bio;
            // تحديث المجالات
            renderFields(lang);
            // تغيير اتجاه الصفحة
            document.documentElement.setAttribute('dir', lang === 'ar' ? 'rtl' : 'ltr');
            document.documentElement.setAttribute('lang', lang);
            // تحديث نص زر اللغة
            const langToggleSpan = document.querySelector('#langToggle span');
            if (langToggleSpan) langToggleSpan.innerText = (lang === 'ar' ? 'English' : 'العربية');
            // تحديث نص الثيم حسب اللغة الجديدة
            updateThemeText();
        }

        function setTheme(theme) {
            currentTheme = theme;
            if (theme === 'light') {
                document.body.classList.add('light');
                const themeIcon = document.querySelector('#themeToggle i');
                if (themeIcon) themeIcon.className = 'fas fa-sun';
            } else {
                document.body.classList.remove('light');
                const themeIcon = document.querySelector('#themeToggle i');
                if (themeIcon) themeIcon.className = 'fas fa-moon';
            }
            updateThemeText();
        }

        // إضافة مستمعي الأحداث
        document.getElementById('themeToggle').addEventListener('click', () => {
            const newTheme = currentTheme === 'dark' ? 'light' : 'dark';
            setTheme(newTheme);
        });
        
        document.getElementById('langToggle').addEventListener('click', () => {
            const newLang = currentLang === 'ar' ? 'en' : 'ar';
            setLanguage(newLang);
        });

        // التهيئة الافتراضية
        setLanguage('ar');
        setTheme('dark');

        // إضافة تأثير صغير للروابط الخارجية (اختياري)
        const allBtns = document.querySelectorAll('.btn');
        allBtns.forEach(btn => {
            btn.addEventListener('click', function(e) {
                this.style.transform = 'scale(0.98)';
                setTimeout(() => { this.style.transform = ''; }, 150);
            });
        });
    </script>
</body>
</html>
