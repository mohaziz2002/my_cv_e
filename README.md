# Personal CV (GitHub Pages)

Bilingual personal résumé site: **Arabic** (`index.html`) and **English** (`index-en.html`), built with HTML, Tailwind CSS, and Chart.js.

## Live site

| Language | URL |
|----------|-----|
| Arabic (default) | [https://mohaziz2002.github.io/my_cv/](https://mohaziz2002.github.io/my_cv/) |
| English | [https://mohaziz2002.github.io/my_cv/index-en.html](https://mohaziz2002.github.io/my_cv/index-en.html) |

## Repository layout

```
my_cv/
├── index.html          # Arabic CV (main entry for Pages)
├── index-en.html       # English CV
└── README.md           # This file (copy to repo root when you publish)
```

Optional helper (not required at runtime):

- `snippet-link-in-arabic-page.html` — HTML snippets to paste into `index.html` for an **English** link in the nav and mobile menu.

## Tech stack

- [Tailwind CSS](https://tailwindcss.com/) (CDN)
- [Chart.js](https://www.chartjs.org/) (skills doughnut chart)
- [Google Fonts](https://fonts.google.com/) — Cairo (Arabic), Inter (English)

## Deploy on GitHub Pages

1. Push `index.html` and `index-en.html` to the **root** of the repository (usually `main`).
2. In the repo: **Settings → Pages → Build and deployment → Source**: *Deploy from a branch*.
3. Choose branch **`main`** and folder **`/ (root)`**, then save.
4. After a minute, the site is available at `https://<username>.github.io/<repo>/`.

## Cross-links between languages

- `index-en.html` links back to **`index.html`** (“العربية”).
- Add links from Arabic to English using the snippets in `snippet-link-in-arabic-page.html`.

## Local preview

Open `index.html` or `index-en.html` in a browser, or serve the folder with any static server.

## Author

**Mohammed Zaki** — Computer Engineering student; volunteer and student-union roles as listed on the site.

---

### ملخص عربي سريع

- انسخ محتويات مجلد `my-cv-english-for-github` إلى جذر مستودعك على GitHub.
- ضع `index-en.html` بجانب `index.html`.
- أضف رابط **English** من ملف `snippet-link-in-arabic-page.html` داخل الصفحة العربية.




























<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>السيرة الذاتية | محمد زكي</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700&display=swap" rel="stylesheet">
    
    <style>
        body {
            font-family: 'Cairo', sans-serif;
        }
        .timeline-item::before {
            content: '';
            position: absolute;
            top: 1rem;
            right: -0.8rem;
            width: 1.5rem;
            height: 1.5rem;
            border-radius: 50%;
            background-color: #dc2626; /* red-600 */
            border: 3px solid #fee2e2; /* red-100 */
        }
    </style>
</head>
<body class="bg-gray-50 text-gray-800">

    <header id="home" class="bg-white shadow-md sticky top-0 z-50">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <div class="text-xl font-bold text-red-600">محمد زكي</div>
            <div class="hidden md:flex space-x-8 space-x-reverse">
                <a href="#about" class="nav-link text-gray-600 hover:text-red-600 transition duration-300">عني</a>
                <a href="#education" class="nav-link text-gray-600 hover:text-red-600 transition duration-300">المؤهل الأكاديمي</a>
                <a href="#experience" class="nav-link text-gray-600 hover:text-red-600 transition duration-300">الخبرات</a>
                <a href="#skills" class="nav-link text-gray-600 hover:text-red-600 transition duration-300">المهارات والدورات</a>
            </div>
            <div class="md:hidden">
                <button id="menu-btn" class="text-gray-600 focus:outline-none">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
                    </svg>
                </button>
            </div>
        </nav>
        <div id="mobile-menu" class="hidden md:hidden">
            <a href="#about" class="nav-link block py-2 px-4 text-sm hover:bg-red-50">عني</a>
            <a href="#education" class="nav-link block py-2 px-4 text-sm hover:bg-red-50">المؤهل الأكاديمي</a>
            <a href="#experience" class="nav-link block py-2 px-4 text-sm hover:bg-red-50">الخبرات</a>
            <a href="#skills" class="nav-link block py-2 px-4 text-sm hover:bg-red-50">المهارات والدورات</a>
        </div>
    </header>

    <main class="container mx-auto px-6">

        <section id="about" class="pt-24 pb-16">
             <div class="container mx-auto px-6 flex flex-col md:flex-row items-center justify-center gap-10 md:gap-16">
                <div class="flex-shrink-0">
                    <img src="photo.jpg" onerror="this.src='https://placehold.co/400x400/fee2e2/dc2626?text=صورة+شخصية'" alt="صورة محمد زكي الشخصية" class="w-48 h-48 rounded-full object-cover border-4 border-red-200 shadow-xl">
                </div>
                <div class="text-center md:text-right mt-6 md:mt-0">
                    <h1 class="text-4xl md:text-5xl font-bold text-red-700 mb-8">محمد زكي</h1>
                    <p class="font-semibold text-red-800 bg-red-100 rounded-full inline-block px-6 py-2">مرشح الهيئة الادارية لمنصب مسؤول الفروع</p>
                </div>
            </div>
            <div class="max-w-3xl mx-auto mt-16 text-center">
                 <h2 class="text-2xl font-semibold text-gray-700 mb-4">ملخص شخصي</h2>
                 <p class="text-gray-600 leading-relaxed">
                     أنا طالب طموح حريص على تحقيق كل ما لدي من أهداف. لدي شغف بالعمل التطوعي واكتساب مهارات جديدة ومتنوعة تساهم في تطويري الشخصي والمجتمعي، وأؤمن بأهمية المشاركة الفعالة في بناء مجتمع طلابي مترابط وفعال
                 </p>
             </div>
        </section>

        <section id="education" class="py-16 bg-white rounded-2xl shadow-sm border border-gray-100 mb-16 px-6 md:px-12">
            <h2 class="text-3xl font-bold text-center text-gray-800 mb-12">المؤهل الأكاديمي</h2>
            <div class="max-w-4xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- Academic Item 1 -->
                <div class="bg-gray-50 p-6 sm:p-8 rounded-xl border border-gray-200 hover:shadow-md transition-shadow duration-300 relative overflow-hidden group">
                    <div class="absolute top-0 right-0 w-2 h-full bg-red-500 group-hover:bg-red-600 transition-colors"></div>
                    <div class="flex flex-col xl:flex-row justify-between items-start xl:items-center mb-2 gap-4">
                        <div class="w-full">
                            <h3 class="text-xl font-bold text-gray-800 leading-relaxed block">بكالوريوس هندسة حاسوب</h3>
                            <p class="text-gray-600 font-medium mt-1">جامعة كارابوك</p>
                        </div>
                        <span class="inline-block bg-red-100 text-red-700 text-sm font-semibold px-4 py-1.5 rounded-full whitespace-nowrap self-start">2023 - مستمر</span>
                    </div>
                </div>

                <!-- Academic Item 2 -->
                <div class="bg-gray-50 p-6 sm:p-8 rounded-xl border border-gray-200 hover:shadow-md transition-shadow duration-300 relative overflow-hidden group">
                    <div class="absolute top-0 right-0 w-2 h-full bg-red-500 group-hover:bg-red-600 transition-colors"></div>
                    <div class="flex flex-col xl:flex-row justify-between items-start xl:items-center mb-2 gap-4">
                        <div class="w-full">
                            <h3 class="text-xl font-bold text-gray-800 leading-relaxed block">بكالوريوس علاقات دولية</h3>
                            <p class="text-gray-600 font-medium mt-1">جامعة الأناضول</p>
                        </div>
                        <span class="inline-block bg-red-100 text-red-700 text-sm font-semibold px-4 py-1.5 rounded-full whitespace-nowrap self-start">2025 - مستمر</span>
                    </div>
                </div>
            </div>
        </section>

        <section id="experience" class="py-16">
            <h2 class="text-3xl font-bold text-center text-gray-800 mb-12">مسيرة العمل التطوعي</h2>
            <div class="relative max-w-2xl mx-auto border-r-2 border-red-200">
                <div class="experience-data"></div>
            </div>
        </section>

        <section id="skills" class="py-16">
            <h2 class="text-3xl font-bold text-center text-gray-800 mb-12">المهارات والمؤهلات</h2>
            <p class="text-center text-gray-600 max-w-2xl mx-auto mb-12 leading-relaxed">
                في هذا القسم، استعراض للمؤهلات والدورات التدريبية التي حصلت عليها. الرسم البياني يوضح توزيع هذه المهارات على مجالات مختلفة، مما يعطي فكرة سريعة عن الكفاءات الأساسية. يمكنكم الاطلاع على تفاصيل كل دورة في البطاقات أدناه.
            </p>
            <div class="flex flex-col lg:flex-row items-center justify-center gap-12">
                <div class="w-full lg:w-1/3">
                    <div class="chart-container relative h-80 w-full max-w-sm mx-auto">
                        <canvas id="skillsChart"></canvas>
                    </div>
                </div>
                <div class="w-full lg:w-2/3 grid grid-cols-1 md:grid-cols-2 gap-6 skills-data">
                </div>
            </div>
        </section>

    </main>
    
    <footer class="bg-white mt-16 py-6 border-t border-gray-200">
        <div class="container mx-auto px-6 text-center text-gray-500">
            <p>&copy; 2026  MOHAMMED AZIZ </p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const experienceData = [
                { year: '2026 - مستمر', title: 'مستشار أكاديمية رواد للتدريب والتأهيل', org: 'اتحاد الطلاب اليمنيين في تركيا، فرع كارابوك' },
                { year: '2025 - مستمر', title: 'رئيس لجنة الرقابة والتقييم', org: 'اتحاد الطلاب اليمنيين في تركيا، فرع كارابوك' },
                { year: '2025', title: 'قائد مجموعة، برنامج الذكاء الاصطناعي', org: 'اتحاد الطلاب اليمنيين، فرع سكاريا' },
                { year: '2023-2024' , title: 'أمين عام ', org: 'اتحاد الطلاب اليمنيين في تركيا، فرع كارابوك' },
                { year: '2023-2024', title: 'رئيس أكاديمية رواد للتدريب والتأهيل', org: 'اتحاد الطلاب اليمنيين في تركيا، فرع كارابوك' },
                { year: '2023-2024', title: 'مدرس لغة تركية، برنامج إتقان', org: 'اتحاد الطلاب اليمنيين في تركيا، فرع كارابوك' },
                { year: '2022-مستمر', title: 'متطوع في لجان متعددة (الاقامات ، الجامعة ، الصحية ، الاستقبال ، التسكين)', org: 'اتحاد الطلاب اليمنيين في تركيا، فرعي كارابوك وسكاريا' },
                { year: '2022-2023', title: 'عضو لجنة المتابعة والتدقيق للمنح التركية', org: 'اتحاد الطلاب اليمنيين في تركيا، فرع سكاريا' },
                { year: '2022-2023', title: 'مدرس اللغتين التركية والإنجليزية', org: 'اتحاد الطلاب اليمنيين في تركيا، فرع سكاريا' }
            ];

            const skillsData = [
                { category: 'لغات', title: 'دبلوم في اللغة الإنجليزية', source: 'معهد مالي' },
                { category: 'لغات', title: 'دبلوم في اللغة التركية', source: 'جامعة سكاريا للعلوم التطبيقية' },
                { category: 'تقني', title: 'دبلوم في الرخصة الدولية لقيادة الحاسوب', source: 'جامعة العلوم والتكنولوجيا' },
                { category: 'إنساني', title: 'دورة في الإسعافات الأولية', source: 'معهد ليدرشيب' },
                { category: 'إنساني', title: 'إدارة الكوارث (برنامج اسفير)', source: 'معهد ليدرشيب' },
                { category: 'إداري', title: 'دورة في التسويق الإلكتروني', source: 'اتحاد الطلاب اليمنيين، اسطنبول' },
                { category: 'إداري', title: 'دورة في إدارة المشاريع الصغيرة', source: 'معهد ليدرشيب' },
                { category: 'إنساني', title: 'تدريب عملي في الاسعافات الاولية', source: 'معهد عالمنا الجديد' },
                { category: 'إداري', title: 'ورشة في العمل النقابي', source: 'اتحاد الطلبة اليمنيين في تركيا فرع كارابوك' }
            ];
            
            const experienceContainer = document.querySelector('.experience-data');
            experienceData.forEach(item => {
                const div = document.createElement('div');
                div.className = 'timeline-item mb-8 mr-16 md:mr-32 pl-4 relative';
                div.innerHTML = `
                    <div class="absolute -right-20 md:-right-28 top-2 text-xs md:text-sm font-semibold text-red-600 bg-red-100 rounded-md px-2 py-1 text-center min-w-[70px] md:min-w-[90px]">${item.year}</div>
                    <div class="bg-white p-4 rounded-lg shadow-sm border border-gray-200 hover:shadow-md transition-shadow">
                        <h3 class="text-lg font-semibold text-gray-800">${item.title}</h3>
                        <p class="text-sm text-gray-500 mt-1">${item.org}</p>
                    </div>
                `;
                experienceContainer.appendChild(div);
            });

            const skillsContainer = document.querySelector('.skills-data');
            skillsData.forEach(item => {
                const div = document.createElement('div');
                div.className = 'bg-white p-6 rounded-lg shadow-sm border border-gray-200 transition-transform transform hover:-translate-y-1 hover:shadow-md hover:border-red-100';
                div.innerHTML = `
                    <h3 class="font-semibold text-lg text-gray-800">${item.title}</h3>
                    <p class="text-gray-500 mt-2 text-sm flex items-center">
                        <svg class="w-4 h-4 mr-1 text-red-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"></path></svg>
                        <span class="mr-1">${item.source}</span>
                    </p>
                `;
                skillsContainer.appendChild(div);
            });

            const skillCategories = {};
            skillsData.forEach(skill => {
                if (skillCategories[skill.category]) {
                    skillCategories[skill.category]++;
                } else {
                    skillCategories[skill.category] = 1;
                }
            });
            
            const ctx = document.getElementById('skillsChart').getContext('2d');
            new Chart(ctx, {
                type: 'doughnut',
                data: {
                    labels: Object.keys(skillCategories).map(cat => {
                        const translations = {'لغات': 'لغات', 'تقني': 'مهارات تقنية', 'إنساني': 'عمل إنساني', 'إداري': 'مهارات إدارية'};
                        return translations[cat] || cat;
                    }),
                    datasets: [{
                        label: 'تصنيف المهارات',
                        data: Object.values(skillCategories),
                        backgroundColor: [
                            '#ef4444', // red-500
                            '#f87171', // red-400
                            '#fca5a5', // red-300
                            '#fecaca'  // red-200
                        ],
                        borderColor: '#ffffff',
                        borderWidth: 3,
                        hoverOffset: 4
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            position: 'bottom',
                            labels: {
                                font: {
                                    family: "'Cairo', sans-serif",
                                    size: 14,
                                    weight: '600'
                                },
                                color: '#374151',
                                padding: 20
                            }
                        },
                        tooltip: {
                            backgroundColor: 'rgba(255, 255, 255, 0.9)',
                            titleColor: '#1f2937',
                            bodyColor: '#4b5563',
                            borderColor: '#e5e7eb',
                            borderWidth: 1,
                            bodyFont: {
                                family: "'Cairo', sans-serif",
                                size: 14
                            },
                            titleFont: {
                                family: "'Cairo', sans-serif",
                                size: 14,
                                weight: 'bold'
                            },
                            padding: 10,
                            boxPadding: 4
                        }
                    },
                    cutout: '70%'
                }
            });

            const menuBtn = document.getElementById('menu-btn');
            const mobileMenu = document.getElementById('mobile-menu');
            menuBtn.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
            });
            
            document.querySelectorAll('a.nav-link').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80, // Adjusted offset for sticky header
                            behavior: 'smooth'
                        });
                        if (!mobileMenu.classList.contains('hidden')) {
                            mobileMenu.classList.add('hidden');
                        }
                    }
                });
            });
        });
    </script>
</body>
</html>