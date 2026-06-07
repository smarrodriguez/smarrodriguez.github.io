<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Weaver’s Path - Guest Experience Hub</title>
    <style>
        :root {
            --primary: #d69e2e;
            --dark: #2d3748;
            --light: #f7fafc;
            --text: #4a5568;
        }
        body {
            font-family: 'Helvetica Neue', Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--light);
            color: var(--dark);
        }
        .header {
            background-color: var(--dark);
            color: white;
            text-align: center;
            padding: 30px 20px;
            border-bottom: 5px solid var(--primary);
        }
        .header h1 {
            margin: 0;
            font-size: 24px;
            letter-spacing: 1px;
            text-transform: uppercase;
        }
        .header p {
            margin: 10px 0 0 0;
            font-style: italic;
            color: var(--primary);
            font-size: 14px;
        }
        .container {
            max-width: 500px;
            margin: 0 auto;
            padding: 20px;
        }
        .welcome-card {
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            margin-bottom: 25px;
            border-left: 4px solid var(--primary);
        }
        .section-title {
            font-size: 18px;
            font-weight: bold;
            text-transform: uppercase;
            margin-bottom: 15px;
            color: var(--dark);
            border-bottom: 2px solid #e2e8f0;
            padding-bottom: 5px;
        }
        .track-card {
            background: white;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 12px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 4px rgba(0,0,0,0.02);
        }
        .track-info h4 {
            margin: 0;
            font-size: 14px;
        }
        .track-info p {
            margin: 2px 0 0 0;
            font-size: 12px;
            color: var(--text);
        }
        .play-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 20px;
            cursor: pointer;
            font-size: 12px;
            font-weight: bold;
            transition: all 0.2s;
        }
        .map-menu button {
            width: 100%;
            background: white;
            border: 1px solid #e2e8f0;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 10px;
            text-align: left;
            font-weight: bold;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 4px rgba(0,0,0,0.02);
        }
        .map-content {
            background: #edf2f7;
            padding: 15px;
            border-radius: 8px;
            font-size: 13px;
            line-height: 1.5;
            color: var(--text);
            margin-top: -5px;
            margin-bottom: 15px;
            display: none;
        }
        .footer {
            text-align: center;
            padding: 30px 20px;
            font-size: 11px;
            color: #a0aec0;
            background-color: var(--dark);
            color: white;
            margin-top: 40px;
        }
    </style>
</head>
<body>

    <div class="header">
        <h1>The Weaver’s Path</h1>
        <p>A Journey Through Panama’s Living Roots</p>
    </div>

    <div class="container">
        <div class="welcome-card">
            <p><strong>Na daggua / Bidua bue.</strong> Welcome to Panama, Mr./Mrs. Guest. Our heritage is your home. Use this portal to explore the ancient wisdom and living artistry surrounding your stay.</p>
        </div>

        <div class="section-title">I. Ancestral Audio Guides</div>
        
        <div class="track-card">
            <div class="track-info">
                <h4>Track 1: Cosmic Molas</h4>
                <p>The sacred protection of Guna textile art.</p>
            </div>
            <button class="play-btn" onclick="togglePlay(this)">▶ PLAY</button>
        </div>

        <div class="track-card">
            <div class="track-info">
                <h4>Track 2: The Spirit of Chunga</h4>
                <p>Emberá basketry and rainforest master carvings.</p>
            </div>
            <button class="play-btn" onclick="togglePlay(this)">▶ PLAY</button>
        </div>

        <div class="track-card">
            <div class="track-info">
                <h4>Track 3: Darién Rainforest</h4>
                <p>Ambient sounds & ceremonial flutes soundscape.</p>
            </div>
            <button class="play-btn" onclick="togglePlay(this)">▶ PLAY</button>
        </div>

        <div class="section-title" style="margin-top: 30px;">II. Comarca Interactive Map</div>
        <div class="map-menu">
            <button onclick="toggleMap('guna')">📍 Guna Yala District (Caribbean) <span>▼</span></button>
            <div id="guna" class="map-content">
                <strong>Cultural Riches:</strong> Famous for authentic geometric Molas layered with historical narratives. The designs protect the wearer from spiritual labyrinth dangers and depict a profound harmony with nature and pristine marine ecosystems.
            </div>

            <button onclick="toggleMap('embera')">📍 Darién & Emberá Communities <span>▼</span></button>
            <div id="embera" class="map-content">
                <strong>Cultural Riches:</strong> Renowned for highly intricate baskets hand-woven from Chunga palm fibers and fine sculptures carved from Tagua nuts or dense Cocobolo wood. Body painting using natural Jagua ink tells tales of status and forest equilibrium.
            </div>
        </div>
    </div>

    <div class="footer">
        ITSE - Higher Technical Degree in Hotel Operations<br>
        Group 2 Guest Experience App © 2026
    </div>

    <script>
        function togglePlay(btn) {
            if (btn.innerText === "▶ PLAY") {
                btn.innerText = "⏸ PAUSE";
                btn.style.backgroundColor = "#2d3748";
            } else {
                btn.innerText = "▶ PLAY";
                btn.style.backgroundColor = "#d69e2e";
            }
        }
        function toggleMap(id) {
            var element = document.getElementById(id);
            if (element.style.display === "block") {
                element.style.display = "none";
            } else {
                element.style.display = "block";
            }
        }
    </script>
</body>
</html>
