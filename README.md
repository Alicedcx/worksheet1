# worksheet1<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>杨馨漪 · 个人主页</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background: #f4f7fb;
            line-height: 1.5;
            color: #1e2b3c;
            padding: 2rem 1rem;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .container {
            max-width: 880px;
            width: 100%;
            background: white;
            border-radius: 28px;
            box-shadow: 0 20px 35px -8px rgba(0, 0, 0, 0.08), 0 5px 15px -6px rgba(0, 0, 0, 0.03);
            padding: 2.2rem 2rem;
            transition: box-shadow 0.2s;
        }
        .header-row {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
        }
        .name-title {
            font-size: 2.3rem;
            font-weight: 650;
            letter-spacing: -0.02em;
            background: linear-gradient(145deg, #1f3a5f, #2b4c7c);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            line-height: 1.2;
        }
        .lang-switch {
            display: flex;
            gap: 0.6rem;
            background: #edf2f9;
            padding: 0.3rem;
            border-radius: 48px;
        }
        .lang-btn {
            border: none;
            background: transparent;
            font-size: 0.95rem;
            font-weight: 520;
            padding: 0.5rem 1.3rem;
            border-radius: 40px;
            cursor: pointer;
            color: #3b4e6b;
            transition: all 0.15s;
            border: 1px solid transparent;
        }
        .lang-btn.active {
            background: white;
            color: #14273e;
            box-shadow: 0 4px 12px -5px rgba(0, 0, 0, 0.15);
            border-color: #cbd6e6;
            font-weight: 580;
        }
        .lang-btn:hover {
            background: #dfe7f2;
        }
        .section-card {
            background: #ffffff;
            border: 1px solid #e9eef4;
            border-radius: 24px;
            padding: 1.6rem 1.8rem;
            margin-bottom: 2rem;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.01);
            transition: border 0.2s;
        }
        .section-card:hover {
            border-color: #b9cae0;
        }
        .section-title {
            font-size: 1.4rem;
            font-weight: 620;
            margin-bottom: 1.2rem;
            padding-bottom: 0.4rem;
            border-bottom: 3px solid #e3eaf3;
            letter-spacing: -0.01em;
            color: #1d3452;
        }
        .info-grid {
            display: flex;
            flex-direction: column;
            gap: 0.9rem;
        }
        .info-item {
            font-size: 1.05rem;
            display: flex;
            align-items: baseline;
            flex-wrap: wrap;
        }
        .bio-text {
            font-size: 1.06rem;
            color: #253c5c;
            line-height: 1.65;
            padding: 0.2rem 0;
        }
        .list-bullet {
            list-style: none;
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem 1.2rem;
            margin-top: 0.3rem;
        }
        .list-bullet li {
            background: #eef3fc;
            padding: 0.4rem 1.3rem;
            border-radius: 40px;
            font-size: 1.0rem;
            font-weight: 500;
            color: #1e3a5f;
            border: 1px solid #d0ddee;
        }
        .edu-list {
            list-style: none;
        }
        .edu-list li {
            background: #f9fcff;
            padding: 0.8rem 0 0.8rem 1.8rem;
            border-radius: 0 20px 20px 0;
            border-left: 4px solid #a7bbd9;
            margin-bottom: 1.2rem;
            font-size: 1.04rem;
            color: #1c314b;
            font-weight: 470;
            padding-right: 1rem;
            line-height: 1.5;
        }
        .edu-list li:last-child {
            margin-bottom: 0;
        }
        .footer-updated {
            margin-top: 1.8rem;
            text-align: right;
            font-size: 0.95rem;
            color: #5e728b;
            border-top: 1px dashed #d2deec;
            padding-top: 1.3rem;
            font-style: italic;
        }
        .email-link, .phone-text {
            color: #1f3f6e;
            text-decoration: none;
            border-bottom: 1px dotted #8fa2c2;
        }
        .email-link:hover {
            border-bottom: 1px solid #1f3f6e;
        }
        @media (max-width: 550px) {
            .container { padding: 1.5rem 1.2rem; }
            .name-title { font-size: 2rem; }
            .lang-btn { padding: 0.4rem 1rem; }
            .section-card { padding: 1.2rem; }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- 头部：姓名 + 中英切换按钮 -->
        <div class="header-row">
            <span class="name-title" id="display-name">杨馨漪</span>
            <div class="lang-switch">
                <button class="lang-btn active" id="btn-zh" data-lang="zh">中文</button>
                <button class="lang-btn" id="btn-en" data-lang="en">English</button>
            </div>
        </div>

        <!-- 基本信息卡片 (含电话) -->
        <div class="section-card">
            <div class="section-title" id="basic-title">基本信息</div>
            <div class="info-grid">
                <div class="info-item" id="name-display">姓名：杨馨漪</div>
                <div class="info-item" id="school-display">学校/专业：华东政法大学 商学院</div>
                <div class="info-item" id="interest-display">研究兴趣/职业方向：会计 / 商业分析</div>
                <div class="info-item" id="email-display">邮箱：17717458857@163.com</div>
                <div class="info-item" id="phone-display">电话：177 1745 8857</div>
            </div>
        </div>

        <!-- 个人简介卡片 -->
        <div class="section-card">
            <div class="section-title" id="bio-title">个人简介</div>
            <div class="bio-text" id="bio-display">
                华东政法大学商学院大一学生，平均绩点3.68。担任商学院团委团校副部长，具备良好的沟通协作与团队领导潜力。积极参加社会实践活动，包括香港名企访问项目、巴金故居志愿服务等。具备扎实的英语能力（六级548分）和会计基础知识，熟练使用Office软件，能够独立完成课题研究。业余爱好摄影和滑冰，注重全面发展。
            </div>
        </div>

        <!-- 技能卡片 (硬技能) -->
        <div class="section-card">
            <div class="section-title" id="skills-title">技能</div>
            <ul class="list-bullet" id="skills-list">
                <!-- 动态JS填充，此处占位会被覆盖 -->
                <li>英语六级 (548分)</li>
                <li>初级会计资格</li>
                <li>Microsoft Office</li>
                <li>独立课题研究</li>
            </ul>
        </div>

        <!-- 教育经历 / 课程经历卡片 -->
        <div class="section-card">
            <div class="section-title" id="education-title">教育经历</div>
            <ul class="edu-list" id="education-list">
                <li>华东政法大学 商学院 经济学类 (2024.09 – 至今) · 平均绩点 3.68/4.0</li>
                <li>相关课程：微观经济学、会计学、高等数学、线性代数、大学英语</li>
            </ul>
        </div>

        <!-- 最后更新日期 -->
        <div class="footer-updated" id="last-updated-display">
            最后更新：2026年3月16日
        </div>
    </div>

    <script>
        (function() {
            // ================= 中英文内容配置 (基于杨馨漪简历) =================
            const translations = {
                zh: {
                    // 头部姓名
                    nameHead: '杨馨漪',
                    // 基本信息各项
                    nameDisplay: '姓名：杨馨漪',
                    schoolDisplay: '学校/专业：华东政法大学 商学院',
                    interestDisplay: '研究兴趣/职业方向：会计 / 商业分析',
                    emailDisplay: '邮箱：17717458857@163.com',
                    phoneDisplay: '电话：177 1745 8857',
                    // 个人简介
                    bioDisplay: '华东政法大学商学院大一学生，平均绩点3.68。担任商学院团委团校副部长，具备良好的沟通协作与团队领导潜力。积极参加社会实践活动，包括香港名企访问项目、巴金故居志愿服务等。具备扎实的英语能力（六级548分）和会计基础知识，熟练使用Office软件，能够独立完成课题研究。业余爱好摄影和滑冰，注重全面发展。',
                    // 技能列表 (数组)
                    skillsList: ['英语六级 (548分)', '初级会计资格', 'Microsoft Office', '独立课题研究'],
                    // 教育经历列表 (两个条目)
                    eduList: [
                        '华东政法大学 商学院 经济学类 (2024.09 – 至今) · 平均绩点 3.68/4.0',
                        '相关课程：微观经济学、会计学、高等数学、线性代数、大学英语'
                    ],
                    // 各模块标题
                    basicTitle: '基本信息',
                    bioTitle: '个人简介',
                    skillsTitle: '技能',
                    educationTitle: '教育经历 / 课程经历',
                    lastUpdated: '最后更新：2026年3月16日'
                },
                en: {
                    nameHead: 'Yang Xinyi',
                    nameDisplay: 'Name: Yang Xinyi',
                    schoolDisplay: 'University/Major: East China University of Political Science and Law, Business School',
                    interestDisplay: 'Research Interest / Career Focus: Accounting / Business Analysis',
                    emailDisplay: 'Email: 17717458857@163.com',
                    phoneDisplay: 'Phone: +86 177 1745 8857',
                    bioDisplay: 'First-year student at East China University of Political Science and Law, Business School, with a GPA of 3.68/4.0. Served as Vice Minister of the Youth League Committee\'s League School, demonstrating strong communication, collaboration, and leadership potential. Actively participated in social practices, including a Hong Kong business visit program and volunteer work at Ba Jin\'s Former Residence. Proficient in English (CET-6 548), with foundational accounting knowledge and Microsoft Office skills. Capable of independent research. Hobbies include photography and ice skating, embracing a well-rounded development.',
                    skillsList: ['CET-6 (548)', 'Preliminary Accounting Qualification', 'Microsoft Office', 'Independent Research'],
                    eduList: [
                        'East China University of Political Science and Law, Business School (Sept 2024 – Present) · GPA 3.68/4.0',
                        'Relevant courses: Microeconomics, Accounting, Calculus, Linear Algebra, College English'
                    ],
                    basicTitle: 'Basic Information',
                    bioTitle: 'Biography',
                    skillsTitle: 'Skills',
                    educationTitle: 'Education / Coursework',
                    lastUpdated: 'Last Updated: March 16, 2026'
                }
            };

            // ----- DOM 元素 -----
            const nameHeadEl = document.getElementById('display-name');
            const nameDisplayEl = document.getElementById('name-display');
            const schoolDisplayEl = document.getElementById('school-display');
            const interestDisplayEl = document.getElementById('interest-display');
            const emailDisplayEl = document.getElementById('email-display');
            const phoneDisplayEl = document.getElementById('phone-display');   // 新增电话
            const bioDisplayEl = document.getElementById('bio-display');
            const skillsListEl = document.getElementById('skills-list');
            const eduListEl = document.getElementById('education-list');
            const basicTitleEl = document.getElementById('basic-title');
            const bioTitleEl = document.getElementById('bio-title');
            const skillsTitleEl = document.getElementById('skills-title');
            const educationTitleEl = document.getElementById('education-title');
            const lastUpdatedEl = document.getElementById('last-updated-display');

            // 按钮
            const btnZh = document.getElementById('btn-zh');
            const btnEn = document.getElementById('btn-en');

            let currentLang = 'zh';   // 默认中文

            // 渲染函数：根据语言更新所有内容
            function renderPage(lang) {
                const t = translations[lang];
                if (!t) return;

                // 头部姓名
                nameHeadEl.textContent = t.nameHead;

                // 基本信息行
                nameDisplayEl.textContent = t.nameDisplay;
                schoolDisplayEl.textContent = t.schoolDisplay;
                interestDisplayEl.textContent = t.interestDisplay;
                emailDisplayEl.textContent = t.emailDisplay;
                phoneDisplayEl.textContent = t.phoneDisplay;

                // 个人简介
                bioDisplayEl.textContent = t.bioDisplay;

                // 模块标题
                basicTitleEl.textContent = t.basicTitle;
                bioTitleEl.textContent = t.bioTitle;
                skillsTitleEl.textContent = t.skillsTitle;
                educationTitleEl.textContent = t.educationTitle;
                lastUpdatedEl.textContent = t.lastUpdated;

                // 技能列表 (重新填充)
                skillsListEl.innerHTML = '';
                t.skillsList.forEach(skill => {
                    const li = document.createElement('li');
                    li.textContent = skill;
                    skillsListEl.appendChild(li);
                });

                // 教育经历列表
                eduListEl.innerHTML = '';
                t.eduList.forEach(edu => {
                    const li = document.createElement('li');
                    li.textContent = edu;
                    eduListEl.appendChild(li);
                });

                // 切换按钮 active 样式
                if (lang === 'zh') {
                    btnZh.classList.add('active');
                    btnEn.classList.remove('active');
                } else {
                    btnEn.classList.add('active');
                    btnZh.classList.remove('active');
                }
            }

            // 绑定点击事件
            btnZh.addEventListener('click', function() {
                if (currentLang === 'zh') return;
                currentLang = 'zh';
                renderPage('zh');
            });

            btnEn.addEventListener('click', function() {
                if (currentLang === 'en') return;
                currentLang = 'en';
                renderPage('en');
            });

            // 初始渲染 (中文)
            renderPage('zh');

            // 若想自定义个人信息，直接修改上方 translations 对象内的文本即可
        })();
    </script>

    <!-- 本页面完全基于简历内容生成，符合GitHub Pages部署要求，无需任何软件 -->
</body>
</html>
