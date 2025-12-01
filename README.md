<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Laraib</title>
<style>
html, body {
  margin: 0;
  padding: 0;
  height: 100%;
  font-family: 'Arial', sans-serif;
  overflow: hidden;
  background: #f0e6f7;
}
.section {
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: #333;
  padding: 20px;
  position: absolute;
  top: 0;
  left: 0;
  opacity: 0;
  transition: opacity 1s, transform 1s;
  font-size: 24px;
}
.active {
  opacity: 1;
  transform: translateY(0);
  z-index: 2;
}
.hidden {
  transform: translateY(50px);
}
.btn-next {
  margin-top: 40px;
  padding: 14px 28px;
  border: none;
  border-radius: 8px;
  background: #8b2eff;
  color: #fff;
  font-size: 18px;
  cursor: pointer;
}
#sec1 { background: url('https://i.ibb.co/3R1R0H9/birthday1.jpg') no-repeat center/cover; color: #fff; font-size: 36px; }
#sec2 { background: url('https://i.ibb.co/D7N7K3t/birthday2.jpg') no-repeat center/cover; color: #fff; }
#sec3 { background: url('https://i.ibb.co/2n64m4K/birthday3.jpg') no-repeat center/cover; color: #fff; }
#sec4 { background: url('https://i.ibb.co/f09RYrR/birthday4.jpg') no-repeat center/cover; color: #fff; }
#sec5 { background: url('https://i.ibb.co/T8fQz3H/birthday5.jpg') no-repeat center/cover; color: #fff; }
#sec6 { background: url('https://i.ibb.co/4jJH4pR/birthday6.jpg') no-repeat center/cover; color: #fff; }
#cat {
  position: fixed;
  bottom: 20px;
  right: -150px;
  width: 120px;
  transition: right 2s;
}
</style>
</head>
<body>

<div id="sec1" class="section active">
  <h1>Happy Birthday Laraib</h1>
  <button class="btn-next" onclick="nextSection()">Next</button>
</div>

<div id="sec2" class="section hidden">
  <h2>Aap Jaisi Khoobsurat Insaan</h2>
  <p>Aap jaisi achi, pyari, seedhi aur sachi insaan ko hamesha duniya ki sab se behtareen cheezein milni chahiye. Aapka ikhlaq, lehja aur soch aap ko sab se alag banati hain.</p>
  <button class="btn-next" onclick="nextSection()">Next</button>
</div>

<div id="sec3" class="section hidden">
  <h2>Yaadein Jo Reh Gayi</h2>
  <p>Mujhe abhi tak woh din yaad hai jab hum shed se wapis aa rahe thay aur barish ho rahi thi. Mere mana karne ke bawajood aap ne paani me jump kiya tha.</p>
  <p>Aur phir aap ke haath ka banaya hua pulao aur custard — abhi tak uski khushboo yaad aati hai.</p>
  <button class="btn-next" onclick="nextSection()">Next</button>
</div>

<div id="sec4" class="section hidden">
  <h2>Aap Ki Aankhein</h2>
  <p>Aap ki aankhein… woh gehra kaala rang jo sirf khoobsurat nahi balkay expressive bhi hai.</p>
  <button class="btn-next" onclick="nextSection()">Next</button>
</div>

<div id="sec5" class="section hidden">
  <h2>Duaen & Motivation</h2>
  <p>Allah aap ke tamam goals aasaan kare. Aap jahan bhi jaayein, izzat aur ache log milain. Aapka dil hamesha halka aur khush rahe.</p>
  <p>Laraib… aap intelligent aur sincere hain. <strong>“Jahan niyat saaf hoti hai, wahan raasta ban hi jaata hai.”</strong></p>
  <p><strong>“Aap kamzor nahi — bas nazuk dil ki hain. Aur nazuk dil wale hi asli strong hote hain.”</strong></p>
  <button class="btn-next" onclick="nextSection()">Next</button>
</div>

<div id="sec6" class="section hidden">
  <h2>End Note</h2>
  <p>Happy Birthday once again, Laraib! Allah kare yeh saal aap ki zindagi ka sab se behtareen saal ho. Aap hamesha muskurayein, chamkain aur khush rahein.</p>
  <audio id="birthdayMusic" src="https://www.bensound.com/bensound-music/bensound-happyrock.mp3"></audio>
  <img id="cat" src="https://i.ibb.co/3Y6Mbc7/cat.png" alt="cute cat">
</div>

<script>
let current = 1;
function nextSection() {
  document.getElementById('sec' + current).classList.remove('active');
  document.getElementById('sec' + current).classList.add('hidden');
  current++;
  if(current <= 6){
    document.getElementById('sec' + current).classList.add('active');
    document.getElementById('sec' + current).classList.remove('hidden');
    if(current === 6){
      // play music and animate cat
      document.getElementById('birthdayMusic').play();
      document.getElementById('cat').style.right = '20px';
    }
  }
}
</script>

</body>
</html>
