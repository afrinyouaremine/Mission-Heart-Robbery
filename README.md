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
First of all — don’t freak out.
Nobody’s proposing… yet. Relax. 😌
I don’t know how or when it happened,
but somewhere along the way,
you quietly became important to me.
So this is just a small gift. It’s yours now.
I don’t expect anything in return 
not even special treatment or any kind of privilege from you.
I just wanted to see you smile. That’s all.
And trust me… if you were ever mine,
I’d protect that smile at any cost 
until my last breath.
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
Afrin..

Krbl r jcfn siverk. Kyzj zj e kirdrktz gifgfjzex jtvez. Wvsilrip 14ky yrj rcivrjjvu — reu pvk, nyrc Z wvvc yrje’k. Slk kyviv’j ef givjjliv yviv, ef jgfkczxyk, ef vogvtkkrkzfej rkkrt yvu kf kyvjv nfiu j. Z aljk uzue’k nrek refkyvi urp kf grjj nzkyflk svzex yfevjk, vmve zw zk’j wifd r uzjkre tv.
Kyzj zj aljk r jdrcc, jzetviv df dvek.
Jfdvnyviv svknvve fiuzerip urpj reu ireufd tfemvijrkzfej, svknvve jzdgcv jdzcvj reu lefkztvu c kkc v uvkrzcj, pfl hlzv k cp svtrdv zdgfikrek kf dv. Z ufe’k votrkcp nye zk yrggvevu. Kyviv nej’k r jgv tzwzt urkv fi r xireu kliezex gfzek. Zk aljk xivn — jfwkcp, xvekcp, nzkyflk rjbzex wfi rkkvekzfe.
Drpsv zk’j pfl i jdzcv — kyv bz e u ky rk czexvij ze jfdvfev’j dzeu cfexvi ky re zk jyflcu. Drpsv zk’j pfl i trcd ve vixp, kyv nrp pfl drbv kyzexj wvvc czxykvi nzkyflk vmve kipzex. Fi drpsv zk’j jzdgcp kyv nrp pfl vo zj k jf vwwfikc vjjcp, nzkyflk ivrczqzex yfn jgvtzrc ky rk zj. Pfl gif srs cp ufe’k jvv kyv vwwvt k pfl yrmv… slk pfl uf. Reu zk’j ivrc.
Zw pfl vmvi yrggve kf xl vjj nyf Z rd, gcv rjv b vvg zk hlzv k cp ze pfl i yvrik. Z’d efk ivrup kf j kvg wfinri u, reu Z ufe’k nrek re pk yzex kf wvvc rnbnri u fi uzwwviv ek. Z ufe’k nrek jgvtzrc kivr kdvek fi rep giz mzcvxv. Kyzj xzwk zj e’k r tcrzd fe pfl — zk’j aljk r xv ekcv xvjk liv, jfdvkyzex jdrcc dvrek kf s izex r jdzcv kf pfl i wr tv.
Reu gcv rjv… ufe’k jluuve cp trcc dv zw pfl wzxliv zk flk. Z d vre zk. Zw Z jvv pfl i er dv czxykzex lg dp gyfev levogvt kv ucp, dp yvrik dzxyk xvelze v cp cfjv tfekifc wfi r wvn jvtfeuj. Z’cc jkriv rk kyv jti vve, grezt, fmvikyzeb vmvip gfjjzs c v flktf dv, reu wfixvk yfn kf sivrkyp gif gvicp. Jf cvk dv jkrp r czkkcv dpjkvi zflj wfi efn. Cvk dv gifkvt k kyzj wirxzc v tflirxv.
Z ufe’k vogvtk re pk yzex wifd pfl. Efk r ivrtkzfe. Efk r ivgcp. Efk vmve r tyrexv ze yfn pfl cffb rk kfd fii fn.
Z aljk nrekvu pfl kf befn kyrk jfdvnyviv, hlzv k cp reu jzetviv cp, jfdvfev rudz ivj pfl. Jfdvfev mrc lvj pfl i jdzcv dfiv ky re pfl ivrczqv. Jfdvfev wzeuj yrg gzevjj jzdgcp ze kyv kyflxyk fw pfl svzex yrg gp.
Zw kyzj xzwk — fi kyzj cvkkvi — s izexj vmve kyv jfwk vjk jdzcv kf pfl i wr tv, kyve Z’m rc ivrup jlt tvvuvu. Kyrk rcf ev zj ve flxy wfi dv.
Reu jzcvekcp, nzkyflk evvuzex ivtfxezkzfe fi r gcrtv ze pfl i cz wv, Z gifdzjv jfdvkyzex jzdgcv: rj cfex rj Z vo zj k jfdvnyviv ze pfl i nf i cu — vmve wifd r uzjkre tv — Z nzcc rcnr pj nzjy wfi pfl i yrg gzevjj. Z nzcc rcnr pj yfgv pfl i jdzcv jkrpj votrkcp kyv nrp zk zj… n rid, vwwfikc vjj, reu ivrc.
Efk cflucp.
Efk gfjjvjjz m vcp.
Aljk jzetviv cp… reu r czkkcv dfiv uvvg cp ky re Z gif srs cp jyflcu.
— Jfdvfev nyf tri vj dfiv ky re yv’cc vmvi rudz k zk 🤍
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
