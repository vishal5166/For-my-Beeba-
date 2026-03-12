# For-my-Beeba-
Bday wish for my bossy girl 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Arushi</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Montserrat:wght@300;500&display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>
    <style>
        body { margin: 0; height: 100vh; display: flex; justify-content: center; align-items: center; background: #fff5f7; font-family: 'Montserrat', sans-serif; overflow: hidden; }
        .container { text-align: center; padding: 40px; border-radius: 30px; background: white; box-shadow: 0 15px 40px rgba(214, 51, 132, 0.15); max-width: 450px; width: 85%; border: 1px solid #ffeef2; }
        
        h1 { font-family: 'Dancing Script', cursive; font-size: 3.5rem; color: #d63384; margin: 0; opacity: 0; transform: scale(0.5); transition: all 1.2s cubic-bezier(0.175, 0.885, 0.32, 1.275); }
        .quote { font-size: 1.1rem; color: #555; margin-top: 25px; line-height: 1.6; opacity: 0; transition: all 2s ease; font-style: italic; }
        
        .reveal-btn { background: #d63384; color: white; border: none; padding: 16px 40px; border-radius: 50px; font-size: 1.1rem; cursor: pointer; font-weight: 500; transition: 0.4s; box-shadow: 0 5px 15px rgba(214, 51, 132, 0.3); }
        .reveal-btn:hover { background: #ff4d94; transform: translateY(-3px); }
        
        .show-name { opacity: 1 !important; transform: scale(1) !important; }
        .show-quote { opacity: 1 !important; }
    </style>
</head>
<body>

<div class="container">
    <div id="pre-text" style="color: #a3a3a3; margin-bottom: 25px; font-weight: 300;">I have something to say...</div>
    
    <h1 id="name">Happy Birthday, Arushi!</h1>
    
    <div id="quote" class="quote">
        "To the girl who makes every day feel like a celebration—may your year be as bright and beautiful as your smile."
    </div>
    
    <br>
    <button class="reveal-btn" id="btn" onclick="celebrate()">Tap to Open 🎁</button>
</div>

<script>
    function celebrate() {
        // Remove button and intro
        document.getElementById('btn').style.display = 'none';
        document.getElementById('pre-text').style.display = 'none';
        
        // Show Name & Quote
        document.getElementById('name').classList.add('show-name');
        setTimeout(() => {
            document.getElementById('quote').classList.add('show-quote');
        }, 800);
        
        // Continuous Confetti for 5 seconds
        var end = Date.now() + (5 * 1000);
        var colors = ['#d63384', '#ff85a1', '#ffffff', '#ffd1dc'];

        (function frame() {
          confetti({ particleCount: 4, angle: 60, spread: 55, origin: { x: 0, y: 0.7 }, colors: colors });
          confetti({ particleCount: 4, angle: 120, spread: 55, origin: { x: 1, y: 0.7 }, colors: colors });

          if (Date.now() < end) {
            requestAnimationFrame(frame);
          }
        }());
    }
</script>

</body>
</html>
