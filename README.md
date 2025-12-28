<!DOCTYPE html>
<html lang="el">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SynIdea - Platform</title>
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
    <style>
        body { font-family: 'Segoe UI', Arial, sans-serif; background-color: #f0f2f5; margin: 0; display: flex; align-items: center; justify-content: center; height: 100vh; }
        .container { background: white; padding: 40px; border-radius: 20px; box-shadow: 0 15px 35px rgba(0,0,0,0.1); text-align: center; max-width: 600px; width: 90%; }
        
        /* Στυλ για το Λογότυπο */
        .logo-container { display: flex; align-items: center; justify-content: center; gap: 10px; margin-bottom: 20px; }
        .logo-icon { font-size: 50px; color: #f1c40f; text-shadow: 2px 2px 5px rgba(0,0,0,0.1); }
        .logo-text { font-size: 40px; font-weight: 800; color: #2c3e50; letter-spacing: -1px; }
        .logo-text span { color: #3498db; }

        p { color: #636e72; font-size: 1.1em; margin-bottom: 30px; }

        /* Μικρότερα και κομψά κουμπιά */
        .btn-container { display: flex; justify-content: center; gap: 15px; }
        
        button { 
            background-color: #3498db; color: white; border: none; 
            padding: 12px 25px; font-size: 16px; cursor: pointer; 
            border-radius: 8px; transition: 0.3s; font-weight: 600;
            min-width: 160px; /* Μικρότερο πλάτος */
        }
        
        button:hover { background-color: #2980b9; transform: scale(1.05); }
        .btn-invest { background-color: #27ae60; }
        .btn-invest:hover { background-color: #219150; }

        .menu-section { display: none; animation: fadeIn 0.5s; }
        .active { display: block; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
    </style>
</head>
<body>

<div class="container">
    <div id="start" class="menu-section active">
        <div class="logo-container">
            <span class="material-icons logo-icon">lightbulb</span>
            <div class="logo-text">Syn<span>Idea</span></div>
        </div>
        <p>Η γέφυρα ανάμεσα στην ιδέα και την επένδυση.</p>
        
        <div class="btn-container">
            <button onclick="showNext('idea-path')">Έχω μια Ιδέα</button>
            <button class="btn-invest" onclick="showNext('invest-path')">Θέλω να Επενδύσω</button>
        </div>
    </div>

    <div id="idea-path" class="menu-section">
        <h2>Ποιος είναι ο τομέας σου;</h2>
        <div class="btn-container">
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
