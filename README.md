<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Nibaan! 🫏</title>
    
    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Bangers&family=Comic+Neue:wght@400;700&display=swap" rel="stylesheet">

    <style>
        /* --- RESET & BASICS --- */
        * { box-sizing: border-box; margin: 0; padding: 0; }

        body {
            font-family: 'Comic Neue', cursive;
            background: linear-gradient(45deg, #ff00cc, #3333ff, #ffcc00, #ff3333);
            background-size: 400% 400%;
            animation: gradientBG 10s ease infinite;
            color: #fff;
            overflow-x: hidden;
            text-align: center;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            -webkit-tap-highlight-color: transparent;
            user-select: none;
            perspective: 1000px; /* For 3D effects */
        }

        /* --- ANIMATIONS --- */
        @keyframes gradientBG { 0% { background-position: 0% 50%; } 50% { background-position: 100% 50%; } 100% { background-position: 0% 50%; } }
        @keyframes float { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-20px); } }
        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
        @keyframes shake { 0% { transform: translate(1px, 1px) rotate(0deg); } 10% { transform: translate(-1px, -2px) rotate(-1deg); } 20% { transform: translate(-3px, 0px) rotate(1deg); } 30% { transform: translate(3px, 2px) rotate(0deg); } 40% { transform: translate(1px, -1px) rotate(1deg); } 50% { transform: translate(-1px, 2px) rotate(-1deg); } 60% { transform: translate(-3px, 1px) rotate(0deg); } 70% { transform: translate(3px, 1px) rotate(-1deg); } 80% { transform: translate(-1px, -1px) rotate(1deg); } 90% { transform: translate(1px, 2px) rotate(0deg); } 100% { transform: translate(1px, -2px) rotate(-1deg); } }
        @keyframes popIn { 0% { opacity: 0; transform: scale(0); } 80% { opacity: 1; transform: scale(1.1); } 100% { transform: scale(1); } }
        
        @keyframes scanMove { 
            0% { top: 10%; left: 10%; } 
            25% { top: 10%; left: 80%; }
            50% { top: 80%; left: 80%; } 
            75% { top: 80%; left: 10%; }
            100% { top: 10%; left: 10%; } 
        }

        @keyframes holoShine {
            0% { background-position: 0% 50%; }
            100% { background-position: 100% 50%; }
        }

        /* --- UTILITY CLASSES --- */
        .hidden { display: none !important; }
        .show { display: block !important; animation: popIn 0.5s ease-out; }
        .shake-element { animation: shake 0.5s; }
        .rainbow-mode { animation: gradientBG 0.5s linear infinite !important; }
        
        h1, h2, h3 {
            font-family: 'Bangers', cursive;
            letter-spacing: 2px;
            text-shadow: 3px 3px 0px #000;
        }

        .container {
            width: 90%;
            max-width: 600px;
            margin: 20px auto;
            padding: 20px;
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            border: 4px solid #fff;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            position: relative;
            z-index: 10;
        }

        /* --- COMPONENTS --- */
        .btn {
            background: #ffcc00;
            color: #000;
            border: 4px solid #000;
            padding: 15px 30px;
            font-size: 1.5rem;
            font-family: 'Bangers', cursive;
            cursor: pointer;
            border-radius: 50px;
            transition: all 0.2s;
            margin-top: 20px;
            box-shadow: 5px 5px 0px #000;
            text-transform: uppercase;
        }

        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 8px 8px 0px #000;
            background: #fff;
        }

        .author-credit {
            font-size: 1.2rem;
            color: #fff;
            background: #000;
            padding: 5px 15px;
            border-radius: 20px;
            display: inline-block;
            margin-bottom: 15px;
            border: 2px solid #ffcc00;
            transform: rotate(-1deg);
        }

        .donkey-avatar {
            font-size: 8rem;
            display: inline-block;
            filter: drop-shadow(0 0 10px rgba(0,0,0,0.5));
            cursor: pointer;
        }
        
        .spinning { animation: spin 3s linear infinite; }

        /* --- ROAST & SCANNER --- */
        .roast-line {
            font-size: 1.4rem;
            margin: 10px 0;
            padding: 10px;
            background: rgba(0,0,0,0.7);
            border-radius: 10px;
            border: 2px dashed #fff;
            color: #ffeb3b;
        }

        /* Custom Scanning Visual */
        #visual-scanner {
            position: relative;
            width: 300px;
            height: 300px;
            margin: 20px auto;
            border: 4px solid #fff;
            background: rgba(255,255,255,0.9);
            border-radius: 20px;
            overflow: hidden;
        }

        #scan-donkey {
            font-size: 10rem;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 1;
            font-family: "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
        }

        #magnifying-glass {
            font-size: 4rem;
            position: absolute;
            z-index: 10;
            animation: scanMove 3s linear infinite;
        }

        .head-poop {
            position: absolute;
            font-size: 2.5rem;
            top: 65px;
            left: 65px; 
            z-index: 5;
            display: none;
        }

        .knee-brain {
            position: absolute;
            font-size: 1.8rem;
            bottom: 70px;
            left: 110px;
            z-index: 5;
            display: none;
            background: yellow;
            border-radius: 50%;
            padding: 2px;
            border: 2px solid red;
        }

        #scan-status {
            font-weight: bold; 
            color: red; 
            font-size: 1.2rem;
            margin-top: 10px;
        }

        /* --- TERMINAL (LEAKED HISTORY) --- */
        .terminal-box {
            background: #000;
            color: #00ff00;
            font-family: 'Courier New', monospace;
            padding: 15px;
            border-radius: 10px;
            border: 2px solid #00ff00;
            text-align: left;
            margin-top: 20px;
            min-height: 150px;
            font-size: 0.9rem;
            box-shadow: 0 0 10px #00ff00;
        }
        .terminal-line { margin-bottom: 5px; opacity: 0; }
        .fade-in { opacity: 1; transition: opacity 0.5s; }

        /* --- 3D ID CARD (REPLACES CERTIFICATE) --- */
        .flip-container {
            background-color: transparent;
            width: 300px;
            height: 450px;
            perspective: 1000px;
            margin: 20px auto;
            cursor: pointer;
        }

        .flip-card-inner {
            position: relative;
            width: 100%;
            height: 100%;
            text-align: center;
            transition: transform 0.8s;
            transform-style: preserve-3d;
        }

        .flip-container.flipped .flip-card-inner {
            transform: rotateY(180deg);
        }

        .flip-card-front, .flip-card-back {
            position: absolute;
            width: 100%;
            height: 100%;
            -webkit-backface-visibility: hidden;
            backface-visibility: hidden;
            border-radius: 15px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            box-shadow: 0 10px 20px rgba(0,0,0,0.5);
            border: 4px solid #fff;
        }

        /* Front Side: Secret Folder */
        .flip-card-front {
            background: #333;
            color: white;
            background-image: repeating-linear-gradient(
                45deg,
                #333 0px,
                #333 10px,
                #444 10px,
                #444 20px
            );
        }

        /* Back Side: The ID */
        .flip-card-back {
            background: linear-gradient(135deg, #FFD700, #ffcc00, #FFD700);
            color: black;
            transform: rotateY(180deg);
            background-size: 200% 200%;
            animation: holoShine 3s ease infinite;
            padding: 10px;
        }

        .id-header {
            background: #000;
            color: #fff;
            width: 100%;
            padding: 10px;
            font-family: 'Courier New', monospace;
            font-weight: bold;
            margin-bottom: 10px;
            border-radius: 5px;
        }

        .id-photo {
            width: 120px;
            height: 120px;
            background: #fff;
            border: 3px solid #000;
            border-radius: 10px;
            margin-bottom: 10px;
            font-size: 4rem;
            line-height: 120px;
        }

        .id-stats {
            text-align: left;
            width: 90%;
            font-size: 0.9rem;
            background: rgba(255,255,255,0.5);
            padding: 10px;
            border-radius: 5px;
        }

        /* Canvas for confetti */
        #confetti-canvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 100;
        }

        /* Floating emojis background */
        .bg-emoji {
            position: fixed;
            font-size: 2rem;
            opacity: 0.3;
            z-index: 0;
            animation: float 5s ease-in-out infinite;
        }

        /* Warning Modal Popup */
        .warning-modal {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: #fff;
            color: #000;
            padding: 20px;
            border: 5px solid #000;
            z-index: 600;
            text-align: center;
            box-shadow: 10px 10px 0px #000;
            display: none;
            width: 320px;
        }
        .warning-modal h2 { text-shadow: none; color: red; }

        /* Security Scanner Section Styles */
        #security-scanner-ui {
            margin: 20px auto;
            max-width: 400px;
            border: 4px dashed #fff;
            padding: 20px;
            background: rgba(0, 0, 0, 0.8);
            border-radius: 15px;
            position: relative;
            overflow: hidden;
        }
        .scan-line-ui {
            width: 100%; height: 4px; background: #00ff00; position: absolute; top: 0; left: 0;
            animation: scanMoveVertical 1.5s linear infinite; display: none; box-shadow: 0 0 15px #00ff00;
        }
        @keyframes scanMoveVertical { 0% { top: 0%; } 100% { top: 100%; } }

    </style>
</head>
<body onclick="initAudio()">

    <canvas id="confetti-canvas"></canvas>
    <div id="emoji-container"></div>

    <!-- MAIN CONTAINER -->
    <div class="container" id="main-card">
        
        <!-- SECTION 1: HERO -->
        <div id="section-hero">
            <p class="author-credit">Gift from your friend Chaitanya Aggarwal</p>
            <div class="subtext">🎂 HAPPY 15th BIRTHDAY NIBAAN 🎂</div>
            <h1>AKA... NODDY</h1>
            <div class="donkey-avatar spinning" onclick="playSound('donkey')">🫏</div>
            <p style="font-size:0.8rem; margin-top:5px;">(Tap the donkey)</p>
            <h2 style="margin-top:20px; color: #ffe600;">15 Years of Being a Walking Meme 💀</h2>
            
            <button class="btn" onclick="startRoast()">Click To Expose True Identity 😈</button>
        </div>

        <!-- SECTION 2: ROAST & VISUAL SCAN -->
        <div id="section-roast" class="hidden">
            <h2>Scanning Subject... 📡</h2>
            <div id="roast-lines"></div>
            
            <!-- FUNNY VISUAL SCANNER -->
            <div id="visual-scanner" class="hidden">
                <div id="magnifying-glass">🔍</div>
                <div id="scan-donkey">🫏</div>
                <div class="head-poop">💩</div>
                <div class="knee-brain">🧠</div>
            </div>
            <p id="scan-status" class="hidden">LOCATING BRAIN CELLS...</p>

            <button id="next-special-btn" class="btn hidden" onclick="goToSpecialGifts()">🎁 Open Top Secret Vault 🎁</button>
        </div>

        <!-- SECTION 3: TOP SECRET ARCHIVES -->
        <div id="section-special-gifts" class="hidden">
            <h2>🎁 TOP SECRET ARCHIVES 🎁</h2>
            <p style="margin-bottom:15px; font-size:1.1rem;">Bio-Metric Scan Required...</p>

            <!-- SCANNER UI -->
            <div id="security-scanner-ui">
                <div class="scan-line-ui" id="scan-line-effect"></div>
                <div style="font-size: 5rem;" id="scanner-icon">🕵️‍♂️</div>
                <div id="scan-text" style="font-family:'Courier New'; color:#00ff00; font-weight:bold; margin-top:10px;">
                    SYSTEM LOCKED<br><span style="font-size:0.8rem; color:#fff;">(Tap to Verify Humanity)</span>
                </div>
                <button id="start-scan-btn" class="btn" style="font-size: 1rem; padding: 10px 20px; margin-top: 15px;" onclick="startSecurityScan()">🔓 START SCAN</button>
            </div>

            <!-- UNLOCKED CONTENT: LEAKED HISTORY -->
            <div id="unlocked-content" class="hidden">
                <h3 style="color: #00ff00; margin-top: 20px; font-size: 2rem;">ACCESS GRANTED! ✅</h3>
                <p style="font-size: 1.2rem; margin-top: 10px; color: yellow;">⚠️ WARNING: LEAKED SEARCH HISTORY ⚠️</p>
                
                <div class="terminal-box" id="terminal-box">
                    <div id="terminal-content"></div>
                </div>

                <button id="reveal-leaks-btn" class="btn" style="background: red; color: #fff; border-color: #fff; margin: 20px 0; padding: 15px;" onclick="revealLeaks()">
                    🕵️‍♂️ READ PRIVATE SEARCHES
                </button>
                
                <br>
                <button class="btn" style="background: #fff; color: #000;" onclick="goToMainGift()">Proceed to Final Surprise ➡️</button>
            </div>
        </div>

        <!-- SECTION 4: MAIN GIFT -->
        <div id="section-gift" class="hidden">
            <h2>UNBOX YOUR SURPRISE! 🎁</h2>
            <p>Click the box gently...</p>
            <div class="gift-box" onclick="openGift()">🎁</div>
            <div id="gift-reveal" class="hidden">
                <h1 style="color: #ff3333; font-size: 3rem; margin-top: 20px;">MORE HOMEWORK! 📚😂</h1>
                <p style="margin: 20px 0; font-size: 1.3rem;">Just kidding.<br>You are already an expert at doing absolutely nothing. 💀🔥</p>
                <div style="font-size: 5rem;" class="shake-element">🫏💃</div>
                <button class="btn" onclick="activateNoddyMode()">Accept You Are Officially 15 🫏</button>
            </div>
        </div>

        <!-- SECTION 5: ID CARD (REPLACES CERTIFICATE) -->
        <div id="section-cert" class="hidden">
            <h1 style="margin-bottom: 10px;">IDENTITY CONFIRMED 🚨</h1>
            <p style="margin-bottom: 20px;">(Tap Card to Flip)</p>

            <div class="flip-container" onclick="this.classList.toggle('flipped'); playSound('boing');">
                <div class="flip-card-inner">
                    <!-- FRONT -->
                    <div class="flip-card-front">
                        <div style="font-size: 5rem;">📁</div>
                        <h2 style="color:red; transform: rotate(-10deg); border: 4px solid red; padding: 5px;">TOP SECRET</h2>
                        <p style="margin-top:20px;">CLASSIFIED NODDY DOCS</p>
                    </div>
                    <!-- BACK -->
                    <div class="flip-card-back">
                        <div class="id-header">OFFICIAL DONKEY ID</div>
                        <div class="id-photo">🫏</div>
                        <div class="id-stats">
                            <p><strong>Name:</strong> Nibaan (Noddy)</p>
                            <p><strong>Rank:</strong> Chief Distraction Officer</p>
                            <p><strong>Brain Usage:</strong> 0% (Loading...)</p>
                            <p><strong>Yap Level:</strong> 100% (High)</p>
                            <p><strong>Weakness:</strong> Basic Math</p>
                            <p style="color:red; font-weight:bold; margin-top:5px; text-align:center;">STATUS: CERTIFIED LEGEND</p>
                        </div>
                    </div>
                </div>
            </div>

            <button class="btn" onclick="finalPrint()">Celebrate 🎉</button>
        </div>
    </div>

    <!-- Warning Popup -->
    <div id="warning-modal" class="warning-modal">
        <h2>⚠️ SYSTEM CRASH ⚠️</h2>
        <p style="font-size: 1.2rem; font-weight: bold;">Too Much Swag Detected!</p>
        <p>Your coolness broke the website.</p>
        <button class="btn" style="padding: 10px 20px; font-size: 1rem;" onclick="closeWarningModal()">Restart System 🙄</button>
    </div>

    <audio id="bg-music">
        <source src="Noddy ja birthday .mp3" type="audio/mpeg">
    </audio>

    <script>
        // --- SOUND ENGINE ---
        let audioCtx;
        function initAudio() {
            if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
            if (audioCtx.state === 'suspended') audioCtx.resume();
        }

        function playSound(type) {
            if (!audioCtx) initAudio();
            const osc = audioCtx.createOscillator();
            const gainNode = audioCtx.createGain();
            osc.connect(gainNode);
            gainNode.connect(audioCtx.destination);
            const now = audioCtx.currentTime;

            if (type === 'boing') {
                osc.type = 'sine'; osc.frequency.setValueAtTime(150, now); osc.frequency.exponentialRampToValueAtTime(600, now + 0.3);
                gainNode.gain.setValueAtTime(0.5, now); gainNode.gain.exponentialRampToValueAtTime(0.01, now + 0.3);
                osc.start(now); osc.stop(now + 0.3);
            } 
            else if (type === 'error') {
                osc.type = 'sawtooth'; osc.frequency.setValueAtTime(100, now); osc.frequency.linearRampToValueAtTime(80, now + 0.2);
                gainNode.gain.setValueAtTime(0.5, now); gainNode.gain.linearRampToValueAtTime(0.01, now + 0.2);
                osc.start(now); osc.stop(now + 0.2);
            }
            else if (type === 'success') {
                osc.type = 'square'; osc.frequency.setValueAtTime(400, now); osc.frequency.setValueAtTime(600, now + 0.1);
                gainNode.gain.setValueAtTime(0.1, now); gainNode.gain.linearRampToValueAtTime(0, now + 0.3);
                osc.start(now); osc.stop(now + 0.3);
            }
            else if (type === 'donkey') {
                osc.type = 'triangle'; osc.frequency.setValueAtTime(200, now); osc.frequency.linearRampToValueAtTime(300, now + 0.3);
                gainNode.gain.setValueAtTime(0.5, now); gainNode.gain.linearRampToValueAtTime(0, now + 0.4);
                osc.start(now); osc.stop(now + 0.4);
            }
        }

        function revealLeaks() {
            document.getElementById('reveal-leaks-btn').style.display = 'none';
            const terminal = document.getElementById('terminal-content');
            const leaks = [
                "> google.com: how to stop being a donkey",
                "> youtube.com: cool poses for boys 2026",
                "> amazon.com: brain extension kit price",
                "> wiki: is nibaan a legendary creature?",
                "> google.com: how to do homework without doing it",
                "> ERROR: TOO MANY EMBARRASSING SEARCHES..."
            ];
            
            let i = 0;
            function typeLine() {
                if (i < leaks.length) {
                    playSound('donkey');
                    const div = document.createElement('div');
                    div.className = 'terminal-line fade-in';
                    div.innerText = leaks[i];
                    terminal.appendChild(div);
                    i++;
                    setTimeout(typeLine, 800);
                }
            }
            typeLine();
        }

        // --- ROAST MESSAGES ---
        const roastMessages = [
            "Initiating Quick Scan...",
            "Detected Species: Donkey 🫏",
            "IQ Test: 404 Not Found 🚫",
            "Mental Age: 2 years old 👶"
        ];

        function getEl(id) { return document.getElementById(id); }
        function show(id) { getEl(id).classList.remove('hidden'); getEl(id).classList.add('show'); }
        function hide(id) { getEl(id).classList.add('hidden'); getEl(id).classList.remove('show'); }

        // --- CONFETTI ---
        function createFloatingEmojis() {
            const emojis = ['😂', '🎉', '🔥', '🫏', '💀', '🎂', '💩'];
            const container = getEl('emoji-container');
            for(let i=0; i<15; i++) {
                let el = document.createElement('div');
                el.innerText = emojis[Math.floor(Math.random() * emojis.length)];
                el.className = 'bg-emoji';
                el.style.left = Math.random() * 100 + 'vw';
                el.style.top = Math.random() * 100 + 'vh';
                el.style.animationDuration = (Math.random() * 5 + 5) + 's';
                el.style.fontSize = (Math.random() * 2 + 1) + 'rem';
                container.appendChild(el);
            }
        }
        createFloatingEmojis();

        const canvas = getEl('confetti-canvas');
        const ctx = canvas.getContext('2d');
        let particles = [];
        function resizeCanvas() { canvas.width = window.innerWidth; canvas.height = window.innerHeight; }
        window.addEventListener('resize', resizeCanvas);
        resizeCanvas();

        function createConfetti(x, y, count = 50) {
            for (let i = 0; i < count; i++) {
                particles.push({ x: x, y: y, vx: (Math.random() - 0.5) * 15, vy: (Math.random() - 0.5) * 15 - 5, size: Math.random() * 10 + 5, color: `hsl(${Math.random() * 360}, 100%, 50%)`, rotation: Math.random() * 360, rotationSpeed: (Math.random() - 0.5) * 10, life: 100 });
            }
        }
        function animateConfetti() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            particles.forEach((p, index) => {
                p.x += p.vx; p.y += p.vy; p.vy += 0.2; p.rotation += p.rotationSpeed; p.life -= 1; p.size *= 0.98;
                ctx.save(); ctx.translate(p.x, p.y); ctx.rotate(p.rotation * Math.PI / 180); ctx.fillStyle = p.color; ctx.fillRect(-p.size / 2, -p.size / 2, p.size, p.size); ctx.restore();
                if (p.life <= 0) particles.splice(index, 1);
            });
            requestAnimationFrame(animateConfetti);
        }
        animateConfetti();

        // --- FLOW LOGIC ---
        function startRoast() {
            playSound('boing');
            hide('section-hero'); show('section-roast');
            
            // Audio try
            let music = getEl('bg-music');
            music.volume = 0.5;
            music.play().catch(e => console.log("Audio waiting"));

            let roastContainer = getEl('roast-lines');
            let index = 0;
            // Faster roast speed (800ms)
            function showNextLine() {
                if (index < roastMessages.length) {
                    playSound('boing');
                    let p = document.createElement('div');
                    p.className = 'roast-line show';
                    p.innerText = roastMessages[index];
                    roastContainer.appendChild(p);
                    index++;
                    p.scrollIntoView({behavior: "smooth"});
                    setTimeout(showNextLine, 800);
                } else {
                    startVisualScan();
                }
            }
            showNextLine();
        }

        function startVisualScan() {
            show('visual-scanner');
            show('scan-status');
            let status = getEl('scan-status');
            
            // Sequence for scanner
            setTimeout(() => {
                status.innerText = "SEARCHING HEAD...";
                playSound('donkey');
            }, 1000);

            setTimeout(() => {
                // Show Poop
                document.querySelector('.head-poop').style.display = 'block';
                status.innerText = "ERROR: HEAD FULL OF POOP 💩";
                status.style.color = "red";
                playSound('error');
            }, 2500);

            setTimeout(() => {
                status.innerText = "SEARCHING LEGS...";
                status.style.color = "yellow";
            }, 4000);

            setTimeout(() => {
                // Show Brain in Knee
                document.querySelector('.knee-brain').style.display = 'block';
                status.innerText = "SUCCESS: TINY BRAIN FOUND IN KNEE! 🧠";
                status.style.color = "#00ff00";
                playSound('success');
                createConfetti(window.innerWidth/2, window.innerHeight/2, 50);
            }, 5500);

            setTimeout(() => {
                show('next-special-btn');
            }, 6500);
        }

        function goToSpecialGifts() { 
            playSound('success');
            hide('section-roast'); show('section-special-gifts'); 
        }
        function goToMainGift() { 
            playSound('boing');
            hide('section-special-gifts'); show('section-gift'); 
        }

        // --- SECURITY SCAN UI ---
        function startSecurityScan() {
            playSound('boing');
            let text = getEl('scan-text');
            let btn = getEl('start-scan-btn');
            let icon = getEl('scanner-icon');
            let line = getEl('scan-line-effect');
            
            btn.style.display = 'none';
            line.style.display = 'block';
            icon.classList.add('shake-element');
            
            let steps = [
                "SCANNING FACE... 📸",
                "ERROR: TOO FUNNY 😂",
                "MATCH: 100% DONKEY 🫏"
            ];
            
            let i = 0;
            let interval = setInterval(() => {
                if (i < steps.length) {
                    playSound('boing');
                    text.innerHTML = steps[i];
                    i++;
                } else {
                    clearInterval(interval);
                    playSound('success');
                    getEl('security-scanner-ui').style.display = 'none';
                    show('unlocked-content');
                    createConfetti(window.innerWidth/2, window.innerHeight/2, 150);
                }
            }, 800);
        }

        function openGift() {
            let box = document.querySelector('.gift-box');
            box.style.animation = "shake 0.1s infinite";
            playSound('donkey');
            setTimeout(() => {
                box.style.transform = "scale(0)"; 
                createConfetti(window.innerWidth/2, window.innerHeight/2, 200);
                playSound('success');
                setTimeout(() => {
                    box.style.display = 'none';
                    show('gift-reveal');
                }, 200);
            }, 1500);
        }

        function activateNoddyMode() {
            playSound('success');
            hide('section-gift');
            document.body.classList.add('rainbow-mode');
            getEl('main-card').classList.add('shake-element');
            let rainInterval = setInterval(() => { createConfetti(Math.random() * window.innerWidth, -10); }, 100);
            setTimeout(() => { clearInterval(rainInterval); getEl('main-card').classList.remove('shake-element'); }, 3000);
            setTimeout(() => { playSound('error'); getEl('warning-modal').style.display = 'block'; }, 500);
        }

        function closeWarningModal() {
            getEl('warning-modal').style.display = 'none';
            show('section-cert');
        }

        function finalPrint() {
            playSound('success');
            createConfetti(window.innerWidth/2, window.innerHeight/2, 300);
        }
    </script>
</body>
</html>


