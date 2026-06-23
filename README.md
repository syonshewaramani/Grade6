# 🎓 Syon Grade 6 Quiz App

An interactive multiple-choice quiz app for Grade 6 students covering all NCERT subjects.

## 🌐 Live App

👉 [Click here to play the quiz](https://syonshewaramani.github.io/syon-grade6-quiz/Syon-Grade-6.html)

> Replace `YOUR-USERNAME` with your GitHub username after deployment.

---

## 📚 Subjects Covered

| Subject | Chapters |
|---|---|
| 🔬 Science | 12 Chapters |
| ➕ Mathematics | 10 Chapters |
| 🌍 Social Science | 14 Chapters |
| 📖 English Grammar | 10 Chapters |
| 📗 Gems English Reader | 3 Chapters |
| ✏️ Gems English Language Practice | 3 Chapters |
| 🇮🇳 Hindi | Multiple Chapters |
| 🕉️ Sanskrit | Multiple Chapters |

---

## 🎮 How to Play

1. Open the app link in any browser (mobile or desktop)
2. Select a **Subject** and **Chapter** from the dropdowns
3. Click **Start Game**
4. Answer 4-option MCQs — earn 1 point per correct answer
5. Reach **20 points** to win 🏆

---

## ✨ Features

- ✅ 50 questions per chapter
- ✅ Randomized question order
- ✅ Instant feedback on each answer
- ✅ Score tracker
- ✅ Victory screen at 20 points
- ✅ Works on phone and desktop
- ✅ No internet required after loading

---

## 📁 Files

| File | Description |
|---|---|
| `Syon-Grade-6.html` | Main quiz app (single file, open in browser) |
| `README.md` | This file |

---

## 🛠️ How to Update

1. Edit `Syon-Grade-6.html` to add/change questions or chapters
2. Go to your GitHub repository
3. Click **Add file → Upload files**
4. Re-upload the updated file
5. Click **Commit changes** — the live app updates automatically

---

## 👦 Made for

**Syon** — Grade 6 student  
School: GEMS Education  
Academic Year: 2025–26

---

## 📜 License

Free to use for personal and educational purposes.
# Grade6
<!DOCTYPE html>
<html lang="en" data-theme="light">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Syon-Grade 6</title>
<style>
:root{--bg:#f7f1e7;--card:#fffaf3;--line:#e5d8c7;--text:#241f1b;--muted:#756b61;--primary:#0f8b7a;--accent:#f4dca6;--soft:#eef6fb;--shadow:0 10px 28px rgba(56,44,25,.08);--radius:22px;--radius2:28px;--font:'Segoe UI',system-ui,sans-serif}
[data-theme=dark]{--bg:#161413;--card:#231f1c;--line:#3a342f;--text:#f4efe8;--muted:#b7aea0;--primary:#43c2ad;--accent:#5b4f2a;--soft:#1f2b31;--shadow:0 10px 30px rgba(0,0,0,.3)}
*{box-sizing:border-box}body{margin:0;font-family:var(--font);background:var(--bg);color:var(--text)}
.wrap{max-width:1220px;margin:0 auto;padding:18px}
.top{display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap}
.brand{display:flex;align-items:center;gap:12px}.logo{width:44px;height:44px;border-radius:14px;background:linear-gradient(135deg,#2c7be5,#7e59ff);display:grid;place-items:center;color:#fff;font-weight:800;font-size:1.4rem;box-shadow:var(--shadow)}
.brand h1{margin:0;font-size:clamp(1.6rem,2.6vw,2.4rem);line-height:1;font-weight:900}.brand p{margin:4px 0 0;color:var(--muted)}
.theme{border:1px solid var(--line);background:var(--card);color:var(--text);width:48px;height:48px;border-radius:999px;cursor:pointer;box-shadow:var(--shadow)}
.hero,.panel,.quiz,.setup,.result,.info{background:var(--card);border:1px solid var(--line);border-radius:var(--radius2);box-shadow:var(--shadow)}
.hero{padding:28px;margin-top:16px;display:grid;grid-template-columns:1.2fr .8fr;gap:20px;align-items:center}
.eyebrow{display:inline-block;background:linear-gradient(90deg,#fff0bf,#ffe7c7);padding:8px 12px;border-radius:999px;font-weight:800;color:#8f6510}
.hero h2{font-size:clamp(2rem,4vw,4rem);line-height:1.02;margin:14px 0 10px;font-weight:900}
.hero p{color:var(--muted);font-size:1.04rem;max-width:60ch}
.pills{display:flex;flex-wrap:wrap;gap:10px;margin-top:18px}
.pill{background:var(--soft);border:1px solid var(--line);padding:10px 14px;border-radius:999px;font-weight:700}
.art{min-height:250px;border-radius:24px;background:linear-gradient(135deg,#fff2cf,#eef7ff);position:relative;overflow:hidden}
.shape{position:absolute}
.s1{top:40px;left:80px;width:140px;height:4px;background:#1d8f82;transform:rotate(-18deg);border-radius:999px}
.s2{top:130px;left:60px;width:170px;height:4px;background:#4a84ff;border-radius:999px}
.s3{right:68px;top:78px;width:110px;height:110px;border-left:6px solid #f0b323;border-bottom:6px solid #f0b323;border-radius:16px;transform:rotate(20deg)}
.s3::after{content:'90°';position:absolute;left:22px;bottom:14px;font-size:1.5rem;font-weight:900;transform:rotate(-20deg)}
.grid{display:grid;grid-template-columns:320px 1fr;gap:18px;align-items:start;margin-top:18px}
.setup,.quiz{padding:18px}
.title{font-size:1.2rem;font-weight:900;margin:0 0 8px}
.muted{color:var(--muted);line-height:1.45}
.field{margin-top:14px}
label{display:block;font-weight:800;margin-bottom:7px}
select,input,button{font:inherit}
select,input{width:100%;padding:12px 13px;border-radius:12px;border:1px solid var(--line);background:transparent;color:var(--text)}
button{border:none;cursor:pointer;border-radius:999px;padding:12px 16px;font-weight:800}
.btn-primary{background:var(--primary);color:#fff}
.btn-soft{background:var(--soft);border:1px solid var(--line);color:var(--text)}
.btn-row{display:flex;gap:10px;flex-wrap:wrap;margin-top:14px}
.statrow{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:14px}
.stat{background:var(--soft);border:1px solid var(--line);border-radius:18px;padding:14px}
.stat span{display:block;color:var(--muted)}.stat strong{font-size:2rem;display:block;margin-top:2px}
.progressbox{display:flex;justify-content:space-between;align-items:center;gap:10px;margin-bottom:8px;font-weight:800}
.bar{height:13px;background:var(--soft);border:1px solid var(--line);border-radius:999px;overflow:hidden}
.bar>div{height:100%;width:0%;background:linear-gradient(90deg,var(--primary),#4a90ff);border-radius:inherit;transition:width .25s}
.quiz{min-height:260px}
.tag{display:inline-block;background:#fff0c2;border:1px solid #edd79b;color:#8f6510;padding:7px 12px;border-radius:999px;font-weight:800;margin-bottom:10px}
.qtext{font-size:clamp(1.2rem,1rem + 1vw,1.8rem);font-weight:900;line-height:1.25;margin:6px 0 16px}
.choices{display:grid;gap:10px}
.choice{background:var(--card);border:1px solid var(--line);border-radius:18px;padding:14px 16px;text-align:left;color:var(--text)}
.choice:hover{background:var(--soft)}
.choice.correct{background:#e8f7ee;border-color:#42b36e}
.choice.wrong{background:#ffe9ee;border-color:#ef5d79}
.feedback{display:none;margin-top:14px;padding:14px 16px;border-radius:18px;font-weight:800}
.feedback.show{display:block}
.feedback.ok{background:#e8f7ee;color:#1f7a42}
.feedback.bad{background:#ffe9ee;color:#b43d56}
.hidden{display:none}
.books{margin-top:18px;padding:18px}
.bookgrid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:12px}
.book{padding:14px;border:1px solid var(--line);border-radius:18px;background:var(--soft)}
.book h3{margin:0 0 8px;font-size:1.05rem}
.chapters{margin:0;padding-left:18px;color:var(--muted)}
.linkbox{margin-top:12px;padding:12px 14px;border-radius:14px;background:#fff8d7;border:1px solid #efd77c;color:#83600d;font-weight:700}
.result{display:none;padding:18px;margin-top:18px}
.result.show{display:block}
.scorebig{font-size:3rem;font-weight:900;line-height:1}
.small{font-size:.94rem;color:var(--muted)}
.loading{padding:14px;color:var(--muted);font-weight:700;text-align:center}
@media(max-width:940px){.hero,.grid{grid-template-columns:1fr}.art{min-height:220px}}
@media(max-width:640px){.wrap{padding:12px}.setup,.quiz,.hero,.books,.result{padding:14px}.btn-row{flex-direction:column}.btn-row button{width:100%}}
</style>
</head>
<body>
<div class="wrap">

  <div class="top">
    <div class="brand">
      <div class="logo">6</div>
      <div><h1>Syon-Grade 6</h1><p>Updated Grade 6 NCERT quiz app with all subjects</p></div>
    </div>
    <button class="theme" id="themeBtn">☾</button>
  </div>

  <section class="hero">
    <div>
      <div class="eyebrow">⭐ Syon-Grade 6 • Score 20 to win</div>
      <h2>Wrong answer? The game adds another question.</h2>
      <p>The quiz keeps going until the player reaches 20 points. Correct answers earn one point. Wrong answers highlight the right answer but give no point.</p>
      <div class="pills">
        <span class="pill">Game ends only at score 20</span>
        <span class="pill">Fresh random questions</span>
        <span class="pill">All Grade 6 books listed below</span>
      </div>
    </div>
    <div class="art" aria-hidden="true">
      <div class="shape s1"></div>
      <div class="shape s2"></div>
      <div class="shape s3"></div>
    </div>
  </section>

  <div class="grid">
    <aside class="setup">
      <div class="title">Game setup</div>
      <div class="muted">Choose a subject and a chapter. Questions load from your shared Google Drive folder.</div>
      <div class="field"><label>Subject</label><select id="subject"></select></div>
      <div class="field"><label>Chapter</label><select id="chapter"></select></div>
      <div class="statrow">
        <div class="stat"><span>Target score</span><strong>20</strong></div>
        <div class="stat"><span>Question pool</span><strong id="poolCount">—</strong></div>
      </div>
      <div class="btn-row">
        <button class="btn-primary" id="startBtn">Start game</button>
        <button class="btn-soft" id="shuffleBtn">Shuffle questions</button>
      </div>
      <div class="linkbox" id="statusBox">Loading index from Google Drive…</div>
    </aside>

    <main>
      <div class="panel" style="padding:14px 16px;margin-bottom:14px">
        <div class="progressbox">
          <span>Questions played: <span id="asked">0</span></span>
          <span>Score: <span id="score">0</span> / 20</span>
        </div>
        <div class="bar"><div id="progress"></div></div>
      </div>

      <section class="quiz">
        <div class="tag" id="qtag">Warm-up</div>
        <div class="qtext" id="qText">Press "Start game" to begin.</div>
        <div class="choices" id="choices"></div>
        <div class="feedback" id="feedback"></div>
        <div class="btn-row" style="margin-top:14px">
          <button class="btn-soft hidden" id="nextBtn">Next question</button>
          <button class="btn-soft hidden" id="restartBtn">Play again</button>
        </div>
      </section>

      <section class="result" id="resultBox">
        <div class="tag">🏆 Victory unlocked</div>
        <div class="scorebig" id="finalScore">20/20</div>
        <p class="muted" id="resultMsg">You reached the target score of 20. Amazing work!</p>
        <div class="btn-row" style="margin-top:14px">
          <button class="btn-primary" id="playAgainBtn">Play again</button>
        </div>
      </section>
    </main>
  </div>

  <section class="books">
    <div class="title">Loaded Grade 6 books</div>
    <div class="bookgrid" id="bookGrid"></div>
  </section>

</div>
<script>
const INDEX_URL = 'https://drive.google.com/uc?export=download&id=1frUnrKj0Da3nwqIgh8afSAi_FMRJ6xqL';
const bookData = {
  Mathematics:['Patterns in Mathematics','Lines and Angles','Number Play','Data Handling and Presentation','Prime Time','Perimeter and Area','Fractions','Playing with Constructions','Symmetry','The Other Side of Zero'],
  Science:['The Wonderful World of Science','Diversity in the Living World','Mindful Eating: A Path to a Healthy Body','Exploring Magnets','Measurement of Length and Motion','Materials Around Us','Temperature and Its Measurement','A Journey through States of Water','Methods of Separation in Everyday Life',"Living Creatures: Exploring Their Characteristics","Nature's Treasure",'Beyond Earth'],
  English:['English Reader','Grammar'],
  Hindi:['Pathan Vyakaran Sahitya Lekhan'],
  Sanskrit:['Sanskrit'],
  'Social Science':['Locating Places on the Earth','Oceans and Continents','Landforms and Life','Timeline and Sources of History','India, That Is Bharat','The Beginnings of Indian Civilization',"India's Cultural Roots","Unity in Diversity, or Many in the One",'Family and Community','Grassroots Democracy Part 1 Governance','Grassroots Democracy Part 2 Local Government in Rural Areas','Grassroots Democracy Part 3 Local Government in Urban Areas','The Value of Work','Economic Activities Around Us']
};

const subjectEl=document.getElementById('subject');
const chapterEl=document.getElementById('chapter');
const poolCountEl=document.getElementById('poolCount');
const askedEl=document.getElementById('asked');
const scoreEl=document.getElementById('score');
const progressEl=document.getElementById('progress');
const qTextEl=document.getElementById('qText');
const qtagEl=document.getElementById('qtag');
const choicesEl=document.getElementById('choices');
const feedbackEl=document.getElementById('feedback');
const nextBtn=document.getElementById('nextBtn');
const restartBtn=document.getElementById('restartBtn');
const resultBox=document.getElementById('resultBox');
const finalScoreEl=document.getElementById('finalScore');
const resultMsgEl=document.getElementById('resultMsg');
const bookGrid=document.getElementById('bookGrid');
const statusBox=document.getElementById('statusBox');
const themeBtn=document.getElementById('themeBtn');

let quizData={};
let current=[], wrongPool=[], currentQ=null, score=0, asked=0, locked=false;
const TARGET=20;
const cheers=['Great job! 🎉','Excellent! 🌟','Nice one! 👏','Super! 🚀','Brilliant! 💡','Keep going! 🔥','Perfect! ✅'];
const nudges=['Keep going, you can do it!','Try again — you are learning!','Stay focused, next one is yours!','One more try — you are improving!'];

function shuffle(arr){const a=[...arr];for(let i=a.length-1;i>0;i--){const j=Math.floor(Math.random()*(i+1));[a[i],a[j]]=[a[j],a[i]]}return a}
function pick(a){return a[Math.floor(Math.random()*a.length)]}
function normalizeUrl(u){const m=u.match(/\/file\/d\/([a-zA-Z0-9_-]+)/);return m?`https://drive.google.com/uc?export=download&id=${m[1]}`:u;}
function parseIndex(text){
  const map={};
  text.split(/\r?\n/).map(s=>s.trim()).filter(Boolean).forEach(line=>{
    if(line.startsWith('#'))return;
    const parts=line.split('|').map(s=>s.trim());
    if(parts.length<3)return;
    const[subject,chapter,url]=parts;
    map[subject]=map[subject]||{};
    map[subject][chapter]=url;
  });
  return map;
}
function parseQFile(text){
  const items=[];
  text.split(/\n\s*\n/).map(b=>b.trim()).filter(Boolean).forEach(block=>{
    const lines=block.split(/\r?\n/).map(s=>s.trim()).filter(Boolean);
    if(lines.length<6)return;
    const q=lines[0].replace(/^Q[:\-\d\.]+\s*/i,'').trim();
    const opts=lines.slice(1,5).map(x=>x.replace(/^[A-D][\).\-:]\s*/i,'').trim());
    const ansLine=lines[5].replace(/^Answer[:\-]\s*/i,'').trim();
    let a=0;const m=ansLine.match(/([A-D]|[1-4])/i);
    if(m){const v=m[1].toUpperCase();a=/[1-4]/.test(v)?Number(v)-1:'ABCD'.indexOf(v);}
    const e=lines.slice(6).join(' ');
    items.push({q,o:opts,a,e});
  });
  return items;
}
function currentPool(){return (quizData[subjectEl.value]&&quizData[subjectEl.value][chapterEl.value])||[];}
function updatePoolCount(){poolCountEl.textContent=currentPool().length||'—';}
function fillChapters(){
  chapterEl.innerHTML='';
  const chs=quizData[subjectEl.value]?Object.keys(quizData[subjectEl.value]):[];
  chs.forEach(c=>{const o=document.createElement('option');o.value=c;o.textContent=c;chapterEl.appendChild(o);});
  updatePoolCount();
}
function renderSubjects(){
  subjectEl.innerHTML='';
  Object.keys(quizData).forEach(s=>{const o=document.createElement('option');o.value=s;o.textContent=s;subjectEl.appendChild(o);});
  fillChapters();
}
function renderBooks(){
  bookGrid.innerHTML='';
  Object.entries(bookData).forEach(([sub,chs])=>{
    const d=document.createElement('div');d.className='book';
    d.innerHTML=`<h3>${sub}</h3><div class="small">${chs.length} chapters</div><ol class="chapters">${chs.map(c=>`<li>${c}</li>`).join('')}</ol>`;
    bookGrid.appendChild(d);
  });
}
function setProgress(){
  scoreEl.textContent=score;
  askedEl.textContent=asked;
  progressEl.style.width=`${Math.min(100,(score/TARGET)*100)}%`;
}
function showResult(){
  resultBox.classList.add('show');
  finalScoreEl.textContent=`${score}/${TARGET}`;
  resultMsgEl.textContent=`You reached the target score of 20 in ${asked} questions. Amazing work!`;
}
function drawQuestion(){
  if(score>=TARGET){showResult();return;}
  if(!current.length){
    if(wrongPool.length){current=shuffle(wrongPool);wrongPool=[];}
    else{showResult();return;}
  }
  currentQ=current.shift();locked=false;asked++;setProgress();
  qTagEl.textContent=`Q${asked}`;
  qTextEl.textContent=currentQ.q;
  feedbackEl.className='feedback';feedbackEl.textContent='';
  choicesEl.innerHTML='';
  nextBtn.classList.add('hidden');restartBtn.classList.add('hidden');
  currentQ.o.forEach((opt,i)=>{
    const btn=document.createElement('button');
    btn.className='choice';
    btn.textContent=`${String.fromCharCode(65+i)}. ${opt}`;
    btn.onclick=()=>answer(i,btn);
    choicesEl.appendChild(btn);
  });
}
function answer(i,btn){
  if(locked)return;locked=true;
  [...choicesEl.children].forEach(x=>x.disabled=true);
  const correctBtn=[...choicesEl.children][currentQ.a];
  if(i===currentQ.a){
    score++;btn.classList.add('correct');
    feedbackEl.className='feedback show ok';
    feedbackEl.textContent=`${pick(cheers)} ${currentQ.e||''}`;
  }else{
    btn.classList.add('wrong');correctBtn.classList.add('correct');
    wrongPool.push(currentQ);
    feedbackEl.className='feedback show bad';
    feedbackEl.textContent=`Correct answer: ${String.fromCharCode(65+currentQ.a)}. ${currentQ.e||''} ${pick(nudges)}`;
  }
  setProgress();
  if(score>=TARGET){showResult();restartBtn.classList.remove('hidden');}
  else{nextBtn.classList.remove('hidden');}
}
function startGame(){
  current=shuffle(currentPool());
  wrongPool=[];score=0;asked=0;
  resultBox.classList.remove('show');
  setProgress();
  if(!current.length){qTextEl.textContent='No questions loaded for this chapter. Please check your index file.';return;}
  drawQuestion();
}
const qTagEl=document.getElementById('qtag');
async function loadFromIndex(){
  statusBox.textContent='Loading questions from Google Drive…';
  try{
    const res=await fetch(INDEX_URL,{mode:'cors'});
    const text=await res.text();
    const index=parseIndex(text);
    const loaded={};
    for(const subject of Object.keys(index)){
      loaded[subject]={};
      for(const chapter of Object.keys(index[subject])){
        try{
          const fileUrl=normalizeUrl(index[subject][chapter]);
          const t=await(await fetch(fileUrl,{mode:'cors'})).text();
          loaded[subject][chapter]=parseQFile(t);
        }catch(e){loaded[subject][chapter]=[];}
      }
    }
    quizData=loaded;
    renderSubjects();
    updatePoolCount();
    statusBox.textContent='Questions loaded from Google Drive.';
  }catch(e){
    statusBox.textContent='Could not load index. Check that the index file is publicly shared.';
    console.error(e);
  }
}

document.getElementById('startBtn').onclick=startGame;
document.getElementById('shuffleBtn').onclick=()=>{current=shuffle(currentPool());startGame();};
document.getElementById('playAgainBtn').onclick=startGame;
nextBtn.onclick=drawQuestion;
restartBtn.onclick=startGame;
subjectEl.onchange=fillChapters;
chapterEl.onchange=updatePoolCount;
themeBtn.onclick=()=>{const t=document.documentElement.getAttribute('data-theme')==='dark'?'light':'dark';document.documentElement.setAttribute('data-theme',t);themeBtn.textContent=t==='dark'?'☀':'☾';};

renderBooks();
loadFromIndex();
</script>
</body>
</html>


NCERT Grade 6 Study Quiz
