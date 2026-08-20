<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>For Alaa 🌹</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,500&family=Cormorant+Garamond:ital,wght@0,400;0,500;1,400&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --wine: #5c0a1e;
    --wine-deep: #3a0512;
    --rose: #b3122f;
    --rose-light: #e8a1ad;
    --cream: #f7ece2;
    --gold: #c9a15a;
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html,body{
    background: var(--wine-deep);
    color: var(--cream);
    font-family: 'Cormorant Garamond', serif;
    overflow-x:hidden;
    min-height:100vh;
    -webkit-text-size-adjust: 100%;
  }
  body::before{
    content:"";
    position:fixed; inset:0;
    background:
      radial-gradient(circle at 20% 15%, rgba(179,18,47,0.35), transparent 40%),
      radial-gradient(circle at 80% 85%, rgba(201,161,90,0.15), transparent 45%),
      var(--wine-deep);
    z-index:-2;
  }

  /* ---------- Petals Animation ---------- */
  .petal{
    position:fixed; top:-5vh; pointer-events:none; z-index:5;
    font-size: 18px; opacity:.85; color: var(--rose);
    animation: fall linear infinite;
    filter: drop-shadow(0 0 3px rgba(0,0,0,0.3));
  }
  @keyframes fall{
    0%{ transform: translateY(-10vh) translateX(0) rotate(0deg); }
    100%{ transform: translateY(110vh) translateX(30px) rotate(360deg); }
  }

  /* ---------- Password Gate ---------- */
  #gate{
    position:fixed; inset:0; z-index:50;
    display:flex; align-items:center; justify-content:center;
    background: var(--wine-deep);
    transition: opacity .9s ease, visibility .9s ease;
  }
  .gate-card{
    text-align:center;
    padding: 48px 36px;
    max-width: 380px;
    width:88%;
  }
  .gate-mark{
    font-family:'Poppins', sans-serif;
    font-size: 13px;
    letter-spacing: .3em;
    color: var(--gold);
    text-transform:uppercase;
    margin-bottom: 18px;
    opacity:.85;
  }
  .gate-title{
    font-size: 44px;
    color: var(--cream);
    margin-bottom: 8px;
    font-weight:700;
  }
  .gate-sub{
    font-size:19px;
    color: var(--rose-light);
    margin-bottom: 34px;
  }
  #pwd{
    width:100%;
    padding: 14px 18px;
    border-radius: 999px;
    border: 1px solid rgba(201,161,90,0.5);
    background: rgba(255,255,255,0.05);
    color: var(--cream);
    font-size: 20px;
    text-align:center;
    letter-spacing: .3em;
    outline:none;
    font-family: 'Poppins', sans-serif;
    -webkit-appearance: none;
  }
  #pwd:focus{ border-color: var(--gold); box-shadow: 0 0 0 3px rgba(201,161,90,0.15); }
  #gate-btn{
    margin-top: 18px;
    padding: 12px 34px;
    border-radius: 999px;
    border: 1px solid var(--gold);
    background: transparent;
    color: var(--gold);
    font-family:'Poppins', sans-serif;
    font-size: 15px;
    letter-spacing:.15em;
    cursor:pointer;
    transition: all .35s ease;
    -webkit-appearance: none;
  }
  #gate-btn:hover{ background: var(--gold); color: var(--wine-deep); }
  #gate-error{
    margin-top: 14px;
    font-size: 15px;
    color: var(--rose-light);
    min-height: 18px;
    font-family:'Poppins', sans-serif;
    opacity:0;
    transition: opacity .3s;
  }
  #gate-error.show{ opacity:1; }
  .shake{ animation: shake .5s; }
  @keyframes shake{
    10%,90%{ transform: translateX(-2px); }
    20%,80%{ transform: translateX(4px); }
    30%,50%,70%{ transform: translateX(-8px); }
    40%,60%{ transform: translateX(8px); }
  }

  /* ---------- Main Content ---------- */
  #content{
    display:none;
    position:relative;
    z-index:1;
    padding: 70px 6vw 120px;
    max-width: 900px;
    margin: 0 auto;
  }
  header.hero{
    text-align:center;
    margin-bottom: 60px;
  }
  .eyebrow{
    font-family:'Poppins', sans-serif;
    letter-spacing:.35em;
    font-size:12px;
    color: var(--gold);
    text-transform:uppercase;
    margin-bottom:22px;
  }
  .hero h1{
    font-size: clamp(46px, 9vw, 84px);
    font-weight:700;
    color: var(--cream);
    line-height:1.1;
    text-shadow: 0 4px 30px rgba(179,18,47,0.5);
  }
  .hero .from{
    margin-top:18px;
    font-size: 20px;
    color: var(--rose-light);
    font-family:'Poppins', sans-serif;
  }
  .divider{
    width: 60px; height:2px;
    background: var(--gold);
    margin: 34px auto;
    position:relative;
  }
  .divider::before{
    content:"❁";
    position:absolute; top:50%; left:50%;
    transform: translate(-50%,-50%);
    background: var(--wine-deep);
    color: var(--gold);
    padding: 0 12px;
    font-size:16px;
  }

  /* ---------- Gallery / Polaroids ---------- */
  .gallery{
    display:flex;
    flex-wrap:wrap;
    justify-content:center;
    gap: 22px;
    margin: 20px 0 80px;
  }
  .polaroid{
    background: var(--cream);
    padding: 14px 14px 35px;
    box-shadow: 0 18px 40px rgba(0,0,0,0.45);
    width: 260px;
    border-radius: 3px;
    transition: transform .4s ease, box-shadow .4s ease;
  }
  .polaroid:nth-child(1){ transform: rotate(-5deg); }
  .polaroid:nth-child(2){ transform: rotate(3deg) translateY(12px); }
  .polaroid:nth-child(3){ transform: rotate(-3deg); }
  .polaroid:hover{ transform: rotate(0deg) scale(1.05) translateY(-6px); box-shadow: 0 26px 55px rgba(0,0,0,0.55); z-index:3; }
  .polaroid img{
    width:100%; display:block; border-radius:2px;
    aspect-ratio: 3/4; object-fit:cover;
  }
  .polaroid .cap{
    text-align:center;
    color: var(--wine);
    font-family:'Poppins', sans-serif;
    font-size: 12px;
    letter-spacing:.1em;
    margin-top: 12px;
  }

  /* ---------- Letter ---------- */
  .letter{
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(201,161,90,0.25);
    border-radius: 18px;
    padding: 46px 40px;
    position:relative;
  }
  .letter::before{
    content:"“";
    position:absolute; top:-6px; right: 28px;
    font-size: 100px;
    color: rgba(201,161,90,0.25);
    font-family: Georgia, serif;
  }
  .letter p{
    font-size: 21px;
    line-height:1.9;
    color: var(--cream);
    margin-bottom: 20px;
    direction: ltr;
    text-align: left;
    font-family: 'Cormorant Garamond', serif;
  }
  .signature{
    margin-top: 30px;
    text-align:right;
    font-family:'Poppins', sans-serif;
    color: var(--gold);
    font-size: 16px;
    letter-spacing:.1em;
  }

  footer{
    text-align:center;
    margin-top: 90px;
    font-family:'Poppins', sans-serif;
    font-size: 12px;
    letter-spacing:.25em;
    color: rgba(232,161,173,0.5);
    text-transform:uppercase;
  }

  @media (max-width:640px){
    .letter{ padding: 32px 22px; }
    .letter p{ font-size: 18px; }
    .polaroid{ width: 82vw; }
    .polaroid:nth-child(2){ transform: rotate(2deg); }
  }
</style>
</head>
<body>

<!-- Passcode Gate -->
<div id="gate">
  <div class="gate-card">
    <div class="gate-mark">From Seif</div>
    <div class="gate-title">Alaa</div>
    <div class="gate-sub">There's something for you here 🌹</div>
    <input type="password" id="pwd" placeholder="• • • •" inputmode="numeric" maxlength="6">
    <br>
    <button id="gate-btn">Open</button>
    <div id="gate-error">Not quite.. try again</div>
  </div>
</div>

<!-- Main Content -->
<div id="content">

  <header class="hero">
    <div class="eyebrow">My Pot Lid</div>
    <h1>Alaa</h1>
    <div class="from">from Seif, with all my heart</div>
  </header>

  <div class="divider"></div>

  <!-- Photo Gallery -->
  <section class="gallery">
    <div class="polaroid">
      <img src="photo1.jpg" alt="Alaa & Seif">
      <div class="cap">US 🌹</div>
    </div>
    <div class="polaroid">
      <img src="photo2.jpg" alt="Alaa & Seif">
      <div class="cap">FAVORITE MOMENTS</div>
    </div>
    <div class="polaroid">
      <img src="photo3.jpg" alt="Alaa & Seif">
      <div class="cap">TOGETHER</div>
    </div>
  </section>

  <!-- Letter Section -->
  <div class="letter">
    <p>My pot lid 😚</p>
    <p>Honestly, I can't find the words to describe how much I love you, and no words are ever enough to truly describe you. I love every single detail about you—your smile, your eyes, the way you talk, your personality, all of it. I love everything about you, Alaa.</p>
    <p>Every day that passes, I am more and more sure that you are the best choice I've ever made in my life. And I promise you, I will always be right by your side, the very first person standing with you in every step you take, through the bad before the good.</p>
    <div class="signature">— Seif</div>
  </div>

  <footer>
    Made with love for Alaa
  </footer>

</div>

<script>
  // Falling Petals
  function createPetal(){
    const petal = document.createElement('div');
    petal.className = 'petal';
    petal.innerHTML = '🌸';
    petal.style.left = Math.random() * 100 + 'vw';
    petal.style.animationDuration = (Math.random() * 3 + 4) + 's';
    petal.style.fontSize = (Math.random() * 10 + 12) + 'px';
    document.body.appendChild(petal);
    setTimeout(() => petal.remove(), 7000);
  }
  setInterval(createPetal, 400);

  // Password Logic
  const gateBtn = document.getElementById('gate-btn');
  const pwdInput = document.getElementById('pwd');
  const gate = document.getElementById('gate');
  const content = document.getElementById('content');
  const gateError = document.getElementById('gate-error');

  const CORRECT_PWD = "2829";

  function checkPassword(){
    if(pwdInput.value === CORRECT_PWD){
      gate.style.opacity = '0';
      gate.style.visibility = 'hidden';
      content.style.display = 'block';
    } else {
      gateError.classList.add('show');
      pwdInput.classList.add('shake');
      setTimeout(() => {
        pwdInput.classList.remove('shake');
      }, 500);
    }
  }

  gateBtn.addEventListener('click', checkPassword);
  pwdInput.addEventListener('keypress', function(e) {
    if (e.key === 'Enter') {
      checkPassword();
    }
  });
</script>

</body>
</html>
