<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Presidential Election Map</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        header {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1em 0;
        }
        #map {
            height: 60vh;
            width: 100%;
            border: 1px solid #ddd;
        }
        .year-slider {
            margin: 20px;
            text-align: center;
        }
        .candidate-container {
            display: flex;
            justify-content: space-around;
            margin: 20px;
            padding: 10px;
        }
        .candidate {
            text-align: center;
            width: 30%;
            border: 1px solid #ddd;
            padding: 10px;
            border-radius: 8px;
        }
        .candidate img {
            border-radius: 50%;
            width: 150px;
            height: 150px;
        }
        .candidate .name {
            font-size: 1.2em;
            font-weight: bold;
        }
        .candidate .details {
            margin-top: 10px;
        }
    </style>
</head>
<body>

<header>
    <h1>Interactive Presidential Election Map (1996 - 2024)</h1>
</header>

<div id="map">
    <!-- Placeholder for interactive map -->
    <h2 style="text-align:center; margin-top: 50px;">Interactive Election Map Coming Soon</h2>
</div>

<div class="year-slider">
    <label for="years">Select Election Year: </label>
    <input type="range" id="years" name="years" min="1996" max="2024" value="2020" oninput="updateYear(this.value)">
    <span id="year-display">2020</span>
</div>

<!-- Example data for Florida, 2020 election -->
<div class="candidate-container" id="candidate-container">
    <div class="candidate">
        <img src="trump-placeholder.jpg" alt="Donald Trump">
        <div class="name">Donald Trump (R)</div>
        <div class="details">
            <span class="vote-total">Total Votes: 5,668,731</span><br>
            <span class="vote-percentage">Percentage: 51.2%</span>
        </div>
    </div>
    <div class="candidate">
        <img src="biden-placeholder.jpg" alt="Joe Biden">
        <div class="name">Joe Biden (D)</div>
        <div class="details">
            <span class="vote-total">Total Votes: 5,297,045</span><br>
            <span class="vote-percentage">Percentage: 47.9%</span>
        </div>
    </div>
</div>

<script>
    const electionData = {
        2020: {
            "Florida": {
                republican: {
                    name: "Donald Trump",
                    votes: 5668731,
                    percentage: "51.2%",
                    img: "trump-placeholder.jpg"
                },
                democrat: {
                    name: "Joe Biden",
                    votes: 5297045,
                    percentage: "47.9%",
                    img: "biden-placeholder.jpg"
                }
            }
        }
        // Add more data for other years/states here...
    };

    function updateYear(year) {
        document.getElementById('year-display').innerText = year;
        // Update data for the selected year
        const data = electionData[year]["Florida"];
        document.querySelectorAll(".candidate img")[0].src = data.republican.img;
        document.querySelectorAll(".candidate img")[1].src = data.democrat.img;
        document.querySelectorAll(".candidate .name")[0].innerText = `${data.republican.name} (R)`;
        document.querySelectorAll(".candidate .name")[1].innerText = `${data.democrat.name} (D)`;
        document.querySelectorAll(".candidate .vote-total")[0].innerText = `Total Votes: ${data.republican.votes}`;
        document.querySelectorAll(".candidate .vote-total")[1].innerText = `Total Votes: ${data.democrat.votes}`;
        document.querySelectorAll(".candidate .vote-percentage")[0].innerText = `Percentage: ${data.republican.percentage}`;
        document.querySelectorAll(".candidate .vote-percentage")[1].innerText = `Percentage: ${data.democrat.percentage}`;
    }
</script>

</body>
</html>
