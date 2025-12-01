<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Римское Право | В таблицах и схемах</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700;900&family=Noto+Serif:ital,wght@0,400;0,700;1,400;1,700&display=swap" rel="stylesheet">
    <style>
        :root {
            --imperial-red: #750000; /* Глубокий красный */
            --bright-red: #8f1212;
            --roman-gold: #d4af37; /* Золото */
            --laurel-green: #3a5f0b; /* Зеленый для венков */
            --marble-bg: #f9f7f2;
        }
        body {
            font-family: 'Noto Serif', serif;
            background-color: #e6e2d3;
            color: #2d2d2d;
            font-size: 17px;
            line-height: 1.6;
            /* Статичный фон Рима */
            background-image: linear-gradient(rgba(255, 252, 245, 0.94), rgba(255, 252, 245, 0.94)), url('https://upload.wikimedia.org/wikipedia/commons/d/d8/Colosseum_in_Rome-April_2009-1-_copie_2B.jpg');
            background-size: cover;
            background-attachment: fixed;
            background-position: center;
        }
        h1, h2, h3, h4, .roman-font {
            font-family: 'Cinzel', serif;
            text-transform: uppercase;
            letter-spacing: 0.05em;
        }
        /* Сайдбар */
        .sidebar-gradient {
            background: linear-gradient(180deg, var(--imperial-red) 0%, #4a0000 100%);
            border-right: 4px solid var(--roman-gold);
        }
        /* Золотые элементы */
        .text-gold { color: var(--roman-gold); }
        .border-gold { border-color: var(--roman-gold); }
        .gold-box {
            border: 2px solid var(--roman-gold);
            background: #fff;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            position: relative;
        }
        .gold-box::after {
            content: '';
            position: absolute;
            top: 4px; left: 4px; right: 4px; bottom: 4px;
            border: 1px solid #e5d39e;
            pointer-events: none;
        }
        /* Таблицы */
        .roman-table {
            width: 100%;
            border-collapse: collapse;
            font-size: 0.95rem;
        }
        .roman-table th {
            background-color: var(--imperial-red);
            color: #fff;
            padding: 12px;
            text-align: left;
            font-family: 'Cinzel', serif;
            border: 1px solid #5a0000;
        }
        .roman-table td {
            padding: 10px;
            border: 1px solid #d4c5a0;
            background-color: #fff;
        }
        .roman-table tr:nth-child(even) td {
            background-color: #faf7f0;
        }
        /* Аккордеон */
        .accordion-btn {
            width: 100%;
            text-align: left;
            background: linear-gradient(to right, #fffcf5, #f5e6cc);
            padding: 1rem;
            font-family: 'Cinzel', serif;
            font-weight: 700;
            color: var(--imperial-red);
            border: 1px solid var(--roman-gold);
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .accordion-btn:hover { background: #ffeebb; }
        .accordion-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease-out;
            background: white;
            border: 1px solid var(--roman-gold);
            border-top: none;
        }
        .accordion-content.open { max-height: 4000px; }
        .icon-rotate { transition: transform 0.3s; }
        .accordion-btn.active .icon-rotate { transform: rotate(180deg); }
        /* Схемы */
        .diagram-container { display: flex; flex-wrap: wrap; justify-content: center; gap: 1rem; margin: 1.5rem 0; }
        .diagram-node {
            background: white;
            border: 2px solid var(--imperial-red);
            padding: 1rem;
            border-radius: 4px;
            text-align: center;
            flex: 1;
            min-width: 200px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        /* Принципы */
        .principle-card {
            background: #fff;
            border-left: 5px solid var(--imperial-red);
            padding: 1rem;
            margin-bottom: 1rem;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        .latin-term { font-weight: bold; color: var(--imperial-red); font-size: 1.1rem; display: block; margin-bottom: 0.2rem; }
        .rus-def { font-style: italic; color: #444; }
        /* Скроллбар */
        ::-webkit-scrollbar { width: 10px; }
        ::-webkit-scrollbar-track { background: #2c2c2c; }
        ::-webkit-scrollbar-thumb { background: linear-gradient(var(--imperial-red), var(--roman-gold)); border-radius: 5px; }
        /* Цитаты (Стиль свитка) */
        .quote-box {
            position: relative;
            background: #fffbf0;
            border-top: 3px solid var(--roman-gold);
            border-bottom: 3px solid var(--roman-gold);
            padding: 2.5rem 2rem;
            margin: 3rem auto;
            max-width: 850px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        /* Декоративные элементы цитаты */
        .quote-box::before, .quote-box::after {
            content: "❖";
            color: var(--imperial-red);
            font-size: 1.5rem;
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
        }
        .quote-box::before { top: -14px; background: #e6e2d3; padding: 0 10px; }
        .quote-box::after { bottom: -14px; background: #e6e2d3; padding: 0 10px; }
        .quote-latin {
            font-family: 'Cinzel', serif;
            font-size: 1.3rem;
            font-weight: 600;
            color: var(--imperial-red);
            margin-bottom: 1rem;
            line-height: 1.5;
        }
        .quote-rus {
            font-family: 'Noto Serif', serif;
            font-size: 1.1rem;
            font-style: italic;
            color: #555;
            margin-bottom: 1.5rem;
            border-top: 1px solid rgba(212, 175, 55, 0.4);
            padding-top: 1rem;
            display: inline-block;
        }
        .quote-author {
            font-family: 'Cinzel', serif;
            font-size: 0.85rem;
            color: var(--roman-gold);
            font-weight: 800;
            text-transform: uppercase;
            letter-spacing: 0.1em;
        }
        /* Стиль для логотипа в сайдбаре */
        .sidebar-logo-container {
            position: relative;
            padding: 2rem 1rem;
            border-bottom: 1px solid rgba(212, 175, 55, 0.3);
            text-align: center;
        }
        .emoji-logo {
            font-size: 5rem;
            line-height: 1;
            margin-bottom: 0.5rem;
            filter: drop-shadow(0 0 10px rgba(212, 175, 55, 0.6));
            display: inline-block;
            transition: transform 0.3s;
        }
        .emoji-logo:hover { transform: scale(1.1); }     
        .sidebar-logo-text {
            font-family: 'Cinzel', serif;
            font-weight: 900;
            letter-spacing: 0.15em;
            color: white;
            text-shadow: 0 2px 4px rgba(0,0,0,0.5);
            font-size: 1.4rem;
            border-bottom: 2px solid var(--roman-gold);
            display: inline-block;
            padding-bottom: 5px;
        }
    </style>
</head>
<body class="flex flex-col md:flex-row min-h-screen">
    <!-- Сайдбар (Красный с золотом) -->
    <aside class="w-full md:w-72 sidebar-gradient text-[#f3e5ab] flex-shrink-0 flex flex-col shadow-2xl z-50">
        <div class="sidebar-logo-container">
            <!-- Эмодзи -->
            <div class="emoji-logo">🏛️</div>
            <h1 class="sidebar-logo-text roman-font">IUS ROMANUM</h1>
            <div class="text-[#d4af37] text-xs font-bold mt-1 tracking-widest">S.P.Q.R.</div>
        </div>
        <nav class="flex-1 overflow-y-auto py-4">
            <ul class="space-y-1">
                <li><a href="#intro" class="block py-3 px-6 hover:bg-[#8f1212] hover:text-white transition border-l-4 border-transparent hover:border-[#d4af37]">Введение</a></li>
                <li><a href="#chap1" class="block py-3 px-6 hover:bg-[#8f1212] hover:text-white transition border-l-4 border-transparent hover:border-[#d4af37]"><span class="font-bold w-6 inline-block">I.</span> Источники</a></li>
                <li><a href="#chap2" class="block py-3 px-6 hover:bg-[#8f1212] hover:text-white transition border-l-4 border-transparent hover:border-[#d4af37]"><span class="font-bold w-6 inline-block">II.</span> Субъекты</a></li>
                <li><a href="#chap3" class="block py-3 px-6 hover:bg-[#8f1212] hover:text-white transition border-l-4 border-transparent hover:border-[#d4af37]"><span class="font-bold w-6 inline-block">III.</span> Семья</a></li>
                <li><a href="#chap4" class="block py-3 px-6 hover:bg-[#8f1212] hover:text-white transition border-l-4 border-transparent hover:border-[#d4af37]"><span class="font-bold w-6 inline-block">IV.</span> Вещное право</a></li>
                <li><a href="#chap5" class="block py-3 px-6 hover:bg-[#8f1212] hover:text-white transition border-l-4 border-transparent hover:border-[#d4af37]"><span class="font-bold w-6 inline-block">V.</span> Обязательства</a></li>
                <li><a href="#chap6" class="block py-3 px-6 hover:bg-[#8f1212] hover:text-white transition border-l-4 border-transparent hover:border-[#d4af37]"><span class="font-bold w-6 inline-block">VI.</span> Наследство</a></li>
                <li><a href="#chap7" class="block py-3 px-6 hover:bg-[#8f1212] hover:text-white transition border-l-4 border-transparent hover:border-[#d4af37]"><span class="font-bold w-6 inline-block">VII.</span> Процесс</a></li>
                <li><a href="#principles" class="block py-3 px-6 bg-[#3a0000] text-[#d4af37] mt-4 border-t border-[#d4af37] hover:bg-[#4a0000] transition"><i class="fas fa-scroll w-6 text-center mr-2"></i>Regulae Iuris</a></li>
            </ul>
        </nav>
        <div class="p-4 text-xs text-center border-t border-[#d4af37]/30 text-yellow-100/60">
            Мазанов Т.О. © 2025
        </div>
    </aside>
    <!-- Основной контент -->
    <main class="flex-1 overflow-y-auto h-screen scroll-smooth relative">   
        <!-- Герой-блок -->
        <header id="intro" class="min-h-[60vh] flex flex-col justify-center items-center p-8 text-center">   
            <!-- Заголовок с венками (Размер оптимизирован) -->
            <div class="relative mb-6">
                <i class="fas fa-leaf text-5xl md:text-6xl text-[#3a5f0b] absolute -left-12 md:-left-16 top-1/2 transform -translate-y-1/2 -rotate-45 opacity-90 drop-shadow-md"></i>
                <i class="fas fa-leaf text-5xl md:text-6xl text-[#3a5f0b] absolute -right-12 md:-right-16 top-1/2 transform -translate-y-1/2 rotate-45 opacity-90 drop-shadow-md"></i>      
                <h1 class="text-4xl md:text-6xl font-black text-[#750000] drop-shadow-lg roman-font leading-tight bg-white/80 px-6 py-4 rounded shadow-xl border-4 double border-[#d4af37]">
                    РИМСКОЕ<br>ПРАВО
                </h1>
            </div>
            <h2 class="text-lg md:text-xl font-bold uppercase tracking-widest text-[#fff] bg-[#750000] px-6 py-2 rounded shadow-lg border border-[#d4af37] mb-10">
                Учебный курс в таблицах и схемах
            </h2>
            <!-- Цитата (Новый стиль) -->
            <div class="quote-box">
                <p class="quote-latin">
                    Iuris praecepta sunt haec: honeste vivere, alterum non laedere, suum cuique tribuere.
                </p>
                <div>
                    <span class="quote-rus">
                        «Предписания права таковы: честно жить, другого не обижать, каждому воздавать свое».
                    </span>
                </div>
                <div class="quote-author">
                    — Ульпиан (Ulpianus), Digesta 1.1.10.1 —
                </div>
            </div>
        </header>
        <div class="max-w-6xl mx-auto p-6 md:p-12 space-y-20 pb-32">
            <!-- ГЛАВА I -->
            <section id="chap1">
                <div class="flex items-center mb-6 border-b-4 border-[#750000] pb-2">
                    <span class="text-5xl text-[#750000] font-bold mr-4 roman-font">I</span>
                    <h2 class="text-3xl font-bold text-gray-900 roman-font">ИСТОЧНИКИ И СИСТЕМА</h2>
                </div>
                <div class="gold-box p-6 mb-8">
                    <h3 class="text-xl font-bold text-[#750000] mb-4 text-center">СИСТЕМЫ РИМСКОГО ПРАВА</h3>
                    <div class="grid md:grid-cols-3 gap-4 text-center">
                        <div class="bg-gray-50 p-4 border border-gray-200">
                            <i class="fas fa-shield-alt text-3xl text-[#750000] mb-2"></i>
                            <h4 class="font-bold">IUS CIVILE</h4>
                            <p class="text-xs mt-1 text-gray-600">Строгое национальное право только для граждан Рима.</p>
                        </div>
                        <div class="bg-gray-50 p-4 border border-gray-200">
                            <i class="fas fa-globe text-3xl text-[#c5a017] mb-2"></i>
                            <h4 class="font-bold">IUS GENTIUM</h4>
                            <p class="text-xs mt-1 text-gray-600">Право народов. Гибкое, для общения с иностранцами.</p>
                        </div>
                        <div class="bg-gray-50 p-4 border border-gray-200">
                            <i class="fas fa-balance-scale text-3xl text-[#3a5f0b] mb-2"></i>
                            <h4 class="font-bold">IUS HONORARIUM</h4>
                            <p class="text-xs mt-1 text-gray-600">Преторское право. Дополняло и исправляло цивильное.</p>
                        </div>
                    </div>
                </div>
                <h3 class="text-lg font-bold mb-2 roman-font text-[#750000]">ЭВОЛЮЦИЯ ИСТОЧНИКОВ</h3>
                <div class="overflow-x-auto shadow-lg">
                    <table class="roman-table">
                        <thead>
                            <tr>
                                <th width="25%">Период</th>
                                <th>Основные Источники Права</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><strong>Архаичный</strong><br>(754–367 до н.э.)</td>
                                <td>Обычаи предков (<strong>Mores maiorum</strong>), <strong>Законы XII Таблиц</strong> (450 г. до н.э.), Толкование понтификов.</td>
                            </tr>
                            <tr>
                                <td><strong>Предклассический</strong><br>(367–27 до н.э.)</td>
                                <td>Законы (<strong>Leges</strong>), Плебисциты, Эдикты магистратов (преторов), Деятельность юристов.</td>
                            </tr>
                            <tr>
                                <td><strong>Классический</strong><br>(27 до н.э. – 284 н.э.)</td>
                                <td>Сенатусконсульты, Конституции принцепсов, Ответы юристов (<strong>Responsa</strong>).</td>
                            </tr>
                            <tr>
                                <td><strong>Постклассический</strong><br>(284–565 н.э.)</td>
                                <td>Единоличная воля императора. <strong>Свод Юстиниана (Corpus Iuris Civilis)</strong>.</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </section>
            <!-- ГЛАВА II -->
            <section id="chap2">
                <div class="flex items-center mb-6 border-b-4 border-[#750000] pb-2">
                    <span class="text-5xl text-[#750000] font-bold mr-4 roman-font">II</span>
                    <h2 class="text-3xl font-bold text-gray-900 roman-font">СУБЪЕКТЫ ПРАВА</h2>
                </div>
                <div class="mb-8">
                    <h3 class="text-center font-bold text-lg mb-4 text-[#750000]">ТРИ СТАТУСА ПРАВОСПОСОБНОСТИ (CAPUT)</h3>
                    <div class="diagram-container">
                        <div class="diagram-node">
                            <div class="font-bold text-[#750000] uppercase mb-1">Status Libertatis</div>
                            <div class="text-sm">Свобода. Главный статус.<br>Утрата = <strong>Maxima</strong> (Рабство)</div>
                        </div>
                        <div class="diagram-node">
                            <div class="font-bold text-[#750000] uppercase mb-1">Status Civitatis</div>
                            <div class="text-sm">Гражданство.<br>Утрата = <strong>Media</strong> (Изгнание)</div>
                        </div>
                        <div class="diagram-node">
                            <div class="font-bold text-[#750000] uppercase mb-1">Status Familiae</div>
                            <div class="text-sm">Положение в семье.<br>Утрата = <strong>Minima</strong> (Смена семьи)</div>
                        </div>
                    </div>
                </div>
                <div class="gold-box p-6 mb-6">
                    <h4 class="font-bold text-[#750000] mb-2">ГРАЖДАНСТВО И МАНУМИССИЯ</h4>
                    <p class="text-sm mb-2"><strong>Манумиссия (Manumissio)</strong> — освобождение раба. Способы: <em>Vindicta</em> (палочкой), <em>Censu</em> (перепись), <em>Testamento</em> (завещание). Раб становился либертином.</p>
                    <p class="text-sm border-t border-[#d4af37] pt-2 mt-2">
                        <strong class="text-[#750000]">212 г. н.э. Конституция Антонина (Каракаллы)</strong> — дарование римского гражданства всем свободным жителям Империи.
                    </p>
                </div>
                <h3 class="font-bold mb-2">Юридические лица (Universitas)</h3>
                <ul class="list-disc list-inside bg-white p-4 rounded shadow">
                    <li><strong>Populus Romanus:</strong> Римское государство, казна.</li>
                    <li><strong>Municipia:</strong> Городские общины.</li>
                    <li><strong>Collegia:</strong> Частные корпорации (минимум 3 человека).</li>
                    <li><strong>Piae causae:</strong> Благотворительные учреждения.</li>
                </ul>
            </section>
            <!-- ГЛАВА III -->
            <section id="chap3">
                <div class="flex items-center mb-6 border-b-4 border-[#750000] pb-2">
                    <span class="text-5xl text-[#750000] font-bold mr-4 roman-font">III</span>
                    <h2 class="text-3xl font-bold text-gray-900 roman-font">СЕМЕЙНОЕ ПРАВО</h2>
                </div>
                <div class="grid md:grid-cols-2 gap-6 mb-8">
                    <div class="bg-white p-6 shadow-md border-t-4 border-[#750000]">
                        <h3 class="text-center font-bold text-xl mb-4 roman-font">ВЛАСТЬ ОТЦА (Pater Familias)</h3>
                        <ul class="space-y-3">
                            <li class="flex items-start"><i class="fas fa-gavel text-[#750000] mt-1 mr-2"></i><span><strong>Patria Potestas:</strong> Власть над детьми. Включала право жизни и смерти, продажи.</span></li>
                            <li class="flex items-start"><i class="fas fa-ring text-[#750000] mt-1 mr-2"></i><span><strong>Manus:</strong> Власть над женой (в браке Cum Manu).</span></li>
                            <li class="flex items-start"><i class="fas fa-paw text-[#750000] mt-1 mr-2"></i><span><strong>Dominica Potestas:</strong> Власть над рабами.</span></li>
                        </ul>
                    </div>
                    <div class="bg-white p-6 shadow-md border-t-4 border-[#c5a017]">
                        <h3 class="text-center font-bold text-xl mb-4 roman-font">БРАК И РОДСТВО</h3>
                        <div class="mb-3">
                            <strong>Agnatio (Агнатское):</strong> Юридическое родство по власти отца. Жена in manu — агнатка. Эманципированный сын — чужой.
                        </div>
                        <div class="mb-3">
                            <strong>Cognatio (Когнатское):</strong> Кровное родство. Стало основным при Юстиниане.
                        </div>
                        <div class="text-sm italic mt-4 border-t pt-2">
                            Брак: <strong>Cum manu</strong> (с властью мужа, жена теряет имущество) и <strong>Sine manu</strong> (без власти, имущество раздельно).
                        </div>
                    </div>
                </div>
            </section>
            <!-- ГЛАВА IV -->
            <section id="chap4">
                <div class="flex items-center mb-6 border-b-4 border-[#750000] pb-2">
                    <span class="text-5xl text-[#750000] font-bold mr-4 roman-font">IV</span>
                    <h2 class="text-3xl font-bold text-gray-900 roman-font">ВЕЩНОЕ ПРАВО</h2>
                </div>
                <!-- Классификация вещей -->
                <button class="accordion-btn" onclick="toggleAccordion(this)">
                    <span>СХЕМА: КЛАССИФИКАЦИЯ ВЕЩЕЙ (RES)</span>
                    <i class="fas fa-chevron-down icon-rotate"></i>
                </button>
                <div class="accordion-content mb-6">
                    <div class="p-6">
                        <div class="grid md:grid-cols-2 gap-6">
                            <div class="bg-red-50 p-4 border border-red-200">
                                <h4 class="font-bold text-[#750000] text-center mb-2">RES MANCIPI</h4>
                                <p class="text-center text-xs uppercase mb-2">Манципируемые (Ценные)</p>
                                <ul class="list-disc list-inside text-sm">
                                    <li>Земля в Италии</li>
                                    <li>Рабы</li>
                                    <li>Рабочий скот</li>
                                    <li>Сельские сервитуты</li>
                                </ul>
                                <p class="mt-2 text-sm font-bold text-center">Передача: MANCIPATIO (Обряд с весами)</p>
                            </div>
                            <div class="bg-gray-50 p-4 border border-gray-200">
                                <h4 class="font-bold text-gray-800 text-center mb-2">RES NEC MANCIPI</h4>
                                <p class="text-center text-xs uppercase mb-2">Неманципируемые</p>
                                <ul class="list-disc list-inside text-sm">
                                    <li>Деньги, одежда</li>
                                    <li>Провинциальная земля</li>
                                    <li>Мелкий скот</li>
                                </ul>
                                <p class="mt-2 text-sm font-bold text-center">Передача: TRADITIO (Вручение)</p>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- Собственность и Владение -->
                <div class="grid md:grid-cols-2 gap-8 mb-8">
                    <div class="gold-box p-6">
                        <h3 class="font-bold text-[#750000] mb-2 roman-font">DOMINIUM (Собственность)</h3>
                        <p class="mb-2 text-sm">Полное господство (Plena in re potestas).</p>
                        <ul class="list-decimal list-inside font-bold text-sm text-[#333]">
                            <li>Ius Utendi (Пользование)</li>
                            <li>Ius Fruendi (Плоды)</li>
                            <li>Ius Abutendi (Распоряжение)</li>
                        </ul>
                        <div class="mt-4 text-sm font-bold text-[#750000]">Защита: Rei Vindicatio</div>
                    </div>
                    <div class="gold-box p-6">
                        <h3 class="font-bold text-[#750000] mb-2 roman-font">POSSESSIO (Владение)</h3>
                        <p class="mb-2 text-sm">Фактическое господство + Воля.</p>
                        <ul class="list-decimal list-inside font-bold text-sm text-[#333]">
                            <li>Corpus (Тело/Факт)</li>
                            <li>Animus (Намерение владеть для себя)</li>
                        </ul>
                        <div class="mt-4 text-sm font-bold text-[#750000]">Защита: Interdicta (Интердикты)</div>
                    </div>
                </div>
                <div class="overflow-x-auto shadow bg-white">
                    <table class="roman-table">
                        <tr>
                            <th colspan="2" class="text-center">ПРАВА НА ЧУЖИЕ ВЕЩИ (IURA IN RE ALIENA)</th>
                        </tr>
                        <tr>
                            <td class="font-bold w-1/4">Сервитуты</td>
                            <td>
                                <strong>Предиальные:</strong> Сельские (iter, actus, via, aquaeductus) и Городские.<br>
                                <strong>Личные:</strong> Ususfructus (узуфрукт - плоды), Usus, Habitatio.
                            </td>
                        </tr>
                        <tr>
                            <td class="font-bold">Залог</td>
                            <td>
                                <strong>Fiducia</strong> (Собственность), <strong>Pignus</strong> (Владение), <strong>Hypotheca</strong> (Без владения).
                            </td>
                        </tr>
                        <tr>
                            <td class="font-bold">Аренда</td>
                            <td>Emphyteusis (Вечная аренда земли), Superficies (Право застройки).</td>
                        </tr>
                    </table>
                </div>
            </section>
            <!-- ГЛАВА V: ОБЯЗАТЕЛЬСТВА -->
            <section id="chap5">
                <div class="flex items-center mb-6 border-b-4 border-[#750000] pb-2">
                    <span class="text-5xl text-[#750000] font-bold mr-4 roman-font">V</span>
                    <h2 class="text-3xl font-bold text-gray-900 roman-font">ОБЯЗАТЕЛЬСТВЕННОЕ ПРАВО</h2>
                </div>
                <!-- Цитата -->
                <div class="quote-box mb-10">
                    <p class="quote-latin">
                        Obligatio est iuris vinculum, quo necessitate adstringimur alicuius solvendae rei...
                    </p>
                    <p class="quote-rus">
                        «Обязательство есть правовые узы, в силу которых мы связаны необходимостью что-либо исполнить...»
                    </p>
                    <div class="quote-author">
                        — Институции Юстиниана (Institutiones Iustiniani), 3.13.pr. —
                    </div>
                </div>
                <!-- 1. КОНТРАКТЫ -->
                <button class="accordion-btn active" onclick="toggleAccordion(this)">
                    <span>1. СИСТЕМА КОНТРАКТОВ (Contractus)</span>
                    <i class="fas fa-chevron-down icon-rotate"></i>
                </button>
                <div class="accordion-content open mb-4">
                    <div class="p-6 grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div class="border p-4 rounded bg-red-50/30">
                            <h4 class="font-bold text-[#750000] mb-2">RE (Реальные)</h4>
                            <p class="text-xs mb-2">Возникают с передачи вещи.</p>
                            <ul class="text-sm space-y-1 list-disc list-inside">
                                <li><strong>Mutuum (Заем):</strong> Переход собственности (деньги). Возврат того же количества.</li>
                                <li><strong>Commodatum (Ссуда):</strong> Временное пользование. Возврат той же вещи.</li>
                                <li><strong>Depositum (Хранение):</strong> Безвозмездно.</li>
                                <li><strong>Pignus (Залог).</strong></li>
                            </ul>
                        </div>
                        <div class="border p-4 rounded bg-yellow-50/30">
                            <h4 class="font-bold text-[#750000] mb-2">VERBIS & LITTERIS</h4>
                            <ul class="text-sm space-y-1 list-disc list-inside">
                                <li><strong>Stipulatio:</strong> Устный контракт ("Spondesne? - Spondeo").</li>
                                <li><strong>Litteris:</strong> Письменный контракт (запись в книгу).</li>
                            </ul>
                        </div>
                        <div class="border p-4 rounded bg-green-50/30 col-span-1 md:col-span-2">
                            <h4 class="font-bold text-[#750000] mb-2">CONSENSU (Консенсуальные)</h4>
                            <p class="text-xs mb-2">Возникают из простого соглашения (Consensus).</p>
                            <div class="grid grid-cols-2 gap-4 text-sm">
                                <div><strong>1. Emptio-Venditio:</strong> Купля-продажа.</div>
                                <div><strong>2. Locatio-Conductio:</strong> Наем вещей, услуг, работ.</div>
                                <div><strong>3. Mandatum:</strong> Поручение.</div>
                                <div><strong>4. Societas:</strong> Товарищество.</div>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- 2. ДЕЛИКТЫ -->
                <button class="accordion-btn" onclick="toggleAccordion(this)">
                    <span>2. ДЕЛИКТЫ (Delicta Privata)</span>
                    <i class="fas fa-chevron-down icon-rotate"></i>
                </button>
                <div class="accordion-content mb-4">
                    <div class="p-6">
                        <table class="roman-table">
                            <tr>
                                <td class="font-bold">Furtum (Кража)</td>
                                <td>Тайное хищение. Штраф: двойной (nec manifestum) или четверной (manifestum).</td>
                            </tr>
                            <tr>
                                <td class="font-bold">Iniuria (Обида)</td>
                                <td>Посягательство на личность (телесные повреждения, оскорбление). Штраф по оценке.</td>
                            </tr>
                            <tr>
                                <td class="font-bold">Damnum Iniuria Datum</td>
                                <td>Повреждение имущества. <strong>Lex Aquilia</strong>: за убийство раба — высшая цена за год.</td>
                            </tr>
                        </table>
                    </div>
                </div>
                <!-- 3. КВАЗИ И ПАКТЫ -->
                <button class="accordion-btn" onclick="toggleAccordion(this)">
                    <span>3. ПАКТЫ И КВАЗИ-ОБЯЗАТЕЛЬСТВА</span>
                    <i class="fas fa-chevron-down icon-rotate"></i>
                </button>
                <div class="accordion-content mb-4">
                    <div class="p-6">
                        <ul class="list-disc list-inside text-sm space-y-2">
                            <li><strong>Negotiorum gestio:</strong> Ведение чужих дел без поручения.</li>
                            <li><strong>Solutio indebiti:</strong> Исполнение недолжного (ошибочный платеж).</li>
                            <li><strong>Pacta:</strong> "Голые" пакты (без иска) и "Одетые" (с иском).</li>
                        </ul>
                    </div>
                </div>
            </section>
            <!-- ГЛАВА VI: НАСЛЕДСТВО -->
            <section id="chap6">
                <div class="flex items-center mb-6 border-b-4 border-[#750000] pb-2">
                    <span class="text-5xl text-[#750000] font-bold mr-4 roman-font">VI</span>
                    <h2 class="text-3xl font-bold text-gray-900 roman-font">НАСЛЕДСТВЕННОЕ ПРАВО</h2>
                </div>
                <div class="gold-box p-6 mb-8">
                    <h3 class="text-center font-bold text-lg mb-4 text-[#750000]">ЭВОЛЮЦИЯ ОЧЕРЕДЕЙ НАСЛЕДОВАНИЯ ПО ЗАКОНУ</h3>
                    <div class="grid md:grid-cols-3 gap-4 text-sm">
                        <div class="bg-gray-100 p-4">
                            <strong class="block text-center mb-2">ЦИВИЛЬНОЕ (XII Таблиц)</strong>
                            <p class="text-xs text-center mb-2">Принцип: Агнатство</p>
                            <ol class="list-decimal list-inside">
                                <li>Sui Heredes (Свои)</li>
                                <li>Agnatus Proximus</li>
                                <li>Gentiles (Родичи)</li>
                            </ol>
                        </div>
                        <div class="bg-yellow-50 p-4 border border-[#d4af37]">
                            <strong class="block text-center mb-2 text-[#750000]">ПРЕТОРСКОЕ</strong>
                            <p class="text-xs text-center mb-2">Принцип: Смешанный</p>
                            <ol class="list-decimal list-inside">
                                <li>Unde Liberi (Дети)</li>
                                <li>Unde Legitimi</li>
                                <li>Unde Cognati</li>
                                <li>Unde Vir et Uxor</li>
                            </ol>
                        </div>
                        <div class="bg-red-50 p-4 border border-[#750000]">
                            <strong class="block text-center mb-2 text-[#750000]">ЮСТИНИАНА</strong>
                            <p class="text-xs text-center mb-2">Принцип: Кровь</p>
                            <ol class="list-decimal list-inside">
                                <li>Нисходящие</li>
                                <li>Восходящие + Братья</li>
                                <li>Неполнородные</li>
                                <li>Прочие когнаты</li>
                            </ol>
                        </div>
                    </div>
                </div>
                <div class="bg-white p-6 shadow-md border-l-4 border-[#750000]">
                    <h4 class="font-bold text-[#750000] mb-2">Сингулярное преемство (Отказы)</h4>
                    <div class="grid md:grid-cols-2 gap-6 text-sm">
                        <div>
                            <strong>Legatum (Легат):</strong> Строго формальный дар, возлагаемый на наследника <em>в завещании</em>.
                        </div>
                        <div>
                            <strong>Fideicommissum (Фидеикомисс):</strong> Неформальная просьба к "совести" наследника.
                        </div>
                    </div>
                </div>
            </section>
            <!-- ГЛАВА VII: ПРОЦЕСС -->
            <section id="chap7">
                <div class="flex items-center mb-6 border-b-4 border-[#750000] pb-2">
                    <span class="text-5xl text-[#750000] font-bold mr-4 roman-font">VII</span>
                    <h2 class="text-3xl font-bold text-gray-900 roman-font">ГРАЖДАНСКИЙ ПРОЦЕСС</h2>
                </div>
                <!-- Легисакционный -->
                <button class="accordion-btn" onclick="toggleAccordion(this)">
                    <span>1. ЛЕГИСАКЦИОННЫЙ ПРОЦЕСС (Legis Actiones)</span>
                    <i class="fas fa-chevron-down icon-rotate"></i>
                </button>
                <div class="accordion-content mb-4">
                    <div class="p-6">
                        <p class="mb-4 text-sm italic">Строгий формализм. Две стадии: In Iure и Apud Iudicem. 5 видов исков (Гай):</p>
                        <ul class="list-decimal list-inside text-sm space-y-1">
                            <li><strong>Sacramentum:</strong> Процесс-пари с залогом.</li>
                            <li><strong>Per iudicis postulationem:</strong> Просьба о судье (раздел).</li>
                            <li><strong>Per condictionem:</strong> Кондикция (для точных сумм).</li>
                            <li><strong>Per manus iniectionem:</strong> Наложение руки (исполнительный).</li>
                            <li><strong>Per pignoris capionem:</strong> Захват залога (внесудебный).</li>
                        </ul>
                    </div>
                </div>
                <!-- Формулярный -->
                <button class="accordion-btn active" onclick="toggleAccordion(this)">
                    <span>2. ФОРМУЛЯРНЫЙ ПРОЦЕСС (Per Formulas)</span>
                    <i class="fas fa-chevron-down icon-rotate"></i>
                </button>
                <div class="accordion-content open mb-4">
                    <div class="p-6">
                        <p class="mb-4">Претор составляет письменную <strong>Формулу</strong> — инструкцию для судьи.</p>
                        <div class="bg-gray-100 p-4 border border-gray-300 mb-4">
                            <h5 class="font-bold text-center text-[#750000] mb-2">ЧАСТИ ФОРМУЛЫ</h5>
                            <ul class="text-sm grid grid-cols-1 md:grid-cols-2 gap-2">
                                <li><strong>Intentio:</strong> Требование истца (основа).</li>
                                <li><strong>Demonstratio:</strong> Описание фактов.</li>
                                <li><strong>Condemnatio:</strong> Приказ осудить (денежная!).</li>
                                <li><strong>Adiudicatio:</strong> Присуждение (при разделе).</li>
                                <li class="col-span-1 md:col-span-2 border-t pt-2"><em>Exceptio</em> (Возражение) и <em>Praescriptio</em>.</li>
                            </ul>
                        </div>
                    </div>
                </div>
                <!-- Экстраординарный -->
                <button class="accordion-btn" onclick="toggleAccordion(this)">
                    <span>3. ЭКСТРАОРДИНАРНЫЙ (Cognitio Extra Ordinem)</span>
                    <i class="fas fa-chevron-down icon-rotate"></i>
                </button>
                <div class="accordion-content mb-4">
                    <div class="p-6">
                        <p>Государственный процесс. Одна стадия. Судья — чиновник. Письменное производство. Появление апелляции. Исполнение в натуре.</p>
                    </div>
                </div>
                <!-- Преторская защита -->
                <div class="gold-box p-6 mt-8 bg-[#fffcf0]">
                    <h3 class="font-bold text-[#750000] mb-4 flex items-center"><i class="fas fa-shield-alt mr-2"></i>СРЕДСТВА ПРЕТОРСКОЙ ЗАЩИТЫ</h3>
                    <div class="grid md:grid-cols-2 gap-6 text-sm">
                        <div>
                            <span class="block font-bold">1. Interdictum (Интердикт)</span>
                            <span class="text-gray-700">Приказ претора о запрете или совершении действия.</span>
                        </div>
                        <div>
                            <span class="block font-bold">2. Restitutio in integrum</span>
                            <span class="text-gray-700">Восстановление в первоначальное состояние.</span>
                        </div>
                        <div>
                            <span class="block font-bold">3. Stipulatio praetoria</span>
                            <span class="text-gray-700">Обещание по приказу претора.</span>
                        </div>
                        <div>
                            <span class="block font-bold">4. Missio in possessionem</span>
                            <span class="text-gray-700">Ввод во владение имуществом должника.</span>
                        </div>
                    </div>
                </div>
            </section>
            <!-- REGULAE IURIS -->
            <section id="principles">
                <div class="text-center mb-8 pt-8 border-t-2 border-[#c5a017]">
                    <h2 class="text-3xl font-bold text-[#750000] roman-font">REGULAE IURIS</h2>
                    <p class="text-gray-500 italic">Основные принципы права</p>
                </div> 
                <div class="grid md:grid-cols-2 gap-4">
                    <div class="principle-card">
                        <span class="latin-term">Dura lex, sed lex</span>
                        <span class="rus-def">Закон суров, но это закон.</span>
                    </div>
                    <div class="principle-card">
                        <span class="latin-term">Nemo iudex in propria causa</span>
                        <span class="rus-def">Никто не может быть судьей в собственном деле.</span>
                    </div>
                    <div class="principle-card">
                        <span class="latin-term">Pacta sunt servanda</span>
                        <span class="rus-def">Договоры должны соблюдаться.</span>
                    </div>
                    <div class="principle-card">
                        <span class="latin-term">Ei incumbit probatio qui dicit</span>
                        <span class="rus-def">Доказывание лежит на том, кто утверждает, а не на том, кто отрицает.</span>
                    </div>
                    <div class="principle-card">
                        <span class="latin-term">Audiatur et altera pars</span>
                        <span class="rus-def">Пусть будет выслушана и другая сторона.</span>
                    </div>
                    <div class="principle-card">
                        <span class="latin-term">Superficies solo cedit</span>
                        <span class="rus-def">Строение следует за землей (принадлежит собственнику земли).</span>
                    </div>
                </div>
            </section>
        </div>
        <!-- Футер -->
        <footer class="bg-[#1a1a1a] text-[#8b6c42] py-10 text-center border-t-8 border-[#8b6c42] mt-12">
            <div class="container mx-auto px-4">
                <i class="fas fa-columns text-4xl mb-4 text-[#d4af37]"></i>
                <p class="font-bold text-xl roman-font mb-2 text-[#d4af37]">DURA LEX SED LEX</p>
                <div class="border-t border-[#3d3d3d] pt-6 mt-6 max-w-2xl mx-auto">
                    <p class="text-xs text-gray-500 mb-2">На основе учебного пособия: Бортенев А.И., Сергачева О.А., Коваленко Е.Н. (2017)</p>
                    <div class="inline-block border border-[#8b6c42] px-6 py-3 rounded mt-2 bg-[#2b2b2b]">
                        <p class="text-xs uppercase tracking-widest text-[#d4af37] font-bold mb-1">Разработал</p>
                        <p class="text-white font-serif text-lg">Мазанов Тимофей Олегович</p>
                        <p class="text-xs text-gray-400 mt-1">1 курс юрфака, группа 4201-25-02 • 2025</p>
                    </div>
                </div>
            </div>
        </footer>
    </main>
    <script>
        function toggleAccordion(button) {
            button.classList.toggle('active');
            var content = button.nextElementSibling;
            if (content.style.maxHeight) {
                content.style.maxHeight = null;
                content.classList.remove('open');
            } else {
                content.style.maxHeight = content.scrollHeight + "px";
                content.classList.add('open');
            }
        }
    </script>
</body>
</html>
