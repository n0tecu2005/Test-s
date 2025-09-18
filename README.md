you wont to make your own lua config for FiveM comm in my discord server 


<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ECU</title>
    <style>
        body {
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #1e1e1e, #3c3c3c);
            font-family: 'Arial Black', sans-serif;
        }

        h1 {
            font-size: 15vw; /* Sehr große Schrift */
            color: #ffcc00;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.7);
            letter-spacing: 5px;
        }
    </style>
</head>
<body>
    <h1>ECU</h1>

    <script>
        // Optional: kleine Animation, z.B. leichtes Pulsieren
        const title = document.querySelector('h1');
        let growing = true;

        setInterval(() => {
            let currentSize = parseFloat(getComputedStyle(title).fontSize);
            if (growing) {
                currentSize += 1;
                if (currentSize >= window.innerWidth * 0.15) growing = false;
            } else {
                currentSize -= 1;
                if (currentSize <= window.innerWidth * 0.14) growing = true;
            }
            title.style.fontSize = currentSize + 'px';
        }, 100);
    </script>
</body>
</html>
