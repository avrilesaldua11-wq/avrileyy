Save this as `index.html` in your GitHub repository, and put your song in the same folder as `kahit-maputi-na-ang-buhok-ko.mp3`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Happy First Monthsary 💚🩷</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    *{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif}
    body{background:linear-gradient(135deg,#d9f8df,#ffd9e8);overflow:hidden}
    .page{display:none;height:100vh;justify-content:center;align-items:center;padding:25px}
    .active{display:flex}
    .card{background:rgba(255,255,255,.9);backdrop-filter:blur(10px);padding:28px;border-radius:24px;max-width:720px;width:100%;text-align:center;box-shadow:0 15px 35px rgba(0,0,0,.15)}
    h1,h2{color:#4a7c59;margin-bottom:10px}
    p{color:#555;line-height:1.7;margin:10px 0}
    button{padding:12px 22px;border:none;border-radius:999px;margin:8px;cursor:pointer;font-weight:600;background:#7ed6a8;color:white;transition:.25s}
    .pink{background:#f7a8c2}.white{background:white;color:#5b7a67;border:2px solid #d8eedd}.big{font-size:38px}.calendar{display:grid;grid-template-columns:repeat(7,1fr);gap:8px;margin:20px 0}.calendar div{padding:10px;border-radius:12px;background:#fff}.head{background:none;font-weight:700;color:#4a7c59}.circle{background:#ff7da9!important;color:#fff;font-weight:700}.envelope{width:260px;height:170px;margin:20px auto;position:relative;cursor:pointer}.base{position:absolute;bottom:0;width:100%;height:120px;background:#f8b5c9;border-radius:0 0 12px 12px}.flap{position:absolute;width:100%;height:100px;background:#f39ab7;clip-path:polygon(0 0,50% 100%,100% 0);transform-origin:top;transition:.8s}.letter{position:absolute;left:5%;top:90px;width:90%;height:60px;background:white;border-radius:10px;padding:12px;overflow:hidden;transition:.8s;text-align:left}.open .flap{transform:rotateX(180deg)}.open .letter{top:-170px;height:300px;overflow:auto}audio{width:100%;margin:12px 0}small{color:#888}  </style>
</head>
<body>
  <section class="page active"><div class="card"><h1>💌 You got a mail!</h1><p>before opening it, play our song first ♡</p><audio controls><source src="kahit-maputi-na-ang-buhok-ko.mp3" type="audio/mpeg"></audio><small>Put your MP3 file in the same folder.</small><br><button onclick="nextPage()">Accept</button><button class="pink">Not yet</button></div></section>
  <section class="page"><div class="card"><h2>are you available on saturday?</h2><button onclick="yesDate()">yes 🤍</button><button class="pink" id="noBtn">no</button><p id="answer"></p></div></section>
  <section class="page"><div class="card"><h2>📅 September 2026</h2><div class="calendar"><div class="head">S</div><div class="head">M</div><div class="head">T</div><div class="head">W</div><div class="head">T</div><div class="head">F</div><div class="head">S</div><div></div><div>1</div><div>2</div><div>3</div><div>4</div><div>5</div><div>6</div><div>7</div><div>8</div><div>9</div><div>10</div><div>11</div><div>12</div><div>13</div><div>14</div><div>15</div><div>16</div><div>17</div><div>18</div><div>19</div><div>20</div><div>21</div><div>22</div><div class="circle">23</div><div>24</div><div>25</div><div>26</div><div>27</div><div>28</div><div>29</div><div>30</div></div><p>i know we can't celebrate on our exact monthsary, so i thought we'd move it to Saturday instead.</p><p>📍 <b>Agoo, La Union</b><br>🕗 <b>8:00 AM</b></p><p>so we can arrive early and enjoy the whole day together. and if you're not ready by 8am, that's okay too—i'll wait for you, baby.</p><button onclick="nextPage()">continue 💌</button></div></section>
  <section class="page"><div class="card"><h2>tap the envelope 💗</h2><div class="envelope" id="env" onclick="openLetter()"><div class="flap"></div><div class="base"></div><div class="letter"><h3>hello baby,</h3><p>happy first monthsary!! 🤍</p><p>first of all, i love you so much, and i hope you never forget that. i'm still in disbelief that i get to call you my girlfriend, and i can't wait for the day i get to call you my wifey.</p><p>we've already been through so many ups and downs, and my favorite thing about us is that at the end of every day, we still choose each other.</p><p>baby ko, i hope it's always us against the problem.</p><p>thank you for your patience, your soft heart, your reassurance, and for staying.</p><p>i promise to keep growing with you, to love you louder through my actions, communicate better, and become someone who gives you peace, not pressure.</p><p>here's to our first monthsary and to many more memories together.</p><p><b>i love you endlessly, baby.</b></p><p>— your avriley 💚</p></div></div><button onclick="nextPage()">next 🌷</button></div></section>
  <section class="page"><div class="card"><h1 class="big">Happy First Monthsary, My Baby! 🌷</h1><p>that's it, from your avrile 🤍</p><button class="white">So… it's a date? 💌</button><button>yes! it's a date</button><button class="pink">all yours baby</button></div></section>
<script>
let current=0;
const pages=document.querySelectorAll('.page');
function nextPage(){pages[current].classList.remove('active');current++;if(current<pages.length)pages[current].classList.add('active');}
function yesDate(){document.getElementById('answer').innerHTML="i'll take your whole day with me. 🤍";setTimeout(nextPage,1200)}
const no=document.getElementById('noBtn');
function move(){const x=Math.random()*220-110;const y=Math.random()*120-60;no.style.transform=`translate(${x}px,${y}px)`}
no.addEventListener('mouseover',move);no.addEventListener('click',move);
function openLetter(){document.getElementById('env').classList.toggle('open')}
</script>
</body>
</html>
```

### GitHub folder

first-monthsary/

`index.html`

`kahit-maputi-na-ang-buhok-ko.mp3`

Enable GitHub Pages and your monthsary website will be live.
