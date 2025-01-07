<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FlightCoin.io</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: #333;
        }
        header {
            background: url('luxury-jet.jpg') no-repeat center center/cover;
            color: white;
            padding: 40px;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: space-around;
            background: #333;
            color: white;
            padding: 15px;
        }
        nav a {
            color: white;
            text-decoration: none;
            padding: 0 15px;
            font-size: 18px;
        }
        nav a:hover {
            text-decoration: underline;
        }
        .container {
            max-width: 1200px;
            margin: 20px auto;
            padding: 20px;
        }
        .countdown {
            text-align: center;
            font-size: 24px;
            margin: 30px 0;
        }
        .rewards, .winners, .about {
            margin-bottom: 50px;
        }
        .footer {
            text-align: center;
            background: #333;
            color: white;
            padding: 20px;
        }
        .gallery img {
            max-width: 100%;
            height: auto;
            margin: 10px 0;
        }
        textarea {
            width: 100%;
            height: 150px;
            margin-bottom: 20px;
            padding: 10px;
            font-size: 16px;
        }
        .luxury-gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }
        .luxury-gallery img {
            flex: 1 1 calc(33.333% - 10px);
            max-width: calc(33.333% - 10px);
            border-radius: 5px;
        }
        .cta {
            background: #f4f4f4;
            text-align: center;
            padding: 30px;
            margin: 50px 0;
            border-radius: 10px;
        }
        .cta a {
            display: inline-block;
            background: #333;
            color: white;
            text-decoration: none;
            padding: 15px 30px;
            font-size: 18px;
            border-radius: 5px;
        }
        .cta a:hover {
            background: #555;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to FlightCoin.io</h1>
        <p>Your gateway to luxury flight rewards powered by cryptocurrency.</p>
    </header>

    <nav>
        <a href="#rewards">Rewards Program</a>
        <a href="#winners">Winners</a>
        <a href="#gallery">Luxury Flights</a>
        <a href="#about">About Us</a>
        <a href="#feedback">Feedback</a>
    </nav>

    <div class="container">
        <div id="rewards" class="rewards">
            <h2>Rewards Program</h2>
            <p>Stake $10,000 in FlightCoin for at least 3 months to enter our luxury rewards program. Weekly rewards include 5 first-class roundtrip tickets valued at $5,000 each. Quarterly rewards include 5 midsized private jet roundtrips valued at $500,000 each.</p>
            <div class="countdown">
                <p>Next Weekly Reward Countdown: <span id="weekly-timer">Loading...</span></p>
                <p>Next Quarterly Reward Countdown: <span id="quarterly-timer">Loading...</span></p>
            </div>
        </div>

        <div id="winners" class="winners">
            <h2>Winners</h2>
            <p>Check out our latest winners and their luxury experiences!</p>
            <div class="luxury-gallery">
                <img src="winner1.jpg" alt="Winner enjoying a luxury jet">
                <img src="winner2.jpg" alt="First-class cabin experience">
                <img src="winner3.jpg" alt="Winner's story in flight">
            </div>
        </div>

        <div id="gallery" class="gallery">
            <h2>Luxury Flights</h2>
            <p>Explore the first-class cabins and midsized private jets you could experience.</p>
            <div class="luxury-gallery">
                <img src="jet1.jpg" alt="Luxury midsize jet interior">
                <img src="cabin1.jpg" alt="First-class cabin">
                <img src="cabin2.jpg" alt="Spacious first-class seating">
                <img src="jet2.jpg" alt="Private jet luxury">
                <img src="cabin3.jpg" alt="Exclusive first-class suites">
                <img src="jet3.jpg" alt="High-end jet interior">
            </div>
        </div>

        <div class="cta">
            <h2>Ready to Fly in Style?</h2>
            <p>Start staking FlightCoin today and unlock unparalleled luxury travel rewards.</p>
            <a href="#">Buy FlightCoin Now</a>
        </div>

        <div id="about" class="about">
            <h2>About FlightCoin</h2>
            <p>FlightCoin is dedicated to connecting cryptocurrency enthusiasts with the luxury travel experiences they deserve. By staking FlightCoin, you gain access to unparalleled rewards, including first-class flights and private jet experiences. Join our community and redefine your travel standards.</p>
        </div>

        <div id="feedback" class="feedback">
            <h2>Feedback</h2>
            <textarea placeholder="Leave your feedback here..."></textarea>
            <button>Submit</button>
        </div>
    </div>

    <footer class="footer">
        <p>&copy; 2025 FlightCoin.io - All Rights Reserved</p>
        <p><a href="https://twitter.com" target="_blank">Follow us on Twitter</a> | <a href="#">Buy FlightCoin</a></p>
    </footer>

    <script>
        // Countdown timer logic
        function countdown(dateString, elementId) {
            const targetDate = new Date(dateString);
            setInterval(() => {
                const now = new Date();
                const timeLeft = targetDate - now;
                const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
                const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);
                document.getElementById(elementId).textContent = `${days}d ${hours}h ${minutes}m ${seconds}s`;
            }, 1000);
        }

        countdown('2025-01-13T00:00:00', 'weekly-timer'); // Weekly reward countdown
        countdown('2025-03-31T00:00:00', 'quarterly-timer'); // Quarterly reward countdown
    </script>
</body>
</html>
