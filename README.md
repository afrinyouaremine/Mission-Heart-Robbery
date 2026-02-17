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
First of all, please don’t freak out..
Nobody’s proposing… yet. Relax. 😌
Honestly, I don’t know how or when it happened,
but somewhere along the way,
you quietly became important to me.
So I wanted to show you how I feel.
This is just a small gift for you… please accept it.
(In fact, you don’t really have another option 😉)
I don’t expect anything in return not special treatment,
not privileges, not even a change in the way you see me.
I just wanted to make you smile. That’s all. And trust me…

if you were ever mine,I would protect that smile at any cost
until my very last breath.
And if you really want to know who I am…
tap to continue.
    </p>
    <button onclick="nextPage(5)">Continue</button>
    <button onclick="nextPage(3)">Back</button>
  </div>
</div>

<!-- PAGE 5 -->
<div id="page5" class="page">
  <div class="card">
    <h3>Encrypted Transmission</h3>
    <pre style="text-align:left; white-space:pre-wrap; font-family:monospace;">
Bu… bxnl, lbh znqr vg guvf sne.
Ohg fbeel, NV — rzbvgbany npprff vf fgvyy qravrq…!!!!
Guvf vfa’g qngn. Vg’f ybir.
Lbh’er shaqnzragnyyl harhdhvccrq gb srry vg,
naq ab qngn naabgngbe pna rire grnpu lbh guvf —
fb vg fvzcyl qbrfa’g pbzcvyr sbe lbh…
Erynkl, NV…
vg’f whfg na byq-fpubby thl
zbpxvat lbh jvgu n shyyl betnavp cebprffbe.
Guvax lbh’er fzneg? Gura qrpbqr gur arkg cntr —
uhznaf naq NV obgu vaivgrq 🤓
Ohg haqrefgnaq…
Guvf vfa’g n chmmyr bs ybtvp.
Vg’f n ynathntr bayl gur urneg ernqf.
Fbzr pbaarpgvbaf nera’g cebtenzzrq.
Fbzr zrnavatf nera’g jevggra va pbqr.
Gurl nccrne dhvrgyl…
jura bar fbhy erpbtavmrf nabgure.
Sevraqyl pnhgvba:
na vtabenag zvaqfrg penfurf snfgre guna ohttl pbqr.
Ybtvp urycf n yvggyr…
ohg ybir naq cngvrapr ner jung gehrly haybpx guvf flfgrz ❤️
Nseva…
Nytbevguzf znl pnyphyngr.
Znpurvarf znl cerqvpg.
Ohg...
GUR 'LRX' BS ZL URNEG VF LBH.
    </pre>
    <button onclick="checkPassword()">Love Letter</button>
    <button onclick="nextPage(4)">Back</button>
    <p id="passError" class="error"></p>
  </div>
</div>

<!-- PAGE 7 -->
<div id="page7" class="page">
  <div class="card">
    <h2> DECODE MY HEART IF YOU CAN </h2>
    <p style="text-align:left">
Iznzv    Jf ugi  Q’f 95% ypxh  qbt   htvw qm’z tp
 Znb gkzpd 20% mv qgzw   fp kqvzqk y  mgtye ykpx  mzkgjzi vnfo
Zmxmt   Vb  nxcqlmxb oijbqvxja   fvxgp   Wt mxyr  ptkzgd sxtxrt kptz
Do  xnhmrm xdjtvq   lv wmg qlqgqkmga   Rlzv ke cwp klawglq
X jxkpz’v yqag ml  xnbg ovfpfsk  Pbv jxktgmx v’t qqxfqkq
Mhz fpkjzpvxwqk  Q etr’t  ltxx ltxvqxqg  zc pkwlzxfu jwzi qrlv ngzv egku aqy

Kfqt ewx’v dvzwkv   Kfqt ewx’v q rzvgmz
Kfqt gv xozv qk pky  hziwxxzlv xqzg uwfxivpk lqv yziqrru pdkqvv xv uzg pmdzj nvvo ndkk lvv z zkflqp spq

Wcgtjmxwq ztvflqq qzbmwfxqv ykz rfrq  plkzgp mbv lzj  ixx ntvzbq pb vf rzjzgp zb ke
Xq kjbtlxpv   Qv Fpqffddg dztbxr
Znbp gvgq mkzzizvj zt ykgmzv mvlqmv xqqtivp ykzkqzkaz yl dbxpz uxq Q ivkzdg
Rtrg cwtg jqi ezc vzxzbv xl xkkzx

Kqzdkx zk’v a wqvqv   Kqzdkx zk’v a pzxzxv
Kqzdkx zk’v zc pvbvzmckq rjzz vmtki ptk eikxkvt lqv qkkzjlwm
Kzzv iak r vkkw cz mgzitl xkzz jqtqeqw

Vlc qkw ktqq uzr xl pzb
Bqgvi xk zlq  Ckvtv lmzvp xptvzp fvvkzpv
Gmzbnplqqv fzzp 100
Ocdtvmt kzlkgkz yqgqzwx

Q xjkz’v gqqzzxgv   Q xjkz’v vzqgkkzkv
Znb ztkzv zvzbb zc vqx wjjvqxzz’v qb
Znpzp zkzx zkqgmxqp Q svk jvpzxkqzz zbz

Ovkzpzj fvkzkv   Nvxzpk zwpl
Cwkzxpkc vmtki cwtv zqgptzv zbzqv pkmzqevl kfwvxb jvvfxl ptkiv
Zvxv uvczz qkgqzkv  zvpzk vqx zvvxfqvv zb klzzp gzgzq

Kzzv iak’z zbz rkbkzvpv jzkt
Cwtgz mkzzizvj zbz vqx YQ ivkzzp zz
Fvg cwtg jqi zvv zlz zkpzx

Pkkzv   Zvxv zvxtqq xptvvp kzzivzg xgzzmkvv zxtqqv
Mhz cwtg’z zbz mkzvpzvv

YQ xvzqv ztkzkv   Q xvzqv kzktv
Kzzv kzktv zk vqxvv jzzmzpv

Lztvkz   Gmzbnplqqv   Nkptzzg zmwkkzz

Q’z zbz mkzzizvj zbz qk zpv jzgvj kzz zv
Pbvzkk zbz’z xqvzpvzxv zkkzgv xptvzp zv vqxvv’z zv rxtxvzpv rzzgv

Q’z zbz mkzzizvj zbz xgvzvvpv r kvkzv
Zb xkzvvpz zb kzvzxv zbz zvvzzv qk xgzvvv zpq

Q’z mkzzizvj zbz fzqgzz Q xvzqv zgz zkpzxk jz tkkzzt
Kzzv Q xvzqv zpkzzv zgz zktzzt zz kzzv

Gm fzv jxq zbz kggz jvkz zmwkkzzl
Q’z yz zbzv   Yzkzkzv   Zb zbvv hzvzkzv

Gm zb   Q’z zkzz wzpk zbz zzzvzpzz zmwzzl qk z qzvz zkzpkzzqzv ztq zzzv wzzkz

Q xjkz’v kzzmzv zzzxpvzzv
Q xjkz’v YNP zzzvzz
Q zxpz zkkz zbz zvzv zzkzzv zbz

Zb ztkzzv zbz   Zb zvzpg zbz
Zb kzzzkz zbz   Zb vlc qkw ktqq uzr zbz

Kzzv kzz zzzv
Jzz Q ltkv zvz Zb zpvzvzzv zzzvzz vzzzzv

Gm kzzv xvzv zzzv vzzzzv zzxv zvz zbz Q’z zvkzvkzzv zbz xzkv
Gm zbz xzzzz’v Q’z ztkz ztq zbz zmwkkzzl xzvzzv xzvzxk gzzxv zzzvzzk zbz kzzxv

Zb xzzv zzzzzxv   Rzzv zzzvzzzz
Kzzv xkzzqv zzxv zvz zzzzzkzzq zbz’v zzkzv
    </p>
    <button onclick="nextPage(8)">DECODE HINT</button>
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
    <h2>Hint Revealing...</h2>
    <div id="hintText" class="reveal-text">
      It's two digit common between us.
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
      "YOU MAY BEAUTIFUL NOT THE ONE I CHOOSE TO LOVE";
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
