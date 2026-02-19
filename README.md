<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MISSION-2 | Boss Console</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    background:#000;
    font-family:"Courier New", monospace;
    overflow:hidden;
}

/* Matrix Background */
canvas{
    position:fixed;
    top:0;
    left:0;
    z-index:-1;
}

/* Dark Overlay */
.overlay{
    position:absolute;
    top:0;
    left:0;
    width:100%;
    height:100%;
    background:rgba(0,0,0,0.92);
}

/* Main Terminal */
.terminal{
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    text-align:center;
    color:#ff0022;
    text-shadow:0 0 15px #ff0022;
}

/* Title */
.title{
    font-size:32px;
    letter-spacing:4px;
    margin-bottom:20px;
    animation:flicker 1.5s infinite alternate;
}

/* Subtext */
.sub{
    font-size:18px;
    letter-spacing:2px;
}

/* Flicker Effect */
@keyframes flicker{
    0%{opacity:1;}
    50%{opacity:0.8;}
    100%{opacity:1;}
}

/* Button */
a{
    display:inline-block;
    margin-top:40px;
    padding:14px 35px;
    border:2px solid #ff0022;
    color:#ff0022;
    text-decoration:none;
    letter-spacing:2px;
    transition:0.3s;
}

a:hover{
    background:#ff0022;
    color:#000;
    box-shadow:0 0 25px #ff0022;
}

/* Cursor */
.cursor{
    display:inline-block;
    width:10px;
    height:22px;
    background:#ff0022;
    margin-left:6px;
    animation:blink 1s infinite;
}

@keyframes blink{
    0%,50%,100%{opacity:1;}
    25%,75%{opacity:0;}
}
</style>
</head>

<body>

<canvas id="matrix"></canvas>
<div class="overlay"></div>

<div class="terminal">
<div class="title">MISSION-2</div>
<div class="sub" id="typing"></div>
<a href="https://afrinyouaremine.github.io/herewebegin/">
ENTER NEXT PHASE
</a>
</div>

<script>
// MATRIX GREEN BACKGROUND
const canvas = document.getElementById("matrix");
const ctx = canvas.getContext("2d");

canvas.height = window.innerHeight;
canvas.width = window.innerWidth;

const letters = "01MISSIONBOSSMAFIAHACKER";
const fontSize = 12;
const columns = canvas.width/fontSize;
const drops = [];

for(let x=0;x<columns;x++) drops[x]=1;

function draw(){
    ctx.fillStyle="rgba(0,0,0,0.12)";
    ctx.fillRect(0,0,canvas.width,canvas.height);

    ctx.fillStyle="rgba(0,255,0,0.6)";
    ctx.font=fontSize+"px monospace";

    for(let i=0;i<drops.length;i++){
        const text=letters[Math.floor(Math.random()*letters.length)];
        ctx.fillText(text,i*fontSize,drops[i]*fontSize);

        if(drops[i]*fontSize>canvas.height && Math.random()>0.975)
            drops[i]=0;

        drops[i]++;
    }
}
setInterval(draw,35);


// TYPEWRITER EFFECT
const text = "IMOTIONS DEPLOYING TO PRODUCTION...";
let i = 0;
const speed = 40;
const typing = document.getElementById("typing");

function type(){
    if(i < text.length){
        typing.innerHTML += text.charAt(i);
        i++;
        setTimeout(type, speed);
    } else {
        typing.innerHTML += "<span class='cursor'></span>";
    }
}

type();
</script>

</body>
</html>