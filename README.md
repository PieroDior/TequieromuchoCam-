# TequieromuchoCam-<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Te quiero mucho</title>

<style>
body {
    margin: 0;
    height: 100vh;
    overflow: hidden;
    background: linear-gradient(135deg, #ff758c, #ff7eb3);
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: Arial, sans-serif;
}

h1 {
    color: white;
    font-size: 3.5rem;
    text-shadow: 0 0 10px rgba(0,0,0,0.4);
    z-index: 2;
}

/* Corazones */
.heart {
    position: fixed;
    top: -10px;
    font-size: 24px;
    animation: fall linear infinite;
}

@keyframes fall {
    to {
        transform: translateY(110vh);
    }
}
</style>
</head>

<body>

<h1>💖 Te quiero mucho 💖</h1>

<!-- Música -->
<audio autoplay loop>
    <source src="musica.mp3" type="audio/mpeg">
</audio>

<script>
function crearCorazon() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = (3 + Math.random() * 5) + "s";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 8000);
}

setInterval(crearCorazon, 300);
</script>

</body>
</html>
