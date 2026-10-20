
<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#7c3aed">
<meta name="description" content="Masti Zone - शायरी, जोक्स, दोस्ती और YouTube वीडियो">
<title>Masti Zone | जय हिंद यादव</title>

<style>
*{box-sizing:border-box}
body{
  margin:0;
  font-family:Arial,"Noto Sans Devanagari",sans-serif;
  color:#fff;
  background:linear-gradient(135deg,#7c3aed,#ec4899,#f97316,#0891b2);
  background-attachment:fixed;
}
header{text-align:center;padding:22px 12px 15px}
h1{margin:8px 0;font-size:32px}
.moving{
  overflow:hidden;white-space:nowrap;
  background:#111827;color:#fde047;
  padding:12px 0;font-weight:bold;
}
.moving span{
  display:inline-block;padding-left:100%;
  animation:move 13s linear infinite;
}
@keyframes move{to{transform:translateX(-100%)}}
nav{
  display:flex;flex-wrap:wrap;justify-content:center;
  gap:8px;padding:12px;
}
nav a,.btn{
  border:0;border-radius:22px;padding:11px 15px;
  background:#fff;color:#6d28d9;text-decoration:none;
  font-weight:bold;cursor:pointer;display:inline-block;
}
main{max-width:850px;margin:auto;padding:12px}
section{
  background:rgba(20,15,45,.88);
  border:1px solid rgba(255,255,255,.25);
  border-radius:18px;padding:17px;margin:15px 0;
  box-shadow:0 5px 18px #0002;
}
h2{color:#fde047;margin-top:0}
.card{
  background:#ffffff12;border-radius:13px;
  padding:14px;margin:12px 0;line-height:1.8;
}
.btn{margin:5px 3px}
.whatsapp{background:#25d366;color:#073b20}
.status{background:#d9f99d;color:#14532d}
.video-frame{
  width:100%;aspect-ratio:16/9;border:0;
  border-radius:12px;background:#111827;
}
input{
  width:100%;padding:12px;border-radius:10px;
  border:1px solid #ccc;margin:8px 0;color:#111;
}
.small{font-size:13px;line-height:1.6;color:#e5e7eb}
footer{text-align:center;padding:25px 12px}
.bubble{
  position:fixed;pointer-events:none;z-index:99;
  animation:rise 1.5s ease-out forwards;
}
@keyframes rise{
  0%{transform:translateY(0) scale(.6);opacity:1}
  100%{transform:translateY(-180px) scale(1.5);opacity:0}
}
</style>
</head>

<body>
<header>
  <div style="font-size:42px">🎉😎🌈</div>
  <h1>🎊 Masti Zone 🎊</h1>
  <p>शायरी • जोक्स • दोस्ती • मस्ती</p>
</header>

<div class="moving"><span>🇮🇳 जय हिंद यादव ❤️ आपका अपना Masti Zone ❤️ जय हिंद यादव 🇮🇳</span></div>

<nav>
  <a href="#videos">📺 वीडियो</a>
  <a href="#shayari">❤️ शायरी</a>
  <a href="#jokes">😂 जोक्स</a>
  <a href="#dosti">🤝 दोस्ती</a>
</nav>

<main>
<section>
  <h2>🌈 स्वागत है आपका!</h2>
  <p>यहाँ मिलेगा मनोरंजन, दिल की बातें और दोस्तों के साथ शेयर करने लायक मजेदार कंटेंट।</p>
  <button class="btn whatsapp" onclick="shareWhatsApp()">📲 दोस्तों को शेयर करें</button>
  <button class="btn status" onclick="shareStatus()">🟢 WhatsApp Status शेयर विकल्प</button>
  <p class="small">Status का विकल्प आपके फोन और WhatsApp के अनुसार खुलेगा। Status अपने-आप पोस्ट नहीं होगा; आपको खुद शेयर करना होगा।</p>
</section>

<section id="videos">
  <h2>📺 YouTube शायरी वीडियो</h2>
  <p>वीडियो इसी वेबसाइट के अंदर चलाने के लिए अपनी सार्वजनिक YouTube प्लेलिस्ट जोड़ें।</p>

  <iframe id="playlistPlayer" class="video-frame"
    title="YouTube Shayari Playlist"
    src="about:blank"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    allowfullscreen>
  </iframe>

  <label for="playlistLink">अपनी YouTube प्लेलिस्ट का लिंक यहाँ डालें:</label>
  <input id="playlistLink" type="url"
    placeholder="https://www.youtube.com/playlist?list=...">
  <button class="btn" onclick="loadPlaylist()">▶️ प्लेलिस्ट चलाएँ</button>

  <p class="small">
    ध्यान दें: ऊपर लिंक डालने से प्लेलिस्ट इसी फोन के ब्राउज़र में खुलेगी।
    सभी वेबसाइट विज़िटर के लिए प्लेलिस्ट स्थायी रूप से सेट करने हेतु नीचे दिए गए
    कोड में YOUTUBE_PLAYLIST_ID बदलना होगा। प्लेलिस्ट सार्वजनिक होनी चाहिए।
  </p>
  <p id="videoMessage" class="small">अभी प्लेलिस्ट सेट नहीं है।</p>
</section>

<section id="shayari">
  <h2>❤️ दिल वाली शायरी</h2>
  <div class="card">
    तेरी मुस्कान से दिन मेरा खास हो जाता है,<br>
    तू पास हो तो हर पल एहसास हो जाता है। 💖
    <br><button class="btn" onclick="shareText('तेरी मुस्कान से दिन मेरा खास हो जाता है, तू पास हो तो हर पल एहसास हो जाता है। ❤️')">शायरी शेयर करें</button>
  </div>
  <div class="card">
    कुछ रिश्ते दिल से निभाए जाते हैं,<br>
    हर बात शब्दों से नहीं बताई जाती है। 🌹
    <br><button class="btn" onclick="shareText('कुछ रिश्ते दिल से निभाए जाते हैं, हर बात शब्दों से नहीं बताई जाती है। 🌹')">शायरी शेयर करें</button>
  </div>
  <div class="card">
    मुस्कुराते रहो, दुनिया को जलने दो,<br>
    अपने सपनों को आसमान में उड़ने दो। ✨
    <br><button class="btn" onclick="shareText('मुस्कुराते रहो, दुनिया को जलने दो, अपने सपनों को आसमान में उड़ने दो। ✨')">शायरी शेयर करें</button>
  </div>
</section>

<section id="jokes">
  <h2>😂 मजेदार जोक्स</h2>
  <div class="card">
    टीचर: बताओ, सबसे ज्यादा नशा किस चीज में होता है?<br>
    छात्र: किताबों में! खोलते ही नींद आ जाती है। 😂
    <br><button class="btn" onclick="shareText('टीचर: सबसे ज्यादा नशा किस चीज में होता है? छात्र: किताबों में! खोलते ही नींद आ जाती है। 😂')">जोक शेयर करें</button>
  </div>
  <div class="card">
    दोस्त: भाई, पढ़ाई कैसी चल रही है?<br>
    मैं: जैसे फोन की बैटरी—बस नाम की बाकी है! 🤣
    <br><button class="btn" onclick="shareText('दोस्त: भाई, पढ़ाई कैसी चल रही है? मैं: जैसे फोन की बैटरी—बस नाम की बाकी है! 🤣')">जोक शेयर करें</button>
  </div>
</section>

<section id="dosti">
  <h2>🤝 दोस्ती का कोना</h2>
  <div class="card">
    दोस्त वो नहीं जो हर वक्त साथ हो,<br>
    दोस्त वो है जो दूर होकर भी दिल के पास हो। 🫂
    <br><button class="btn" onclick="shareText('दोस्त वो नहीं जो हर वक्त साथ हो, दोस्त वो है जो दूर होकर भी दिल के पास हो। 🫂')">दोस्ती शेयर करें</button>
  </div>
  <div class="card">
    सच्ची दोस्ती किस्मत वालों को मिलती है,<br>
    जो हर मुश्किल में हिम्मत बनकर खिलती है। 💛
    <br><button class="btn" onclick="shareText('सच्ची दोस्ती किस्मत वालों को मिलती है, जो हर मुश्किल में हिम्मत बनकर खिलती है। 💛')">दोस्ती शेयर करें</button>
  </div>
</section>

<section>
  <h2>💬 अपनी मस्ती शेयर करें</h2>
  <p>अपने दोस्तों को Masti Zone का लिंक भेजें और उन्हें भी मस्ती में शामिल करें!</p>
  <button class="btn whatsapp" onclick="shareWhatsApp()">WhatsApp पर शेयर करें</button>
</section>
</main>

<footer>
  <strong>🇮🇳 जय हिंद यादव | Masti Zone 🇮🇳</strong>
  <p>मस्ती करते रहिए, मुस्कुराते रहिए! ❤️</p>
</footer>

<script>
/*
  वेबसाइट के सभी विज़िटर के लिए वीडियो सेट करने का तरीका:
  1. अपनी सार्वजनिक YouTube प्लेलिस्ट बनाइए।
  2. उसके लिंक में list= के बाद वाला ID कॉपी कीजिए।
  3. नीचे PASTE_PUBLIC_PLAYLIST_ID_HERE की जगह वह ID डालिए।
  4. index.html सेव कीजिए।
*/
const YOUTUBE_PLAYLIST_ID = "PASTE_PUBLIC_PLAYLIST_ID_HERE";

function setPlaylist(id){
  if(!id || id === "PASTE_PUBLIC_PLAYLIST_ID_HERE"){
    document.getElementById("videoMessage").textContent =
      "वीडियो दिखाने के लिए सार्वजनिक YouTube प्लेलिस्ट का ID सेट करें।";
    return;
  }
  document.getElementById("playlistPlayer").src =
    "https://www.youtube-nocookie.com/embed/videoseries?list=" +
    encodeURIComponent(id);
  document.getElementById("videoMessage").textContent =
    "प्लेलिस्ट लोड करने की कोशिश की जा रही है।";
}

function loadPlaylist(){
  const link = document.getElementById("playlistLink").value.trim();
  let id = "";
  try{
    const url = new URL(link);
    id = url.searchParams.get("list") || "";
  }catch(e){}
  if(!id){
    document.getElementById("videoMessage").textContent =
      "कृपया सही YouTube प्लेलिस्ट लिंक डालें, वीडियो का साधारण लिंक नहीं।";
    return;
  }
  setPlaylist(id);
}

function getSiteUrl(){
  return location.href.split("#")[0];
}

function shareWhatsApp(){
  const text = "🎉 Masti Zone पर शायरी, जोक्स और दोस्ती का मजा लें! " + getSiteUrl();
  location.href = "https://wa.me/?text=" + encodeURIComponent(text);
}

function shareText(text){
  const message = text + "\n\n— Masti Zone | जय हिंद यादव\n" + getSiteUrl();
  location.href = "https://wa.me/?text=" + encodeURIComponent(message);
}

async function shareStatus(){
  const text = "🎉 Masti Zone | शायरी • जोक्स • दोस्ती ❤️\n" + getSiteUrl();
  if(navigator.share){
    try{
      await navigator.share({title:"Masti Zone",text:text,url:getSiteUrl()});
    }catch(e){}
  }else{
    location.href = "https://wa.me/?text=" + encodeURIComponent(text);
  }
}

setPlaylist(YOUTUBE_PLAYLIST_ID);

document.addEventListener("click",function(e){
  const b=document.createElement("span");
  b.className="bubble";
  b.textContent=["💖","✨","🎉","❤️","🌈"][Math.floor(Math.random()*5)];
  b.style.left=e.clientX+"px";
  b.style.top=e.clientY+"px";
  b.style.fontSize=(18+Math.random()*18)+"px";
  document.body.appendChild(b);
  setTimeout(()=>b.remove(),1600);
});
</script>
</body>
</html>
