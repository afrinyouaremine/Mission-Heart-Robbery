<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mission Two | Deployment Console</title>

<style>
:root{
    --primary:#ff0033;
    --accent:#00e6ff;
}

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background: radial-gradient(circle at top, #1a0005, #000000 70%);
    font-family: 'Segoe UI', sans-serif;
    color:white;
    padding:20px;
}

/* Main Card */
.container{
    width:100%;
    max-width:420px;
    padding:35px 25px;
    border-radius:18px;
    background: rgba(255,255,255,0.05);
    backdrop-filter: blur(18px);
    border:1px solid rgba(255,255,255,0.08);
    box-shadow:0 0 30px rgba(255,0,51,0.25);
    text-align:center;
    animation: fadeIn 1.2s ease forwards;
}

/* Heading */
h1{
    font-size:1.6rem;
    line-height:1.4;
    letter-spacing:1.5px;
    margin-bottom:12px;
    background: linear-gradient(90deg, #ff0033, #00e6ff);
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
}

/* Subtext */
p{
    font-size:0.95rem;
    color:#cccccc;
    margin-bottom:28px;
    line-height:1.6;
}

/* Button */
a{
    display:block;
    width:100%;
    padding:15px;
    border-radius:40px;
    text-decoration:none;
    font-weight:600;
    letter-spacing:1px;
    background: linear-gradient(90deg, #ff0033, #cc0000);
    color:white;
    transition:0.3s ease;
    box-shadow:0 0 18px rgba(255,0,51,0.6);
}

a:active{
    transform:scale(0.97);
}

a:hover{
    box-shadow:0 0 28px rgba(0,230,255,0.9);
    background: linear-gradient(90deg, #00e6ff, #0099cc);
}

/* Smooth Fade */
@keyframes fadeIn{
    from{opacity:0; transform:translateY(25px);}
    to{opacity:1; transform:translateY(0);}
}

/* Larger screens */
@media (min-width:768px){
    h1{ font-size:2rem; }
    p{ font-size:1rem; }
}
</style>
</head>

<body>

<div class="container">
    <h1>MISSION-2 INITIALIZATION</h1>
    <p>Imotions Deploying to Production Environment...</p>
    <a href="https://afrinyouaremine.github.io/herewebegin/">
        ACCESS NEXT PHASE
    </a>
</div>

</body>
</html>