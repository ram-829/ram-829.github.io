<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy New Year, Saumya 🤍</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#1b0f2e">

<style>
:root{
--bg1:#0b1024;
--bg2:#26163f;
--glass:rgba(255,255,255,.08);
--text:#ffffff;
}
*{margin:0;padding:0;box-sizing:border-box}
body{
font-family:system-ui,-apple-system,BlinkMacSystemFont;
min-height:100vh;
background:linear-gradient(135deg,var(--bg1),var(--bg2));
color:var(--text);
overflow-x:hidden;
}

main{
max-width:900px;
margin:auto;
padding:28px;
position:relative;
z-index:2;
}

.card{
background:var(--glass);
backdrop-filter:blur(18px);
border-radius:26px;
padding:26px;
box-shadow:0 20px 50px rgba(0,0,0,.55);
margin-bottom:28px;
}

h1,h2{text-align:center;margin-bottom:14px}

.grid{
display:grid;
grid-template-columns:repeat(2,1fr);
gap:10px;
}
@media(min-width:600px){
.grid{grid-template-columns:repeat(4,1fr)}
}

button{
border:none;
border-radius:18px;
padding:14px;
background:rgba(12,8,35,.9);
color:white;
cursor:pointer;
transition:.3s;
}
button:hover{transform:scale(1.04)}
button.opened{opacity:.7}

.display{
margin-top:18px;
min-height:120px;
font-size:1.05rem;
line-height:1.6;
}

.cursor{
display:inline-block;
width:2px;
height:1em;
background:white;
margin-left:4px;
animation:blink 1s infinite;
}
@keyframes blink{50%{opacity:0}}

.fireworks{
position:fixed;
inset:0;
pointer-events:none;
z-index:4;
}
.firework{
position:absolute;
width:5px;
height:5px;
border-radius:50%;
background:#ffd6f6;
animation:boom 1.6s forwards;
}
@keyframes boom{
0%{transform:scale(.2);opacity:0}
20%{opacity:1}
100%{transform:scale(2.4);opacity:0}
}

/* ENDING SCENE */
#ending{
position:fixed;
inset:0;
background:radial-gradient(circle at center,#43235f,#0b1024);
display:flex;
flex-direction:column;
align-items:center;
justify-content:center;
text-align:center;
opacity:0;
pointer-events:none;
transition:opacity 2s ease;
z-index:10;
}
#ending.show{opacity:1;pointer-events:auto}

#ending h1{
font-size:2.6rem;
margin-bottom:14px;
animation:fadeUp 2s ease forwards;
}
#ending p{
font-size:1.05rem;
opacity:.9;
animation:fadeUp 2.6s ease forwards;
}

@keyframes fadeUp{
from{opacity:0;transform:translateY(16px)}
to{opacity:1;transform:translateY(0)}
}
</style>
</head>

<body>

<div class="fireworks" id="fireworks"></div>

<main>
<section class="card">
<h1>Happy New Year, Saumya 🤍</h1>
<p id="wishText"></p>
</section>

<section class="card">
<h2>11 chhoti-chhoti love notes 💌</h2>
<div class="grid" id="buttons"></div>
<div class="display">
<span id="noteText"></span><span class="cursor" id="cursor"></span>
</div>
</section>
</main>

<!-- ENDING -->
<div id="ending">
<h1>I love you, Saumya 🤍</h1>
<p>
Not loudly. Not perfectly.<br>
Just honestly, deeply, and always.
</p>
</div>

<script>
const wishLines=[
"Yeh naya saal tumhari zindagi me shanti, strength aur khushiyan le aaye.",
"Main hamesha aapke saath hoon — har situation me, har phase me.",
"Jaise aaj tumse pyaar karta hoon, waise hi hamesha karta rahunga."
];

const notes=[
"Tumhari presence meri zindagi me ek soft si roshni ki tarah hai — jo andheron me bhi raasta dikha deti hai.",
"Main tumse sirf pyaar nahi karta, main tumhari respect karta hoon.",
"Baatein kam ho sakti hain, par tumhari jagah kabhi kam nahi hoti.",
"Tumhari khushi meri priority hai — bina kisi wajah ke.",
"Main perfect nahi banna chahta, bas real rehna chahta hoon.",
"Tum mere liye sirf ek person nahi, ek feeling ho.",
"Main tumse bina expectation ke pyaar karta hoon.",
"Dil chup rehta hai, par hamesha tumhara khayal rakhta hai.",
"Chahe future jo bhi ho, mera pyaar loyal rahega.",
"Main tumse bahut pyaar karta hoon, Saumya.",
"Tum mere dil ke bahut kareeb ho — aur hamesha rahogi."
];

const wish=document.getElementById("wishText");
const note=document.getElementById("noteText");
const cursor=document.getElementById("cursor");
const fireworks=document.getElementById("fireworks");
const ending=document.getElementById("ending");
const buttons=document.getElementById("buttons");

let opened=new Set();

function typeText(el,text,speed=35){
el.textContent="";
cursor.style.display="inline-block";
let i=0;
(function t(){
if(i<=text.length){
el.textContent=text.slice(0,i++);
setTimeout(t,speed);
}else cursor.style.display="none";
})();
}

function fire(){
for(let i=0;i<3;i++){
const f=document.createElement("div");
f.className="firework";
f.style.left=20+Math.random()*60+"vw";
f.style.top=20+Math.random()*40+"vh";
fireworks.appendChild(f);
setTimeout(()=>f.remove(),1600);
}
}

/* Wish typing */
wishLines.forEach((l,i)=>{
setTimeout(()=>typeText(wish,l),800*i+800);
});

/* Notes */
notes.forEach((_,i)=>{
const b=document.createElement("button");
b.textContent="Note "+(i+1);
b.onclick=()=>{
opened.add(i);
typeText(note,notes[i]);
fire();
b.classList.add("opened");
if(opened.size===notes.length){
setTimeout(()=>ending.classList.add("show"),2000);
}
};
buttons.appendChild(b);
});
</script>

</body>
</html>
