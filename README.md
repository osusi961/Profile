<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>osusi961 | 革新的漫画クリエイター</title>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;700&family=Permanent+Marker&display=swap" rel="stylesheet">
    <style>
        *,
        *::before,
        *::after {
            box-sizing: border-box;
        }

        html, body {
            margin: 0;
            padding: 0;
            width: 100%;
            overflow-x: hidden;
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
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        :root {
            --primary-color: #2c3e50;
            --secondary-color: #e74c3c;
            --accent-color: #3498db;
            --background-color: #ecf0f1;
            --text-color: #34495e;
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
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('your-image-path.jpg');
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

        .social-links {
            margin-top: 1rem;
            text-align: center;
        }

        .social-links a {
            color: white;
            font-size: 1.5rem;
            margin: 0 10px;
            transition: color 0.3s ease;
            text-decoration: none;
        }

        .social-links a:hover {
            color: var(--secondary-color);
        }

        footer {
            background-color: var(--primary-color);
            color: white;
            text-align: center;
            padding: 2rem;
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
        <!-- 作品ギャラリーの内容はここに続く -->
    </section>

    <section id="about" class="section">
        <h2 class="section-title">About osusi961</h2>
        <!-- Aboutセクションの内容はここに続く -->
    </section>

    <section id="contact" class="section">
        <h2 class="section-title">Contact</h2>
        <p style="text-align: center;">作品や仕事の依頼についてのお問い合わせは、以下のSNSやメールでお気軽にどうぞ！</p>
        <div class="social-links">
            <!-- Twitterリンク -->
            <a href="https://x.com/osusi961" aria-label="Twitter" target="_blank">🐦 Twitter</a>
            <!-- Pixivリンク -->
            <a href="https://www.pixiv.net/users/40373322" aria-label="Pixiv" target="_blank">🎨 Pixiv</a>
            <!-- メールアドレスリンク -->
            <a href="mailto:osusi961@gmail.com" aria-label="Email">✉️ メール</a>
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
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
