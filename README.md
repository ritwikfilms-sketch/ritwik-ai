<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>About - Ritwik Films AI</title>
<style>
body { margin:0; font-family:'Segoe UI',Arial; background: linear-gradient(135deg,#0f0f0f,#1a1a1a); color:white; text-align:center; }
nav { background:#111; display:flex; justify-content:center; padding:15px; }
nav a { color:white; margin:0 20px; text-decoration:none; font-weight:bold; transition:0.3s; }
nav a:hover { color:#ff3366; }
h1 { margin-top:50px; font-size:40px; }
p { margin:15px; font-size:18px; color:#ccc; }
.btn { display:inline-block; margin-top:20px; padding:12px 25px; background:#ff004f; color:white; border-radius:50px; text-decoration:none; transition:0.3s; }
.btn:hover { background:#ff3366; transform:translateY(-3px); }
@media(max-width:768px){ h1{ font-size:32px; } }
</style>
</head>
<body>

<nav>
<a href="index.html">Home</a>
<a href="about.html">About</a>
<a href="contact.html">Contact</a>
</nav>

<h1>About Me</h1>
<p id="about-text">I am Ritwik, the creator of Ritwik Films AI. This platform showcases AI tools, creative projects, and digital innovations.</p>
<button class="btn" onclick="speakText(document.getElementById('about-text').innerText)">🔊 Listen</button>

<a href="index.html" class="btn">Back to Home</a>

<script>
function speakText(text){
  if('speechSynthesis' in window){
    let utterance=new SpeechSynthesisUtterance(text);
    utterance.rate=1;
    utterance.pitch=1;
    speechSynthesis.speak(utterance);
  }else{
    alert("Sorry, your browser does not support AI voice.");
  }
}
</script>

</body>
</html>
