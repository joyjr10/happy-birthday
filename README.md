<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Happy Birthday Kannammaa</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0; padding: 0;
      box-sizing: border-box;
    }

    html, body {
      min-height: 100%;
      background-color: #0d0d0d;
      font-family: 'Great Vibes', cursive;
      color: white;
      overflow-x: hidden;
    }

    .section {
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      min-height: 100vh; /* changed */
      width: 100%;
      position: absolute;
      top: 0; left: 0;
      transition: opacity 1s ease, transform 1s ease;
      z-index: 1;
      text-align: center;
      padding: 60px 20px 20px; /* added top padding */
      overflow-y: auto;
    }

    .hidden {
      opacity: 0;
      pointer-events: none;
      transform: scale(0.95);
    }

    #page1 input {
      background: transparent;
      border: none;
      border-bottom: 2px solid pink;
      font-size: 2rem;
      color: white;
      text-align: center;
      outline: none;
      margin-bottom: 20px;
    }

    #page1 button,
    #letterBtn {
      background-color: pink;
      color: black;
      border: none;
      padding: 10px 20px;
      font-size: 1.5rem;
      cursor: pointer;
      border-radius: 30px;
      transition: 0.3s ease;
    }

    #page1 button:hover,
    #letterBtn:hover {
      background-color: hotpink;
      color: white;
    }

    #page2 img {
      max-width: 300px;
      border-radius: 20px;
      box-shadow: 0 0 30px pink;
      margin-bottom: 20px;
    }

    #birthdayText {
      font-size: 3rem;
      color: pink;
      text-shadow: 0 0 10px white;
      margin-bottom: 20px;
    }

    #promises h2 {
      color: #ff66cc;
      font-size: 2.5rem;
      margin-bottom: 20px;
    }

    #promises ol {
      text-align: left;
      max-width: 700px;
      margin: 20px auto 0;
      font-size: 1.2rem;
      line-height: 2;
    }

    #tsparticles {
      position: absolute;
      width: 100%;
      height: 100%;
      z-index: 0;
    }

    .sparkle {
      position: fixed;
      width: 6px;
      height: 6px;
      background: radial-gradient(white, pink);
      border-radius: 50%;
      pointer-events: none;
      animation: sparkle-fly 6s linear infinite;
      opacity: 0.8;
      z-index: 9999;
    }

    @keyframes sparkle-fly {
      0% {
        transform: translateY(0) scale(1);
        opacity: 1;
      }
      100% {
        transform: translateY(-100vh) scale(0.5);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

  <div id="tsparticles"></div>

  <!-- Page 1 -->
  <div class="section" id="page1">
    <input type="text" id="nameInput" placeholder="Enter Your Name Princess.."/>
    <button onclick="showWish()"> Drop </button>
  </div>

  <!-- Page 2 -->
  <div class="section hidden" id="page2">
    <img src="ug.jpg" alt="Birthday Photo" />
    <div id="birthdayText">Happy Birthday Kannammaa</div>
    <button id="letterBtn" onclick="showLetter()">Letter 💌</button>
  </div>

  <!-- Page 3 -->
  <div class="section hidden" id="page3">
    <div id="promises">
      <h2>19 Promises for My Kannammaa💗 on Your 19th Birthday</h2>
      <ol>
        <li>I Promise to always come back to you.. no matter how much angry i get because your "Kannaa" melts every storm in me</li>
        <li>I promise to cherish your loyalty and care like it’s the rarest treasure I’ve ever received</li>
        <li>I promise to protect you from your insecurities and this cruel world.. you’re too precious to be touched by their darkness.</li>
        <li>I promise to never take your forgiveness for granted. I see it, I feel it, and I’m blessed by it.</li>
        <li>I promise to be your safe space, not just for your smiles but also for your tears, stress, anger, and silence. I’m your home.</li>
        <li>I promise that one day we’ll hold our little ‘Teddy’ in our arms.. a dream born from our love.</li>
        <li>I promise that whenever you cry, I’ll be right there,whispering,“You’re not alone..I’m here..Always”</li>
        <li>I promise to control my anger and words because you deserve understanding, not damage.</li>
        <li>I promise to be your horse, elephant, or whatever silly ride you want — your childish happiness is my fuel</li>
        <li>I promise to never judge you.. only love you more through everything.</li>
        <li>I promise to stand by you when society tries to shake your self-worth. I’ll never let their voices be louder than mine.</li>
        <li>I promise to remind you of your beauty inside and out when the mirror or others make you doubt it.</li>
        <li>I promise to hold your hand through every breakdown, every silence, every damn battle life throws.</li>
        <li>I promise that your happiness will never be optional for me.. it’s my priority, my mission.</li>
        <li>I promise that even in fights, I’ll choose to make it us vs the problem, never me vs you.</li>
        <li>I promise to spoil your inner child — with care, love, and patience, always</li>
        <li>I promise to love not only the best of you, but also the parts you try to hide.</li>
        <li>I promise that “forever” is not just a word — it’s a vow I make with every heartbeat.</li>
        <li>I promise you this: No matter what happens between us, I will never let you walk alone.. not in this life, not in any</li>
      </ol>
    </div>
  </div>

  <!-- Scripts -->
  <script src="https://cdn.jsdelivr.net/npm/tsparticles@2.11.1/tsparticles.bundle.min.js"></script>
  <script>
    tsParticles.load("tsparticles", {
      particles: {
        number: { value: 30 },
        shape: {
          type: "image",
          image: {
            src: "https://pngimg.com/uploads/rose/rose_PNG65885.png",
            width: 32,
            height: 32
          }
        },
        size: {
          value: 15,
          random: true
        },
        move: {
          direction: "bottom",
          enable: true,
          outModes: { default: "out" },
          speed: 2
        },
        opacity: {
          value: 0.9
        }
      },
      background: {
        color: "#0d0d0d"
      }
    });

    function showWish() {
      const name = document.getElementById("nameInput").value.trim();
      if (name.toLowerCase() === "akesha") {
        document.getElementById("page1").classList.add("hidden");
        document.getElementById("page2").classList.remove("hidden");
      } else {
        alert("Oops! Only Kannammaa can enter 😘");
      }
    }

    function showLetter() {
      document.getElementById("page2").classList.add("hidden");
      const page3 = document.getElementById("page3");
      page3.classList.remove("hidden");
      page3.scrollTop = 0;
    }

    function createSparkle() {
      const sparkle = document.createElement('div');
      sparkle.classList.add('sparkle');
      sparkle.style.left = Math.random() * 100 + 'vw';
      sparkle.style.top = '100vh';
      sparkle.style.animationDuration = (4 + Math.random() * 3) + 's';
      document.body.appendChild(sparkle);
      setTimeout(() => sparkle.remove(), 7000);
    }

    setInterval(createSparkle, 200);
  </script>
</body>
</html>
