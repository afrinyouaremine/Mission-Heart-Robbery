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
    font-family: "Courier New", monospace;
    color:#00ff41;
    overflow:hidden;
}

/* Matrix background */
canvas{
    position:fixed;
    top:0;
    left:0;
    z-index:-1;
}

/* Dark readable overlay */
.terminal{
    position:absolute;
    top:0;
    left:0;
    width:100%;
    height:100%;
    padding:40px;
    background:rgba(0,0,0,0.85); /* makes text clearly visible */
    overflow:auto;
}

/* Title */
.title{
    font-size:22px;
    margin-bottom:25px;
    letter-spacing:2px;
    color:#00ff41;
    text-shadow:0 0 10px #00ff41;
}

/* Button */
a{
    display:inline-block;
    margin-top:30px;
    padding:12px 25px;
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
    height:18px;
    background:#00ff41;
    animation:blink 1s infinite;
    margin-left:5px;
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
<div class="title">MISSION-2 : IMOTIONS DEPLOYING TO PRODUCTION</div>
<pre id="output"></pre>

<a href="https://afrinyouaremine.github.io/herewebegin/">
PROCEED TO NEXT PHASE
</a>
</div>

<script>
// MATRIX EFFECT (dimmed for readability)
const canvas = document.getElementById("matrix");
const ctx = canvas.getContext("2d");

canvas.height = window.innerHeight;
canvas.width = window.innerWidth;

const letters = "01IMOTIONSPRODUCTION";
const fontSize = 14;
const columns = canvas.width/fontSize;
const drops = [];

for(let x=0;x<columns;x++) drops[x]=1;

function draw(){
    ctx.fillStyle="rgba(0,0,0,0.15)";  // darker fade for better readability
    ctx.fillRect(0,0,canvas.width,canvas.height);

    ctx.fillStyle="rgba(0,255,65,0.4)";  // dimmed matrix text
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


// TYPEWRITER DEPLOYMENT LOG (clean & professional)
const lines = [
"> Initializing Mission-2...",
"> Establishing secure production channel...",
"> Verifying system integrity...",
"> Compiling modules...",
"> Deploying Imotions package...",
"> Syncing runtime environment...",
"> Deployment Status: SUCCESS",
"> Ready for Phase-3 execution."
];

let index = 0;
let char = 0;
const output = document.getElementById("output");

function type(){
    if(index < lines.length){
        if(char < lines[index].length){
            output.innerHTML += lines[index].charAt(char);
            char++;
            setTimeout(type, 25);
        } else {
            output.innerHTML += "\n";
            index++;
            char = 0;
            setTimeout(type, 150);
        }
    } else {
        output.innerHTML += "<span class='cursor'></span>";
    }
}

type();
</script>

</body>
</html>