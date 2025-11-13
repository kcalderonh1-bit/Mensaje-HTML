<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Buenos días, Christopher</title>
<style>
*{margin:0;padding:0;box-sizing:border-box}
body{
  height:100vh;
  background:radial-gradient(circle at 20% 20%, #444 0, #000 55%);
  color:#fff;
  font-family:-apple-system,Segoe UI,Roboto,"Comic Sans MS",cursive;
  display:flex;
  justify-content:center;
  align-items:center;
  overflow:hidden;
}

/* Texto central */
.center{
  position:relative;
  text-align:center;
  z-index:5;
  padding:20px 25px;
  border-radius:20px;
  background:rgba(0,0,0,0.45);
  box-shadow:0 0 25px rgba(0,0,0,0.6);
  animation:fadeIn 2s ease-out;
}
h1{
  font-size:clamp(26px,6vw,40px);
  color:#ffe066;
  text-shadow:0 0 12px #fffa,0 0 24px #ff9;
  margin-bottom:8px;
}
p.frase{
  font-size:clamp(15px,4vw,20px);
  margin-bottom:10px;
}
p.firma{
  margin-top:6px;
  font-size:clamp(14px,3.5vw,18px);
  color:#ffd1f4;
  font-style:italic;
}
@keyframes fadeIn{
  from{opacity:0;transform:translateY(20px)}
  to{opacity:1;transform:translateY(0)}
}

/* Fuegos artificiales */
.firework{
  position:absolute;
  width:4px;
  height:120px;
  background:linear-gradient(to top,rgba(255,255,255,0.9),transparent);
  bottom:-80px;
  transform-origin:center bottom;
  animation:shoot 2.2s infinite ease-out;
  opacity:0;
}
.firework:before,
.firework:after{
  content:"";
  position:absolute;
  inset:auto;
  width:6px;
  height:6px;
  border-radius:50%;
  box-shadow:
    0 0 0 0 #ff5fa2,
    12px 0 0 0 #ffd166,
    -12px 0 0 0 #7bdff2,
    0 12px 0 0 #f4a261,
    0 -12px 0 0 #b5e48c,
    8px 8px 0 0 #ffcad4,
    -8px -8px 0 0 #9bf6ff;
  opacity:0;
}
.firework:before{
  top:-10px;
}
.firework:after{
  top:-10px;
  transform:rotate(45deg);
}

@keyframes shoot{
  0%{
    bottom:-60px;
    opacity:0;
  }
  20%{
    bottom:40vh;
    opacity:1;
  }
  40%{
    bottom:55vh;
    opacity:1;
  }
  45%{
    height:0;
  }
  46%{
    height:0;
  }
  55%,100%{
    opacity:0;
  }
}
@keyframes explode{
  from{transform:scale(0);opacity:1}
  to{transform:scale(1.4);opacity:0}
}

/* Posiciones y tiempos distintos */
.firework.f1{left:15%;animation-delay:0s}
.firework.f2{left:35%;animation-delay:.4s}
.firework.f3{left:55%;animation-delay:.9s}
.firework.f4{left:75%;animation-delay:1.3s}
.firework.f5{left:50%;animation-delay:1.7s}

/* estrellitas de fondo */
.star{
  position:absolute;
  width:2px;
  height:2px;
  background:#fff;
  border-radius:50%;
  opacity:.3;
  animation:twinkle 3s infinite ease-in-out;
}
@keyframes twinkle{
  0%,100%{opacity:.2;transform:scale(1)}
  50%{opacity:1;transform:scale(1.8)}
}
</style>
</head>
<body>

<!-- estrellitas simples -->
<div class="star" style="top:10%;left:20%;animation-delay:.2s"></div>
<div class="star" style="top:25%;left:70%;animation-delay:1s"></div>
<div class="star" style="top:40%;left:10%;animation-delay:.5s"></div>
<div class="star" style="top:60%;left:80%;animation-delay:1.6s"></div>
<div class="star" style="top:15%;left:50%;animation-delay:.9s"></div>

<!-- fuegos -->
<div class="firework f1"></div>
<div class="firework f2"></div>
<div class="firework f3"></div>
<div class="firework f4"></div>
<div class="firework f5"></div>

<!-- texto central -->
<div class="center">
  <h1>🎆 Buenos días, Christopher 🎆</h1>
  <p class="frase">
    Que hoy te acompañen la paz, la alegría<br>
    y muchos motivos para sonreír. ✨
  </p>
  <p class="firma">Con cariño, Vanessa 💖</p>
</div>

</body>
</html>
