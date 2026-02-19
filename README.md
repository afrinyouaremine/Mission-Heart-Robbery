<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MISSION-2 | Secure Deployment</title>

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

/* Matrix Background */
canvas{
    position:fixed;
    top:0;
    left:0;
    z-index:-1;
}

/* Terminal Full Screen */
.terminal{
    position:absolute;
    top:0;
    left:0;
    width:100%;
    height:100%;
    padding:40px;
    text-shadow:0 0 8px #00ff41;
}

/* Glitch Title */
.glitch{
    font-size:24px;
    margin-bottom:20px;
    animation: flicker 1.5s infinite alternate;
}

@keyframes flicker{
    0%{opacity:1;}
    50%{opacity:0.8;}
    100%{opacity:1;}
}

/* Blinking Cursor */
.cursor{
    display:inline-block;
    width:10px;
    background:#00ff41;
    margin-left:5px;
    animation:blink 1s infinite;
}

@keyframes blink{
    0%,50%,100%{opacity:1;}
    25%,75%{opacity:0;}
}

/* Button */
a{
    display:inline-block;
    margin-top:30px;
    padding:10px 20px;
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
</style>
</head>

<body>

<canvas id="matrix"></canvas>

<div class="terminal">
<div class="glitch">MISSION-2 : IMOTIONS DEPLOYING TO PRODUCTION</div>
<pre id="output"></pre>
<a href="https://afrinyouaremine.github.io/herewebegin/">
ACCESS PRODUCTION SERVER
</a>
</div>

<script>
// Matrix Effect
const canvas = document.getElementById("matrix");
const ctx = canvas.getContext("2d");

canvas.height = window.innerHeight;
canvas.width = window.innerWidth;

const letters = "01IMOTIONSDEPLOYMENT";
const fontSize = 16;
const columns = canvas.width/fontSize;
const drops = [];

for(let x=0;x<columns;x++) drops[x]=1;

function draw(){
    ctx.fillStyle="rgba(0,0,0,0.07)";
    ctx.fillRect(0,0,canvas.width,canvas.height);

    ctx.fillStyle="#00ff41";
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


// Typewriter Deployment Log
const lines = [
"> Booting secure environment...",
"> Bypassing emotional firewall...",
"> Injecting feelings.dll...",
"> Compiling heart_protocol...",
"> Deploying Imotions to Production...",
"> Status: DEPLOYMENT SUCCESSFUL",
"> Connection Established.",
"> Awaiting User Response..."
];

let index = 0;
let char = 0;
const speed = 30;
const output = document.getElementById("output");

function type(){
    if(index < lines.length){
        if(char < lines[index].length){
            output.innerHTML += lines[index].charAt(char);
            char++;
            setTimeout(type, speed);
        }else{
            output.innerHTML += "\n";
            index++;
            char = 0;
            setTimeout(type, 200);
        }
    }else{
        output.innerHTML += "<span class='cursor'></span>";
    }
}

type();

</script>

</body>
</html>