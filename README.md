<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gaming Website</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #121212;
            color: white;
            scroll-behavior: smooth;
        }

        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: #333;
            padding: 10px 0;
            text-align: center;
            z-index: 1000;
        }

        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
            display: flex;
            justify-content: center;
        }

        nav ul li {
            margin: 0 15px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-size: 18px;
            transition: 0.3s;
        }

        nav ul li a:hover {
            color: #ff5722;
        }

        section {
            padding: 80px 20px;
            text-align: center;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s, transform 0.6s;
        }

        section.active {
            opacity: 1;
            transform: translateY(0);
        }

        h1 {
            font-size: 36px;
            margin-bottom: 20px;
            color: #ff5722;
        }

        .apk-list, .social-links, .video-container {
            margin-top: 20px;
        }

        .social-links li {
            list-style: none;
            margin: 10px 0;
        }

        .social-links a {
            color: #ff5722;
            text-decoration: none;
            font-size: 20px;
        }

        .social-links a:hover {
            text-decoration: underline;
        }

        footer {
            margin-top: 40px;
            padding: 10px;
            background: #222;
            text-align: center;
            font-size: 14px;
            color: gray;
        }

        iframe {
            width: 80%;
            height: 315px;
            border: none;
        }

    </style>
</head>
<body>

    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#download">Download</a></li>
            <li><a href="#blog">Blog</a></li>
        </ul>
    </nav>

    <section id="home">
        <h1>Latest APKs</h1>
        <div class="apk-list">
            <p>New APKs will be listed here...</p>
        </div>
    </section>

    <section id="about">
        <h1>About</h1>
        <p>Follow me on:</p>
        <ul class="social-links">
            <li><a href="https://youtube.com/@ShayanPresident96" target="_blank">YouTube</a></li>
            <li><a href="https://tiktok.com" target="_blank">TikTok</a></li>
            <li><a href="https://instagram.com" target="_blank">Instagram</a></li>
            <li><a href="https://t.me" target="_blank">Telegram</a></li>
        </ul>
        <footer>
            <p>&copy; 2025. Created by Shayan. All Rights Reserved.</p>
        </footer>
    </section>

    <section id="download">
        <h1>Download</h1>
        <p>Current downloads in progress will be displayed here...</p>
    </section>

    <section id="blog">
        <h1>Blog</h1>
        <div class="video-container">
            <iframe src="https://www.youtube.com/embed/YOUR_VIDEO_ID" allowfullscreen></iframe>
        </div>
    </section>

    <script>
        document.addEventListener("DOMContentLoaded", function() {
            const sections = document.querySelectorAll("section");

            function revealSections() {
                sections.forEach((section) => {
                    const rect = section.getBoundingClientRect();
                    if (rect.top < window.innerHeight * 0.75) {
                        section.classList.add("active");
                    }
                });
            }

            window.addEventListener("scroll", revealSections);
            revealSections();
        });
    </script>

</body>
</html>
