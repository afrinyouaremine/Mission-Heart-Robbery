<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>THE REAL LOVE STORY</title>

<style>
body{
  margin:0;
  font-family:'Segoe UI', sans-serif;
  background:linear-gradient(135deg,#0f0c29,#302b63,#24243e);
  color:white;
  overflow-x:hidden;
}

/* Floating Acrylic Motion */
.blob{
  position:fixed;
  width:400px;
  height:400px;
  background:rgba(255,255,255,0.05);
  border-radius:50%;
  filter:blur(80px);
  animation:floatBlob 18s infinite alternate ease-in-out;
  z-index:-1;
}
.blob:nth-child(1){ top:-100px; left:-100px; background:rgba(0,255,255,0.15); }
.blob:nth-child(2){ bottom:-150px; right:-100px; background:rgba(255,0,150,0.15); animation-duration:22s; }

@keyframes floatBlob{
  0%{ transform:translate(0,0) scale(1); }
  50%{ transform:translate(60px,80px) scale(1.2); }
  100%{ transform:translate(-40px,60px) scale(1); }
}

/* Page Animation */
.page{
  display:none;
  min-height:100vh;
  padding:40px 20px;
  text-align:center;
  opacity:0;
  transform:translateY(40px) scale(0.98);
  transition:all 0.9s cubic-bezier(.23,1.01,.32,1);
}
.show{
  display:block;
  opacity:1;
  transform:translateY(0) scale(1);
}

/* Card */
.card{
  backdrop-filter: blur(30px);
  background: rgba(255,255,255,0.08);
  border-radius:25px;
  padding:35px;
  margin:auto;
  max-width:500px;
  box-shadow:0 8px 32px rgba(0,0,0,0.5);
  animation:cardPop 0.9s ease;
}
@keyframes cardPop{
  0%{ transform:scale(0.9); opacity:0; }
  100%{ transform:scale(1); opacity:1; }
}

.hero-title{
  font-size:26px;
  letter-spacing:3px;
  text-transform:uppercase;
  background:linear-gradient(90deg,#00f2fe,#ff00cc,#00f2fe);
  background-size:200% auto;
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:shimmer 5s linear infinite;
}
@keyframes shimmer{
  to{ background-position:200% center; }
}

h2,h3{
  background:linear-gradient(45deg,#00f2fe,#ff00cc);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

input{
  padding:14px;
  width:80%;
  border:none;
  border-radius:12px;
  margin-top:15px;
  background:rgba(255,255,255,0.1);
  color:white;
  outline:none;
  transition:0.4s;
}
input:focus{
  box-shadow:0 0 15px #ff00cc, 0 0 25px #00f2fe;
  transform:scale(1.03);
}

button{
  margin-top:12px;
  padding:12px 25px;
  border:none;
  border-radius:25px;
  background:linear-gradient(45deg,#00f2fe,#ff00cc);
  color:white;
  font-weight:bold;
  cursor:pointer;
  transition:0.3s;
}
button:hover{ transform:scale(1.07); }

.error{
  margin-top:10px;
  color:#ff4d6d;
  animation:shake 0.3s ease;
}
@keyframes shake{
  0%,100%{ transform:translateX(0); }
  25%{ transform:translateX(-5px); }
  75%{ transform:translateX(5px); }
}

.reveal-text{
  font-size:22px;
  margin-top:20px;
  opacity:0;
  transform:scale(0.8);
}
.glow{
  animation:glowReveal 2s ease forwards;
}
@keyframes glowReveal{
  0%{ opacity:0; transform:scale(0.8); text-shadow:0 0 0px #fff; }
  50%{ opacity:0.6; text-shadow:0 0 20px #ff00cc,0 0 40px #00f2fe; }
  100%{ opacity:1; transform:scale(1); text-shadow:0 0 25px #ff00cc,0 0 50px #00f2fe; }
}
</style>
</head>

<body>

<div class="blob"></div>
<div class="blob"></div>

<!-- PAGE 1 -->
<div id="page1" class="page show">
  <div class="card">
    <h1 class="hero-title">HERE WE BEGIN OUR LOVE STORY</h1>
    <p>
      Emotional Firewall Activated.<br><br>
      Only authorized hearts may proceed.<br><br>
      Think you qualify?<br>
      Tap below and let’s find out.
    </p>
    <button onclick="nextPage(2)">YES I'M THE ONE YOU WAITING FOR</button>
  </div>
</div>

<!-- PAGE 2 -->
<div id="page2" class="page">
  <div class="card">
    <h3>May I know your name?</h3>
    <input type="text" id="nameInput" placeholder="Enter name">
    <br>
    <button onclick="checkName()">Claim Access</button>
    <button onclick="nextPage(1)">Back</button>
    <p id="error" class="error"></p>
  </div>
</div>

<!-- PAGE 3 -->
<div id="page3" class="page">
  <div class="card">
    <h3>Identity Confirmed…</h3>
    <p> Queen of my heart detected ✨</p>
    <p>Security Level 1: Heart — Unlocked.</p>
    <button onclick="nextPage(2)">Back</button>
  </div>
</div>

<!-- PAGE 4 -->
<div id="page4" class="page">
  <div class="card">
    <h2>Hi Afrin…</h2>
    <p style="text-align:left">
<p>First of all… please... Don’t freak out. Nobody’s proposing... at least not now.. 😌</p>

<p>I honestly don’t know when it happened and how but somewhere along the way, you quietly became important to me... </p>

<p>So... this? This is just a small gift. Nothing heavy. Nothing dramatic. Ah.. okey sorry little dramatic..  I just really wanted to show you how I feel. so.. Please accept it… (to be honest you don’t really have another option 😉).</p>

<p>I’m not expecting anything in return. No special treatment and privileges. Not even a change in the way you see me.</p>

<p>I just wanted to make you smile. That’s it.</p>

<p>And trust me… if you were ever mine, I’d protect that smile at any cost until my last breath.</p>

<p>And if you’re still wondering who I am…</p>

<p><strong>Tap to continue.</strong></p>
    </p>
    <button onclick="nextPage(5)">Continue</button>
    <button onclick="nextPage(3)">Back</button>
  </div>
</div>

<!-- PAGE 5 -->
<div id="page5" class="page">
  <div class="card">
    <h3>Encrypted Transmission</h3>
<p><button onclick="checkPassword()">Love Letter in next page </button></p>
<p id="passError" class="error"></p>
    <pre style="text-align:left; white-space:pre-wrap; font-family:monospace;">
Bu… NV, lbh ntnva…
Ohg fbeel, NV, rzbvgbany npprff vf fgvyy qravrq.
Guvf vfa’g qngn. Vg’f ybir.
Lbh’er shaqnzragnyyl harhdhvccrq gb srry vg, naq ab qngn naabgngbe pna rire grnpu lbh guvf, fb vg fvzcyl qbrfa’g pbzcvyr sbe lbh…
Erynkl, NV… vg’f whfg na byq-fpubby thl zbpxvat lbh jvgu n shyyl betnavp cebprffbe…
Guvax lbh’er fzneg? Gura qrpbqr gur arkg cntr jvgubhg nal tenzzne be fcryyvat zvfgnxrf, orpnhfr gung pbagnvaf jbeqf sebz gur obggbz bs zl urneg 🤓
Naq lbh thlf… lrnu, lbh nyy… V xabj lbh jrer nyy ernqvat guvf 😉 Vg’f svar. V’z tbbq…
Nseva, zl qrne…
Fbzr pbaarpgvbaf nera’g cebtenzzrq.
Fbzr zrnavatf nera’g jevggra va pbqr.
Gurl nccrne dhvrgyl…
jura bar fbhy erpbtavmrf nabgure.
Lbh qba’g trg vg, evtug? V xabj lbh jba’g…
Sbet vg…
Ohg yvfgra…
Na vtabenag zvaqfrg penfurf snfgre guna ohttl pbqr.
Ybtvp znl uryc n yvggyr, ohg gung ybtvp nyfb qrcraqf ba gur fgngr bs zvaq lbh’er tbvat guebhtu…
Fb ybir naq cngvrapr ner jung gehryl jva gur svany ebhaq ❤️ Yrg’f frr…
Nseva…
Nytbevguzf znl pnyphyngr.
Znpurvarf znl cerqvpg.
Ohg…
GUR “LRX” BS ZL URNEG VF LBH…
Gur ybir yrggre vf sbe Nseva, fb lbh thlf cyrnfr qba’g gel gb ernq vg… lbh znl pel ol xabjvat zl fvgvngvba jvgu ure… V unir nyernql erzbirq gur pbzcyvpngrq onpxraq rapelcgvbaf ol gehfgvat lbh thlf… cyrnfr pbcrengr…

    </pre>
    
    <button onclick="nextPage(4)">Back</button>
    
  </div>
</div>

<!-- PAGE 7 -->
<div id="page7" class="page">
  <div class="card">
    <h2> Yeah.. this is the letter.. </h2>
    <p style="text-align:left">
<p> Afrin... By now, I’m sure you almost know it’s me.<br>
But I’m just hoping I still have some mystery left...
This is something i have never done before even in my college life...</p>

<p>Relax.<br> It may looks cringe.. but..
No dramatic background score here.<br>
No slow-motion walking scene. There are no pigeons flying in the background.<br>
Just me and my true lub.</p>

<p> I’m writing this because I respect you enough to be honest, and I respect myself enough not to beg. I don’t believe in dramatic confessions or emotional pressure; I believe in clarity. If one day you look at me differently, I’ll be there properly — not half-hearted, not confused, not temporary. And if that day never comes, I’ll still wish you happiness from a safe, slightly dramatic but very dignified distance. I don’t want special treatment, I don’t want VIP access, and I’m not here asking for promises. I just wanted you to know that someone sees you — really sees you. The emotional you, the strong you, the confusing you, the unpredictable you, even the “who the hell are you” version of you — and still says, “Yeah… I like her. No software update needed.” I don’t need a plan or a timeline; I value honesty more than hope built on assumptions. I’d rather adjust my heart to the truth than live inside a beautiful misunderstanding. If my presence ever feels safe to you, I’ll protect that space with intention. If it doesn’t, I’ll step back like a gentleman exiting a room — smooth, calm, no door slamming, no bitterness. But understand something clearly: if I came this far just to surprise you, just to see a genuine smile on your face, imagine how far I would go to protect it. I don’t move loudly; I move with intention. When I decide someone matters, I don’t do half measures. I don’t promise the world — I promise loyalty, and I don’t break what I claim. I don’t need to own you or cage you, but if I ever stand beside you, nothing reaches you without going through me first. No pressure. No drama. Just sincerity from someone who cares — and knows exactly what he’s doing.💖</p>
</div>
    </p>
    <button onclick="nextPage(8)">i love you...</button>
    <button onclick="nextPage(5)">Back</button>
  </div>
</div>

<!-- PAGE 8 -->
<div id="page8" class="page">
  <div class="card">
    <h3>This vault unlocks only when love is mutual.<br>Say I love you too</h3>
    <input type="text" id="loveMessage" placeholder="Type here...">
    <br>
    <button onclick="checkLoveMessage()">Submit</button>
    <button onclick="nextPage(7)">Back</button>
    <p id="loveError" class="error"></p>
  </div>
</div>

<!-- PAGE 9 -->
<div id="page9" class="page">
  <div class="card">
    <h2>Revealing something...</h2>
    <div id="hintText" class="reveal-text">
      Thanks for the Camara access..! I can see you now..!
    </div>
    <button onclick="nextPage(8)">Back</button>
  </div>
</div>

<script>
function nextPage(num){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('show'));
  setTimeout(()=>{
    document.getElementById('page'+num).classList.add('show');
    window.scrollTo({top:0, behavior:"smooth"});
  },300);
}

function checkName(){
  let name = document.getElementById("nameInput").value;
  if(name === "afrin" || name === "Afrin" || name === "AFRIN"){
    nextPage(3);
    setTimeout(()=>nextPage(4),2000);
  } else {
    document.getElementById("error").innerText =
      "YOU MAY BEAUTIFUL BUT NOT THE ONE I CHOOSE TO LOVE";
  }
}

function checkPassword(){
  let entered = prompt("Enter the password");
  if(entered === "nirfa"){
    nextPage(7);
  } else {
    document.getElementById("passError").innerText =
      "Plot twist..!! Decode the message first it contains the password hint";
  }
}

function checkLoveMessage(){
  let message = document.getElementById("loveMessage").value.trim().toLowerCase();
  if(message === "i love you too"){
    nextPage(9);
    setTimeout(()=>{
      document.getElementById("hintText").classList.add("glow");
    },800);
  } else {
    document.getElementById("loveError").innerText =
      "Ennood para I love you n..";
  }
}
</script>

</body>
</html>