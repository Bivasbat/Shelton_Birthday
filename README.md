<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday! - Minecraft Theme</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #5B7C3D; /* Minecraft grass green */
            color: white;
            text-align: center;
            margin: 0;
            padding: 0;
            background-image: url('https://www.minecraft.net/content/dam/games/minecraft/key-art/Minecraft-xbox-one.jpg');
            background-size: 300px;
            image-rendering: pixelated;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.7);
            border: 8px solid #8B8B8B;
            border-image: url('image') 8 stretch;
            margin-top: 50px;
            border-radius: 5px;
        }
        
        h1 {
            color: #FFAA00; /* Minecraft gold */
            font-size: 3em;
            text-shadow: 3px 3px 0 #000;
        }
        
        .minecraft-text {
            font-family: 'Minecraft', monospace;
            image-rendering: pixelated;
        }
        
        .cake {
            width: 200px;
            height: 200px;
            margin: 20px auto;
            background-image: url('https://www.amysbakehouse.co.uk/cdn/shop/products/minecraft_e08a18b3-edc9-4ee2-b047-105d51f1ca89.jpg?v=1678803293');
            background-size: cover;
            image-rendering: pixelated;
        }
        
        .creeper {
            width: 100px;
            height: 100px;
            margin: 20px auto;
            background-image: url('https://static1.srcdn.com/wordpress/wp-content/uploads/2021/10/Minecraft-Surprise-Birthday-Party.jpg');
            background-size: cover;
            image-rendering: pixelated;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }
        
        .message {
            background-color: #3B3B3B;
            padding: 20px;
            border: 4px solid #5B5B5B;
            margin: 20px 0;
            text-align: left;
        }
        
        button {
            background-color: #5B7C3D;
            color: white;
            border: 4px solid #3B5C1D;
            padding: 10px 20px;
            font-size: 1.2em;
            cursor: pointer;
            margin: 10px;
            font-family: 'Minecraft', monospace;
        }
        
        button:hover {
            background-color: #7B9C5D;
        }
        
        .firework {
            position: absolute;
            width: 5px;
            height: 5px;
            background-color: #FFAA00;
            border-radius: 50%;
            animation: explode 1s forwards;
            opacity: 0;
        }
        
        @keyframes explode {
            0% { transform: scale(0); opacity: 0; }
            50% { opacity: 1; }
            100% { transform: scale(20); opacity: 0; }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 class="minecraft-text">HAPPY BIRTHDAY!</h1>
        
        <div class="cake"></div>
        
        <div class="message">
            <p>Dear Shelton Blake,</p>
            <p>Gusto ko happy ka sa birthday mo! 🎉</p>
            <p>Love love  ka ng buong family at ni Brown! Hehehe!</p>
            <p>Love,</p>
            <p>Tita Ganda</p>
        </div>
        
        <div class="creeper"></div>
        
        <button onclick="launchFireworks()">Click for Fireworks!</button>
    </div>
    
    <script>
        function launchFireworks() {
            const colors = ['#FFAA00', '#FF5555', '#55FF55', '#5555FF', '#FFFFFF'];
            
            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    const firework = document.createElement('div');
                    firework.className = 'firework';
                    firework.style.left = Math.random() * 100 + 'vw';
                    firework.style.top = Math.random() * 100 + 'vh';
                    firework.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                    document.body.appendChild(firework);
                    
                    // Remove firework after animation
                    setTimeout(() => {
                        firework.remove();
                    }, 1000);
                }, i * 100);
            }
        }
    </script>
</body>
</html>
