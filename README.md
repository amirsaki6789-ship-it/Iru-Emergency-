                background-color: var(--bg);
            margin: 0; padding: 0;
            color: var(--text);
            /* SCROLL FIX: Native scrolling with padding */
            padding-top: 160px; 
            padding-bottom: 90px; 
        }

        /* --- 2. FIXED HEADER --- */
        .header-fixed {
            position: fixed; top: 0; left: 0; right: 0;
            background: rgba(255,255,255,0.96);
            backdrop-filter: blur(10px);
            z-index: 1000;
            border-bottom: 1px solid rgba(0,0,0,0.1);
        }

        .top-bar {
            padding: 15px 20px;
            display: flex; justify-content: space-between; align-items: center;
        }

        .logo h1 { margin: 0; font-size: 24px; font-weight: 800; letter-spacing: -0.5px; }
        .logo span { color: var(--primary); }
        .logo p { margin: 0; font-size: 11px; color: var(--subtext); font-weight: 600; text-transform: uppercase; letter-spacing: 1px;}

        /* Tools (Whistle & Torch) */
        .tools { display: flex; gap: 12px; }
        .tool-btn {
            width: 40px; height: 40px;
            border-radius: 50%; border: none;
            display: flex; align-items: center; justify-content: center;
            cursor: pointer; transition: 0.2s;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .btn-whistle { background: var(--orange); color: white; }
        .btn-torch { background: var(--text); color: white; }
        .tool-btn:active { transform: scale(0.9); }
        
        /* Animation */
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.1); } 100% { transform: scale(1); } }

        /* Search & Tabs */
        .search-container { padding: 0 20px 10px; }
        .search-input {
            width: 100%; padding: 12px 16px;
            border-radius: 12px; border: none;
            background: #e5e5ea; font-size: 15px; color: var(--text);
        }

        .tabs-container {
            padding: 5px 20px 15px;
            overflow-x: auto; white-space: nowrap;
            scrollbar-width: none;
        }
        .tabs-container::-webkit-scrollbar { display: none; }
        
        .chip {
            display: inline-block; padding: 8px 16px; margin-right: 8px;
            background: #e5e5ea; border-radius: 20px;
            font-size: 13px; font-weight: 600; color: var(--subtext);
            transition: 0.2s;
        }
        .chip.active { background: var(--text); color: white; }

        /* --- 3. LIST & CARDS --- */
        .content-area { padding: 0 20px; display: none; }
        .content-area.active { display: block; }

        .card {
            background: var(--card);
            border-radius: var(--radius);
            padding: 16px;
            margin-bottom: 14px;
            display: flex; align-items: center;
            box-shadow: var(--shadow);
            transition: transform 0.1s;
        }
        .card:active { transform: scale(0.97); background: #f9f9f9; }

        .icon-box {
            width: 50px; height: 50px;
            border-radius: 14px;
            display: flex; align-items: center; justify-content: center;
            margin-right: 16px; flex-shrink: 0;
            color: white; font-weight: bold;
        }
        .icon-box svg { width: 26px; height: 26px; fill: currentColor; }

        .info { flex: 1; }
        .info h3 { margin: 0 0 4px; font-size: 17px; font-weight: 700; }
        .info p { margin: 0; font-size: 13px; color: var(--subtext); }

        .arrow-icon { color: #d1d1d6; }

        /* --- 4. MODAL (ABOUT SERVICE) --- */
        .modal-overlay {
            position: fixed; top: 0; left: 0; right: 0; bottom: 0;
            background: rgba(0,0,0,0.5); z-index: 2000;
            display: none; align-items: flex-end; /* Bottom sheet style */
            backdrop-filter: blur(4px);
        }
        .modal-overlay.open { display: flex; animation: slideUp 0.3s; }

        .modal {
            background: white; width: 100%;
            border-top-left-radius: 24px; border-top-right-radius: 24px;
            padding: 30px 24px;
            box-shadow: 0 -10px 40px rgba(0,0,0,0.2);
        }

        .modal-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px; }
        .modal-title { font-size: 22px; font-weight: 800; }
        .btn-close { background: #f2f2f7; border: none; width: 32px; height: 32px; border-radius: 50%; font-size: 20px; line-height: 1; }

        .modal-body p { font-size: 15px; line-height: 1.6; color: #555; margin-bottom: 25px; }
        .modal-number { font-size: 32px; font-weight: 800; color: var(--primary); display: block; margin-bottom: 20px; letter-spacing: 1px; }

        .modal-btn {
            display: block; width: 100%; padding: 16px;
            background: var(--green); color: white;
            text-align: center; border-radius: 16px; text-decoration: none;
            font-weight: 700; font-size: 18px;
        }
        @keyframes slideUp { from { transform: translateY(100%); } to { transform: translateY(0); } }

        /* --- 5. OTHER SECTIONS --- */
        /* SMS Tool */
        .tool-box { background: white; padding: 20px; border-radius: 20px; box-shadow: var(--shadow); text-align: center; }
        .sms-display { background: #f2f2f7; padding: 15px; border-radius: 12px; font-family: monospace; text-align: left; margin: 15px 0; min-height: 60px; font-size: 12px;}
        .action-btn-lg { background: var(--blue); color: white; padding: 12px; width: 100%; border-radius: 12px; border:none; font-weight: 600; font-size: 14px; margin-bottom: 10px; }

        /* Safety Timer (New) */
        .timer-display { font-size: 40px; font-weight: 800; margin: 20px 0; color: var(--text); }
        .timer-controls { display: flex; gap: 10px; justify-content: center; }
        .timer-btn { padding: 10px 20px; border-radius: 10px; border: none; font-weight: 600; }

        /* --- 6. BOTTOM NAV --- */
        .bottom-nav {
            position: fixed; bottom: 0; left: 0; right: 0;
            background: rgba(255,255,255,0.95);
            backdrop-filter: blur(20px);
            border-top: 1px solid rgba(0,0,0,0.1);
            display: flex; justify-content: space-around;
            padding: 10px 0 20px; z-index: 1000;
        }
        .nav-item { text-align: center; font-size: 10px; color: var(--subtext); padding: 5px 15px; cursor: pointer; }
        .nav-item svg { width: 24px; height: 24px; display: block; margin: 0 auto 4px; fill: currentColor; }
        .nav-item.active { color: var(--blue); }

        /* Flash Overlay */
        #flashOverlay { position: fixed; top:0; left:0; right:0; bottom:0; background:white; z-index:9999; display:none; }

        /* Colors */
        .bg-red { background: var(--primary); }
        .bg-blue { background: var(--blue); }
        .bg-green { background: var(--green); }
        .bg-orange { background: var(--orange); }
        .bg-dark { background: #2c3e50; }
        .bg-purple { background: #af52de; }

    </style>
</head>
<body>

    <!-- HEADER -->
    <div class="header-fixed">
        <div class="top-bar">
            <div class="logo">
                <h1>Iru <span>Pro</span></h1>
                <p>Offline Safety</p>
            </div>
            <div class="tools">
                <button class="tool-btn btn-whistle" onclick="toggleWhistle()" id="whistleBtn">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M14 15v-4h-2v4h2zm-4 0h2v-4h-2v4zm-3-4v4h2v-4H7zm11-1.5V6l-6-4-6 4v3.5A7.5 7.5 0 0 0 2 17h2c0-3.04 2.46-5.5 5.5-5.5h6c3.04 0 5.5 2.46 5.5 5.5h2c0-4.86-3.56-8.9-8-9.5z"/></svg>
                </button>
                <button class="tool-btn btn-torch" onclick="toggleFlashlight()">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M9 21c0 .55.45 1 1 1h4c.55 0 1-.45 1-1v-1H9v1zm3-19C8.14 2 5 5.14 5 9c0 2.38 1.19 4.47 3 5.74V17c0 .55.45 1 1 1h6c.55 0 1-.45 1-1v-2.26c1.81-1.27 3-3.36 3-5.74 0-3.86-3.14-7-7-7zm2.85 11.1l-.85.6V16h-4v-2.3l-.85-.6A4.997 4.997 0 0 1 7 9c0-2.76 2.24-5 5-5s5 2.24 5 5c0 1.63-.8 3.16-2.15 4.1z"/></svg>
                </button>
            </div>
        </div>

        <div class="search-container">
            <input type="text" id="searchInput" class="search-input" placeholder="Search (e.g. Police, Snow)..." onkeyup="renderList()">
        </div>

        <div class="tabs-container">
            <div class="chip active" onclick="filterList('All', this)">All</div>
            <div class="chip" onclick="filterList('Emergency', this)">Emergency</div>
            <div class="chip" onclick="filterList('Medical', this)">Medical</div>
            <div class="chip" onclick="filterList('Utility', this)">Utility</div>
            <div class="chip" onclick="filterList('Admin', this)">Admin</div>
        </div>
    </div>

    <!-- VIEW 1: HOME LIST -->
    <div id="view-home" class="content-area active">
        <div id="listContainer"></div>
    </div>

    <!-- VIEW 2: SMS & GPS -->
    <div id="view-sms" class="content-area">
        <h2 style="margin-top:0;">📡 GPS & SMS</h2>
        <div class="tool-box">
            <p>Generates an emergency SMS with your coordinates to send when internet is down.</p>
            <button class="action-btn-lg" onclick="getGPS()">Get Location</button>
            <div id="smsOutput" class="sms-display">Location will appear here...</div>
            <a id="sendSmsLink" href="#" style="display:block; padding:12px; background:var(--green); color:white; border-radius:12px; text-decoration:none; font-weight:bold;">Open SMS App</a>
        </div>
    </div>

    <!-- VIEW 3: SAFETY TIMER (NEW) -->
    <div id="view-timer" class="content-area">
        <h2 style="margin-top:0;">⏱️ Safety Check</h2>
        <div class="tool-box">
            <p>Set a timer before entering a risky area. If you don't stop it, the alarm will sound.</p>
            <div id="timerDisplay" class="timer-display">00:00</div>
            <div class="timer-controls">
                <button class="timer-btn" style="background:var(--blue); color:white;" onclick="startTimer(5)">5 Min</button>
                <button class="timer-btn" style="background:var(--blue); color:white;" onclick="startTimer(10)">10 Min</button>
                <button class="timer-btn" style="background:var(--primary); color:white;" onclick="stopTimer()">STOP</button>
            </div>
            <p style="font-size:12px; margin-top:15px; color:#888;">Alarm plays automatically when time hits 00:00</p>
        </div>
    </div>

    <!-- MODAL: ABOUT SERVICE -->
    <div id="serviceModal" class="modal-overlay" onclick="closeModal(event)">
        <div class="modal">
            <div class="modal-header">
                <div class="modal-title" id="mTitle">Service Name</div>
                <button class="btn-close" onclick="forceCloseModal()">×</button>
            </div>
            <div class="modal-body">
                <p id="mDesc">Description...</p>
                <span class="modal-number" id="mNumber">100</span>
                <a href="#" id="mCallBtn" class="modal-btn">CALL NOW</a>
            </div>
        </div>
    </div>

    <!-- FLASHLIGHT OVERLAY -->
    <div id="flashOverlay" onclick="toggleFlashlight()"></div>

    <!-- BOTTOM NAV -->
    <div class="bottom-nav">
        <div class="nav-item active" onclick="switchView('home', this)">
            <svg viewBox="0 0 24 24"><path d="M10 20v-6h4v6h5v-8h3L12 3 2 12h3v8z"/></svg>
            Home
        </div>
        <div class="nav-item" onclick="switchView('sms', this)">
            <svg viewBox="0 0 24 24"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg>
            GPS
        </div>
        <div class="nav-item" onclick="switchView('timer', this)">
            <svg viewBox="0 0 24 24"><path d="M15 1H9v2h6V1zm-4 13h2V8h-2v6zm8.03-6.61l1.42-1.42c-.43-.51-.9-.99-1.41-1.41l-1.42 1.42C16.07 4.74 14.12 4 12 4c-4.97 0-9 4.03-9 9s4.02 9 9 9 9-4.03 9-9c0-2.12-.74-4.07-1.97-5.61zM12 20c-3.87 0-7-3.13-7-7s3.13-7 7-7 7 3.13 7 7-3.13 7-7 7z"/></svg>
            Timer
        </div>
    </div>

    <script>
        // --- 1. ICONS & DATA ---
        const icons = {
            shield: '<svg viewBox="0 0 24 24"><path d="M12 1L3 5v6c0 5.55 3.84 10.74 9 12 5.16-1.26 9-6.45 9-12V5l-9-4zm0 10.99h7c-.53 4.12-3.28 7.79-7 8.94V12H5V6.3l7-3.11v8.8z"/></svg>',
            star: '<svg viewBox="0 0 24 24"><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z"/></svg>',
            amb: '<svg viewBox="0 0 24 24"><path d="M19 3H5c-1.1 0-1.99.9-1.99 2L3 19c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-1 11h-4v4h-4v-4H6v-4h4V6h4v4h4v4z"/></svg>',
            fire: '<svg viewBox="0 0 24 24"><path d="M13.5.67s.74 2.65.74 4.8c0 2.06-1.35 3.73-3.41 3.73-2.07 0-3.63-1.67-3.63-3.73l.03-.36C5.21 7.51 4 10.62 4 14c0 4.42 3.58 8 8 8s8-3.58 8-8C20 8.61 17.41 3.8 13.5.67zM11.71 19c-1.78 0-3.22-1.4-3.22-3.14 0-1.62 1.05-2.76 2.81-3.12 1.77-.36 3.6-1.21 4.62-2.58.39 1.29.59 2.65.59 4.04 0 2.65-2.15 4.8-4.8 4.8z"/></svg>',
            bolt: '<svg viewBox="0 0 24 24"><path d="M7 2v11h3v9l7-12h-4l4-8z"/></svg>',
            water: '<svg viewBox="0 0 24 24"><path d="M12 2c1.1 0 2 .9 2 2s-.9 2-2 2-2-.9-2-2 .9-2 2-2zm9 7h-6v13h-2v-6h-2v6H9V9H3V7h18v2z"/></svg>',
            arrow: '<svg viewBox="0 0 24 24"><path d="M8.59 16.59L13.17 12 8.59 7.41 10 6l6 6-6 6-1.41-1.41z"/></svg>'
        };

        const db = [
            { name: "PCR Bandipora", cat: "Emergency", num: "01957225278", icon: icons.shield, color: "bg-blue", desc: "Main Police Control Room for Bandipora District. Call for crime, accidents, or law & order issues." },
            { name: "National Emergency", cat: "Emergency", num: "112", icon: icons.star, color: "bg-red", desc: "Pan-India Single Emergency Number. Connects to Police, Fire, and Ambulance services automatically." },
            { name: "Ambulance", cat: "Medical", num: "108", icon: icons.amb, color: "bg-green", desc: "Free Medical Emergency Transport. Call for heart attacks, trauma, or severe illness requiring hospital." },
            { name: "Fire & Rescue", cat: "Emergency", num: "101", icon: icons.fire, color: "bg-orange", desc: "Fire Brigade Control. Call immediately for house fires, forest fires, or rescue from heights/water." },
            { name: "Disaster Mgmt", cat: "Emergency", num: "01957226085", icon: icons.water, color: "bg-dark", desc: "DC Office Bandipora Control Room. Contact during floods, heavy snow, landslides, or earthquakes." },
            { name: "Electricity (PDD)", cat: "Utility", num: "1912", icon: icons.bolt, color: "bg-orange", desc: "Power Development Department Helpline. Report power outages, fallen wires, or transformer faults." },
            { name: "Water (PHE)", cat: "Utility", num: "18001807045", icon: icons.water, color: "bg-blue", desc: "Jal Shakti Department. Report no water supply, leakage, or contaminated water issues." },
            { name: "Women Helpline", cat: "Emergency", num: "181", icon: icons.shield, color: "bg-purple", desc: "24/7 Helpline for women in distress. Domestic violence, harassment, or shelter assistance." },
            { name: "Child Helpline", cat: "Emergency", num: "1098", icon: icons.star, color: "bg-green", desc: "Childline Service. For reporting lost children, child labour, or abuse cases." },
            { name: "Doctor on Call", cat: "Medical", num: "104", icon: icons.amb, color: "bg-blue", desc: "Health Advice Helpline J&K. Get medical advice from doctors over phone for minor issues." },
            { name: "Cyber Crime", cat: "Admin", num: "1930", icon: icons.shield, color: "bg-dark", desc: "National Cyber Crime Portal. Call immediately if you lose money in online banking fraud." },
            { name: "Municipality", cat: "Utility", num: "01957225026", icon: icons.water, color: "bg-green", desc: "Bandipora Municipal Council. For sanitation, garbage collection, and street light complaints." },
        ];

        // --- 2. RENDER & FILTER ---
        const listEl = document.getElementById('listContainer');
        let currentFilter = 'All';

        function renderList() {
            const searchVal = document.getElementById('searchInput').value.toLowerCase();
            listEl.innerHTML = '';

            const filtered = db.filter(s => {
                const matchCat = currentFilter === 'All' || s.cat === currentFilter;
                const matchSearch = s.name.toLowerCase().includes(searchVal);
                return matchCat && matchSearch;
            });

            filtered.forEach(s => {
                const div = document.createElement('div');
                div.className = 'card';
                div.onclick = () => openModal(s); // Click opens "About" modal
                div.innerHTML = `
                    <div class="icon-box ${s.color}">${s.icon}</div>
                    <div class="info">
                        <h3>${s.name}</h3>
                        <p>${s.desc.substring(0, 35)}...</p>
                    </div>
                    <div class="arrow-icon">${icons.arrow}</div>
                `;
                listEl.appendChild(div);
            });
        }

        function filterList(cat, btn) {
            document.querySelectorAll('.chip').forEach(c => c.classList.remove('active'));
            btn.classList.add('active');
            currentFilter = cat;
            renderList();
        }

        // --- 3. MODAL LOGIC (About Service) ---
        const modal = document.getElementById('serviceModal');
        
        function openModal(item) {
            document.getElementById('mTitle').innerText = item.name;
            document.getElementById('mDesc').innerText = item.desc; // Full description
            document.getElementById('mNumber').innerText = item.num;
            document.getElementById('mCallBtn').href = `tel:${item.num}`;
            modal.classList.add('open');
        }

        function closeModal(e) {
            if(e.target === modal) modal.classList.remove('open');
        }
        function forceCloseModal() {
            modal.classList.remove('open');
        }

        // --- 4. FEATURES ---
        
        // Whistle
        let audioCtx, osc;
        let isWhistling = false;
        function toggleWhistle() {
            if(isWhistling) {
                if(osc) osc.stop();
                isWhistling = false;
                document.getElementById('whistleBtn').style.animation = 'none';
            } else {
                startSirenSound();
                document.getElementById('whistleBtn').style.animation = 'pulse 0.5s infinite';
            }
        }
        
        function startSirenSound() {
            const AudioC = window.AudioContext || window.webkitAudioContext;
            if(!AudioC) return alert("Audio not supported");
            audioCtx = new AudioC();
            osc = audioCtx.createOscillator();
            const gain = audioCtx.createGain();
            osc.type = 'triangle';
            osc.frequency.setValueAtTime(3000, audioCtx.currentTime);
            osc.connect(gain);
            gain.connect(audioCtx.destination);
            osc.start();
            isWhistling = true;
        }

        // Flashlight
        function toggleFlashlight() {
            const overlay = document.getElementById('flashOverlay');
            overlay.style.display = (overlay.style.display === 'block') ? 'none' : 'block';
        }

        // GPS / SMS
        function getGPS() {
            const out = document.getElementById('smsOutput');
            const link = document.getElementById('sendSmsLink');
            out.innerText = "Locating...";
            
            if(!navigator.geolocation) return out.innerText = "GPS Not Supported";

            navigator.geolocation.getCurrentPosition(pos => {
                const lat = pos.coords.latitude.toFixed(5);
                const lng = pos.coords.longitude.toFixed(5);
                const msg = `EMERGENCY! Help needed. Location: https://maps.google.com/?q=${lat},${lng}`;
                out.innerText = msg;
                link.href = `sms:?body=${encodeURIComponent(msg)}`;
            }, () => out.innerText = "GPS Error: Enable Location.");
        }

        // Safety Timer (New)
        let timerInterval;
        let timeLeft = 0;

        function startTimer(min) {
            clearInterval(timerInterval);
            timeLeft = min * 60;
            updateTimerDisplay();
            timerInterval = setInterval(() => {
                timeLeft--;
                updateTimerDisplay();
                if(timeLeft <= 0) {
                    clearInterval(timerInterval);
                    toggleWhistle(); // Trigger alarm
                    alert("ALARM: Safety Timer Expired!");
                }
            }, 1000);
        }

        function stopTimer() {
            clearInterval(timerInterval);
            timeLeft = 0;
            updateTimerDisplay();
            if(isWhistling) toggleWhistle(); // Stop alarm if playing
        }

        function updateTimerDisplay() {
            const m = Math.floor(timeLeft / 60).toString().padStart(2, '0');
            const s = (timeLeft % 60).toString().padStart(2, '0');
            document.getElementById('timerDisplay').innerText = `${m}:${s}`;
        }

        // Navigation
        function switchView(id, btn) {
            document.querySelectorAll('.content-area').forEach(d => d.classList.remove('active'));
            document.getElementById('view-'+id).classList.add('active');
            document.querySelectorAll('.nav-item').forEach(n => n.classList.remove('active'));
            btn.classList.add('active');
            window.scrollTo(0,0);
        }

        // Init
        renderList();

    </script>
</body>
</html>
