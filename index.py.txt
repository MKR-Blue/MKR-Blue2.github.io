```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Her Little World 💜</title>

<style>
*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

body{
    font-family: "Trebuchet MS", Arial, sans-serif;
    min-height:100vh;
    background:
        radial-gradient(circle at 20% 20%, #f0d9ff 0%, transparent 28%),
        radial-gradient(circle at 80% 80%, #dfc2ff 0%, transparent 30%),
        linear-gradient(135deg,#ead8ff,#f7eaff,#dfc8ff);
    color:#4d3265;
    overflow-x:hidden;
}

/* FLOATING FLOWERS */

.flower{
    position:fixed;
    font-size:25px;
    opacity:.55;
    pointer-events:none;
    animation:float 8s infinite ease-in-out;
    z-index:0;
}

.f1{left:5%;top:15%;}
.f2{left:90%;top:20%;animation-delay:2s;}
.f3{left:15%;top:80%;animation-delay:4s;}
.f4{left:80%;top:70%;animation-delay:1s;}
.f5{left:50%;top:8%;animation-delay:3s;}

@keyframes float{
    0%,100%{transform:translateY(0) rotate(0deg);}
    50%{transform:translateY(-25px) rotate(15deg);}
}

/* HEADER */

header{
    text-align:center;
    padding:35px 20px 20px;
    position:relative;
    z-index:2;
}

header h1{
    font-size:42px;
    color:#75469b;
}

header p{
    margin-top:8px;
    font-size:17px;
}

/* PROGRESS */

.progress-container{
    width:min(700px,90%);
    margin:20px auto;
    position:relative;
    z-index:2;
}

.progress-text{
    text-align:center;
    margin-bottom:8px;
    font-weight:bold;
}

.progress-bar{
    height:14px;
    background:#ffffff80;
    border-radius:20px;
    overflow:hidden;
}

.progress-fill{
    height:100%;
    width:0%;
    background:linear-gradient(90deg,#9b63c7,#d29cff);
    border-radius:20px;
    transition:.6s;
}

/* MAIN */

main{
    width:min(1000px,92%);
    margin:auto;
    position:relative;
    z-index:2;
}

/* HOME */

.home{
    text-align:center;
    padding:25px 0;
}

.home h2{
    font-size:30px;
    margin-bottom:10px;
}

.home p{
    max-width:650px;
    margin:0 auto 25px;
    line-height:1.6;
}

/* CARDS */

.cards{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:18px;
}

.card{
    background:#ffffffaa;
    backdrop-filter:blur(10px);
    border:1px solid #ffffff;
    border-radius:25px;
    padding:25px;
    cursor:pointer;
    transition:.3s;
    box-shadow:0 10px 25px #6c408020;
}

.card:hover{
    transform:translateY(-8px) scale(1.02);
    box-shadow:0 15px 30px #6c408035;
}

.card .icon{
    font-size:42px;
    margin-bottom:10px;
}

.card h3{
    margin-bottom:8px;
}

.card.done{
    border:2px solid #9b63c7;
}

.done-badge{
    margin-top:10px;
    font-size:14px;
    color:#80509e;
    font-weight:bold;
}

/* SECTIONS */

.section{
    display:none;
    padding:25px 0 50px;
}

.section.active{
    display:block;
}

.section-title{
    text-align:center;
    font-size:32px;
    margin-bottom:20px;
}

.game-box{
    max-width:650px;
    margin:20px auto;
    background:#ffffffb8;
    backdrop-filter:blur(12px);
    border-radius:28px;
    padding:30px;
    text-align:center;
    box-shadow:0 15px 35px #70459525;
}

button{
    border:none;
    border-radius:20px;
    padding:12px 22px;
    margin:7px;
    background:#8d55b5;
    color:white;
    font-size:15px;
    cursor:pointer;
    transition:.2s;
}

button:hover{
    transform:scale(1.05);
    background:#74429a;
}

button.secondary{
    background:#ffffff;
    color:#74429a;
    border:1px solid #cda8e7;
}

input{
    padding:13px 16px;
    border-radius:15px;
    border:2px solid #d6b9e8;
    outline:none;
    width:min(350px,90%);
    margin:10px;
    font-size:16px;
}

/* WORD SCRAMBLE */

.scramble-word{
    font-size:38px;
    font-weight:bold;
    letter-spacing:8px;
    margin:25px;
    color:#75469b;
}

.message{
    min-height:28px;
    margin:15px;
    font-weight:bold;
}

/* XO */

.xo-board{
    display:grid;
    grid-template-columns:repeat(3,90px);
    gap:8px;
    justify-content:center;
    margin:25px auto;
}

.xo-cell{
    width:90px;
    height:90px;
    background:#ffffff;
    border-radius:15px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:35px;
    cursor:pointer;
    color:#75469b;
    font-weight:bold;
}

/* BINGO */

.bingo-board{
    display:grid;
    grid-template-columns:repeat(5,55px);
    gap:6px;
    justify-content:center;
    margin:20px auto;
}

.bingo-cell{
    width:55px;
    height:55px;
    background:white;
    border-radius:10px;
    display:flex;
    align-items:center;
    justify-content:center;
    cursor:pointer;
    font-weight:bold;
}

.bingo-cell.selected{
    background:#b783d5;
    color:white;
}

/* FLAMES */

.flames-result{
    font-size:45px;
    font-weight:bold;
    color:#8a4daf;
    margin:25px;
}

.flames-description{
    line-height:1.7;
    max-width:550px;
    margin:auto;
}

/* FINAL */

.final-box{
    text-align:center;
    padding:50px 20px;
}

.lock{
    font-size:60px;
    margin-bottom:20px;
}

.final-message{
    display:none;
    animation:appear 1.5s ease;
}

.final-message h2{
    font-size:42px;
    color:#79459f;
    margin-bottom:20px;
}

.final-message p{
    font-size:20px;
    line-height:1.9;
    max-width:700px;
    margin:auto;
}

@keyframes appear{
    from{
        opacity:0;
        transform:translateY(30px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

/* BACK */

.back{
    display:block;
    margin:20px auto;
}

/* MOBILE */

@media(max-width:600px){

    header h1{
        font-size:32px;
    }

    .section-title{
        font-size:27px;
    }

    .xo-board{
        grid-template-columns:repeat(3,75px);
    }

    .xo-cell{
        width:75px;
        height:75px;
    }

    .scramble-word{
        font-size:28px;
    }

    .bingo-board{
        grid-template-columns:repeat(5,48px);
    }

    .bingo-cell{
        width:48px;
        height:48px;
    }
}
</style>
</head>

<body>

<!-- FLOATING DECORATIONS -->

<div class="flower f1">🌸</div>
<div class="flower f2">🌷</div>
<div class="flower f3">🌼</div>
<div class="flower f4">🌸</div>
<div class="flower f5">💜</div>

<header>
    <h1>your little world ♡</h1>
    <p>made with a ridiculous amount of love 💜</p>
</header>

<div class="progress-container">
    <div class="progress-text" id="progressText">
        0 / 5 discovered
    </div>

    <div class="progress-bar">
        <div class="progress-fill" id="progressFill"></div>
    </div>
</div>

<main>

<!-- HOME -->

<section id="home" class="section active">

    <div class="home">

        <h2>hey you ♡</h2>

        <p>
            There are five little things hidden around this place.
            Complete them all and maybe... just maybe...
            you'll find what's waiting at the end. 👀💜
        </p>

    </div>

    <div class="cards">

        <div class="card" onclick="openSection('scramble')" id="card-scramble">
            <div class="icon">🔤</div>
            <h3>Word Scramble</h3>
            <p>Unscramble the words.</p>
        </div>

        <div class="card" onclick="openSection('xo')" id="card-xo">
            <div class="icon">❌⭕</div>
            <h3>XO</h3>
            <p>Beat the little computer.</p>
        </div>

        <div class="card" onclick="openSection('bingo')" id="card-bingo">
            <div class="icon">🎯</div>
            <h3>Bingo</h3>
            <p>Complete a line.</p>
        </div>

        <div class="card" onclick="openSection('flames')" id="card-flames">
            <div class="icon">🔥</div>
            <h3>FLAMES</h3>
            <p>Okay... let's see what the ancient science says.</p>
        </div>

        <div class="card" onclick="openSection('happiness')" id="card-happiness">
            <div class="icon">☀️</div>
            <h3>Little Happiness</h3>
            <p>Click for a tiny surprise.</p>
        </div>

    </div>

</section>


<!-- WORD SCRAMBLE -->

<section id="scramble" class="section">

    <h2 class="section-title">🔤 Word Scramble</h2>

    <div class="game-box">

        <p>Unscramble this word:</p>

        <div class="scramble-word" id="scrambleWord"></div>

        <input
            type="text"
            id="scrambleInput"
            placeholder="your answer..."
        >

        <br>

        <button onclick="checkScramble()">Check ♡</button>
        <button class="secondary" onclick="scrambleHint()">Hint</button>

        <div class="message" id="scrambleMessage"></div>

        <p id="scrambleScore"></p>

    </div>

    <button class="back" onclick="goHome()">← Back to everything</button>

</section>


<!-- XO -->

<section id="xo" class="section">

    <h2 class="section-title">❌⭕ XO</h2>

    <div class="game-box">

        <p>You are X. Try to beat me 😌</p>

        <div class="xo-board" id="xoBoard"></div>

        <div class="message" id="xoMessage"></div>

        <button onclick="resetXO()">Play Again</button>

    </div>

    <button class="back" onclick="goHome()">← Back to everything</button>

</section>


<!-- BINGO -->

<section id="bingo" class="section">

    <h2 class="section-title">🎯 Mini Bingo</h2>

    <div class="game-box">

        <p>Click numbers and complete one full row, column or diagonal.</p>

        <div class="bingo-board" id="bingoBoard"></div>

        <div class="message" id="bingoMessage"></div>

        <button onclick="newBingo()">New Card</button>

    </div>

    <button class="back" onclick="goHome()">← Back to everything</button>

</section>


<!-- FLAMES -->

<section id="flames" class="section">

    <h2 class="section-title">🔥 FLAMES</h2>

    <div class="game-box">

        <p>
            Because apparently we're trusting a childhood
            game to determine everything. 😂
        </p>

        <input
            type="text"
            id="name1"
            placeholder="Your name"
        >

        <br>

        <input
            type="text"
            id="name2"
            placeholder="Her name"
        >

        <br>

        <button onclick="calculateFlames()">Reveal 🔥</button>

        <div class="flames-result" id="flamesResult"></div>

        <div class="flames-description" id="flamesDescription"></div>

    </div>

    <button class="back" onclick="goHome()">← Back to everything</button>

</section>


<!-- HAPPINESS -->

<section id="happiness" class="section">

    <h2 class="section-title">☀️ Little Happiness</h2>

    <div class="game-box">

        <p>
            Press the button whenever you need a tiny bit of happiness.
        </p>

        <div
            class="message"
            id="happinessMessage"
            style="font-size:20px;line-height:1.8;"
        >
        </div>

        <button onclick="newHappiness()">
            Give me one ♡
        </button>

    </div>

    <button class="back" onclick="goHome()">← Back to everything</button>

</section>


<!-- FINAL -->

<section id="final" class="section">

    <div class="final-box">

        <div id="finalLocked">

            <div class="lock">🔒</div>

            <h2>Not yettt 👀</h2>

            <p>
                There are still things left to discover.
            </p>

        </div>

        <div class="final-message" id="finalMessage">

            <div style="font-size:65px;">🌷💜🌸</div>

            <h2>okay... you found everything ♡</h2>

            <p>
                Happy Birthday to the person who somehow managed
                to become one of the most special parts of my life.
                <br><br>

                I hope today reminds you of just how loved,
                appreciated and important you are.
                <br><br>

                Thank you for all the little moments,
                the laughs, the conversations,
                the stupid jokes,
                and all the memories we've made.
                <br><br>

                I don't know what the future is going to look like,
                but I know I want to keep collecting little moments
                with you.
                <br><br>

                So here's to you,
                to your smile,
                to your dreams,
                and to another beautiful year of being you.
                <br><br>

                <strong>
                    Happy Birthday, you beautiful human. 💜
                </strong>
                <br><br>

                And yes...
                I made an entire website just for you.
                😂🌷
            </p>

        </div>

    </div>

    <button class="back" onclick="goHome()">← Back</button>

</section>

</main>


<script>

/* =========================================
   PROGRESS SYSTEM
========================================= */

let completed = JSON.parse(
    localStorage.getItem("birthdayCompleted") || "[]"
);

function saveProgress(){
    localStorage.setItem(
        "birthdayCompleted",
        JSON.stringify(completed)
    );

    updateProgress();
}

function markComplete(game){

    if(!completed.includes(game)){
        completed.push(game);
        saveProgress();
    }

    updateCards();
}

function updateProgress(){

    const count = completed.length;

    document.getElementById("progressText").innerText =
        count + " / 5 discovered";

    document.getElementById("progressFill").style.width =
        (count / 5 * 100) + "%";

    if(count >= 5){
        document.getElementById("finalLocked").style.display="none";
        document.getElementById("finalMessage").style.display="block";
    }
}

function updateCards(){

    completed.forEach(game => {

        const card =
            document.getElementById("card-" + game);

        if(card){

            card.classList.add("done");

            if(!card.querySelector(".done-badge")){

                const badge =
                    document.createElement("div");

                badge.className="done-badge";
                badge.innerText="✓ Completed ♡";

                card.appendChild(badge);
            }
        }
    });
}

function openSection(id){

    document.querySelectorAll(".section")
        .forEach(section =>
            section.classList.remove("active")
        );

    document.getElementById(id)
        .classList.add("active");

    window.scrollTo({
        top:0,
        behavior:"smooth"
    });
}

function goHome(){
    openSection("home");
}


/* =========================================
   WORD SCRAMBLE
========================================= */

const scrambleWords = [

    "LOVE",
    "SMILE",
    "HUG",
    "CUTE",
    "HEART",
    "FLOWER",
    "SUNSET",
    "FOREVER",
    "MEMORY",
    "DATE",
    "HAPPY",
    "DREAM",
    "SWEET",
    "TOGETHER"

];

let solvedWords =
    JSON.parse(
        localStorage.getItem("solvedScrambleWords") || "[]"
    );

let currentScramble = null;

function shuffleWord(word){

    let arr = word.split("");

    do{
        arr.sort(() => Math.random() - .5);
    }
    while(arr.join("") === word);

    return arr.join("");
}

function chooseScramble(){

    const remaining =
        scrambleWords.filter(
            word => !solvedWords.includes(word)
        );

    if(remaining.length === 0){

        document.getElementById("scrambleWord")
            .innerText="🎉 ALL DONE!";

        document.getElementById("scrambleMessage")
            .innerText=
            "You solved every word! 💜";

        markComplete("scramble");

        return;
    }

    currentScramble =
        remaining[
            Math.floor(Math.random()*remaining.length)
        ];

    document.getElementById("scrambleWord")
        .innerText=
        shuffleWord(currentScramble);

    document.getElementById("scrambleInput")
        .value="";

    document.getElementById("scrambleMessage")
        .innerText="";

    document.getElementById("scrambleScore")
        .innerText=
        "Solved: " +
        solvedWords.length +
        " / " +
        scrambleWords.length;
}

function checkScramble(){

    const answer =
        document.getElementById("scrambleInput")
        .value
        .trim()
        .toUpperCase();

    if(answer === currentScramble){

        if(!solvedWords.includes(currentScramble)){

            solvedWords.push(currentScramble);

            localStorage.setItem(
                "solvedScrambleWords",
                JSON.stringify(solvedWords)
            );
        }

        document.getElementById("scrambleMessage")
            .innerText=
            "YESSS! You got it! 💜✨";

        setTimeout(chooseScramble,900);

    }else{

        document.getElementById("scrambleMessage")
            .innerText=
            "Nopeee 😂 try again!";
    }
}

function scrambleHint(){

    if(!currentScramble) return;

    document.getElementById("scrambleMessage")
        .innerText=
        "Hint: starts with " +
        currentScramble[0] +
        " and has " +
        currentScramble.length +
        " letters 👀";
}


/* =========================================
   XO
========================================= */

let xoBoard;
let xoGameOver=false;

function initXO(){

    xoBoard=["","","","","","","","",""];
    xoGameOver=false;

    const board =
        document.getElementById("xoBoard");

    board.innerHTML="";

    xoBoard.forEach((cell,index)=>{

        const div=document.createElement("div");

        div.className="xo-cell";

        div.onclick=()=>playerMove(index);

        board.appendChild(div);
    });

    document.getElementById("xoMessage")
        .innerText="";
}

function playerMove(index){

    if(xoGameOver || xoBoard[index]) return;

    xoBoard[index]="X";

    renderXO();

    if(checkWinner("X")){

        xoGameOver=true;

        document.getElementById("xoMessage")
            .innerText=
            "WHATTT 😭 YOU WON!! 💜";

        markComplete("xo");

        return;
    }

    if(xoBoard.every(Boolean)){

        xoGameOver=true;

        document.getElementById("xoMessage")
            .innerText="Draw! 😭";

        markComplete("xo");

        return;
    }

    setTimeout(computerMove,400);
}

function computerMove(){

    if(xoGameOver)return;

    let available=
        xoBoard
        .map((v,i)=>v?null:i)
        .filter(v=>v!==null);

    let move=
        available[
            Math.floor(Math.random()*available.length)
        ];

    xoBoard[move]="O";

    renderXO();

    if(checkWinner("O")){

        xoGameOver=true;

        document.getElementById("xoMessage")
            .innerText=
            "hehe I win 😌";

        return;
    }

    if(xoBoard.every(Boolean)){

        xoGameOver=true;

        document.getElementById("xoMessage")
            .innerText="Draw!";

        markComplete("xo");
    }
}

function renderXO(){

    document
        .querySelectorAll(".xo-cell")
        .forEach((cell,index)=>{
            cell.innerText=xoBoard[index];
        });
}

function checkWinner(player){

    const wins=[
        [0,1,2],
        [3,4,5],
        [6,7,8],
        [0,3,6],
        [1,4,7],
        [2,5,8],
        [0,4,8],
        [2,4,6]
    ];

    return wins.some(
        combo =>
            combo.every(
                index => xoBoard[index]===player
            )
    );
}

function resetXO(){
    initXO();
}


/* =========================================
   BINGO
========================================= */

let bingoNumbers=[];

function newBingo(){

    bingoNumbers =
        Array.from(
            {length:25},
            (_,i)=>i+1
        );

    bingoNumbers.sort(
        ()=>Math.random()-.5
    );

    const board =
        document.getElementById("bingoBoard");

    board.innerHTML="";

    bingoNumbers.forEach((num,index)=>{

        const cell =
            document.createElement("div");

        cell.className="bingo-cell";

        cell.innerText=num;

        cell.onclick=()=>{
            cell.classList.toggle("selected");
            checkBingo();
        };

        board.appendChild(cell);
    });

    document.getElementById("bingoMessage")
        .innerText="";
}

function checkBingo(){

    const cells =
        [...document.querySelectorAll(".bingo-cell")];

    const selected =
        cells.map(
            cell=>cell.classList.contains("selected")
        );

    const lines=[

        [0,1,2,3,4],
        [5,6,7,8,9],
        [10,11,12,13,14],
        [15,16,17,18,19],
        [20,21,22,23,24],

        [0,5,10,15,20],
        [1,6,11,16,21],
        [2,7,12,17,22],
        [3,8,13,18,23],
        [4,9,14,19,24],

        [0,6,12,18,24],
        [4,8,12,16,20]

    ];

    const won =
        lines.some(
            line =>
                line.every(index=>selected[index])
        );

    if(won){

        document.getElementById("bingoMessage")
            .innerText=
            "BINGOOOO! 🎉💜";

        markComplete("bingo");
    }
}


/* =========================================
   FLAMES
========================================= */

function calculateFlames(){

    let a=
        document.getElementById("name1")
        .value
        .toLowerCase()
        .replace(/[^a-z]/g,"");

    let b=
        document.getElementById("name2")
        .value
        .toLowerCase()
        .replace(/[^a-z]/g,"");

    if(!a || !b){

        document.getElementById("flamesResult")
            .innerText="Enter both names 👀";

        return;
    }

    let arrA=a.split("");
    let arrB=b.split("");

    for(let i=arrA.length-1;i>=0;i--){

        let index=arrB.indexOf(arrA[i]);

        if(index!==-1){

            arrA.splice(i,1);
            arrB.splice(index,1);
        }
    }

    let count=arrA.length+arrB.length;

    let flames=["F","L","A","M","E","S"];

    let index=0;

    while(flames.length>1){

        index=
            (index+count-1)
            % flames.length;

        flames.splice(index,1);
    }

    let result=flames[0];

    const meanings={
        F:"Friends 🤝",
        L:"Love ❤️",
        A:"Affection 💜",
        M:"Marriage 💍",
        E:"Enemies 😂",
        S:"Siblings 😭"
    };

    document.getElementById("flamesResult")
        .innerText=result;

    document.getElementById("flamesDescription")
        .innerText=meanings[result];

    markComplete("flames");
}


/* =========================================
   LITTLE HAPPINESS
========================================= */

const happinessMessages=[

    "You are doing better than you think. 💜",

    "Go drink some water and come back. 😂",

    "I hope something unexpectedly nice happens to you today.",

    "Reminder: you deserve little happy moments too. 🌷",

    "Someone out there is probably smiling because of you.",

    "Today's mission: find something that makes you laugh.",

    "Take a deep breath. You're okay. ♡",

    "You make ordinary moments feel special.",

    "Go get yourself a little treat. You earned it. 🍰",

    "Just a reminder that you're very, very loved. 💜",

    "Smile. Yes, right now. I'm serious. 👀",

    "I hope your day becomes softer from here.",

    "Tiny happiness unlocked. ✨"

];

function newHappiness(){

    const message =
        happinessMessages[
            Math.floor(
                Math.random()*happinessMessages.length
            )
        ];

    document.getElementById("happinessMessage")
        .innerText=message;

    markComplete("happiness");
}


/* =========================================
   START
========================================= */

updateProgress();
updateCards();
chooseScramble();
initXO();
newBingo();

</script>

</body>
</html>
```
