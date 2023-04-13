# lindgrenar
<!-- README.md -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: 'Courier New', monospace;
      background-color: black;
      color: lime;
      overflow: hidden;
    }

    h1, h2 {
      font-size: 2em;
      text-transform: uppercase;
      margin: 0;
      animation: glitch 1s infinite;
    }

    a {
      color: lime;
      text-decoration: none;
    }

    .container {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
      align-items: center;
      height: 100vh;
      position: relative;
    }

    .profile-info {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      z-index: 1;
    }

    .floating-element {
      position: absolute;
      animation: float 3s infinite alternate;
    }

    @keyframes float {
      0% {
        transform: translateY(0);
      }
      100% {
        transform: translateY(-10px);
      }
    }

    @keyframes glitch {
      0%, 100% {
        text-shadow: none;
      }
      3%, 5%, 18%, 20%, 30%, 32%, 45%, 47%, 60%, 62%, 80%, 82% {
        text-shadow: 2px 0 lime;
      }
      7%, 9%, 15%, 17%, 26%, 28%, 42%, 44%, 52%, 54%, 75%, 77% {
        text-shadow: -2px 0 lime;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="profile-info">
      <h1>lindgrenar</h1>
      <h2>hello</h2>
      <p>🔭 I’m currently working on: <a href="https://github.com/username/project">Project Name</a></p>
      <p>🌱 I’m currently learning: <a href="https://www.example.com">New Technology</a></p>
      <p>📫 How to reach me: <a href="mailto:email@example.com">email@example.com</a></p>
    </div>
    <img class="floating-element" src="https://placekitten.com/100/100" alt="kitten" style="top: 10%; left: 20%;">
    <img class="floating-element" src="https://placekitten.com/150/150" alt="kitten" style="top: 80%; left: 30%;">
    <img class="floating-element" src="https://placekitten.com/75/75" alt="kitten" style="top: 50%; left: 70%;">
  </div>
  <script>
    const glitchElements = document.querySelectorAll('h1, h2, p');
    glitchElements.forEach(el => {
      el.addEventListener('mouseover', ()
  => {
    el.style.animation = 'glitch 100ms infinite';
  });

  el.addEventListener('mouseout', () => {
    el.style.animation = '';
  });
});

const floatingElements = document.querySelectorAll('.floating-element');
floatingElements.forEach(el => {
  const randomDelay = Math.random() * 3;
  el.style.animationDelay = `${randomDelay}s`;
});

  </script>
</body>
</html>
