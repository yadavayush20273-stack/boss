<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Boss ❤️</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family: 'Poppins', sans-serif;
}

body{
min-height:100vh;
overflow:hidden;
color:white;
display:flex;
align-items:center;
justify-content:center;
text-align:center;
background:#0f0c29;
position:relative;
}

/* Cinematic Glow Background */
body::before{
content:"";
position:absolute;
width:200%;
height:200%;
background:radial-gradient(circle at 30% 40%, #ff416c55, transparent 40%),
           radial-gradient(circle at 70% 60%, #7b2ff755, transparent 40%),
           radial-gradient(circle at 50% 80%, #00c6ff44, transparent 40%);
animation:moveBg 15s linear infinite alternate;
z-index:0;
}

@keyframes moveBg{
0%{transform:translate(-10%, -10%);}
100%{transform:translate(-30%, -30%);}
}

.container{
position:relative;
z-index:2;
max-width:500px;
padding:20px;
}

button{
padding:10px 22px;
font-size:16px;
border:none;
border-radius:30px;
margin:10px;
cursor:pointer;
transition:0.3s;
}

#yes{
background:white;
color:#ff416c;
}

#no{
background:transparent;
border:1px solid white;
color:white;
}

/* Gift Overlay */
.giftOverlay{
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,0.8);
display:none;
align-items:center;
justify-content:center;
flex-direction:column;
z-index:10;
}

/* Gift Box */
.gift{
font-size:120px;
animation:shake 1s infinite;
cursor:pointer;
}

@keyframes shake{
0%{transform:rotate(0);}
25%{transform:rotate(5deg);}
50%{transform:rotate(-5deg);}
75%{transform:rotate(5deg);}
100%{transform:rotate(0);}
}

/* Reveal Text */
.revealText{
font-size:28px;
margin-top:20px;
opacity:0;
transform:scale(0.5);
transition:1s;
color:#ffccd5;
text-shadow:0 0 15px #ff4d6d;
}

.showText{
opacity:1;
transform:scale(1.2);
}

</style>
</head>

<body>

<div class="container">
<h1>Welcome Boss ❤️</h1>
<p>Will you stay with me forever ? 💍</p>

<button id="yes">YES 💖</button>
<button id="no">NO 😜</button>
</div>

<!-- Gift Surprise -->
<div class="giftOverlay" id="giftOverlay">
<div class="gift" id="gift">🎁</div>
<div class="revealText" id="sweetText">
You are so sweet Boss.... 🥰🤭
</div>
</div>

<script>

// NO button move
let noBtn=document.getElementById("no");
noBtn.addEventListener("click",()=>{
let x=Math.random()*150-75;
let y=Math.random()*150-75;
noBtn.style.transform=`translate(${x}px,${y}px)`;
});

// YES click show gift
document.getElementById("yes").onclick=function(){
document.getElementById("giftOverlay").style.display="flex";

setTimeout(()=>{
// Open gift
document.getElementById("gift").innerHTML="💝";
document.getElementById("gift").style.animation="none";

// Show text
document.getElementById("sweetText").classList.add("showText");

},2000);

};

</script>

</body>
</html>
