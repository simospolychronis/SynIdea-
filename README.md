<!DOCTYPE html>
<html lang="el">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SynIdea - Επιχειρηματικότητα</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background-color: #f4f7f6; color: #333; text-align: center; padding: 40px; }
        .container { max-width: 800px; margin: auto; background: white; padding: 30px; border-radius: 20px; box-shadow: 0 10px 25px rgba(0,0,0,0.1); }
        h1 { color: #2c3e50; font-size: 2.5em; }
        p { font-size: 1.2em; color: #7f8c8d; }
        
        .menu-section { display: none; animation: fadeIn 0.6s; }
        .active { display: block; }

        .btn-container { display: flex; justify-content: center; gap: 20px; margin-top: 30px; flex-wrap: wrap; }
        
        button { 
            background-color: #3498db; color: white; border: none; 
            padding: 20px 40px; font-size: 20px; cursor: pointer; 
            border-radius: 12px; transition: all 0.3s ease; width: 250px;
            font-weight: bold; box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        
        button:hover { background-color: #2980b9; transform: translateY(-5px); box-shadow: 0 8px 15px rgba(0,0,0,0.2); }
        .btn-invest { background-color: #27ae60; }
        .btn-invest:hover { background-color: #219150; }
        .btn-back { background-color: #95a5a6; width: auto; padding: 10px 20px; font-size: 15px; margin-top: 30px; }

        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
    </style>
</head>
<body>

<div class="container">
    <div id="start" class="menu-section active">
        <h1>Καλώς ήρθες στο SynIdea</h1>
        <p>Ποιος είναι ο στόχος σου σήμερα;</p>
        <div class="btn-container">
            <button onclick="showNext('idea-path')">Έχω μια Ιδέα</button>
            <button class="btn-invest" onclick="showNext('invest-path')">Θέλω να Επενδύσω</button>
        </div>
    </div>

    <div id="idea-path" class="menu-section">
        <h1>Υπέροχα! 💡</h1>
        <p>Σε ποιον τομέα ανήκει η ιδέα σου;</p>
        <div class="btn-container">
            <button onclick="alert('Σύντομα διαθέσιμο: Τεχνολογία')">Τεχνολογία</button>
            <button onclick="alert('Σύντομα διαθέσιμο: Περιβάλλον')">Περιβάλλον</button>
            <button onclick="alert('Σύντομα διαθέσιμο: Υπηρεσίες')">Υπηρεσίες</button>
        </div>
        <button class="btn-back" onclick="showNext('start')">⬅ Πίσω στην αρχή</button>
    </div>

    <div id="invest-path" class="menu-section">
        <h1>Γίνε Επενδυτής 📈</h1>
        <p>Τι είδους Projects σε ενδιαφέρουν;</p>
        <div class="btn-container">
            <button class="btn-invest" onclick="alert('Αναζήτηση Startup...')">Startups</button>
            <button class="btn-invest" onclick="alert('Αναζήτηση Ακινήτων...')">Ακίνητα</button>
        </div>
        <button class="btn-back" onclick="showNext('start')">⬅ Πίσω στην αρχή</button>
    </div>
</div>

<script>
    function showNext(id) {
        document.querySelectorAll('.menu-section').forEach(section => {
            section.classList.remove('active');
        });
        document.getElementById(id).classList.add('active');
    }
</script>

</body>
</html>
