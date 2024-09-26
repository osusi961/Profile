<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>osusi961 | 革新的漫画クリエイター</title>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;700&family=Permanent+Marker&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #e74c3c;
            --accent-color: #3498db;
            --background-color: #ecf0f1;
            --text-color: #34495e;
        }
        body, html {
            margin: 0;
            padding: 0;
            font-family: 'Noto Sans JP', sans-serif;
            background-color: var(--background-color);
            color: var(--text-color);
            line-height: 1.6;
            scroll-behavior: smooth;
        }
        header {
            background-color: var(--primary-color);
            color: white;
            padding: 1rem;
            position: fixed;
            width: 100%;
            z-index: 1000;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }
        .logo {
            font-family: 'Permanent Marker', cursive;
            font-size: 2rem;
            color: var(--secondary-color);
        }
        nav ul {
            display: flex;
            list-style: none;
        }
        nav ul li {
            margin-left: 20px;
        }
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s ease;
        }
        nav ul li a:hover {
            color: var(--secondary-color);
        }
        .hero {
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('/api/placeholder/1200/800');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
        }
        .hero-content h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
        }
        .hero-content p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
        }
        .btn {
            display: inline-block;
            background-color: var(--secondary-color);
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }
        .btn:hover {
            background-color: #c0392b;
        }
        .section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        .section-title {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            color: var(--primary-color);
        }
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            grid-gap: 2rem;
        }
        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        .gallery-item:hover {
            transform: translateY(-10px);
        }
        .gallery-item img {
            width: 100%;
            height: auto;
            display: block;
        }
        .gallery-item .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.7);
            display: flex;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        .gallery-item:hover .overlay {
            opacity: 1;
        }
        .gallery-item .overlay-content {
            color: white;
            text-align: center;
        }
        .about {
            display: flex;
            align-items: center;
            gap: 2rem;
        }
        .about-image {
            flex: 1;
        }
        .about-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }
        .about-content {
            flex: 2;
        }
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
            padding: 2rem 0;
        }
        .timeline::after {
            content: '';
            position: absolute;
            width: 6px;
            background-color: var(--primary-color);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -3px;
        }
        .timeline-item {
            padding: 10px 40px;
            position: relative;
            background-color: inherit;
            width: 50%;
        }
        .timeline-item::after {
            content: '';
            position: absolute;
            width: 25px;
            height: 25px;
            right: -17px;
            background-color: var(--background-color);
            border: 4px solid var(--secondary-color);
            top: 15px;
            border-radius: 50%;
            z-index: 1;
        }
        .left {
            left: 0;
        }
        .right {
            left: 50%;
        }
        .left::before {
            content: " ";
            height: 0;
            position: absolute;
            top: 22px;
            width: 0;
            z-index: 1;
            right: 30px;
            border: medium solid var(--primary-color);
            border-width: 10px 0 10px 10px;
            border-color: transparent transparent transparent var(--primary-color);
        }
        .right::before {
            content: " ";
            height: 0;
            position: absolute;
            top: 22px;
            width: 0;
            z-index: 1;
            left: 30px;
            border: medium solid var(--primary-color);
            border-width: 10px 10px 10px 0;
            border-color: transparent var(--primary-color) transparent transparent;
        }
        .right::after {
            left: -16px;
        }
        .timeline-content {
            padding: 20px 30px;
            background-color: white;
            position: relative;
            border-radius: 6px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }
        footer {
            background-color: var(--primary-color);
            color: white;
            text-align: center;
            padding: 2rem;
        }
        .social-links {
            margin-top: 1rem;
        }
        .social-links a {
            color: white;
            font-size: 1.5rem;
            margin: 0 10px;
            transition: color 0.3s ease;
        }
        .social-links a:hover {
            color: var(--secondary-color);
        }
        @media screen and (max-width: 768px) {
            .about {
                flex-direction: column;
            }
            .timeline::after {
                left: 31px;
            }
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            .timeline-item::before {
                left: 60px;
                border: medium solid white;
                border-width: 10px 10px 10px 0;
                border-color: transparent white transparent transparent;
            }
            .left::after, .right::after {
                left: 15px;
            }
            .right {
                left: 0%;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">osusi961</div>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#works">Works</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="hero-content">
            <h1>osusi961</h1>
            <p>革新的な漫画で世界を彩る</p>
            <a href="#works" class="btn">作品を見る</a>
        </div>
    </section>

    <section id="works" class="section">
        <h2 class="section-title">作品ギャラリー</h2>
        <div class="gallery">
            <div class="gallery-item">
                <img src="/api/placeholder/400/300" alt="SF漫画シリーズ">
                <div class="overlay">
                    <div class="overlay-content">
                        <h3>未来都市物語</h3>
                        <p>SF漫画シリーズ</p>
                    </div>
                </div>
            </div>
            <div class="gallery-item">
                <img src="/api/placeholder/400/300" alt="日常系コメディ">
                <div class="overlay">
                    <div class="overlay-content">
                        <h3>わくわく学園生活</h3>
                        <p>日常系コメディ</p>
                    </div>
                </div>
            </div>
            <div class="gallery-item">
                <img src="/api/placeholder/400/300" alt="ミステリー作品">
                <div class="overlay">
                    <div class="overlay-content">
                        <h3>影の探偵</h3>
                        <p>ミステリー作品</p>
                    </div>
                </div>
            </div>
            <div class="gallery-item">
                <img src="/api/placeholder/400/300" alt="ファンタジー短編集">
                <div class="overlay">
                    <div class="overlay-content">
                        <h3>魔法の国の物語</h3>
                        <p>ファンタジー短編集</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="about" class="section">
        <h2 class="section-title">About osusi961</h2>
        <div class="about">
            <div class="about-image">
                <img src="/api/placeholder/400/400" alt="osusi961">
            </div>
            <div class="about-content">
                <p>こんにちは、osusi961です。5年間の漫画家としてのキャリアの中で、SF、コメディ、ミステリー、ファンタジーなど、幅広いジャンルで作品を発表してきました。</p>
                <p>2022年には「新鋭漫画賞」を受賞し、さらなる創作意欲を掻き立てられました。私の目標は、読者の皆様に新しい世界観と感動を届けることです。</p>
                <p>これからも挑戦を続け、より魅力的な作品を生み出していきたいと思います。</p>
            </div>
        </div>
        <div class="timeline">
            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2>2019</h2>
                    <p>漫画家としてデビュー。初連載「未来都市物語」開始</p>
                </div>
            </div>
            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2>2020</h2>
                    <p>日常系コメディ「わくわく学園生活」がヒット</p>
                </div>
            </div>
            <div class="timeline-item left">
                <div class="timeline-content">
                    <h2>2021</h2>
                    <p>ミステリー作品「影の探偵」で新境地を開拓</p>
                </div>
            </div>
            <div class="timeline-item right">
                <div class="timeline-content">
                    <h2>2022</h2>
                    <p>「新鋭漫画賞」受賞。ファンタジー短編集「魔法の国の物語」発表</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="section">
        <h2 class="section-title">Contact</h2>
        <p style="text-align: center;">作品や仕事の依頼についてのお問い合わせは、以下のSNSからお気軽にどうぞ！</p>
        <div class="social-links">
            <a href="#" aria-label="Twitter">🐦</a>
            <a href="#" aria-label="Instagram">📷</a>
            <a href="#" aria-label="オンラインショップ">🛒</a>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 osusi961. All rights reserved.</p>
    </footer>

    <script>
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
