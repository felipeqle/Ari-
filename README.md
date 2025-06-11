<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Para Arizbeth</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      background-color: black;
      overflow: hidden;
      font-family: 'Arial', sans-serif;
    }
<body>

<div class="centro">Te quiero mucho Arizbeth</div>
<button class="boton">Te quiero mucho</button>

<script>
  function crearTeQuiero() {
    const tqm = document.createElement('div');
    tqm.classList.add('te-quiero');
    tqm.textContent = 'te quiero mucho';
    tqm.style.left = Math.random() * window.innerWidth + 'px';
    tqm.style.top = '-20px';
    tqm.style.fontSize = (Math.random() * 20 + 10) + 'px';
    tqm.style.opacity = Math.random();
    document.body.appendChild(tqm);
    setTimeout(() => tqm.remove(), 5000);
  }

  function crearCorazon() {
    const corazon = document.createElement('div');
    corazon.classList.add('corazon');
    corazon.textContent = '❤';
    corazon.style.left = Math.random() * window.innerWidth + 'px';
    corazon.style.top = window.innerHeight + 'px';
    corazon.style.fontSize = (Math.random() * 20 + 20) + 'px';
    document.body.appendChild(corazon);
    setTimeout(() => corazon.remove(), 8000);
  }

  setInterval(crearTeQuiero, 100);
  setInterval(crearCorazon, 300);

  document.addEventListener('click', function(e) {
    for (let i = 0; i < 30; i++) {
      const tqmExtra = document.createElement('div');
      tqmExtra.classList.add('te-quiero');
      tqmExtra.textContent = 'te quiero mucho';
      tqmExtra.style.left = (e.clientX + (Math.random() * 200 - 100)) + 'px';
      tqmExtra.style.top = (e.clientY + (Math.random() * 100 - 50)) + 'px';
      tqmExtra.style.fontSize = (Math.random() * 20 + 10) + 'px';
      tqmExtra.style.opacity = Math.random();
      document.body.appendChild(tqmExtra);
      setTimeout(() => tqmExtra.remove(), 5000);
    }
  });
</script>

</body>
</html>
