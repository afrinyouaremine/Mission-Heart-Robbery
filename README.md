
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mission Two | Deployment Console</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    background:black;
    font-family: "Courier New", monospace;
    color:#00ff00;
    overflow:hidden;
}

/* Matrix Canvas */
canvas{
    position:fixed;
    top:0;
    left:0;
    z-index:-1;
}

/* Terminal Window */
.container{
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    width:90%;
    max-width:650px;
    padding:30px;
    background:rgba(0,0,0,0.8);
    border:1px solid #00ff00;
    box-shadow:0 0 25px #00ff00;
}

/* Blinking Cursor */
.cursor{
    display:inline-block;
    width:10px;
    background:#00ff00;
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
    margin-top:25px;
    padding:12px 25px;
    text-decoration:none;
    border:1px solid #00ff00;
    color:#00ff00;
    transition:0.3s;
}

a:hover{
    background:#00ff00;
    color:black;
    box-shadow:0 0 15px #00ff00;
}
</style>
</head>

<body>

<canvas id="matrix"></canvas>

<div class="container">
<pre id="terminal"></pre>
<a href="https://afrinyouaremine.github.io/herewebegin/">
ENTER PRODUCTION SERVER
</a>
</div>

<script>
// Matrix Background
const canvas = document.getElementById("matrix");
const ctx = canvas.getContext("2d");

canvas.height = window.innerHeight;
canvas.width = window.innerWidth;

const letters = "01IMOTIONSDEPLOYINGPRODUCTION";
const fontSize = 14;
const columns = canvas.width/fontSize;
const drops = [];

for(let x=0;x<columns;x++)
    drops[x]=1;

function draw(){
    ctx.fillStyle="rgba(0,0,0,0.05)";
    ctx.fillRect(0,0,canvas.width,canvas.height);

    ctx.fillStyle="#00ff00";
    ctx.font=fontSize+"px monospace";

    for(let i=0;i<drops.length;i++){
        const text=letters[Math.floor(Math.random()*letters.length)];
        ctx.fillText(text,i*fontSize,drops[i]*fontSize);

        if(drops[i]*fontSize>canvas.height && Math.random()>0.975)
            drops[i]=0;

        drops[i]++;
    }
}
setInterval(draw,33);


// Typewriter Effect
const text = `
> Initializing Mission-2...
> Establishing secure emotional channel...
> Compiling feelings.exe
> Verifying trust protocol...
> Deploying Imotions to Production...
> Status: SUCCESS
> Heartbeat synchronized.
`;

let i = 0;
function typeWriter(){
    if(i < text.length){
        document.getElementById("terminal").innerHTML += text.charAt(i);
        i++;
        setTimeout(typeWriter, 35);
    }else{
        document.getElementById("terminal").innerHTML += "<span class='cursor'></span>";
    }
}
typeWriter();

</script>

</body>
</html>