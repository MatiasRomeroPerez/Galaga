<!DOCTYPE html>
<html lang="es">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Juego Estilo Galaga</title>
    <!-- Cargando Tailwind CSS desde CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Estilo adicional para el juego */
        body {
            background-color: #111;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .game-container {
            width: 800px;
            height: 600px;
            background-color: black;
            border: 2px solid #fff;
            position: relative;
            overflow: hidden;
        }
        .ship {
            position: absolute;
            bottom: 10px;
            left: 50%;
            transform: translateX(-50%);
            width: 30px;
            height: 30px;
            background-color: #00f;
        }
        .bullet {
            position: absolute;
            bottom: 40px;
            width: 5px;
            height: 10px;
            background-color: #f00;
        }
        .enemy {
            position: absolute;
            width: 30px;
            height: 30px;
            background-color: #0f0;
        }
        .score-board {
            position: absolute;
            top: 10px;
            left: 10px;
            color: white;
            font-size: 18px;
        }
        .instructions {
            position: absolute;
            bottom: 10px;
            left: 50%;
            transform: translateX(-50%);
            color: white;
            font-size: 14px;
            text-align: center;
        }
    </style>
</head>

<body>

    <!-- Contenedor del juego -->
    <div class="game-container" id="gameContainer">
        <div class="score-board" id="score">Puntuación: 0</div>
        <div class="ship" id="ship"></div>
        <div class="instructions">
            Usa las teclas de flecha para mover y espacio para disparar.
        </div>
    </div>

    <script>
        // Definir elementos clave
        const gameContainer = document.getElementById('gameContainer');
        const ship = document.getElementById('ship');
        const scoreBoard = document.getElementById('score');

        let score = 0;
        let shipPosX = 375; // Posición inicial de la nave
        let shipSpeed = 10;
        let bullets = [];
        let enemies = [];
        let gameOver = false;

        // Función para crear un enemigo
        function createEnemy() {
            const enemy = document.createElement('div');
            enemy.classList.add('enemy');
            enemy.style.top = '0px';
            enemy.style.left = `${Math.random() * (gameContainer.offsetWidth - 30)}px`;
            gameContainer.appendChild(enemy);
            enemies.push(enemy);
        }

        // Mover los enemigos
        function moveEnemies() {
            for (let i = 0; i < enemies.length; i++) {
                let enemy = enemies[i];
                let currentTop = parseInt(enemy.style.top, 10);
                if (currentTop >= gameContainer.offsetHeight) {
                    enemy.remove();
                    enemies.splice(i, 1);
                    i--;
                } else {
                    enemy.style.top = `${currentTop + 1}px`;
                }
            }
        }

        // Crear una bala
        function createBullet() {
            const bullet = document.createElement('div');
            bullet.classList.add('bullet');
            bullet.style.left = `${shipPosX + 12.5}px`; // Centrando la bala respecto a la nave
            gameContainer.appendChild(bullet);
            bullets.push(bullet);
        }

        // Mover las balas
        function moveBullets() {
            for (let i = 0; i < bullets.length; i++) {
                let bullet = bullets[i];
                let currentBottom = parseInt(bullet.style.bottom, 10);
                if (currentBottom >= gameContainer.offsetHeight) {
                    bullet.remove();
                    bullets.splice(i, 1);
                    i--;
                } else {
                    bullet.style.bottom = `${currentBottom + 5}px`;
                    checkBulletCollision(bullet, i);
                }
            }
        }

        // Comprobar colisiones entre balas y enemigos
        function checkBulletCollision(bullet, bulletIndex) {
            for (let i = 0; i < enemies.length; i++) {
                let enemy = enemies[i];
                let enemyRect = enemy.getBoundingClientRect();
                let bulletRect = bullet.getBoundingClientRect();
                if (bulletRect.top <= enemyRect.bottom && bulletRect.left >= enemyRect.left && bulletRect.right <= enemyRect.right) {
                    enemy.remove();
                    bullet.remove();
                    enemies.splice(i, 1);
                    bullets.splice(bulletIndex, 1);
                    score++;
                    scoreBoard.innerHTML = `Puntuación: ${score}`;
                    break;
                }
            }
        }

        // Mover la nave
        function moveShip(event) {
            if (event.key === 'ArrowLeft' && shipPosX > 0) {
                shipPosX -= shipSpeed;
            }
            if (event.key === 'ArrowRight' && shipPosX < gameContainer.offsetWidth - 30) {
                shipPosX += shipSpeed;
            }
            ship.style.left = `${shipPosX}px`;
        }

        // Iniciar el juego
        function startGame() {
            // Mover los enemigos y las balas
            setInterval(() => {
                if (!gameOver) {
                    moveEnemies();
                    moveBullets();
                }
            }, 100);

            // Crear enemigos en intervalos
            setInterval(() => {
                if (!gameOver) {
                    createEnemy();
                }
            }, 1000);
        }

        // Controlar las teclas
        document.addEventListener('keydown', (event) => {
            if (event.key === 'ArrowLeft' || event.key === 'ArrowRight') {
                moveShip(event);
            }
            if (event.key === ' ') {
                createBullet();
            }
        });

        // Iniciar el juego
        startGame();
    </script>
</body>

</html>
