
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Wesal 🌹</title>
<style>
* { box-sizing: border-box; }
body {
  margin: 0;
  min-height: 100vh;
  overflow: hidden;
  font-family: Tahoma, Arial, sans-serif;
  background: linear-gradient(135deg,#fff0f5,#ffe0eb,#fff7fa);
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: #8d2148;
}
main { padding: 24px; z-index: 2; }
h1 { font-size: 2rem; }
p { font-size: 1.15rem; line-height: 1.9; }
button {
  border: 0;
  border-radius: 30px;
  padding: 15px 25px;
  font-size: 1.1rem;
  color: white;
  background: #e64b7a;
  cursor: pointer;
  box-shadow: 0 5px 15px #e64b7a55;
}
.rose {
  position: fixed;
  bottom: -60px;
  animation: floatUp linear forwards;
  pointer-events: none;
  z-index: 1;
}
@keyframes floatUp {
  from { transform: translateY(0) rotate(0deg); opacity: 1; }
  to { transform: translateY(-115vh) rotate(360deg); opacity: 0; }
}
#message { display:none; }
</style>
</head>
<body>
<main>
  <div style="font-size:75px">🌹</div>
  <h1>يا وصال، عندي ليكي حاجة 😂❤️</h1>
  <p>مش مشروع تخرج ولا مسألة خرسانة مسلحة...<br>
  اضغطي وشوفي بنفسك 👀</p>
  <button onclick="showRoses()">افتحي المفاجأة 🌷</button>
  <div id="message">
    <h1>كفايا ورد بقى 😂🌹</h1>
    <p>بس إنتِ تستاهلي الورد كله 💐<br>
    يومك يبقى جميل زيك، وبس كده متكبريش الموضوع 😂</p>
    <div style="font-size:42px">🌹🌷🌹🌷🌹</div>
  </div>
</main>
<script>
function showRoses() {
  document.getElementById('message').style.display = 'block';
  document.querySelector('main > p').style.display = 'none';
  document.querySelector('main > button').style.display = 'none';
  document.querySelector('main > div:first-child').style.display = 'none';

  for (let i = 0; i < 90; i++) {
    setTimeout(() => {
      const rose = document.createElement('div');
      rose.className = 'rose';
      rose.textContent = ['🌹','🌷','💐','🌸','❤️'][Math.floor(Math.random()*5)];
      rose.style.left = Math.random()*100 + 'vw';
      rose.style.fontSize = (20+Math.random()*28) + 'px';
      rose.style.animationDuration = (3+Math.random()*5) + 's';
      document.body.appendChild(rose);
      setTimeout(() => rose.remove(), 8500);
    }, i*55);
  }
}
</script>
</body>
</html>
