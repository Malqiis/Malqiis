<!doctype html>
<html lang="en">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>For You Afi!</title>
    <link rel="icon" href="💌" />
    <style>
        :root{
            --bg: #f3a6c1;
            --card: #e1a2a2;
            --pink: #b22d60;
            --soft: #ffd9e6;
            --text: #7a2140;
            --shadow-pink: hsla(339, 79%, 77%, 0.918);
        }
        *{box-sizing:border-box}

        body{
            margin:0;
            min-height:100vh;
            display:flex;
            align-items: flex-start;
            justify-content:center;
            font-family: 'Poppins', 'Comic Sans MS', system-ui, sans-serif;
            background: radial-gradient(circle at 10% 10%, #f6bedb, var(--bg));
            color:var(--text);
            overflow-x: hidden; 
            overflow-y: auto;
        }

        .app{
            width: 100%;
            min-height: 100vh;
            max-width: 1000px; 
            background: linear-gradient(180deg, rgba(255, 240, 245, 0.9), var(--card));
            padding:30px 24px; 
            position:relative;
        }

        header{display:flex;align-items:center;gap:14px}
        @keyframes heartBeat{
            0%, 100% {transform: scale(1); opacity:1}
            25% {transform: scale(1.1); opacity:0.9}
            50% {transform: scale(1); opacity:1}
            75% {transform: scale(1.1); opacity:0.9}
        }
        .logo{width:56px;height:56px;border-radius:12px;background:linear-gradient(180deg,var(--pink),#ff9cc3);display:flex;align-items:center;justify-content:center;color:white;font-weight:700; animation: heartBeat 2s infinite ease-in-out;}
        h1{font-size:20px;margin:0}
        p.lead{margin:6px 0 18px;color:#a43a66}

        .page{
            display:none;
            transition: opacity 0.4s ease-in-out; 
            opacity: 0;
            padding: 20px;
            border-radius: 12px;
            margin-bottom: 20px;
        }
        .page.active{
            display:block;
            opacity: 1;
        }

        #envelope {
            width: 100%;
            max-width: 320px;
            background: #fff0f6;
            border: 2px solid var(--pink);
            border-radius: 12px;
            padding: 40px 20px;
            text-align: center;
            box-shadow: 0 10px 20px rgba(0,0,0,0.15);
            cursor: pointer;
            margin: 100px auto 0;
            position: relative;
            transform-origin: center;
            transition: all 0.7s ease-in-out; 
        }
        .envelope-icon {
            font-size: 70px;
            margin-bottom: 10px;
            display: block;
        }
        .envelope-open-text {
            color: var(--text);
            font-weight: 500;
        }

        .center{display:flex;flex-direction:column;align-items:center;gap:12px}

        button{background:var(--soft);border:none;padding:10px 14px;border-radius:12px;font-size:15px;cursor:pointer;box-shadow:0 6px 14px rgba(0,0,0,0.08); transition: all 0.2s ease}
        button.primary{background:linear-gradient(180deg,var(--pink),#e692af);color:#fff}
        button.primary:hover{transform: translateY(-2px); box-shadow: 0 10px 20px var(--shadow-pink);}
        button:hover:not(.primary){background: #fff; box-shadow: 0 4px 8px var(--shadow-pink);}

        .row{
            display:flex;
            gap:12px;
            flex-wrap:wrap;
            justify-content:center;
            position: relative; 
            min-height: 80px; 
        }
        
        #homeNo {
            transition: all 0.3s ease-out; 
            position: relative;
            z-index: 10;
        }

        @keyframes float {
            0% { transform: translate(0, 0px) scale(1.1); }
            50% { transform: translate(10px, -10px) scale(1.1); }
            100% { transform: translate(0, 0px) scale(1.1); }
        }
        .cat-doodle{
            position:absolute;
            right:16px;
            bottom:8px;
            opacity:0.2; 
            animation: float 4s ease-in-out infinite;
        }
        .left-cat {
  left: 16px;
  right: auto;         /* overwrite property right dari .cat-doodle */
  bottom: 8px;         /* sama jarak dari bawah */
  opacity: 0.25;
  transform: scaleX(-1); /* flip supaya menghadap ke kanan */
  animation-delay: 1.5s; /* buat offset animasi */
  pointer-events: none;
  z-index: 0; /* kalau perlu letak di bawah content, ubah nombor */
}


        

        .choose-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(150px, 1fr));gap:14px;margin-top:16px}
        .card{
            background:linear-gradient(180deg,#fabae3, #fff7fb);
            border-radius:12px;
            padding:16px;
            text-align:left; 
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
            display: flex; 
            flex-direction: column;
            justify-content: space-between; 
            height: 100%; 
        }
        .card button{width: 100%;}
        .card .row {margin-top:auto; padding-top: 10px;}
        .choose-grid h3 {font-size: 16px;color: var(--pink);margin-top: 0;margin-bottom: 10px;}
        .small{font-size:13px;color:#8a3a5a}
        textarea,input[type=text]{width:100%;padding:10px;border-radius:8px;border:1px solid #ffd5e3;background:#fff;font-family:inherit;}

        .hide-header header {
            visibility: hidden;
            height: 0;
            padding: 0;
        }
    </style>
</head>
<body>
    <div class="app" id="app">
        <header>
            <div class="logo">❤</div>
            <div>
                <h1>🤍</h1>
                <p class="small">Things i meant to say, but didn’t. </p>
            </div>
        </header>

        <section id="envelope" class="page active" onclick="openEnvelope()">
            <div class="center" style="margin-top:50px;">
                <span class="envelope-icon">💌</span>
                <p class="envelope-open-text">A Special Letter Has Arrived!</p>
                <button class="primary" style="margin-top:20px;">Open Me 💖</button>
            </div>
        </section>

        <section id="home" class="page">
            <div class="center">
                <h2 style="font-size:30px; color:var(--pink);">ASSALAMUALAIKUM! HAI! GANTENG!</h2>
                <p class="lead">I made this special just for you hehe 🙈<br>idk kalau kau excited ka tidak tapi exciteddd pleaseee,<br> click yesss, kalau no sya marah 😾</p>
                <div class="row">
                    <button class="primary" id="homeYes">Yes </button>
                    <button id="homeNo">No </button>
                </div>
            </div>
        </section>

        <section id="page2" class="page">
            <div class="center">
                <h2 style="color:#3a283d">anywayyy saya sweet kan buat begini HAHAH jkjkj</h2>
                <p class="medium">fyi i made this with a lot of effort yk, hopefully you like it! <br> bukan smua la tapi at least ada effortt la mau communicate</p>
                <div style="margin-top:10px">
                    <button class="primary" onclick="show('choose')">Next ➜</button>
                    <button onclick="show('home')">↩ Back</button>
                </div>
            </div>
        </section>

        <section id="choose" class="page">
            <h2 style="text-align:center">HA NOW CHOOSE LA 🐾</h2>
            <div class="choose-grid">
                <div class="card">
                    <h3>🐈 miaoessay</h3>
                    <p class="small">My full heart message for you.</p> 
                    <div class="row"><button class="primary" onclick="show('essay')">Aww</button></div>
                </div>

                <div class="card">
                    <h3>😻 Why I Have An Eye For You?</h3>
                    <p class="small">The list of your charms yayyy.</p>
                    <div class="row"><button class="primary" onclick="show('reasons')">Aww</button></div>
                </div>

                <div class="card">
                    <h3>✉️ miaoconfess Box</h3>
                    <p class="small">Your secret message for me before asing.</p>
                    <div class="row"><button class="primary" onclick="show('confess')">Aww</button></div>
                </div>

                <div class="card" style="grid-column: span 2 / auto;">
                    <h3>🎶 miaolyrics for you </h3>
                    <div class="row"><button class="primary" onclick="show('lyrics')">Aww</button></div>
                </div>
            </div>

            <div style="margin-top:20px;text-align:center"><button onclick="show('page2')">↩ Back</button></div>
        </section>

        <section id="essay" class="page">
            <h2>secret message 📝</h2>
            <div class="card">
                <div id="essayText">
                    <p>Hey, actually saya lost — tapi just so yk sya rasa bersalah idk sbb apa tapi its related to you la and now saya mau say sorry if sya prnah buat kau rimas okey, and before betul2 
                    asing, saya mau asing dengan baik sebab kalau tiada any kata putus mcm tiba2 ja asing sebeb streak mati hmmm nnt macam rasa bersalah sampai bila2, dan yap, sorry ja la ya bye2 
                    see youu kalau kmu need anything just text me okey idk maybe kat tiktok or dc inshaAllah saya reply. itu pun kalau kamu rasa mau mau cakao apa2 ja la ya... sekian 
                    tu ja la dari sayaa, byeee aganteng.</p>
                </div>

                <div style="margin-top:10px" class="row">
                    <button onclick="makeEssayEditable()">Edit essay</button>
                    <button onclick="show('choose')">↩ Back</button>
                    <button onclick="show('reasons')">Next ➜</button>
                </div>

                <div id="essayEditor" style="margin-top:10px;display:none">
                    <textarea id="essayArea" rows="6"></textarea>
                    <div style="margin-top:8px" class="row">
                        <button onclick="saveEssay()" class="primary">Save</button>
                        <button onclick="cancelEssay()">Cancel</button>
                    </div>
                    <p class="small">My love - Westlife</p>
                </div>
            </div>
        </section>

        <section id="reasons" class="page">
            <h2>Why Ive got my eyes on you??? 😻</h2>
            <div class="card">
                <p style="font-size:50px; text-align:center; margin:10px 0;">🐈‍⬛️</p>
                <div class="reasons-list" id="reasonsList">
                    <div class="reason"><div>1. sya bole jdi diri sendiri pun kalau dengan kau, nda perlu jadi fake </div><button onclick="toggleLove(this)">💗</button></div>
                    <div class="reason"><div>2. sebab comelll hehe</div><button onclick="toggleLove(this)">💗</button></div>
                    <div class="reason"><div>3. and sebab kacak (cringe ka mian)</div><button onclick="toggleLove(this)">💗</button></div>
                    <div class="reason"><div>4. Bikin rindu bah HAHAHAH jk</div><button onclick="toggleLove(this)">💗</button></div>
                </div>
                <div style="margin-top:15px;text-align:center"><p class="small">Click button love! ⬆️</p></div>
                <div style="margin-top:8px" class="row">
                    <button onclick="show('choose')">↩ Back</button>
                    <button onclick="addReason()">Add reason</button>
                    <button onclick="show('confess')">Next Page ➜</button>
                </div>
            </div>
        </section>

        <section id="confess" class="page">
            <h2>Confess box 🤫</h2>
            <div class="card">
                <p class="small">You can write something here. (Apa yang Afi tulis, saya terima melalui 'Local Storage' browser Afi. Kalau Afi nak saya tahu, **screenshot** dan hantar terus direct ke saya!)</p>
                <textarea id="confessArea" rows="5" placeholder="Type something..."></textarea>
                <div style="margin-top:8px" class="row">
                    <button onclick="sendConfess()" class="primary">Send</button>
                    <button onclick="show('choose')">↩ Back</button>
                    <button onclick="show('lyrics')">Next Page ➜</button>
                </div>
                <div id="confessAck" style="margin-top:8px;color:#ab5573"></div>
            </div>
        </section>

        <section id="lyrics" class="page">
            <h2>🎤 Lyrics </h2>
            <div class="card">
                <pre style="white-space:pre-wrap;font-family:inherit">
resah jadi luka song by daun jatuh

"Ku menemukanmu saat ku terjatuh
Ke dalam ruang yang penuh kepahitan
Kau melindungiku di saat yang lain menyerangku
Ingin rasanya aku melihatmu di setiap langkahku

Tapi mengapa tiba-tiba seakan kau pergi?
Melepas rangkulanmu dan berhenti melindungiku tanpa sebab
Mungkin alam semesta tak menerimanya
Dan waktu tak memberi kesempatannya
Tapi setidaknya kau telah merubahku dari resah menjadi luka

Namun, aku akan tetap di sini
Menunggu alam semesta menerima
Dan angin membawakan jawabannya
Karena detak jantung dan nadiku akan selalu merindukanmu" 

--------------------------------------------------------

Pano song by Zack Tabudlo
"Pa'no naman ako? Nahulog na sa 'yo
Binitawan mo lang ba talaga ako?
Pa'no naman ako? Naghintay nang matagal sa 'yo
Wala lang ba talaga lahat ng 'yon sa 'yo?
Ano na ba'ng gagawin ko?"

--------------------------------------------------------

separuh aku song by NOAH
"Dengar laraku
Suara hati ini memanggil namamu
Kar'na separuh aku
Menyentuh laraku"

--------------------------------------------------------

seasons song by wave to earth
"I can't be your love
Cause I'm afraid I'll ruin your life
While the leaves withered away
And grew again
You have gone far away
I'll be pushing up daisies
And bring all the chances to here
But I'll pray for you all the time
If I could be by your side"

--------------------------------------------------------

we can't be friends song by Ariana Grande
"We can't be friends
But I'd like to just pretend
You cling to your papers and pens
Wait until you like me again"

---------------------------------------------------------


                <div style="margin-top:8px" class="row">
                    <button onclick="show('choose')">↩ Back</button>
                    <button onclick="show('closing')">The End</button>
                </div>
            </div>
        </section>

       <section id="closing" class="page">
    <h2>The Enddd 💌</h2>
    <div class="card">
        <p>Hehe thanks for your time Afi 😳<br>
        I just wanna say thank you for being such a kind, funny, and sweet person.
        You’ve made things a little brighter for me, and I’m really grateful for that 💗
        <br><br>
        I’m sorry if I ever made you uncomfortable or if there were things I couldn’t express properly.
        After this, even if we’ve gone our separate ways, I genuinely wish you all the best in everything you do.
        You deserve good things and happiness always 🌷
        <br><br>
        Take care of yourself okey, and don’t stress too much.
        Here’s a virtual hug from me 🫶🐾<br><br>
        Bye for now, and thank you for being part of my little story 💌
        </p>

        <p style="font-size:60px; text-align:center;">🫂</p>
        <div style="margin-top:12px;text-align:center">
            <button onclick="show('home')">↩ Start Again</button>
        </div>
    </div>
</section>


        <p class="cat-doodle" style="font-size:80px;">🐈</p>
        <p class="cat-doodle left-cat" style="font-size:80px;">🐈‍⬛</p>

    </div>

<script>
    function show(id){
        const currentPage = document.querySelector('.page.active');
        const targetPage = document.getElementById(id);
        if (currentPage) {
            currentPage.classList.remove('active');
            setTimeout(() => {
                currentPage.style.display = 'none';
                if (targetPage) {
                    targetPage.style.display = 'block';
                    setTimeout(() => {targetPage.classList.add('active');window.scrollTo(0,0);}, 10); 
                }
            }, 400); 
        } else if (targetPage) {
            targetPage.style.display = 'block';
            targetPage.classList.add('active');
            window.scrollTo(0,0);
        }
    }

    function openEnvelope() {
        const envelope = document.getElementById('envelope');
        const app = document.getElementById('app');
        envelope.style.transform = 'scale(2.5) rotate(-5deg)';
        envelope.style.opacity = '0';
        app.classList.add('hide-header');
        setTimeout(() => {
            app.classList.remove('hide-header');
            show('home');
        }, 500);
    }

    const homeNo = document.getElementById('homeNo');
    const homeYes = document.getElementById('homeYes');
    const homeSection = document.getElementById('home');

    homeYes.addEventListener('click', ()=>{
        homeSection.innerHTML = `
            <div class="center">
                <h2 style="font-size:30px; color:var(--pink);"> okey naise! 😼</h2>
                <p class="small">aight, let’s begin. </p>
                <div style="margin-top:10px">
                    <button class="primary" onclick="show('page2')">Lihat lagi ➜</button>
                </div>
            </div>`;
    });

    homeNo.addEventListener('mouseenter', ()=>{
        if (!homeSection) return;
        homeNo.style.position = 'absolute';
        const sectionWidth = homeSection.clientWidth;
        const sectionHeight = homeSection.clientHeight;
        const btnWidth = homeNo.offsetWidth;
        const btnHeight = homeNo.offsetHeight;
        const padding = 20; 
        const randomX = Math.random() * (sectionWidth - btnWidth - 2 * padding) + padding;
        const randomY = Math.random() * (sectionHeight - btnHeight - 2 * padding) + padding;
        homeNo.style.left = `${randomX}px`;
        homeNo.style.top = `${randomY}px`;
    });

    function makeEssayEditable(){
        document.getElementById('essayEditor').style.display='block';
        document.getElementById('essayArea').value=document.getElementById('essayText').innerText.trim();
    }
    function saveEssay(){
        const text=document.getElementById('essayArea').value;
        localStorage.setItem('essay',text);
        document.getElementById('essayText').innerHTML=escapeHtml(text);
        document.getElementById('essayEditor').style.display='none';
    }
    function cancelEssay(){document.getElementById('essayEditor').style.display='none';}
    function escapeHtml(text){return text.replace(/[&<>'"\n]/g,m=>({ '&':'&amp;','<':'&lt;','>':'&gt;',"'":'&#39;','"':'&quot;','\n':'<br>' }[m]));}

    function toggleLove(btn){btn.textContent=btn.textContent==='💗'?'💖':'💗';}

    function addReason(){
        const reason=prompt('Enter your reason 💬');
        if(reason){
            const div=document.createElement('div');
            div.className='reason';
            div.innerHTML=`<div>${escapeHtml(reason)}</div><button onclick="toggleLove(this)">💗</button>`;
            document.getElementById('reasonsList').appendChild(div);
        }
    }

    function sendConfess(){
        const text=document.getElementById('confessArea').value.trim();
        if(text===''){alert('Write something dulu la 🙈');return;}
        localStorage.setItem('confess',text);
        document.getElementById('confessAck').innerText='Confession saved locally 💌 (send screenshot to me hehe)';
    }

    window.addEventListener('load',()=>{
        const savedEssay=localStorage.getItem('essay');
        if(savedEssay){
            document.getElementById('essayText').innerHTML=escapeHtml(savedEssay);
        }
    });
</script>
</body>
</html>
