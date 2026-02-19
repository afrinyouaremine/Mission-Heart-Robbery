<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MISSION-2 | Deployment Console</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    background:#000;
    font-family:"Courier New", monospace;
    color:#00ff41;
    overflow:hidden;
}

/* Matrix Background */
canvas{
    position:fixed;
    top:0;
    left:0;
    z-index:-1;
}

/* Terminal Overlay */
.terminal{
    position:absolute;
    top:0;
    left:0;
    width:100%;
    height:100%;
    padding:40px;
    background:rgba(0,0,0,0.85);
}

/* Title */
.title{
    font-size:24px;
    letter-spacing:2px;
    margin-bottom:30px;
    text-shadow:0 0 12px #00ff41;
}

/* Button */
a{
    display:inline-block;
    margin-top:40px;
    padding:12px 28px;
    border:1px solid #00ff41;
    color:#00ff41;
    text-decoration:none;
    transition:0.3s;
}

a:hover{
    background:#00ff41;
    color:#000;
    box-shadow:0 0 20px #00ff41;
}

/* Cursor */
.cursor{
    display:inline-block;
    width:8px;
    height:20px;
    background:#00ff41;
    margin-left:5px;
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

<div class="terminal">
<pre id="output"></pre>

<a href="https://afrinyouaremine.github.io/herewebegin/">
PROCEED TO NEXT PHASE
</a>
</div>

<script>
// Matrix Background
const canvas = document.getElementById("matrix");
const ctx = canvas.getContext("2d");

canvas.height = window.innerHeight;
canvas.width = window.innerWidth;

const letters = "01MISSIONPRODUCTION";
const fontSize = 14;
const columns = canvas.width/fontSize;
const drops = [];

for(let x=0;x<columns;x++) drops[x]=1;

function draw(){
    ctx.fillStyle="rgba(0,0,0,0.15)";
    ctx.fillRect(0,0,canvas.width,canvas.height);

    ctx.fillStyle="rgba(0,255,65,0.4)";
    ctx.font=fontSize+"px monospace";

    for(let i=0;i<drops.length;i++){
        const text=letters[Math.floor(Math.random()*letters.length)];
        ctx.fillText(text,i*fontSize,drops[i]*fontSize);

        if(drops[i]*fontSize>canvas.height && Math.random()>0.975)
            drops[i]=0;

        drops[i]++;
    }
}
setInterval(draw,40);


// Typewriter Effect (Mission Only)
const text = "MISSION-2\nIMOTIONS DEPLOYING TO PRODUCTION...\n\nSTATUS: ACTIVE";

let i = 0;
const speed = 35;
const output = document.getElementById("output");

function typeWriter(){
    if(i < text.length){
        output.innerHTML += text.charAt(i);
        i++;
        setTimeout(typeWriter, speed);
    } else {
        output.innerHTML += "<span class='cursor'></span>";
    }
}

typeWriter();

</script>

</body>
</html>