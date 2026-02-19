<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mission Two | Deployment Console</title>

<style>
:root{
    --primary:#ff0033;
    --secondary:#1a1a1a;
    --accent:#00e6ff;
}

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background: radial-gradient(circle at top, #1a0005, #000000 70%);
    font-family: 'Segoe UI', sans-serif;
    color:white;
    overflow:hidden;
}

/* Glass Container */
.container{
    width:90%;
    max-width:600px;
    padding:40px;
    border-radius:20px;
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(20px);
    border:1px solid rgba(255,255,255,0.1);
    box-shadow:0 0 40px rgba(255,0,51,0.3);
    text-align:center;
    animation: fadeIn 1.5s ease forwards;
}

/* Heading */
h1{
    font-size:2.5rem;
    letter-spacing:3px;
    margin-bottom:10px;
    background: linear-gradient(90deg, #ff0033, #00e6ff);
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
}

/* Subtext */
p{
    font-size:1rem;
    color:#cccccc;
    margin-bottom:30px;
    letter-spacing:1px;
}

/* Button */
a{
    display:inline-block;
    padding:14px 35px;
    border-radius:40px;
    text-decoration:none;
    font-weight:bold;
    letter-spacing:2px;
    background: linear-gradient(90deg, #ff0033, #cc0000);
    color:white;
    transition:0.4s ease;
    box-shadow:0 0 20px rgba(255,0,51,0.6);
}

a:hover{
    transform:scale(1.08);
    box-shadow:0 0 35px rgba(0,230,255,0.9);
    background: linear-gradient(90deg, #00e6ff, #0099cc);
}

/* Animations */
@keyframes fadeIn{
    from{opacity:0; transform:translateY(30px);}
    to{opacity:1; transform:translateY(0);}
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