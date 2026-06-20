(https://github.com/user-attachments/files/29164256/wedding_invitation.2.txt)
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Приглашение на свадьбу | Михаил & Елизавета</title>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=Great+Vibes&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Cormorant Garamond', Georgia, serif;
            overflow-x: hidden;
            background: #faf8f5;
        }

        /* Full-screen hero with photo background */
        .hero {
            position: relative;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('couple_photo.jpg') center center / cover no-repeat;
            filter: brightness(0.55) saturate(1.1);
            z-index: -2;
        }

        .hero::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(
                180deg,
                rgba(250,248,245,0.3) 0%,
                rgba(250,248,245,0.1) 30%,
                rgba(250,248,245,0.05) 50%,
                rgba(250,248,245,0.1) 70%,
                rgba(250,248,245,0.4) 100%
            );
            z-index: -1;
        }

        /* Floating hearts animation */
        .hearts-container {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
            z-index: 1;
        }

        .heart {
            position: absolute;
            color: rgba(255,255,255,0.6);
            font-size: 20px;
            animation: floatUp linear infinite;
        }

        @keyframes floatUp {
            0% {
                transform: translateY(100vh) rotate(0deg) scale(0.5);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-10vh) rotate(360deg) scale(1.2);
                opacity: 0;
            }
        }

        /* Content styling */
        .content {
            position: relative;
            z-index: 2;
            padding: 40px 20px;
            max-width: 700px;
            animation: fadeIn 2s ease-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .subtitle {
            font-size: 1.3rem;
            color: rgba(255,255,255,0.95);
            letter-spacing: 6px;
            text-transform: uppercase;
            font-weight: 300;
            margin-bottom: 15px;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }

        .names {
            font-family: 'Great Vibes', cursive;
            font-size: 5.5rem;
            color: #fff;
            text-shadow: 0 4px 20px rgba(0,0,0,0.4);
            line-height: 1.1;
            margin-bottom: 10px;
        }

        .ampersand {
            font-family: 'Great Vibes', cursive;
            font-size: 3rem;
            color: rgba(255,255,255,0.9);
            margin: -10px 0 5px;
        }

        .date-main {
            font-size: 2.2rem;
            color: #fff;
            letter-spacing: 8px;
            font-weight: 300;
            margin-top: 20px;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }

        .divider {
            width: 80px;
            height: 1px;
            background: rgba(255,255,255,0.6);
            margin: 25px auto;
        }

        .invitation-text {
            font-size: 1.3rem;
            color: rgba(255,255,255,0.95);
            font-style: italic;
            font-weight: 300;
            line-height: 1.8;
            max-width: 500px;
            margin: 0 auto 30px;
            text-shadow: 0 1px 8px rgba(0,0,0,0.3);
        }

        /* Countdown */
        .countdown-section {
            margin: 30px 0;
            padding: 25px 35px;
            background: rgba(255,255,255,0.15);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            border: 1px solid rgba(255,255,255,0.2);
        }

        .countdown-title {
            font-size: 1rem;
            color: rgba(255,255,255,0.9);
            letter-spacing: 4px;
            text-transform: uppercase;
            margin-bottom: 20px;
            font-weight: 400;
        }

        .countdown {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .countdown-item {
            text-align: center;
            min-width: 70px;
        }

        .countdown-value {
            font-size: 2.8rem;
            font-weight: 300;
            color: #fff;
            line-height: 1;
            text-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }

        .countdown-label {
            font-size: 0.85rem;
            color: rgba(255,255,255,0.8);
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-top: 8px;
        }

        /* Details section */
        .details {
            margin-top: 35px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .detail-card {
            background: rgba(255,255,255,0.12);
            backdrop-filter: blur(10px);
            border-radius: 16px;
            padding: 22px 28px;
            border: 1px solid rgba(255,255,255,0.15);
            transition: transform 0.3s ease, background 0.3s ease;
        }

        .detail-card:hover {
            transform: translateY(-3px);
            background: rgba(255,255,255,0.2);
        }

        .detail-time {
            font-size: 1.8rem;
            color: #fff;
            font-weight: 400;
            letter-spacing: 2px;
        }

        .detail-event {
            font-size: 1.15rem;
            color: rgba(255,255,255,0.95);
            margin-top: 6px;
            font-weight: 400;
        }

        .detail-location {
            font-size: 1rem;
            color: rgba(255,255,255,0.8);
            margin-top: 4px;
            font-style: italic;
        }

        .restaurant-name {
            font-family: 'Great Vibes', cursive;
            font-size: 1.6rem;
            color: #fff;
            margin-top: 4px;
        }

        /* Accept button */
        .accept-btn {
            margin-top: 35px;
            padding: 16px 55px;
            font-family: 'Cormorant Garamond', serif;
            font-size: 1.3rem;
            letter-spacing: 3px;
            text-transform: uppercase;
            color: #5a4a3a;
            background: rgba(255,255,255,0.92);
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.4s ease;
            box-shadow: 0 8px 30px rgba(0,0,0,0.2);
        }

        .accept-btn:hover {
            background: #fff;
            transform: translateY(-3px);
            box-shadow: 0 12px 40px rgba(0,0,0,0.3);
        }

        .accept-btn.accepted {
            background: #8b9a6d;
            color: #fff;
        }

        /* Music player */
        .music-player {
            margin-top: 25px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
            color: rgba(255,255,255,0.85);
            font-size: 0.95rem;
            font-style: italic;
        }

        .music-btn {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            border: 1px solid rgba(255,255,255,0.4);
            background: rgba(255,255,255,0.1);
            color: #fff;
            font-size: 1.1rem;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
            backdrop-filter: blur(5px);
        }

        .music-btn:hover {
            background: rgba(255,255,255,0.25);
            transform: scale(1.1);
        }

        /* Scroll indicator */
        .scroll-down {
            position: absolute;
            bottom: 25px;
            left: 50%;
            transform: translateX(-50%);
            color: rgba(255,255,255,0.7);
            font-size: 1.5rem;
            animation: bounce 2s infinite;
            z-index: 2;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateX(-50%) translateY(0); }
            40% { transform: translateX(-50%) translateY(-10px); }
            60% { transform: translateX(-50%) translateY(-5px); }
        }

        /* Second section - light theme */
        .info-section {
            background: #faf8f5;
            padding: 80px 20px;
            text-align: center;
        }

        .info-container {
            max-width: 600px;
            margin: 0 auto;
        }

        .section-title {
            font-family: 'Great Vibes', cursive;
            font-size: 3rem;
            color: #5a4a3a;
            margin-bottom: 25px;
        }

        .section-text {
            font-size: 1.2rem;
            color: #7a6a5a;
            line-height: 1.9;
            font-weight: 400;
        }

        .heart-divider {
            color: #c9a87c;
            font-size: 1.5rem;
            margin: 25px 0;
            letter-spacing: 10px;
        }

        /* Footer */
        .footer {
            background: #f0ece5;
            padding: 30px 20px;
            text-align: center;
            color: #9a8a7a;
            font-size: 0.95rem;
            font-style: italic;
        }

        /* Responsive */
        @media (max-width: 600px) {
            .names { font-size: 3.5rem; }
            .subtitle { font-size: 1rem; letter-spacing: 4px; }
            .date-main { font-size: 1.6rem; letter-spacing: 4px; }
            .countdown-value { font-size: 2rem; }
            .countdown { gap: 12px; }
            .countdown-item { min-width: 55px; }
            .detail-time { font-size: 1.4rem; }
            .section-title { font-size: 2.2rem; }
        }

        /* Pulse animation for heart */
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.15); }
        }

        .heart-icon {
            display: inline-block;
            animation: pulse 2s ease-in-out infinite;
        }
    </style>
</head>
<body>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hearts-container" id="heartsContainer"></div>

        <div class="content">
            <p class="subtitle">Приглашение на свадьбу</p>

            <h1 class="names">Михаил</h1>
            <p class="ampersand">и</p>
            <h1 class="names" style="margin-top: -5px;">Елизавета</h1>

            <p class="date-main">19 . 09 . 2026</p>

            <div class="divider"></div>

            <p class="invitation-text">
                Мы с огромной радостью приглашаем вас разделить с нами<br>
                один из самых важных и счастливых дней в нашей жизни —<br>
                день, когда мы станем семьёй.
            </p>

            <!-- Countdown -->
            <div class="countdown-section">
                <p class="countdown-title">До нашей свадьбы осталось</p>
                <div class="countdown" id="countdown">
                    <div class="countdown-item">
                        <div class="countdown-value" id="days">00</div>
                        <div class="countdown-label">Дней</div>
                    </div>
                    <div class="countdown-item">
                        <div class="countdown-value" id="hours">00</div>
                        <div class="countdown-label">Часов</div>
                    </div>
                    <div class="countdown-item">
                        <div class="countdown-value" id="minutes">00</div>
                        <div class="countdown-label">Минут</div>
                    </div>
                    <div class="countdown-item">
                        <div class="countdown-value" id="seconds">00</div>
                        <div class="countdown-label">Секунд</div>
                    </div>
                </div>
            </div>

            <!-- Event Details -->
            <div class="details">
                <div class="detail-card">
                    <div class="detail-time">11:20</div>
                    <div class="detail-event">Церемония в ЗАГСе</div>
                </div>

                <div class="detail-card">
                    <div class="detail-time">15:00</div>
                    <div class="detail-event">Посадка гостей в банкетном зале</div>
                    <div class="restaurant-name">Imperial Sparta</div>
                    <div class="detail-location">станица Ессентукская, ул. Гагарина, 66</div>
                </div>
            </div>

            <!-- Accept Button -->
            <button class="accept-btn" id="acceptBtn" onclick="acceptInvitation()">
                <span class="heart-icon">&#10084;</span> Принять приглашение
            </button>

            <!-- Music Player -->
            <div class="music-player">
                <button class="music-btn" id="musicBtn" onclick="toggleMusic()">&#9658;</button>
                <span>Christina Perri — A Thousand Years</span>
            </div>
        </div>

        <div class="scroll-down">&#10094;</div>
    </section>

    <!-- Info Section -->
    <section class="info-section">
        <div class="info-container">
            <h2 class="section-title">Дорогие гости!</h2>

            <p class="section-text">
                Для нас большая честь разделить этот незабываемый день с самыми близкими и дорогими людьми.
                Будем счастливы видеть каждого из вас рядом, когда произнесём самые важные слова в нашей жизни.
            </p>

            <div class="heart-divider">&#10084; &#10084; &#10084;</div>

            <p class="section-text">
                Просим подтвердить ваше присутствие до <strong>1 сентября 2026 года</strong>,<br>
                чтобы мы могли всё тщательно подготовить и встретить вас с радостью.
            </p>

            <div class="heart-divider">&#10084; &#10084; &#10084;</div>

            <p class="section-text" style="font-style: italic; color: #9a8a7a;">
                С любовью,<br>
                <span style="font-family: 'Great Vibes', cursive; font-size: 1.8rem; color: #5a4a3a;">Михаил & Елизавета</span>
            </p>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        19 сентября 2026 года &bull; Михаил и Елизавета
    </footer>

    <!-- Audio (YouTube embed for A Thousand Years) -->
    <div id="player" style="display: none;"></div>

    <script src="https://www.youtube.com/iframe_api"></script>
    <script>
        // ===== Floating Hearts Animation =====
        function createHearts() {
            const container = document.getElementById('heartsContainer');
            const heartSymbols = ['&#10084;', '&#9829;', '&#9830;'];

            for (let i = 0; i < 25; i++) {
                const heart = document.createElement('div');
                heart.className = 'heart';
                heart.innerHTML = heartSymbols[Math.floor(Math.random() * heartSymbols.length)];
                heart.style.left = Math.random() * 100 + '%';
                heart.style.fontSize = (Math.random() * 20 + 12) + 'px';
                heart.style.animationDuration = (Math.random() * 8 + 8) + 's';
                heart.style.animationDelay = (Math.random() * 10) + 's';
                heart.style.color = `rgba(255, ${200 + Math.random() * 55}, ${200 + Math.random() * 55}, ${Math.random() * 0.4 + 0.2})`;
                container.appendChild(heart);
            }
        }
        createHearts();

        // ===== Countdown Timer =====
        function updateCountdown() {
            const weddingDate = new Date('2026-09-19T11:20:00').getTime();
            const now = new Date().getTime();
            const diff = weddingDate - now;

            if (diff > 0) {
                const days = Math.floor(diff / (1000 * 60 * 60 * 24));
                const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((diff % (1000 * 60)) / 1000);

                document.getElementById('days').textContent = String(days).padStart(2, '0');
                document.getElementById('hours').textContent = String(hours).padStart(2, '0');
                document.getElementById('minutes').textContent = String(minutes).padStart(2, '0');
                document.getElementById('seconds').textContent = String(seconds).padStart(2, '0');
            }
        }
        updateCountdown();
        setInterval(updateCountdown, 1000);

        // ===== Accept Invitation =====
        function acceptInvitation() {
            const btn = document.getElementById('acceptBtn');
            btn.classList.add('accepted');
            btn.innerHTML = '<span class="heart-icon">&#10084;</span> Приглашение принято!';
            btn.disabled = true;

            // Create celebration hearts
            for (let i = 0; i < 15; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.innerHTML = '&#10084;';
                    heart.style.position = 'fixed';
                    heart.style.left = (Math.random() * 100) + '%';
                    heart.style.top = '50%';
                    heart.style.fontSize = (Math.random() * 25 + 15) + 'px';
                    heart.style.color = '#c9a87c';
                    heart.style.pointerEvents = 'none';
                    heart.style.zIndex = '9999';
                    heart.style.animation = `floatUp ${Math.random() * 2 + 2}s ease-out forwards`;
                    document.body.appendChild(heart);
                    setTimeout(() => heart.remove(), 4000);
                }, i * 100);
            }
        }

        // ===== Music Player =====
        let player;
        let isPlaying = false;

        function onYouTubeIframeAPIReady() {
            player = new YT.Player('player', {
                height: '0',
                width: '0',
                videoId: 'rtOvBOTyX00',
                playerVars: {
                    autoplay: 0,
                    loop: 1,
                    playlist: 'rtOvBOTyX00'
                },
                events: {
                    onReady: function(event) {
                        player.setVolume(40);
                    }
                }
            });
        }

        function toggleMusic() {
            const btn = document.getElementById('musicBtn');
            if (!isPlaying) {
                if (player && player.playVideo) {
                    player.playVideo();
                    btn.innerHTML = '&#10074;&#10074;';
                    isPlaying = true;
                }
            } else {
                if (player && player.pauseVideo) {
                    player.pauseVideo();
                    btn.innerHTML = '&#9658;';
                    isPlaying = false;
                }
            }
        }
    </script>

</body>
</html>
