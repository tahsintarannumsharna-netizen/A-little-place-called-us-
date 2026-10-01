# A-little-place-called-us-
a-little-place-called-us
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A Little Place Called Us ❤️</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=DM+Sans:wght@400;500;600&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    background:#11100f;
    color:#f3eee5;
    font-family:"DM Sans",sans-serif;
    overflow-x:hidden;
}

section{
    min-height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    padding:80px 7%;
    position:relative;
}

h1,h2,h3{
    font-family:"Cormorant Garamond",serif;
    font-weight:500;
}

button{
    font-family:"DM Sans",sans-serif;
}

.hero{
    text-align:center;
    background:
    linear-gradient(rgba(17,16,15,.55),rgba(17,16,15,.88)),
    url("https://images.unsplash.com/photo-1516589178581-6cd7833ae3b2?auto=format&fit=crop&w=2000&q=80")
    center/cover;
}

.hero-content{
    animation:fadeUp 1.5s ease forwards;
}

.eyebrow{
    letter-spacing:4px;
    font-size:11px;
    margin-bottom:25px;
    color:#c7b9a5;
}

.hero h1{
    font-size:clamp(55px,10vw,125px);
    line-height:.9;
    margin-bottom:25px;
}

.hero p{
    color:#d1c9bf;
    font-size:15px;
}

.btn{
    margin-top:35px;
    padding:14px 27px;
    border:1px solid rgba(243,238,229,.35);
    background:transparent;
    color:#f3eee5;
    cursor:pointer;
    letter-spacing:2px;
    font-size:11px;
    transition:.4s;
}

.btn:hover{
    background:#f3eee5;
    color:#11100f;
}

.intro{
    text-align:center;
}

.intro-content{
    max-width:800px;
}

.intro h2{
    font-size:clamp(45px,7vw,85px);
    line-height:1;
}

.intro p{
    margin-top:30px;
    color:#aaa198;
    line-height:1.8;
}

.timeline-section{
    display:block;
    padding-top:120px;
    padding-bottom:120px;
}

.section-title{
    text-align:center;
    margin-bottom:80px;
}

.section-title span{
    font-size:11px;
    letter-spacing:4px;
    color:#9f9386;
}

.section-title h2{
    font-size:clamp(50px,7vw,85px);
    margin-top:12px;
}

.timeline{
    max-width:900px;
    margin:auto;
    position:relative;
}

.timeline:before{
    content:"";
    position:absolute;
    left:50%;
    top:0;
    bottom:0;
    width:1px;
    background:#4b4540;
}

.timeline-item{
    width:50%;
    padding:30px 50px;
    position:relative;
}

.timeline-item:nth-child(odd){
    text-align:right;
}

.timeline-item:nth-child(even){
    margin-left:50%;
}

.timeline-item:after{
    content:"";
    position:absolute;
    width:9px;
    height:9px;
    background:#b8a997;
    border-radius:50%;
    top:42px;
}

.timeline-item:nth-child(odd):after{
    right:-5px;
}

.timeline-item:nth-child(even):after{
    left:-5px;
}

.date{
    font-size:11px;
    letter-spacing:3px;
    color:#9f9386;
}

.timeline-item h3{
    font-size:34px;
    margin:10px 0;
}

.timeline-item p{
    color:#aaa198;
    line-height:1.7;
}

.gallery-section{
    display:block;
}

.gallery{
    max-width:1000px;
    margin:auto;
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:30px;
}

.photo{
    background:#eee6da;
    padding:10px 10px 45px;
    color:#222;
    transform:rotate(-2deg);
    transition:.5s;
    cursor:pointer;
}

.photo:nth-child(2){
    transform:rotate(2deg);
}

.photo:nth-child(3){
    transform:rotate(-1deg);
}

.photo:nth-child(4){
    transform:rotate(2deg);
}

.photo:nth-child(5){
    transform:rotate(-3deg);
}

.photo:nth-child(6){
    transform:rotate(1deg);
}

.photo:hover{
    transform:rotate(0deg) translateY(-10px);
}

.photo img{
    width:100%;
    height:280px;
    object-fit:cover;
    display:block;
}

.photo p{
    font-family:"Cormorant Garamond",serif;
    font-size:20px;
    margin-top:12px;
}

.cards-section{
    display:block;
}

.cards{
    max-width:1000px;
    margin:auto;
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:18px;
}

.card{
    height:260px;
    perspective:1000px;
    cursor:pointer;
}

.card-inner{
    width:100%;
    height:100%;
    position:relative;
    transition:transform .7s;
    transform-style:preserve-3d;
}

.card.open .card-inner{
    transform:rotateY(180deg);
}

.card-front,
.card-back{
    position:absolute;
    inset:0;
    backface-visibility:hidden;
    border:1px solid #393531;
    padding:30px;
    display:flex;
    flex-direction:column;
    justify-content:center;
}

.card-front span{
    color:#8f8479;
    font-size:11px;
    letter-spacing:3px;
}

.card-front h3{
    font-size:32px;
    margin-top:15px;
}

.card-back{
    transform:rotateY(180deg);
    background:#1c1a18;
    color:#d8d0c5;
    line-height:1.7;
}

.compare{
    max-width:850px;
    margin:auto;
    width:100%;
}

.compare-row{
    display:grid;
    grid-template-columns:1fr 1fr;
    border-bottom:1px solid #37332f;
}

.compare-row div{
    padding:25px;
}

.compare-row div:first-child{
    border-right:1px solid #37332f;
}

.compare-label{
    color:#8f8479;
    font-size:10px;
    letter-spacing:3px;
    margin-bottom:7px;
}

.quiz{
    max-width:650px;
    width:100%;
    text-align:center;
}

.question{
    font-family:"Cormorant Garamond",serif;
    font-size:42px;
    margin-bottom:35px;
}

.answers{
    display:grid;
    gap:12px;
}

.answer{
    padding:17px;
    background:transparent;
    color:#eee8df;
    border:1px solid #403b36;
    cursor:pointer;
    transition:.3s;
}

.answer:hover{
    background:#27231f;
}

.quiz-result{
    margin-top:25px;
    min-height:25px;
    color:#b8a997;
}

.emotional{
    text-align:center;
}

.emotional-content{
    max-width:800px;
}

.emotional small{
    color:#8f8479;
    letter-spacing:3px;
    font-size:11px;
}

.emotional h2{
    font-size:clamp(45px,7vw,85px);
    line-height:1.05;
    margin:30px 0;
}

.emotional p{
    color:#aaa198;
    line-height:1.8;
}

.final{
    text-align:center;
    background:
    linear-gradient(rgba(17,16,15,.35),rgba(17,16,15,.9)),
    url("https://images.unsplash.com/photo-1518199266791-5375a83190b7?auto=format&fit=crop&w=2000&q=80")
    center/cover;
}

.final h2{
    font-size:clamp(55px,9vw,110px);
}

.final p{
    max-width:600px;
    margin:25px auto;
    line-height:1.8;
    color:#ddd4c8;
}

.song{
    margin-top:30px;
}

.easter{
    font-size:11px;
    color:#aaa198;
    margin-top:40px;
    letter-spacing:1px;
}

@keyframes fadeUp{
    from{
        opacity:0;
        transform:translateY(30px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

@media(max-width:700px){

    section{
        padding:70px 6%;
    }

    .timeline:before{
        left:8px;
    }

    .timeline-item,
    .timeline-item:nth-child(even){
        width:100%;
        margin-left:0;
        padding:30px 20px 30px 40px;
        text-align:left;
    }

    .timeline-item:nth-child(odd):after,
    .timeline-item:nth-child(even):after{
        left:4px;
        right:auto;
    }

    .gallery{
        grid-template-columns:1fr 1fr;
        gap:15px;
    }

    .photo img{
        height:190px;
    }

    .cards{
        grid-template-columns:1fr;
    }

    .compare-row div{
        padding:18px 12px;
    }

    .question{
        font-size:34px;
    }
}

@media(max-width:450px){

    .gallery{
        grid-template-columns:1fr;
        max-width:320px;
    }

    .photo img{
        height:300px;
    }
}
</style>
</head>

<body>

<section class="hero" id="home">
    <div class="hero-content">
        <div class="eyebrow">A LITTLE PLACE CALLED</div>
        <h1>US</h1>
        <p>Made for one very specific person.</p>
        <button class="btn" onclick="document.getElementById('intro').scrollIntoView()">ENTER →</button>
    </div>
</section>

<section class="intro" id="intro">
    <div class="intro-content">
        <h2>I could've bought you something.</h2>
        <p>
            But I wanted to make you something instead.
            <br><br>
            So… welcome to my little corner of the internet.
        </p>
        <button class="btn" onclick="document.getElementById('timeline').scrollIntoView()">KEEP GOING →</button>
    </div>
</section>

<section class="timeline-section" id="timeline">

    <div class="section-title">
        <span>OUR STORY</span>
        <h2>How We Got Here</h2>
    </div>

    <div class="timeline">

        <div class="timeline-item">
            <div class="date">[DATE]</div>
            <h3>The Beginning</h3>
            <p>This is where our story started.</p>
        </div>

        <div class="timeline-item">
            <div class="date">[DATE]</div>
            <h3>The First ___</h3>
            <p>Still don't know how you managed to make me this attached.</p>
        </div>

        <div class="timeline-item">
            <div class="date">[DATE]</div>
            <h3>That One Day</h3>
            <p>I wish I could put this day in a bottle.</p>
        </div>

        <div class="timeline-item">
            <div class="date">2026</div>
            <h3>Us, Now</h3>
            <p>And somehow, we're here.</p>
        </div>

    </div>

</section>

<section class="gallery-section">

    <div style="width:100%">

        <div class="section-title">
            <span>MEMORIES</span>
            <h2>A Few Of My Favourite People</h2>
            <p style="color:#aaa198;margin-top:15px">
                Okay fine. There's only one person here.
            </p>
        </div>

        <div class="gallery">

            <div class="photo">
                <img src="https://images.unsplash.com/photo-1516589178581-6cd7833ae3b2?auto=format&fit=crop&w=800&q=80">
                <p>You didn't know I took this.</p>
            </div>

            <div class="photo">
                <img src="https://images.unsplash.com/photo-1494774157365-9e04c6720e47?auto=format&fit=crop&w=800&q=80">
                <p>One of my favourite versions of us.</p>
            </div>

            <div class="photo">
                <img src="https://images.unsplash.com/photo-1522673607200-164d1b6ce486?auto=format&fit=crop&w=800&q=80">
                <p>You looked really good here. Annoying.</p>
            </div>

            <div class="photo">
                <img src="https://images.unsplash.com/photo-1506869640319-fe1a24fd76dc?auto=format&fit=crop&w=800&q=80">
                <p>I'd relive this day.</p>
            </div>

            <div class="photo">
                <img src="https://images.unsplash.com/photo-1501901609772-df0848060b33?auto=format&fit=crop&w=800&q=80">
                <p>This one makes me smile.</p>
            </div>

            <div class="photo">
                <img src="https://images.unsplash.com/photo-1529626455594-4ff0802cfb7e?auto=format&fit=crop&w=800&q=80">
                <p>Just us.</p>
            </div>

        </div>

    </div>

</section>

<section class="cards-section">

    <div style="width:100%">

        <div class="section-title">
            <span>JUST BECAUSE</span>
            <h2>Things I Probably Don't Say Enough</h2>
        </div>

        <div class="cards">

            <div class="card" onclick="this.classList.toggle('open')">
                <div class="card-inner">
                    <div class="card-front">
                        <span>01</span>
                        <h3>Your laugh.</h3>
                    </div>
                    <div class="card-back">
                        I don't think you realize how much I love hearing it.
                    </div>
                </div>
            </div>

            <div class="card" onclick="this.classList.toggle('open')">
                <div class="card-inner">
                    <div class="card-front">
                        <span>02</span>
                        <h3>The little things.</h3>
                    </div>
                    <div class="card-back">
                        The tiny things you remember mean more to me than you know.
                    </div>
                </div>
            </div>

            <div class="card" onclick="this.classList.toggle('open')">
                <div class="card-inner">
                    <div class="card-front">
                        <span>03</span>
                        <h3>Your jokes.</h3>
                    </div>
                    <div class="card-back">
                        Even the stupid ones. Especially the stupid ones.
                    </div>
                </div>
            </div>

            <div class="card" onclick="this.classList.toggle('open')">
                <div class="card-inner">
                    <div class="card-front">
                        <span>04</span>
                        <h3>How safe you feel.</h3>
                    </div>
                    <div class="card-back">
                        Being myself around you is one of my favourite things.
                    </div>
                </div>
            </div>

            <div class="card" onclick="this.classList.toggle('open')">
                <div class="card-inner">
                    <div class="card-front">
                        <span>05</span>
                        <h3>Ordinary days.</h3>
                    </div>
                    <div class="card-back">
                        Somehow, ordinary days feel different when you're there.
                    </div>
                </div>
            </div>

            <div class="card" onclick="this.classList.toggle('open')">
                <div class="card-inner">
                    <div class="card-front">
                        <span>06</span>
                        <h3>Just… you.</h3>
                    </div>
                    <div class="card-back">
                        I don't really know how else to explain it. I just love you.
                    </div>
                </div>
            </div>

        </div>

    </div>

</section>

<section>

    <div class="compare">

        <div class="section-title">
            <span>VERY SCIENTIFIC</span>
            <h2>Facts About Us</h2>
        </div>

        <div class="compare-row">
            <div>
                <div class="compare-label">ME</div>
                Overthinks everything.
            </div>
            <div>
                <div class="compare-label">YOU</div>
                “It's fine.”
            </div>
        </div>

        <div class="compare-row">
            <div>
                <div class="compare-label">ME</div>
                Says “I'm not hungry.”
            </div>
            <div>
                <div class="compare-label">YOU</div>
                Steals my food.
            </div>
        </div>

        <div class="compare-row">
            <div>
                <div class="compare-label">ME</div>
                Takes 300 photos.
            </div>
            <div>
                <div class="compare-label">YOU</div>
                Somehow looks good in all of them.
            </div>
        </div>

        <div class="compare-row">
            <div>
                <div class="compare-label">ME</div>
                “I'm going to sleep early.”
            </div>
            <div>
                <div class="compare-label">YOU</div>
                Starts another conversation.
            </div>
        </div>

    </div>

</section>

<section>

    <div class="quiz">

        <div class="section-title">
            <span>ONE LITTLE TEST</span>
            <h2>How Well Do You Know Us?</h2>
        </div>

        <div class="question" id="question">
            Where was our first date?
        </div>

        <div class="answers">
            <button class="answer" onclick="answer(false)">Somewhere random</button>
            <button class="answer" onclick="answer(true)">[CORRECT ANSWER]</button>
            <button class="answer" onclick="answer(false)">You forgot already?</button>
            <button class="answer" onclick="answer(false)">I'm not telling you</button>
        </div>

        <div class="quiz-result" id="result"></div>

        <button class="btn" onclick="document.getElementById('emotional').scrollIntoView()">
            ONE LAST THING →
        </button>

    </div>

</section>

<section class="emotional" id="emotional">

    <div class="emotional-content">

        <small>IF I COULD GIVE YOU ANYTHING…</small>

        <h2>
            I'd give you every ordinary day
            that somehow becomes special
            just because you're in it.
        </h2>

        <p>
            And I'd still choose you.
        </p>

    </div>

</section>

<section class="final">

    <div>

        <div class="eyebrow">FOR YOU</div>

        <h2>Happy Boyfriend Day,<br>[HIS NAME]</h2>

        <p>
            Thank you for being my person.
            For the stupid conversations.
            The random moments.
            The memories.
            And all the ones we haven't made yet.
        </p>

        <h2 style="font-size:55px">I love you. ❤️</h2>

        <button class="btn song" onclick="playSong()">
            PLAY OUR SONG ♫
        </button>

        <div class="easter">
            P.S. You can come back here whenever you miss me.
        </div>

    </div>

</section>

<audio id="song" loop>
    <source src="" type="audio/mpeg">
</audio>

<script>

function answer(correct){
    const result=document.getElementById("result");

    if(correct){
        result.innerHTML="Obviously. ❤️";
    }else{
        result.innerHTML="Excuse me??? We need to talk. 😭";
    }
}

function playSong(){
    const song=document.getElementById("song");

    if(song.src && song.src !== window.location.href){
        song.play();
    }else{
        alert("Add your song file/link first ❤️");
    }
}

</script>

</body>
</html>
