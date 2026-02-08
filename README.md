# naman-sharma52
this is my 9th repository
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Netflix Style UI</title>
    <style>
        :root {
            --netflix-red: #e50914;
            --bg-black: #141414;
        }

        body {
            font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
            background-color: var(--bg-black);
            color: white;
            margin: 0;
            overflow-x: hidden;
        }

        /* Navbar */
        .navbar {
            padding: 20px 50px;
            background: linear-gradient(to bottom, rgba(0,0,0,0.7) 10%, transparent);
            position: fixed;
            width: 100%;
            z-index: 10;
            display: flex;
            align-items: center;
        }

        .logo {
            color: var(--netflix-red);
            font-size: 30px;
            font-weight: bold;
            letter-spacing: -1px;
            margin-right: 40px;
        }

        /* Hero Section */
        .hero {
            position: relative;
            height: 80vh;
            width: 100%;
            overflow: hidden;
        }

        .hero-video {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 100vw;
            height: 100vh;
            transform: translate(-50%, -50%);
            pointer-events: none;
        }

        .hero-video iframe {
            width: 100vw;
            height: 56.25vw; /* 16:9 ratio */
            min-height: 100vh;
            min-width: 177.77vh;
        }

        .hero-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to right, rgba(0,0,0,0.8) 20%, transparent 60%),
                        linear-gradient(to top, var(--bg-black), transparent 40%);
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding-left: 50px;
        }

        .hero-content h1 { font-size: 3.5rem; margin-bottom: 10px; }
        .hero-content p { max-width: 500px; font-size: 1.2rem; margin-bottom: 20px; }

        .btn {
            padding: 10px 25px;
            font-size: 1.1rem;
            font-weight: bold;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin-right: 10px;
        }
        .btn-play { background-color: white; color: black; }
        .btn-info { background-color: rgba(109, 109, 110, 0.7); color: white; }

        /* Content Rows */
        .row {
            padding: 20px 50px;
        }

        .row-title { font-size: 1.5rem; margin-bottom: 10px; }

        .thumbnails {
            display: flex;
            gap: 10px;
            overflow-x: auto;
            padding: 10px 0;
        }

        .thumbnails::-webkit-scrollbar { display: none; }

        .card {
            min-width: 250px;
            height: 140px;
            background-color: #333;
            border-radius: 4px;
            transition: transform 0.3s ease;
            cursor: pointer;
            overflow: hidden;
        }

        .card:hover {
            transform: scale(1.15);
            z-index: 5;
        }

        .card iframe { width: 100%; height: 100%; border: none; }

    </style>
</head>
<body>

    <div class="navbar">
        <div class="logo">NETFLIX</div>
    </div>

    <div class="hero">
        <div class="hero-video">
            <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ?autoplay=1&mute=1&controls=0&loop=1&playlist=dQw4w9WgXcQ" allow="autoplay"></iframe>
        </div>
        <div class="hero-overlay">
            <div class="hero-content">
                <h1>Monostable Pulse</h1>
                <p>A B.Tech student discovers the secret to the 555 timer. Will the circuit hold its stable state, or will the trigger change everything?</p>
                <button class="btn btn-play">▶ Play</button>
                <button class="btn btn-info">ⓘ More Info</button>
            </div>
        </div>
    </div>

    <div class="row">
        <div class="row-title">Trending Now</div>
        <div class="thumbnails">
            <div class="card"><iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ?controls=0"></iframe></div>
            <div class="card"><iframe src="https://www.youtube.com/embed/377pxMNUTwo?controls=0"></iframe></div>
            <div class="card"><iframe src="https://www.youtube.com/embed/5PXg2mqo4f0?controls=0"></iframe></div>
            <div class="card"><iframe src="https://www.youtube.com/embed/VIDEO_ID?controls=0"></iframe></div>
        </div>
    </div>

</body>
</html>
