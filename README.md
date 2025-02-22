<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منصة مدارس الجمهورية</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            direction: rtl;
            text-align: right;
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
        }
        header {
            background-color: #004080;
            color: white;
            padding: 20px;
            text-align: center;
            position: relative;
        }
        .language-switcher {
            position: absolute;
            top: 20px;
            left: 20px;
        }
        .language-switcher button {
            background-color: #003366;
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            border-radius: 5px;
        }
        nav {
            background-color: #003366;
            padding: 15px;
            display: flex;
            justify-content: center;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin: 15px;
            padding: 10px;
            font-weight: bold;
        }
        .container {
            padding: 20px;
        }
        .login-form, .register-form, .application-form {
            background-color: white;
            padding: 20px;
            margin: 20px auto;
            width: 300px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px #ccc;
        }
        .login-form input, .register-form input, .application-form input, .application-form select {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .login-form button, .register-form button, .application-form button {
            width: 100%;
            padding: 10px;
            background-color: #004080;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .login-form button:hover, .register-form button:hover, .application-form button:hover {
            background-color: #003366;
        }
        .scholarships, .curriculum, .profile, .school-account {
            background-color: #e6f2ff;
            padding: 20px;
            margin-top: 20px;
            border-radius: 10px;
        }
        .scholarships ul, .curriculum ul {
            list-style-type: none;
            padding: 0;
        }
        .scholarships li, .curriculum li {
            padding: 8px 0;
        }
        .scholarship-detail, .curriculum-detail {
            background-color: white;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 0 10px #ccc;
            margin-top: 20px;
            display: none;
        }
        .scholarship-detail h3, .curriculum-detail h3 {
            margin-bottom: 10px;
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="language-switcher">
            <button onclick="changeLanguage('ar')">العربية</button>
            <button onclick="changeLanguage('en')">English</button>
        </div>
        <h1>منصة مدارس الجمهورية</h1>
        <p>إدارة المدارس والمناهج والمنح الدراسية</p>
    </header>

    <!-- Navbar -->
    <nav>
        <a href="#" onclick="showMainMenu()">الرئيسية</a>
        <a href="#" onclick="showSchoolsPage()">المدارس</a>
        <a href="#" onclick="showScholarshipsPage()">المنح الدراسية</a>
        <a href="#" onclick="showLoginPage()">تسجيل الدخول</a>
        <a href="#" onclick="showRegisterPage()">إنشاء حساب</a>
    </nav>

    <!-- Main Content -->
    <div class="container" id="mainContent">
        <h2>مرحبًا بكم في منصة مدارس الجمهورية</h2>
        <p>هذه المنصة تهدف إلى تنظيم العملية التعليمية، وإدارة المدارس، وتوفير المناهج الدراسية والمنح الدراسية للطلاب.</p>
    </div>

    <!-- Scripts -->
    <script>
        function changeLanguage(lang) {
            if (lang === 'ar') {
                document.documentElement.lang = 'ar';
                document.documentElement.dir = 'rtl';
                document.querySelector('h1').innerText = 'منصة مدارس الجمهورية';
                document.querySelector('p').innerText = 'إدارة المدارس والمناهج والمنح الدراسية';
            } else if (lang === 'en') {
                document.documentElement.lang = 'en';
                document.documentElement.dir = 'ltr';
                document.querySelector('h1').innerText = 'Republic Schools Platform';
                document.querySelector('p').innerText = 'Managing Schools, Curricula, and Scholarships';
            }
        }

        function showMainMenu() {
            document.getElementById('mainContent').innerHTML = `
                <h2>مرحبًا بكم في منصة مدارس الجمهورية</h2>
                <p>هذه المنصة تهدف إلى تنظيم العملية التعليمية، وإدارة المدارس، وتوفير المناهج الدراسية والمنح الدراسية للطلاب.</p>
            `;
        }

        function showSchoolsPage() {
            document.getElementById('mainContent').innerHTML = `
                <h2>المدارس</h2>
                <ul>
                    <li>مدرسة صنعاء الثانوية</li>
                    <li>مدرسة عدن الثانوية</li>
                    <li>مدرسة تعز الثانوية</li>
                    <li>مدرسة الحديدة الثانوية</li>
                    <li>مدرسة إب الثانوية</li>
                    <!-- يمكنك إضافة المزيد من المدارس هنا -->
                </ul>
            `;
        }

        function showScholarshipsPage() {
            document.getElementById('mainContent').innerHTML = `
                <h2>المنح الدراسية</h2>
                <ul>
                    <li><a href="#" onclick="showScholarshipDetail('chinaGov')">منح الحكومات الصينية</a></li>
                    <li><a href="#" onclick="showScholarshipDetail('chinaProvinces')">منح المقاطعات الصينية</a></li>
                    <li><a href="#" onclick="showScholarshipDetail('malaysiaBukhari')">منحة جامعة البخاري (ماليزيا)</a></li>
                    <li><a href="#" onclick="showScholarshipDetail('malaysiaPerlis')">منحة جامعة برليس (ماليزيا)</a></li>
                    <li><a href="#" onclick="showScholarshipDetail('exchangeProgram')">منح التبادل الثقافي</a></li>
                </ul>
            `;
        }

        function showLoginPage() {
            document.getElementById('mainContent').innerHTML = `
                <div class="login-form">
                    <h3>تسجيل الدخول</h3>
                    <select id="schoolSelect">
                        <option value="">اختر المدرسة</option>
                        <option value="school1">مدرسة صنعاء الثانوية</option>
                        <option value="school2">مدرسة عدن الثانوية</option>
                        <option value="school3">مدرسة تعز الثانوية</option>
                        <!-- يمكنك إضافة المزيد من المدارس هنا -->
                    </select>
                    <input type="text" placeholder="اسم المستخدم">
                    <input type="password" placeholder="كلمة المرور">
                    <button>دخول</button>
                </div>
            `;
        }

        function showRegisterPage() {
            document.getElementById('mainContent').innerHTML = `
                <div class="register-form">
                    <h3>إنشاء حساب جديد</h3>
                    <select id="schoolSelect">
                        <option value="">اختر المدرسة</option>
                        <option value="school1">مدرسة صنعاء الثانوية</option>
                        <option value="school2">مدرسة عدن الثانوية</option>
                        <option value="school3">مدرسة تعز الثانوية</option>
                        <!-- يمكنك إضافة المزيد من المدارس هنا -->
                    </select>
                    <input type="text" placeholder="الاسم الكامل">
                    <input type="email" placeholder="البريد الإلكتروني">
                    <input type="password" placeholder="كلمة المرور">
                    <button>تسجيل</button>
                </div>
            `;
        }

        function showScholarshipDetail(scholarshipType) {
            var scholarshipTitle = '';
            var scholarshipDetails = '';
            var scholarshipDeadline = '';
            var scholarshipLink = '';

            if (scholarshipType === 'chinaGov') {
                scholarshipTitle = 'منح الحكومات الصينية';
                scholarshipDetails = 'الشروط: يجب أن يكون المتقدم حاصلًا على شهادة الثانوية العامة أو ما يعادلها، مع إتقان اللغة الصينية أو الإنجليزية.';
                scholarshipDeadline = 'المواعيد: يبدأ التقديم في يناير، وآخر موعد للتقديم في مايو.';
                scholarshipLink = '<a href="http://www.csc.edu.cn" target="_blank">رابط التقديم</a>';
            } else if (scholarshipType === 'chinaProvinces') {
                scholarshipTitle = 'منح المقاطعات الصينية';
                scholarshipDetails = 'الشروط: تختلف الشروط حسب المقاطعة، ولكن عمومًا يجب أن يكون المتقدم خريجًا من المرحلة الثانوية مع إتقان اللغة الصينية أو الإنجليزية.';
                scholarshipDeadline = 'المواعيد: يختلف موعد التقديم حسب المقاطعة.';
                scholarshipLink = '<a href="http://www.csc.edu.cn" target="_blank">رابط التقديم</a>';
            } else if (scholarshipType === 'malaysiaBukhari') {
                scholarshipTitle = 'منحة جامعة البخاري (ماليزيا)';
                scholarshipDetails = 'الشروط: يجب أن يكون المتقدم قد أكمل دراسته الثانوية أو ما يعادلها، مع تقديم شهادة إجادة اللغة الإنجليزية.';
                scholarshipDeadline = 'المواعيد: يبدأ التقديم في مارس، وآخر موعد للتقديم في مايو.';
                scholarshipLink = '<a href="https://www.bukhary.edu.my" target="_blank">رابط التقديم</a>';
            } else if (scholarshipType === 'malaysiaPerlis') {
                scholarshipTitle = 'منحة جامعة برليس (ماليزيا)';
                scholarshipDetails = 'الشروط: يجب أن يكون المتقدم قد أكمل دراسته الثانوية أو ما يعادلها، مع إجادة اللغة الإنجليزية.';
                scholarshipDeadline = 'المواعيد: يبدأ التقديم في يوليو، وآخر موعد للتقديم في أغسطس.';
                scholarshipLink = '<a href="https://www.unimap.edu.my" target="_blank">رابط التقديم</a>';
            } else if (scholarshipType === 'exchangeProgram') {
                scholarshipTitle = 'منح التبادل الثقافي - وزارة التعليم العالي عدن';
                scholarshipDetails = 'الشروط: يجب أن يكون المتقدم من خريجي الثانوية العامة أو ما يعادلها. منح التبادل الثقافي تتيح للطلاب فرصة الدراسة في عدة دول تشمل الصين وروسيا وتركيا.';
                scholarshipDeadline = 'المواعيد: يبدأ التقديم عادة في شهر يوليو، وآخر موعد هو أكتوبر.';
                scholarshipLink = '<a href="http://www.mohe-aden.edu.ye" target="_blank">رابط التقديم</a>';
            }

            document.getElementById('mainContent').innerHTML = `
                <div class="scholarship-detail">
                    <h3>${scholarshipTitle}</h3>
                    <p>${scholarshipDetails}</p>
                    <p>${scholarshipDeadline}</p>
                    <p>${scholarshipLink}</p>
                    <button onclick="showScholarshipsPage()">العودة إلى المنح الدراسية</button>
                </div>
            `;
        }
    </script>

</body>
</html>
