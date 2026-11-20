
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<meta name="theme-color" content="#080d18">
<title>LOWKEY AI</title>

<style>
*{box-sizing:border-box}
body{
 margin:0;background:#080d18;color:#f5f7ff;
 font-family:Arial,sans-serif
}
header{
 height:68px;padding:0 18px;
 border-bottom:1px solid #202d43;
 display:flex;align-items:center;
 justify-content:space-between;
 position:sticky;top:0;background:#080d18;z-index:5
}
.logo{font-size:24px;font-weight:900;color:#65b3ff}
button{border:0;cursor:pointer;font-weight:bold}
.protag{background:#17365b;color:#80bdff;padding:9px 13px;border-radius:20px}
nav{
 display:flex;gap:7px;padding:12px;
 overflow-x:auto;border-bottom:1px solid #202d43
}
nav button{
 white-space:nowrap;background:#172237;
 color:#b7c8df;padding:11px 15px;border-radius:9px
}
.active{background:#267fe5!important;color:white!important}
main{max-width:760px;margin:auto;padding:20px 16px 120px}
.page{display:none}
.page.show{display:block}
h1{font-size:30px;margin:15px 0 8px}
.sub{color:#8fa2bd;font-size:14px;line-height:1.6}
.panel{
 background:#111c2e;border:1px solid #253650;
 border-radius:16px;padding:17px;margin:15px 0
}
input,textarea,select{
 background:#0a1322;border:1px solid #30425c;
 border-radius:11px;color:white;padding:13px;
 width:100%;font:15px Arial;outline:none
}
textarea{resize:vertical;min-height:140px}
.action{
 background:#267fe5;color:white;padding:13px 17px;
 border-radius:11px;margin-top:10px
}
.secondary{
 background:#1c2b43;color:#d5e5fa;
 padding:12px;border-radius:10px;margin:4px 2px
}
.messages{display:flex;flex-direction:column;gap:12px;margin:20px 0}
.msg{
 padding:13px 15px;border-radius:14px;
 line-height:1.5;white-space:pre-wrap;
 overflow-wrap:anywhere;max-width:92%
}
.user{background:#1556a1;align-self:flex-end}
.bot{background:#17243a;border:1px solid #2a3c57;align-self:flex-start}
.composer{display:flex;gap:8px;margin-top:15px}
.composer input{flex:1;min-width:0}
.composer button{
 background:#267fe5;color:white;
 padding:0 16px;border-radius:11px
}
.muted{color:#8294ad;font-size:12px;line-height:1.6}
.price{font-size:40px;font-weight:900;color:#68b3ff}
.feature{padding:11px 0;border-bottom:1px solid #263650}
.preview{max-width:100%;max-height:240px;border-radius:12px;margin:10px 0}
footer{text-align:center;color:#647891;font-size:11px;margin-top:35px}
#notice{
 position:fixed;bottom:85px;left:15px;right:15px;
 background:#183353;padding:13px;border-radius:12px;
 text-align:center;display:none;z-index:10
}
</style>
</head>

<body>

<header>
 <div class="logo">LOWKEY AI</div>
 <button class="protag" onclick="showPage('pro')">★ GET PRO</button>
</header>

<nav>
 <button class="active" onclick="showPage('home',this)">Chat</button>
 <button onclick="showPage('writing',this)">Writing</button>
 <button onclick="showPage('files',this)">Files</button>
 <button onclick="showPage('pro',this)">Pro</button>
</nav>

<main>

<!-- CHAT -->
<section id="home" class="page show">
 <h1>What's good? 👋</h1>
 <p class="sub">Your AI. Your way. No complicated stuff.</p>

 <div class="panel">
  <strong>LOWKEY AI</strong>
  <p class="sub">Ask anything. Get help. Create something.</p>

  <div id="messages" class="messages">
   <div class="msg bot">
    Yo! Welcome to LOWKEY AI.
    What are we working on today?
   </div>
  </div>

  <div class="composer">
   <input id="chatinput" placeholder="Message LOWKEY AI...">
   <button onclick="sendChat()">SEND</button>
  </div>
  <p class="muted">AI connection coming soon.</p>
 </div>
</section>

<!-- WRITING -->
<section id="writing" class="page">
 <h1>Writing Studio ✍️</h1>
 <p class="sub">Improve your writing while keeping your own voice.</p>

 <div class="panel">
  <strong>Your writing</strong>
  <textarea id="essay" placeholder="Paste your essay or writing here..."></textarea>

  <p class="muted">Choose an editing option.</p>

  <button class="action" onclick="editText('Improve clarity and grammar')">
   Improve writing
  </button>

  <button class="secondary" onclick="editText('Make the writing sound more natural')">
   Make it more natural
  </button>

  <button class="secondary" onclick="editText('Give constructive feedback')">
   Give feedback
  </button>

  <div id="writingresult" class="panel" style="display:none">
   <strong>Writing results</strong>
   <p id="writingtext" class="sub"></p>
  </div>
 </div>
</section>

<!-- FILES -->
<section id="files" class="page">
 <h1>File Center 📁</h1>
 <p class="sub">Choose screenshots, PDFs and documents from your phone.</p>

 <div class="panel">
  <input type="file" id="uploads"
   accept="image/*,.pdf,.txt,.doc,.docx" multiple>

  <div id="filelist" class="muted">No files selected.</div>

  <button class="action" onclick="previewFiles()">
   Review files
  </button>

  <div id="filepreview"></div>

  <p class="muted">
   File selection and image previews work.
   AI file analysis requires a secure backend.
  </p>
 </div>
</section>

<!-- PRO -->
<section id="pro" class="page">
 <h1>LOWKEY AI PRO ⚡</h1>
 <p class="sub">More power. More possibilities.</p>

 <div class="panel">
  <div class="price">$2.00</div>
  <strong>ONE-TIME PAYMENT</strong>

  <div class="feature">✓ Stronger AI reasoning</div>
  <div class="feature">✓ Larger file upload allowance</div>
  <div class="feature">✓ Advanced writing tools</div>
  <div class="feature">✓ Higher usage limits</div>
  <div class="feature">✓ Premium AI features</div>

  <button class="action" style="width:100%"
   onclick="purchase()">
   Get LOWKEY AI Pro
  </button>

  <p class="muted">
   Checkout is not connected yet. No payment will be taken.
  </p>
 </div>
</section>

<footer>
 LOWKEY AI © 2026 · Your AI. Your Way.
</footer>

</main>

<div id="notice"></div>

<script>

// NAVIGATION
function showPage(id,button){
 document.querySelectorAll('.page').forEach(p=>{
  p.classList.remove('show');
 });
 document.getElementById(id).classList.add('show');

 document.querySelectorAll('nav button').forEach(b=>{
  b.classList.remove('active');
 });

 if(button)button.classList.add('active');
 window.scrollTo(0,0);
}

// NOTIFICATIONS
function notify(message){
 const n=document.getElementById('notice');
 n.textContent=message;
 n.style.display='block';
 setTimeout(()=>n.style.display='none',3000);
}

// CHAT
function addMessage(text,type){
 const box=document.getElementById('messages');
 const div=document.createElement('div');
 div.className='msg '+type;
 div.textContent=text;
 box.appendChild(div);
 div.scrollIntoView({behavior:'smooth',block:'end'});
}

function sendChat(){
 const input=document.getElementById('chatinput');
 const text=input.value.trim();
 if(!text)return;

 addMessage(text,'user');
 input.value='';

 setTimeout(()=>{
  addMessage(
   'LOWKEY AI is currently in prototype mode. We still need to connect an AI service to provide real answers!',
   'bot'
  );
 },400);
}

document.getElementById('chatinput')
.addEventListener('keydown',e=>{
 if(e.key==='Enter')sendChat();
});

// WRITING STUDIO
function editText(action){
 const text=document.getElementById('essay').value.trim();

 if(!text){
  notify('Paste your writing first!');
  return;
 }

 document.getElementById('writingresult').style.display='block';

 document.getElementById('writingtext').textContent=
 'Requested action: '+action+
 '\n\nYour text is ready for the AI writing service. '+
 'Actual editing will work after the AI backend is connected.';
}

// FILE UPLOADS
document.getElementById('uploads')
.addEventListener('change',e=>{
 const files=[...e.target.files];

 document.getElementById('filelist').textContent=
 files.map(f=>f.name+' ('+(f.size/1024).toFixed(1)+' KB)')
 .join('\n')||'No files selected.';
});

function previewFiles(){
 const files=[...document.getElementById('uploads').files];
 const area=document.getElementById('filepreview');

 area.replaceChildren();

 if(!files.length){
  notify('Choose a file first!');
  return;
 }

 files.forEach(file=>{
  const item=document.createElement('p');
  item.className='muted';
  item.textContent='Selected: '+file.name;
  area.appendChild(item);

  if(file.type.startsWith('image/')){
   const image=document.createElement('img');
   image.className='preview';
   image.alt=file.name;
   image.src=URL.createObjectURL(file);
   area.appendChild(image);
  }
 });
}

// PRO CHECKOUT PLACEHOLDER
function purchase(){
 notify('LOWKEY AI Pro checkout is coming soon!');
}

</script>
</body>
</html>
