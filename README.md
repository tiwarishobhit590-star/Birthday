# Birthday
<!DOCTYPE html>
<html>
<head>
    <title>18th Birthday Invitation</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', sans-serif;
            text-align: center;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            color: white;
        }

        .container {
            padding: 30px 20px;
        }

        h1 {
            font-size: 40px;
            margin-top: 20px;
        }

        h2 {
            font-size: 26px;
        }

        .card {
            background: rgba(255,255,255,0.2);
            padding: 25px;
            border-radius: 20px;
            margin-top: 25px;
            backdrop-filter: blur(10px);
        }

        .details {
            font-size: 20px;
            margin: 10px 0;
        }

        #countdown {
            font-size: 28px;
            font-weight: bold;
            margin-top: 15px;
        }

        .btn {
            margin-top: 20px;
            padding: 12px 25px;
            border: none;
            border-radius: 25px;
            background: white;
            color: #ff4e8b;
            font-size: 18px;
            cursor: pointer;
            transition: 0.3s;
        }

        .btn:hover {
            background: #ff4e8b;
            color: white;
        }

        .footer {
            margin-top: 40px;
            font-size: 16px;
        }
    </style>
</head>
<body>

<div class="container">

    <h1>🎉 You're Invited 🎉</h1>
    <h2>18th Birthday Celebration</h2>

    <div class="card">
        <h2>Nitya Goyal & Nishtha Goyal</h2>

        <p class="details">📅 Date: 28 February</p>
        <p class="details">🎉 Turning: 18 Years</p>
        <p class="details">📍 Venue: Cold Rock Coffee, RDC Rajnagar</p>

        <div id="countdown"></div>

        <button class="btn" onclick="alert('We are waiting for you ❤️')">
            Join the Celebration
        </button>
    </div>

    <div class="footer">
        Made with ❤️ for a Special 18th Birthday
    </div>

</div>

<script>
    var birthdayDate = new Date("Feb 28, 2026 00:00:00").getTime();

    var x = setInterval(function() {
        var now = new Date().getTime();
        var distance = birthdayDate - now;

        var days = Math.floor(distance / (1000 * 60 * 60 * 24));
        var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        var seconds = Math.floor((distance % (1000 * 60)) / 1000);

        document.getElementById("countdown").innerHTML =
        "⏳ " + days + "d " + hours + "h "
        + minutes + "m " + seconds + "s ";

        if (distance < 0) {
            clearInterval(x);
            document.getElementById("countdown").innerHTML = "🎂 It's Party Time! 🎉";
        }
    }, 1000);
</script>

</body>
</html>
