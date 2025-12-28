<!DOCTYPE html>
<html lang="el">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SynIdea - Platform</title>
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
    <style>
        body { font-family: 'Segoe UI', sans-serif; background-color: #f0f2f5; margin: 0; display: flex; align-items: center; justify-content: center; height: 100vh; }
        .container { background: white; padding: 40px; border-radius: 20px; box-shadow: 0 15px 35px rgba(0,0,0,0.1); text-align: center; max-width: 500px; width: 90%; }
        
        /* Λογότυπο */
        .logo-box { display: flex; align-items: center; justify-content: center; gap: 8px; margin-bottom: 10px; }
        .bulb { font-size: 45px; color: #f1c40f; }
        .logo-text { font-size: 35px; font-weight: 800; color: #2c3e50; }
        .logo-text span { color: #3498db; }

        p { color: #636e72; font-size: 1em; margin-bottom: 30px; }

        /* Κουμπιά */
        .btn-group { display: flex; justify-content: center; gap: 15px; }
        button { 
            background-color: #3498db; color: white; border: none; 
            padding: 10px 20px; font-size: 15px; cursor: pointer; 
            border-radius: 8px; transition: 0.3s; font-weight: 600;
            min-width: 140px;
        }
        button:hover { background-color: #2980b9; transform: scale(1.05); }
        .btn-invest { background-color: #27ae60; }
        .btn-invest:hover { background-color: #219150; }

        .menu-section { display: none; }
        .active { display: block; animation: fadeIn 0.5s; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
    </style>
</head>
<body>

<div class="container">
    <div id="start" class="menu-section active">
        <div class="logo-box">
            <span class="material-icons bulb">lightbulb</span>
            <div class="logo-text">Syn<span>Idea</span></div>
        </div>
        <p>Σύνδεση Ιδεών & Επενδύσεων</p>
        
        <div class="btn-group">
            <button onclick="showNext('idea-path')">Έχω μια Ιδέα</button>
            <button class="btn-invest" onclick="showNext('invest-path')">Θέλω να Επενδύσω</button>
        </div>
    </div>

    <div id="idea-path" class="menu-section">
        <h3>Ποιος είναι ο τομέας σου;</h3>
        <div class="btn-group">
            <button onclick="showNext('start')">Πίσω</button>
        </div>
    </div>

    <div id="invest-path" class="menu-section">
        <h3>Τι αναζητάς;</h3>
        <div class="btn-group">
            <button onclick="showNext('start')">Πίσω</button>
        </div>
    </div>
</div>

<script>
    function showNext(id) {
        document.querySelectorAll('.menu-section').forEach(s => s.classList.remove('active'));
        document.getElementById(id).classList.add('active');
    }
</script>

</body>
</html>
