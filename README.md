<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Notre Dame Football</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #0C2340;
      color: white;
      text-align: center;
    }
    header {
      background: #AE9142;
      padding: 20px;
    }
    h1 {
      margin: 0;
      font-size: 2.5em;
    }
    main {
      padding: 40px 20px;
      max-width: 800px;
      margin: auto;
    }
    a.btn {
      display: inline-block;
      padding: 12px 20px;
      margin-top: 20px;
      background: #AE9142;
      color: #0C2340;
      text-decoration: none;
      font-weight: bold;
      border-radius: 8px;
    }
    a.btn:hover {
      background: #c4a856;
    }
    footer {
      background: #111;
      padding: 20px;
      font-size: 0.9em;
      color: #aaa;
      margin-top: 40px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Notre Dame Football</h1>
  </header>

  <main>
    <h2>Welcome Fighting Irish Fans!</h2>
    <p>
      Notre Dame Fighting Irish football is one of the most storied programs in college sports.
      With legendary players, historic championships, and unforgettable moments, the team embodies
      tradition and excellence on and off the field.
    </p>
    <a class="btn" href="https://fightingirish.com/sports/football/" target="_blank">
      Visit Official Site
    </a>
  </main>

  <footer>
    © <span id="year"></span> Notre Dame Football Fan Page
  </footer>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
