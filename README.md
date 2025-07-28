<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Animated Starfield</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: #000000;
            overflow: hidden;
            font-family: 'Courier New', monospace;
        }
        
        #starfield {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background: #000000;
        }
        
        .star {
            position: absolute;
            background: white;
            border-radius: 50%;
            animation: twinkle 2s infinite alternate;
        }
        
        .star.small {
            width: 1px;
            height: 1px;
        }
        
        .star.medium {
            width: 2px;
            height: 2px;
        }
        
        .star.large {
            width: 3px;
            height: 3px;
        }
        
        @keyframes twinkle {
            0% { opacity: 0.3; }
            100% { opacity: 1; }
        }
        
        @keyframes moveRight {
            0% { transform: translateX(-10px); }
            100% { transform: translateX(100vw); }
        }
        
        @keyframes moveLeft {
            0% { transform: translateX(100vw); }
            100% { transform: translateX(-10px); }
        }
        
        @keyframes moveDown {
            0% { transform: translateY(-10px); }
            100% { transform: translateY(100vh); }
        }
        
        @keyframes moveUp {
            0% { transform: translateY(100vh); }
            100% { transform: translateY(-10px); }
        }
        
        @keyframes moveDiagonal1 {
            0% { transform: translate(-10px, -10px); }
            100% { transform: translate(100vw, 100vh); }
        }
        
        @keyframes moveDiagonal2 {
            0% { transform: translate(100vw, -10px); }
            100% { transform: translate(-10px, 100vh); }
        }
        
        .content {
            position: relative;
            z-index: 10;
            color: white;
            text-align: center;
            padding: 50px 20px;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        
        h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            text-shadow: 0 0 20px rgba(255,255,255,0.5);
        }
        
        p {
            font-size: 1.2rem;
            max-width: 600px;
            line-height: 1.6;
            opacity: 0.9;
        }
    </style>
</head>
<body>
    <div id="starfield"></div>
    
    <div class="content">
        <h1>Soufiane Lamribah</h1>
        <p>Full-Stack Developer navigating through the digital cosmos, building scalable applications across the galaxy of web technologies.</p>
    </div>

    <script>
        const starfield = document.getElementById('starfield');
        const starCount = 150;
        
        // Animation types
        const animations = [
            'moveRight',
            'moveLeft', 
            'moveDown',
            'moveUp',
            'moveDiagonal1',
            'moveDiagonal2'
        ];
        
        // Star sizes
        const sizes = ['small', 'medium', 'large'];
        
        function createStar() {
            const star = document.createElement('div');
            star.className = `star ${sizes[Math.floor(Math.random() * sizes.length)]}`;
            
            // Random starting position
            star.style.left = Math.random() * 100 + 'vw';
            star.style.top = Math.random() * 100 + 'vh';
            
            // Random animation
            const animation = animations[Math.floor(Math.random() * animations.length)];
            const duration = Math.random() * 15 + 10; // 10-25 seconds
            const delay = Math.random() * 5; // 0-5 seconds delay
            
            star.style.animation = `${animation} ${duration}s linear ${delay}s infinite, twinkle 2s infinite alternate`;
            
            return star;
        }
        
        // Create initial stars
        for (let i = 0; i < starCount; i++) {
            starfield.appendChild(createStar());
        }
        
        // Continuously add new stars
        setInterval(() => {
            // Remove old stars that are off-screen
            const stars = starfield.querySelectorAll('.star');
            if (stars.length > starCount * 2) {
                stars[0].remove();
            }
            
            // Add new star
            starfield.appendChild(createStar());
        }, 1000);
        
        // Add some shooting stars occasionally
        function createShootingStar() {
            const shootingStar = document.createElement('div');
            shootingStar.style.position = 'absolute';
            shootingStar.style.width = '2px';
            shootingStar.style.height = '2px';
            shootingStar.style.background = 'white';
            shootingStar.style.borderRadius = '50%';
            shootingStar.style.boxShadow = '0 0 6px 2px rgba(255,255,255,0.8)';
            
            const startX = Math.random() * window.innerWidth;
            const startY = Math.random() * window.innerHeight;
            
            shootingStar.style.left = startX + 'px';
            shootingStar.style.top = startY + 'px';
            
            const endX = startX + (Math.random() - 0.5) * 300;
            const endY = startY + (Math.random() - 0.5) * 300;
            
            shootingStar.style.animation = `shootingstar 1.5s ease-out forwards`;
            
            // Add shooting star animation
            const style = document.createElement('style');
            style.textContent = `
                @keyframes shootingstar {
                    0% { 
                        transform: translate(0, 0); 
                        opacity: 0; 
                    }
                    10% { 
                        opacity: 1; 
                    }
                    90% { 
                        opacity: 1; 
                    }
                    100% { 
                        transform: translate(${endX - startX}px, ${endY - startY}px); 
                        opacity: 0; 
                    }
                }
            `;
            document.head.appendChild(style);
            
            starfield.appendChild(shootingStar);
            
            setTimeout(() => {
                shootingStar.remove();
                style.remove();
            }, 1500);
        }
        
        // Create shooting stars every 3-8 seconds
        setInterval(() => {
            if (Math.random() < 0.7) {
                createShootingStar();
            }
        }, Math.random() * 5000 + 3000);
    </script>
</body>
</html>
