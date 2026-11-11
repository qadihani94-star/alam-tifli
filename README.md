<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>عالم طفلي</title>
<style>
body{
font-family:Arial,sans-serif;
margin:0;text-align:center;
background:linear-gradient(135deg,#fff1c9,#d8f5ff);
color:#34445b;
}
header{padding:25px;background:#ffcf69}
h1{font-size:32px}
.lion{font-size:90px}
.container{padding:20px}
.card{
background:white;padding:20px;margin:14px auto;
border-radius:22px;max-width:330px;
box-shadow:0 4px 12px #0001;
}
button{
border:0;border-radius:15px;padding:15px;
margin:7px;background:#45b9a0;color:white;
font-size:19px;cursor:pointer;
}
button:active{transform:scale(.96)}
#result{font-size:27px;color:#e58c30}
</style>
</head>
<body>
<header>
<div class="lion">🦁</div>
<h1>مرحباً بكم في عالم طفلي</h1>
<p>أنا لولو! هيا نتعلم ونلعب معاً</p>
</header>
<div class="container">
<div class="card">
<h2>🔤 تعلم الحروف</h2>
<button onclick="show('أ - أسد 🦁')">حرف أ</button>
<button onclick="show('ب - بطة 🦆')">حرف ب</button>
<button onclick="show('ت - تفاحة 🍎')">حرف ت</button>
</div>
<div class="card">
<h2>🔢 تعلم الأرقام</h2>
<button onclick="show('واحد 1️⃣')">1</button>
<button onclick="show('اثنان 2️⃣')">2</button>
<button onclick="show('ثلاثة 3️⃣')">3</button>
</div>
<div class="card">
<h2>🎨 تعلم الألوان</h2>
<button onclick="show('أحمر ❤️')">أحمر</button>
<button onclick="show('أزرق 💙')">أزرق</button>
<button onclick="show('أخضر 💚')">أخضر</button>
</div>
<div class="card">
<h2>⭐ ماذا تعلمنا يا لولو؟</h2>
<p id="result">اضغط على أي درس لنبدأ!</p>
<button onclick="speak()">🔊 استمع</button>
</div>
</div>
<script>
function show(value){
document.getElementById('result').innerText=value;
}
function speak(){
let text=document.getElementById('result').innerText;
if('speechSynthesis' in window){
let msg=new SpeechSynthesisUtterance(text);
msg.lang='ar-SA';
speechSynthesis.speak(msg);
}
}
</script>
</body>
</html>
