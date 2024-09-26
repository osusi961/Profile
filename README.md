<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>osusi961 | R18漫画家ポートフォリオ</title>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;700&family=Permanent+Marker&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #1a1a1a;
            --secondary-color: #e74c3c;
            --accent-color: #3498db;
            --background-color: #1c1c1c;
            --text-color: #ecf0f1;
        }

        *,
        *::before,
        *::after {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body, html {
            font-family: 'Noto Sans JP', sans-serif;
            background-color: var(--background-color);
            color: var(--text-color);
            line-height: 1.6;
            scroll-behavior: smooth;
            overflow-x: hidden;
        }

        /* ナビゲーションバー */
        header {
            background-color: rgba(26, 26, 26, 0.8);
            color: white;
            padding: 1rem 2rem;
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            transition: background-color 0.3s ease;
        }

        header.scrolled {
            background-color: var(--primary-color);
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

        /* ヒーローセクション */
        .hero {
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('your-image-path.jpg');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
        }

        .hero h1 {
            font-size: 4.5rem;
            margin-bottom: 1rem;
            text-transform: uppercase;
        }

        .hero p {
            font-size: 1.8rem;
            margin-bottom: 2.5rem;
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary-color);
            color: white;
            padding: 15px 30px;
            font-size: 1.2rem;
            text-decoration: none;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }

        .btn:hover {
            background-color: #c0392b;
        }

        /* セクション共通 */
        .section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
            color: var(--text-color);
        }

        /* ギャラリー */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            grid-gap: 2rem;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
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
            background: rgba(0, 0, 0, 0.7);
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

        /* SNSリンク */
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

        /* フッター */
        footer {
            background-color: var(--primary-color);
            color: white;
            text-align: center;
            padding: 2rem;
        }

        @media screen and (max-width: 768px) {
            .hero h1 {
                font-size: 3rem;
            }

            .hero p {
                font-size: 1.3rem;
            }

            .gallery-item {
                margin-bottom: 2rem;
            }
        }
    </style>
</head>
<body>

    <!-- ナビゲーションバー -->
    <header>
        <nav>
            <div class="logo">osusi961</div>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#works">Works</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- ヒーローセクション -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>osusi961</h1>
            <p>おすし961のポートフォリオサイト</p>
            <a href="#works" class="btn">各種サイトへ</a>
        </div>
    </section>

    <!-- 各種サイトへのリンクセクション -->
    <section id="works" class="section">
        <h2 class="section-title">各種サイトリンク</h2>
        <div class="gallery">
            <!-- DLsiteリンク -->
            <div class="gallery-item">
                <a href="https://www.dlsite.com/maniax/circle/profile/=/maker_id/RG52742.html" target="_blank">
                    <img src="your-dlsite-image.jpg" alt="DLsite">
                    <div class="overlay">
                        <div class="overlay-content">
                            <h3>DLsite</h3>
                        </div>
                    </div>
                </a>
            </div>

            <!-- FANZAリンク -->
            <div class="gallery-item">
                <a href="https://www.dmm.co.jp/dc/doujin/-/list/=/article=maker/id=200788/" target="_blank">
                    <img src="your-fanza-image.jpg" alt="FANZA">
                    <div class="overlay">
                        <div class="overlay-content">
                            <h3>FANZA</h3>
                        </div>
                    </div>
                </a>
            </div>

            <!-- Fantiaリンク -->
            <div class="gallery-item">
                <a href="https://fantia.jp/fanclubs/483167" target="_blank">
                    <img src="your-fantia-image.jpg" alt="Fantia">
                    <div class="overlay">
                        <div class="overlay-content">
                            <h3>Fantia</h3>
                        </div>
                    </div>
                </a>
            </div>

            <!-- Skebリンク -->
            <div class="gallery-item">
                <a href="https://skeb.jp/@osusi961" target="_blank">
                    <img src="your-skeb-image.jpg" alt="Skeb">
                    <div class="overlay">
                        <div class="overlay-content">
                            <h3>Skeb</h3>
                        </div>
                    </div>
                </a>
            </div>
        </div>
    </section>

    <!-- お問い合わせセクション -->
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

    <!-- フッター -->
    <footer>
        <p>&copy; 2024 osusi961. All rights reserved.</p>
    </footer>

    <script>
        // ヘッダーのスクロールエフェクト
        window.addEventListener('scroll', function () {
            const header = document.querySelector('header');
            header.classList.toggle('scrolled', window.scrollY > 0);
        });

        // スムーズスクロール
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
