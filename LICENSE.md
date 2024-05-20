<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GPL Cricket Scores</title>
    <style>
        body { font-family: Arial, sans-serif; background-color: #f4f4f4; color: #333; }
        .scoreboard, .head-to-head { margin: 20px; padding: 20px; border: 1px solid #ddd; background-color: #fff; }
        .match, .team-record { margin-bottom: 10px; }
        .match-header, h2 { font-weight: bold; }
        .team-logo { width: 100px; height: 100px; background-size: cover; border-radius: 50%; }
        .sunrising-indians { background-image: url('sunrising-indians-logo.png'); }
        .knight-mega-kings { background-image: url('knight-mega-kings-logo.png'); }
        .vs { font-size: 24px; font-weight: bold; }
        .team-stats h3 { margin: 0; }
        .team-stats p { margin: 5px 0; }
    </style>
</head>
<body>
    <header>
        <h1>GPL Cricket Scores: Sunrising Indians vs Knight Mega Kings</h1>
    </header>
    <section class="head-to-head">
        <h2>Head-to-Head Record</h2>
        <div class="team-record">
            <div class="team-logo sunrising-indians"></div>
            <div class="team-stats">
                <h3>Sunrising Indians</h3>
                <p>Wins: 7</p>
            </div>
            <div class="vs">VS</div>
            <div class="team-stats">
                <h3>Knight Mega Kings</h3>
                <p>Wins: 3</p>
            </div>
            <div class="team-logo knight-mega-kings"></div>
        </div>
    </section>
    <section class="scoreboard" id="scoreboard">
        <!-- Scores will be updated here -->
    </section>
    <script>
        // Sample data structure for GPL match scores
        const matches = [
            { team1: "Sunrising Indians", team2: "Knight Mega Kings", score1: 0, score2: 0 },
            // Add more match data here
        ];

        // Function to display scores
        function displayScores() {
            const scoreboard = document.getElementById('scoreboard');
            scoreboard.innerHTML = ''; // Clear previous scores
            matches.forEach(match => {
                const matchElement = document.createElement('div');
                matchElement.classList.add('match');
                matchElement.innerHTML = `
                    <div class="match-header">${match.team1} vs ${match.team2}</div>
                    <div>${match.team1}: ${match.score1}</div>
                    <div>${match.team2}: ${match.score2}</div>
                `;
                scoreboard.appendChild(matchElement);
            });
        }

        // Call displayScores to update the scoreboard
        displayScores();
    </script>
</body>
</html>

