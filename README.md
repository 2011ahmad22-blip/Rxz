<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rxz Script | Ultimate Hub</title>
    <style>
        :root {
            --primary-color: #ffffff;
            --accent-color: #3a86ff; /* لون أزرق خفيف للتفاعل */
            --bg-dark: #050505;
            --card-bg: rgba(255, 255, 255, 0.03);
            --border-color: rgba(255, 255, 255, 0.1);
        }

        body {
            margin: 0;
            padding: 0;
            background-color: var(--bg-dark);
            color: var(--primary-color);
            font-family: 'Inter', 'Segoe UI', system-ui, -apple-system, sans-serif;
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* خلفية النجوم المتحركة المتطورة */
        #canvas-stars {
            position: fixed;
            top: 0;
            left: 0;
            z-index: -1;
        }

        /* الهيدر */
        header {
            padding: 120px 20px 60px;
            text-align: center;
        }

        .badge {
            background: linear-gradient(90deg, rgba(58, 134, 255, 0.2), rgba(255, 255, 255, 0.1));
            padding: 6px 18px;
            border-radius: 50px;
            font-size: 0.85rem;
            border: 1px solid var(--border-color);
            display: inline-block;
            margin-bottom: 20px;
            animation: pulse 2s infinite;
        }

        h1 {
            font-size: clamp(3rem, 10vw, 5rem);
            margin: 0;
            font-weight: 900;
            background: linear-gradient(to bottom, #fff 40%, #666 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: -2px;
        }

        .subtitle {
            font-size: 1.4rem;
            color: #888;
            margin-top: -10px;
            font-weight: 300;
        }

        /* حاوية السكربتات */
        .container {
            max-width: 850px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .script-card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 20px;
            padding: 24px;
            margin-bottom: 25px;
            backdrop-filter: blur(12px);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            position: relative;
            overflow: hidden;
        }

        .script-card:hover {
            transform: translateY(-8px);
            border-color: rgba(255, 255, 255, 0.3);
            box-shadow: 0 20px 40px rgba(0,0,0,0.4);
        }

        .script-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }

        .script-name {
            font-size: 1.25rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .script-name::before {
            content: '';
            width: 8px;
            height: 8px;
            background: #3a86ff;
            border-radius: 50%;
            box-shadow: 0 0 10px #3a86ff;
        }

        .lua-box {
            background: #000000;
            padding: 18px;
            border-radius: 12px;
            font-family: 'Fira Code', 'Courier New', monospace;
            font-size: 0.85rem;
            color: #9cdcfe;
            direction: ltr;
            overflow-x: auto;
            border: 1px solid #1a1a1a;
            white-space: nowrap;
        }

        .copy-btn {
            margin-top: 15px;
            background: #fff;
            color: #000;
            border: none;
            padding: 12px 25px;
            border-radius: 10px;
            cursor: pointer;
            font-weight: 700;
            transition: 0.2s;
            width: 100%;
        }

        .copy-btn:hover {
            background: #e0e0e0;
            transform: scale(1.02);
        }

        /* قسم الديسكورد المطور */
        .discord-card {
            background: linear-gradient(135deg, #5865F2 0%, #3a44a9 100%);
            border-radius: 24px;
            padding: 40px;
            text-align: center;
            margin: 80px 0;
            color: white;
        }

        .discord-btn {
            background: white;
            color: #5865F2;
            text-decoration: none;
            padding: 14px 35px;
            border-radius: 12px;
            display: inline-block;
            font-weight: 800;
            margin-top: 20px;
            transition: 0.3s;
        }

        .discord-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        footer {
            padding: 60px 20px;
            text-align: center;
            color: #444;
            border-top: 1px solid var(--border-color);
        }

        @keyframes pulse {
            0% { opacity: 0.6; }
            50% { opacity: 1; }
            100% { opacity: 0.6; }
        }

        /* تخصيص السكرول بار */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #050505; }
        ::-webkit-scrollbar-thumb { background: #222; border-radius: 10px; }
        ::-webkit-scrollbar-thumb:hover { background: #333; }
    </style>
</head>
<body>

<canvas id="canvas-stars"></canvas>

<header>
    <div class="badge">V2.0 — نظام الحماية الجديد مفعل</div>
    <h1>Rxz</h1>
    <div class="subtitle">PREMIUM SCRIPTS</div>
</header>

<div class="container">
    <div class="script-card">
        <div class="script-header">
            <span class="script-name">Alone Hub</span>
        </div>
        <div class="lua-box" id="s1">loadstring(game:HttpGet("https://raw.githubusercontent.com/salihmahdu11-oss/SA-ALONE/refs/heads/main/SA%20%7C%20PVP"))()</div>
        <button class="copy-btn" onclick="copyText('s1')">نسخ الكود 📋</button>
    </div>

    <div class="script-card">
        <div class="script-header">
            <span class="script-name">Z3 Executor</span>
        </div>
        <div class="lua-box" id="s2">loadstring(game:HttpGet("https://api.luarmor.net/files/v4/loaders/89e7717db605d4502c0b92a1a77e49f8.lua"))()</div>
        <button class="copy-btn" onclick="copyText('s2')">نسخ الكود 📋</button>
    </div>

    <div class="discord-card">
        <h2>هل تحتاج مساعدة؟</h2>
        <p>انضم إلى أكثر من 5,000 مطور ولاعب في مجتمعنا</p>
        <a href="https://discord.gg/rxz" class="discord-btn">دخول السيرفر الرسمي</a>
    </div>
</div>

<footer>
    <p>© 2026 Rxz Script Hub. Built for the community.</p>
</footer>

<script>
    // وظيفة النسخ مع تنبيه مودرن
    function copyText(id) {
        const text = document.getElementById(id).innerText;
        navigator.clipboard.writeText(text).then(() => {
            const btn = event.target;
            const originalText = btn.innerText;
            btn.innerText = '✅ تم النسخ!';
            btn.style.background = '#4CAF50';
            btn.style.color = '#fff';
            
            setTimeout(() => {
                btn.innerText = originalText;
                btn.style.background = '#fff';
                btn.style.color = '#000';
            }, 2000);
        });
    }

    // نظام خلفية النجوم المتقدم (Canvas) للأداء الأفضل
    const canvas = document.getElementById('canvas-stars');
    const ctx = canvas.getContext('2d');
    let stars = [];

    function resize() {
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;
    }

    window.addEventListener('resize', resize);
    resize();

    for(let i = 0; i < 200; i++) {
        stars.push({
            x: Math.random() * canvas.width,
            y: Math.random() * canvas.height,
            size: Math.random() * 1.5,
            speed: Math.random() * 0.5 + 0.2
        });
    }

    function animate() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        ctx.fillStyle = '#fff';
        stars.forEach(star => {
            star.y -= star.speed;
            if(star.y < 0) star.y = canvas.height;
            ctx.beginPath();
            ctx.arc(star.x, star.y, star.size, 0, Math.PI * 2);
            ctx.fill();
        });
        requestAnimationFrame(animate);
    }
    animate();
</script>

</body>
</html>
