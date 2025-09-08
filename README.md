# --- Simple Notre Dame Football Website ---
set -e

# Create folder
SITE="nd-football-site"
mkdir -p "$SITE"
cd "$SITE"

# HTML
cat > index.html <<'EOF'
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
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
    h1 { margin: 0; font-size: 2.5em; }
    .content { padding: 40px 20px; max-width: 800px; margin: auto; }
    .btn {
      display: inline-block;
      padding: 12px 20px;
      margin-top: 20px;
      background: #AE9142;
      color: #0C2340;
      text-decoration: none;
      font-weight: bold;
      border-radius: 8px;
    }
    .btn:hover { background: #c4a856; }
    footer {
      background: #111;
      padding: 20px;
      font-size: 0.9em;
      color: #aaa;
    }
  </style>
</head>
<body>
  <header>
    <h1>Notre Dame Football</h1>
  </header>
  <div class="content">
    <h2>Welcome to Fighting Irish Football</h2>
    <p>
      The Notre Dame Fighting Irish football program is one of the most storied
      traditions in college sports. With national championships, Heisman winners,
      and unforgettable moments, it represents excellence on and off the field.
    </p>
    <a class="btn" href="https://fightingirish.com/sports/football/" target="_blank">Official Site</a>
  </div>
  <footer>
    © <span id="year"></span> Notre Dame Football Fan Page
  </footer>
  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
EOF

# Serve locally
echo "Starting server at http://localhost:8000 (Ctrl+C to stop)..."
python3 -m http.server 8000

