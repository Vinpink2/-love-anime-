<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Love Explosion Animation</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: black;
            overflow: hidden;
        }

        .heart {
            position: relative;
            width: 100px;
            height: 100px;
            background-color: red;
            transform: rotate(-45deg);
            animation: shine 1s infinite;
        }

        .heart::before,
        .heart::after {
            content: '';
            position: absolute;
            width: 100px;
            height: 100px;
            background-color: red;
            border-radius: 50%;
        }

        .heart::before {
            top: -50px;
            left: 0;
        }

        .heart::after {
            left: 50px;
            top: 0;
        }

        @keyframes shine {
            0% {
                box-shadow: 0 0 20px rgba(255, 0, 0, 0.5);
            }
            50% {
                box-shadow: 0 0 40px rgba(255, 0, 0, 1);
            }
            100% {
                box-shadow: 0 0 20px rgba(255, 0, 0, 0.5);
            }
        }

        .explosion {
            position: absolute;
            width: 200px;
            height: 200px;
            border-radius: 50%;
            opacity: 0;
            animation: explode 1s forwards;
        }

        @keyframes explode {
            0% {
                opacity: 1;
                transform: scale(1);
            }
            100% {
                opacity: 0;
                transform: scale(3);
            }
        }
    </style>
</head>
<body>
    <div class="heart" id="heart"></div>

    <script>
        const heart = document.getElementById('heart');

        heart.addEventListener('click', () => {
            const colors = ['green', 'blue', 'white'];
            colors.forEach(color => {
                const explosion = document.createElement('div');
                explosion.classList.add('explosion');
                explosion.style.backgroundColor = color;
                explosion.style.left = `${Math.random() * 100}%`;
                explosion.style.top = `${Math.random() * 100}%`;
                document.body.appendChild(explosion);
                setTimeout(() => {
                    explosion.remove();
                }, 1000);
            });
        });
    </script>
</body>
</html>
