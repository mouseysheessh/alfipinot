<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Biodata - Alfi Naura Denaputri</title>
    <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600;700&display=swap" rel="stylesheet" />
    <style>
        /* ─── RESET & BASE ─── */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: 'Quicksand', sans-serif;
            background: linear-gradient(145deg, #0b0e1a 0%, #1a1f2f 100%);
            padding: 20px;
            position: relative;
            overflow-x: hidden;
        }

        /* ─── BINTANG BERKEDIP ─── */
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
            overflow: hidden;
        }

        .star {
            position: absolute;
            background: #fff;
            border-radius: 50%;
            animation: twinkle var(--duration) ease-in-out infinite alternate;
            opacity: 0.3;
        }

        @keyframes twinkle {
            0% {
                opacity: 0.2;
                transform: scale(0.8);
            }
            100% {
                opacity: 1;
                transform: scale(1.2);
            }
        }

        /* ─── KARTU UTAMA ─── */
        .card {
            position: relative;
            z-index: 1;
            max-width: 580px;
            width: 100%;
            background: rgba(255, 255, 255, 0.06);
            backdrop-filter: blur(18px);
            -webkit-backdrop-filter: blur(18px);
            border-radius: 48px 48px 40px 40px;
            padding: 40px 34px 38px;
            box-shadow:
                0 30px 60px rgba(0, 0, 0, 0.7),
                inset 0 1px 0 rgba(255, 255, 255, 0.08);
            border: 1px solid rgba(255, 255, 255, 0.06);
            transition: transform 0.3s ease;
        }

        .card:hover {
            transform: translateY(-4px);
        }

        /* ─── HEADER / AVATAR ─── */
        .header {
            display: flex;
            align-items: center;
            gap: 20px;
            margin-bottom: 28px;
        }

        .avatar {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background: linear-gradient(135deg, #f9d976, #f39c6d);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 34px;
            font-weight: 700;
            color: #1a1f2f;
            flex-shrink: 0;
            box-shadow: 0 8px 24px rgba(243, 156, 109, 0.35);
            border: 2px solid rgba(255, 255, 255, 0.15);
        }

        .title-group h1 {
            font-size: 24px;
            font-weight: 700;
            color: #f0edea;
            letter-spacing: 0.5px;
            line-height: 1.2;
        }

        .title-group .subhead {
            font-size: 14px;
            font-weight: 600;
            color: #f39c6d;
            letter-spacing: 1.2px;
            text-transform: uppercase;
            margin-top: 2px;
            opacity: 0.9;
        }

        /* ─── GARIS DEKORATIF ─── */
        .divider {
            width: 60px;
            height: 3px;
            background: linear-gradient(90deg, #f39c6d, #f9d976);
            border-radius: 4px;
            margin: 6px 0 22px 0;
        }

        /* ─── INFO GRID ─── */
        .info-grid {
            display: flex;
            flex-direction: column;
            gap: 14px;
        }

        .info-item {
            display: flex;
            align-items: flex-start;
            gap: 14px;
            padding: 10px 16px 10px 14px;
            background: rgba(255, 255, 255, 0.04);
            border-radius: 18px;
            border-left: 3px solid rgba(243, 156, 109, 0.5);
            transition: background 0.2s;
        }

        .info-item:hover {
            background: rgba(255, 255, 255, 0.07);
        }

        .info-icon {
            font-size: 20px;
            width: 32px;
            text-align: center;
            flex-shrink: 0;
            margin-top: 1px;
        }

        .info-content {
            flex: 1;
        }

        .info-label {
            font-size: 11px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1.2px;
            color: rgba(255, 255, 255, 0.35);
            margin-bottom: 2px;
        }

        .info-value {
            font-size: 17px;
            font-weight: 600;
            color: #f0edea;
            line-height: 1.4;
            word-break: break-word;
        }

        .info-value .highlight {
            color: #f9d976;
        }

        .info-value .badge {
            display: inline-block;
            background: rgba(243, 156, 109, 0.18);
            padding: 2px 12px;
            border-radius: 30px;
            font-size: 14px;
            font-weight: 600;
            color: #f9d976;
            margin-right: 6px;
        }

        /* ─── HOBBY TAG ─── */
        .hobby-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 4px;
        }

        .hobby-tag {
            background: rgba(255, 255, 255, 0.07);
            padding: 4px 16px 4px 14px;
            border-radius: 30px;
            font-size: 14px;
            font-weight: 600;
            color: #e0dbd4;
            border: 1px solid rgba(255, 255, 255, 0.06);
            display: inline-flex;
            align-items: center;
            gap: 6px;
        }

        .hobby-tag .emoji {
            font-size: 16px;
        }

        /* ─── MOTTO / KUTIPAN ─── */
        .motto-section {
            margin-top: 28px;
            padding: 20px 20px 18px;
            background: rgba(243, 156, 109, 0.08);
            border-radius: 24px;
            border: 1px solid rgba(243, 156, 109, 0.12);
            position: relative;
        }

        .motto-section::before {
            content: "“";
            position: absolute;
            top: 4px;
            left: 14px;
            font-size: 44px;
            font-weight: 700;
            color: rgba(243, 156, 109, 0.2);
            line-height: 1;
            font-family: Georgia, serif;
        }

        .motto-text {
            font-size: 16px;
            font-weight: 600;
            color: #f0edea;
            line-height: 1.6;
            padding-left: 18px;
            font-style: italic;
        }

        .motto-text .highlight-gold {
            color: #f9d976;
        }

        .motto-text .highlight-gold-light {
            color: #f5cba0;
        }

        /* ─── TOMBOL LINK ─── */
        .link-wrapper {
            margin-top: 26px;
            text-align: center;
        }

        .btn-link {
            display: inline-flex;
            align-items: center;
            gap: 12px;
            padding: 14px 32px;
            background: linear-gradient(135deg, #f39c6d, #e67e3a);
            border: none;
            border-radius: 60px;
            font-family: 'Quicksand', sans-serif;
            font-size: 16px;
            font-weight: 700;
            color: #1a1f2f;
            text-decoration: none;
            transition: all 0.25s ease;
            box-shadow: 0 8px 28px rgba(243, 156, 109, 0.30);
            letter-spacing: 0.3px;
        }

        .btn-link:hover {
            transform: scale(1.04);
            box-shadow: 0 12px 36px rgba(243, 156, 109, 0.50);
            background: linear-gradient(135deg, #f9d976, #f39c6d);
        }

        .btn-link:active {
            transform: scale(0.97);
        }

        .btn-link .arrow {
            font-size: 20px;
            transition: transform 0.2s;
        }

        .btn-link:hover .arrow {
            transform: translateX(4px);
        }

        /* ─── FOOTER ─── */
        .footer-note {
            margin-top: 20px;
            text-align: center;
            font-size: 12px;
            font-weight: 600;
            color: rgba(255, 255, 255, 0.2);
            letter-spacing: 0.8px;
        }

        /* ─── RESPONSIF ─── */
        @media (max-width: 480px) {
            .card {
                padding: 28px 18px 28px;
                border-radius: 32px;
            }

            .header {
                gap: 14px;
            }

            .avatar {
                width: 64px;
                height: 64px;
                font-size: 26px;
            }

            .title-group h1 {
                font-size: 20px;
            }

            .info-value {
                font-size: 15px;
            }

            .hobby-tag {
                font-size: 12px;
                padding: 3px 12px 3px 10px;
            }

            .motto-text {
                font-size: 14px;
                padding-left: 14px;
            }

            .btn-link {
                padding: 12px 24px;
                font-size: 14px;
                width: 100%;
                justify-content: center;
            }

            .motto-section::before {
                font-size: 34px;
                left: 10px;
            }
        }

        @media (max-width: 380px) {
            .info-item {
                flex-direction: column;
                gap: 2px;
                padding: 10px 12px;
            }

            .info-icon {
                text-align: left;
            }
        }
    </style>
</head>
<body>

    <!-- ─── BINTANG ─── -->
    <div class="stars" id="starsContainer"></div>

    <!-- ─── KARTU BIODATA ─── -->
    <div class="card">

        <!-- HEADER -->
        <div class="header">
            <div class="avatar">AN</div>
            <div class="title-group">
                <h1>Alfi Naura Denaputri</h1>
                <div class="subhead">✦ Biodata ✦</div>
            </div>
        </div>

        <div class="divider"></div>

        <!-- INFO -->
        <div class="info-grid">

            <!-- Tanggal Lahir -->
            <div class="info-item">
                <div class="info-icon">🎂</div>
                <div class="info-content">
                    <div class="info-label">Tanggal Lahir</div>
                    <div class="info-value">25 Agustus 2012</div>
                </div>
            </div>

            <!-- Hobi -->
            <div class="info-item">
                <div class="info-icon">✨</div>
                <div class="info-content">
                    <div class="info-label">Hobi</div>
                    <div class="hobby-tags">
                        <span class="hobby-tag"><span class="emoji">📺</span> K-Drama</span>
                        <span class="hobby-tag"><span class="emoji">✍️</span> Menulis Cerita</span>
                    </div>
                </div>
            </div>

            <!-- Cita-cita -->
            <div class="info-item">
                <div class="info-icon">🔍</div>
                <div class="info-content">
                    <div class="info-label">Cita-cita</div>
                    <div class="info-value"><span class="badge">🕵️</span> Detektif</div>
                </div>
            </div>

        </div>

        <!-- MOTTO / KUTIPAN -->
        <div class="motto-section">
            <div class="motto-text">
                <span class="highlight-gold">"</span>hidupku hanya sampai esok hari<br />
                jadi aku harus <span class="highlight-gold">bahagia</span> dan <span class="highlight-gold">berhasil</span><br />
                dan apapun yang terjadi<br />
                <span class="highlight-gold-light">kehendak tuhan pasti ada baiknya</span><span class="highlight-gold">"</span>
            </div>
        </div>

        <!-- TOMBOL LINK -->
        <div class="link-wrapper">
            <a href="https://mouseysheessh.github.io/aplikasi-game-3-pesawat-/" target="_blank" class="btn-link">
                <span>🚀 Mainkan Game Pesawat</span>
                <span class="arrow">→</span>
            </a>
        </div>

        <div class="footer-note">✦ dibuat dengan semangat ✦</div>

    </div>

    <script>
        // ─── GENERATE BINTANG ───
        (function createStars() {
            const container = document.getElementById('starsContainer');
            const count = 120;

            for (let i = 0; i < count; i++) {
                const star = document.createElement('div');
                star.classList.add('star');

                const size = Math.random() * 3 + 1.5;
                const x = Math.random() * 100;
                const y = Math.random() * 100;
                const duration = Math.random() * 3 + 2;
                const delay = Math.random() * 5;

                star.style.width = size + 'px';
                star.style.height = size + 'px';
                star.style.left = x + '%';
                star.style.top = y + '%';
                star.style.setProperty('--duration', duration + 's');
                star.style.animationDelay = delay + 's';

                container.appendChild(star);
            }
        })();
    </script>

</body>
</html>
