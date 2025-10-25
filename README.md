<!DOCTYPE html> 
<html lang="ru"> 
<head> 
    <meta charset="UTF-8"> 
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
    <title>Ангелина - Веб-разработчик</title>
    <style>
        body {
            font-family: 'Inter', system-ui, sans-serif;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            position: relative;
            overflow-x: hidden;
        }
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        .star {
            position: absolute;
            background: white;
            border-radius: 50%;
            animation: twinkle 3s infinite;
        }
        @keyframes twinkle {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 1; }
        }
        .hero-section {
            display: flex;
            align-items: center;
            max-width: 1100px;
            margin: 0 auto;
            padding: 40px 20px;
            min-height: 100vh;
            gap: 60px;
            position: relative;
            z-index: 1;
        }
        .hero-content {
            flex: 1;
            margin-top: -60px;
        }
        .hero-content h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            font-weight: 700;
        }
        .hero-content h1 span {
            color: #FFD700;
        }
        .hero-content h2 {
            font-size: 1.5rem;
            margin-bottom: 25px;
            color: rgba(255, 255, 255, 0.9);
            font-weight: 400;
            position: relative;
            padding-left: 20px;
        }
        .hero-content h2::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            height: 100%;
            width: 4px;
            background: #FFD700;
            border-radius: 2px;
        }
        .hero-description {
            font-size: 1.1rem;
            margin-bottom: 30px;
            color: rgba(255, 255, 255, 0.8);
            line-height: 1.7;
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 12px;
            border-left: 4px solid #ef7e0d;
        }
        .cta-button {
            display: inline-block;
            padding: 15px 30px;
            background: #ef7e0d;
            color: white;
            text-decoration: none;
            border-radius: 25px;
            font-weight: 600;
            box-shadow: 0 4px 15px rgba(239, 126, 13, 0.3);
        }
        .hero-image {
            flex: 1;
            text-align: center;
            position: relative;
        }
        .hero-image img {
            width: 400px;
            height: 400px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid rgba(255, 255, 255, 0.3);
        }
        .small-circle {
            position: absolute;
            top: 20px;
            right: 20px;
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 3px solid #FFD700;
            overflow: hidden;
            background: white;
        }
        .small-circle img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border: none;
        }
        .tech-stack {
            margin-top: 25px;
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }
        .tech-item {
            background: rgba(255, 255, 255, 0.15);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
    </style>
</head> 
<body>
    <div class="stars" id="stars"></div>
    <section class="hero-section">
        <div class="hero-content">
            <h1>Привет! Я <span>Ангелина</span> — веб-разработчик</h1>
            <h2>Создаю современные веб-приложения и интерфейсы. Специализируюсь на разработке современных веб-решений. Изучаю современные технологии.</h2>
            <p class="hero-description">Тотемное животное - ленивец</p>
            <a href="#contact" class="cta-button">Связаться со мной</a>
        </div>
        <div class="hero-image">
            <img src="D:\3 курс 1 сем\WEB-дизайн\img\я.jpg" alt="Ангелина - веб-разработчик">
            <div class="small-circle">
                <img src="D:\3 курс 1 сем\WEB-дизайн\img\ленивец.jpg" alt="Ленивец">
            </div>
        </div>
    </section>

    <script>
        // Создание звездочек
        const starsContainer = document.getElementById('stars');
        const starsCount = 100;
        
        for (let i = 0; i < starsCount; i++) {
            const star = document.createElement('div');
            star.className = 'star';
            
            // Случайные параметры для звездочек
            const size = Math.random() * 3 + 1; // Размер от 1px до 4px
            const left = Math.random() * 100; // Позиция по горизонтали
            const top = Math.random() * 100; // Позиция по вертикали
            const delay = Math.random() * 3; // Задержка анимации
            
            star.style.width = `${size}px`;
            star.style.height = `${size}px`;
            star.style.left = `${left}%`;
            star.style.top = `${top}%`;
            star.style.animationDelay = `${delay}s`;
            
            starsContainer.appendChild(star);
        }
    </script>
</body> 
</html>
