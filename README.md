<!DOCTYPE html>
<html lang="el">
<head>
    <meta charset="UTF-8">
    <title>Η Ιδέα μου</title>
    <style>
        body { font-family: 'Comic Sans MS', sans-serif; background-color: #f0f8ff; text-align: center; padding: 50px; }
        .menu-section { display: none; background: white; padding: 20px; border-radius: 15px; box-shadow: 0px 4px 10px rgba(0,0,0,0.1); margin-top: 20px; }
        .active { display: block; animation: fadeIn 0.5s; }
        button { background-color: #4CAF50; color: white; border: none; padding: 15px 32px; font-size: 18px; margin: 10px; cursor: pointer; border-radius: 10px; transition: 0.3s; }
        button:hover { background-color: #45a049; transform: scale(1.1); }
        @keyframes fadeIn { from {opacity: 0;} to {opacity: 1;} }
    </style>
</head>
<body>

    <h1>🌟 Καλώς ήρθες! 🌟</h1>
    <p>Διάλεξε μια διαδρομή για να ξεκινήσεις:</p>

    <div id="start" class="menu-section active">
        <button onclick="showNext('menu-gaming')">Θέλω να παίξω</button>
        <button onclick="showNext('menu-learning')">Θέλω να μάθω</button>
    </div>

    <div id="menu-gaming" class="menu-section">
        <h2>Τι παιχνίδι σου αρέσει;</h2>
        <button onclick="showNext('idea-minecraft')">Minecraft</button>
        <button onclick="showNext('idea-roblox')">Roblox</button>
        <button onclick="showNext('start')">⬅ Πίσω</button>
    </div>

    <div id="menu-learning" class="menu-section">
        <h2>Τι θέλεις να μάθεις;</h2>
        <button onclick="showNext('idea-code')">Προγραμματισμό</button>
        <button onclick="showNext('idea-space')">Για το Διάστημα</button>
        <button onclick="showNext('start')">⬅ Πίσω</button>
    </div>

    <div id="idea-minecraft" class="menu-section">
        <h2>Τέλεια ιδέα! 🧱</h2>
        <p>Μπορείς να χτίσεις έναν δικό σου κόσμο!</p>
        <button onclick="showNext('start')">Ξεκίνα από την αρχή</button>
    </div>

    <script>
        function showNext(id) {
            // Κρύβει όλα τα μενού
            let sections = document.querySelectorAll('.menu-section');
            sections.forEach(s => s.classList.remove('active'));
            
            // Εμφανίζει αυτό που πατήσαμε
            document.getElementById(id).classList.add('active');
        }
    </script>

</body>
</html>
