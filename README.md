<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday, Bugg! 🫂🤍</title>
    <style>
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            background: linear-gradient(to bottom, #ffe6f7, #e6f7ff);
            color: #333;
            text-align: center;
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }

        #fireworksCanvas {
            position: fixed;
            top: 0;
            left: 0;
            z-index: 0;
            pointer-events: none;
        }

        body > * {
            position: relative;
            z-index: 1;
        }

        h1 {
            font-size: 3em;
            color: #ff69b4;
            text-shadow: 2px 2px #fff;
            margin-top: 50px;
        }

        .message {
            font-size: 1.5em;
            margin: 20px auto;
            max-width: 600px;
            line-height: 1.6;
        }

        .cake {
            width: 200px;
            height: 150px;
            background: #f4a261;
            border-radius: 50% 50% 0 0;
            position: relative;
            margin: 20px auto;
            transition: transform 0.3s;
        }

        .cake:hover {
            transform: scale(1.1);
            box-shadow: 0 0 20px #ff69b4;
        }

        .cake::before {
            content: '';
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 50px;
            background: #ff69b4;
            border-radius: 50%;
        }

        .cake::after {
            content: '🎂';
            position: absolute;
            top: -30px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 2em;
        }

        .balloons {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .balloon {
            position: absolute;
            width: 50px;
            height: 70px;
            background: radial-gradient(circle, #ff69b4, #ffb6c1);
            border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
            animation: float 6s infinite ease-in-out;
            cursor: pointer;
            pointer-events: auto;
        }

        .balloon:nth-child(odd) {
            background: radial-gradient(circle, #87ceeb, #add8e6);
        }

        .balloon::before {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 20px;
            background: #333;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .popped {
            opacity: 0;
            transform: scale(0);
            transition: all 0.3s;
        }

        footer {
            margin-top: 50px;
            font-size: 1em;
            color: #666;
        }
