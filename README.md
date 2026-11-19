
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#090909">

<title>SHIHAB | Personal Portfolio</title>

<style>
:root {
  --bg:#090909;
  --card:#121212;
  --red:#a00024;
  --text:#fff;
  --muted:#aaa;
  --border:#292929;
}

* {
  margin:0;
  padding:0;
  box-sizing:border-box;
  scroll-behavior:smooth;
}

body {
  background:var(--bg);
  color:var(--text);
  font-family:Arial,sans-serif;
  overflow-x:hidden;
}

a {
  text-decoration:none;
  color:inherit;
}

/* NAVIGATION */

nav {
  position:sticky;
  top:0;
  z-index:100;
  display:flex;
  justify-content:space-between;
  align-items:center;
  padding:18px 8%;
  background:rgba(9,9,9,.95);
  border-bottom:1px solid var(--border);
  backdrop-filter:blur(15px);
}

.logo {
  font-size:25px;
  font-weight:900;
  letter-spacing:3px;
}

.logo span {
  color:var(--red);
}

.nav-links {
  display:flex;
  align-items:center;
  gap:25px;
}

.nav-links a {
  font-size:13px;
  color:#bbb;
  transition:.3s;
}

.nav-links a:hover {
  color:#ff315b;
}

.controls {
  display:flex;
  gap:10px;
  align-items:center;
}

.control-btn {
  border:1px solid #444;
  color:white;
  background:#171717;
  padding:9px 12px;
  border-radius:5px;
  cursor:pointer;
}

.menu-btn {
  display:none;
}

/* HERO */

.hero {
  min-height:88vh;
  display:flex;
  justify-content:center;
  align-items:center;
  text-align:center;
  padding:30px 20px;
  position:relative;
  overflow:hidden;
}

.hero:before {
  content:"";
  position:absolute;
  width:350px;
  height:350px;
  background:var(--red);
  filter:blur(150px);
  opacity:.17;
  border-radius:50%;
}

.hero-content {
  position:relative;
}

.tag {
  display:inline-block;
  border:1px solid #70001d;
  color:#ff315b;
  padding:10px 18px;
  border-radius:30px;
  font-size:11px;
  letter-spacing:3px;
  margin-bottom:25px;
}

.hero h1 {
  font-size:clamp(65px,13vw,115px);
  font-weight:900;
  letter-spacing:5px;
}

.hero h1 span {
  color:var(--red);
}

.hero h2 {
  font-size:clamp(17px,3vw,23px);
  color:#bbb;
  margin-top:15px;
}

.hero p {
  max-width:520px;
  color:var(--muted);
  line-height:1.9;
  margin:20px auto;
}

.btn {
  display:inline-block;
  background:var(--red);
  color:white;
  padding:14px 27px;
  border-radius:5px;
  margin-top:15px;
  transition:.3s;
}

.btn:hover {
  background:#e00038;
  transform:translateY(-4px);
  box-shadow:0 8px 30px #a0002444;
}

/* SECTIONS */

section {
  padding:90px 9%;
}

.section-title {
  font-size:35px;
  margin-bottom:35px;
}

.section-title span {
  color:var(--red);
}

.about {
  background:#0e0e0e;
}

.about-content {
  max-width:800px;
  color:#aaa;
  line-height:2;
}

/* CARDS */

.cards {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:22px;
}

.card {
  background:var(--card);
  padding:28px;
  border:1px solid var(--border);
  border-radius:10px;
  transition:.35s;
}

.card:hover {
  transform:translateY(-8px);
  border-color:var(--red);
  box-shadow:0 10px 35px #a000241c;
}

.card .number {
  color:#ff315b;
  font-size:13px;
  margin-bottom:18px;
}

.card h3 {
  margin-bottom:13px;
}

.card p {
  color:#999;
  font-size:14px;
  line-height:1.8;
}

/* CONTACT & SOCIAL */

.contact {
  background:#101010;
  text-align:center;
}

.contact p {
  color:#999;
  margin-top:15px;
}

.socials {
  display:flex;
  justify-content:center;
  flex-wrap:wrap;
  gap:15px;
  margin-top:25px;
}

.socials a {
  border:1px solid #444;
  padding:13px 22px;
  border-radius:5px;
  color:#ccc;
  transition:.3s;
}

.socials a:hover {
  border-color:var(--red);
  color:white;
  transform:translateY(-4px);
}

.youtube:hover {
  background:#ff0033;
}

.facebook:hover {
  background:#1877f2;
}

/* FOOTER */

footer {
  padding:25px;
  text-align:center;
  color:#777;
  border-top:1px solid var(--border);
  font-size:13px;
}

footer span {
  color:var(--red);
}

/* BACK TO TOP */

#topBtn {
  position:fixed;
  bottom:25px;
  right:20px;
  display:none;
  border:0;
  border-radius:50%;
  width:45px;
  height:45px;
  background:var(--red);
  color:white;
  font-size:20px;
  cursor:pointer;
  z-index:50;
}

/* ANIMATION */

.reveal {
  opacity:0;
  transform:translateY(30px);
  transition:opacity .7s,transform .7s;
}

.reveal.show {
  opacity:1;
  transform:translateY(0);
}

/* MOBILE */

@media(max-width:700px) {

  nav {
    padding:16px 5%;
  }

  .menu-btn {
    display:block;
  }

  .nav-links {
    display:none;
    position:absolute;
    top:65px;
    left:0;
    width:100%;
    background:#101010;
    padding:25px;
    flex-direction:column;
    border-bottom:1px solid #333;
  }

  .nav-links.active {
    display:flex;
  }

  .hero {
    min-height:80vh;
  }

  section {
    padding:70px 7%;
  }

}
</style>
</head>

<body>

<!-- NAVIGATION -->

<nav>

  <div class="logo">SHIHAB<span>.</span></div>

  <div class="nav-links" id="navLinks">

    <a href="#home" data-en="Home" data-bn="হোম">Home</a>

    <a href="#about" data-en="About" data-bn="পরিচিতি">About</a>

    <a href="#skills" data-en="Interests" data-bn="আগ্রহ">Interests</a>

    <a href="#projects" data-en="Projects" data-bn="প্রজেক্ট">Projects</a>

    <a href="#contact" data-en="Contact" data-bn="যোগাযোগ">Contact</a>

  </div>

  <div class="controls">

    <button class="control-btn" id="langBtn">বাংলা</button>

    <button class="control-btn menu-btn" id="menuBtn">☰</button>

  </div>

</nav>

<!-- HOME -->

<header class="hero" id="home">

  <div class="hero-content">

    <div class="tag"
      data-en="WELCOME TO MY WORLD"
      data-bn="আমার জগতে স্বাগতম">
      WELCOME TO MY WORLD
    </div>

    <h1>SHIHAB<span>.</span></h1>

    <h2>
      <span id="typing">Gamer</span>
    </h2>

    <p
      data-en="Exploring technology, creating new things and building my own digital identity."
      data-bn="প্রযুক্তি অন্বেষণ, নতুন কিছু তৈরি এবং নিজের ডিজিটাল পরিচয় গড়ে তোলাই আমার লক্ষ্য।">
      Exploring technology, creating new things and building my own digital identity.
    </p>

    <a href="#about" class="btn"
      data-en="Explore More"
      data-bn="আরও জানুন">
      Explore More
    </a>

  </div>

</header>

<!-- ABOUT -->

<section class="about reveal" id="about">

  <h2 class="section-title">
    <span data-en="About" data-bn="আমার">About</span>
    <span data-en="Me" data-bn="পরিচিতি">Me</span>
  </h2>

  <p class="about-content"
    data-en="Hello! I am Shihab. I am interested in gaming, technology, digital creativity and learning new skills. I enjoy exploring ideas and turning them into reality."
    data-bn="আসসালামু আলাইকুম! আমি শিহাব। গেমিং, প্রযুক্তি, ডিজিটাল ক্রিয়েটিভিটি এবং নতুন দক্ষতা অর্জনে আমার আগ্রহ রয়েছে। নতুন ধারণা নিয়ে কাজ করতে এবং সেগুলো বাস্তবে রূপ দিতে ভালো লাগে।">

    Hello! I am Shihab. I am interested in gaming, technology, digital creativity and learning new skills.

  </p>

</section>

<!-- INTERESTS -->

<section id="skills" class="reveal">

  <h2 class="section-title">
    <span data-en="My" data-bn="আমার">My</span>
    <span data-en="Interests" data-bn="আগ্রহ">Interests</span>
  </h2>

  <div class="cards">

    <div class="card">

      <div class="number">01 / GAMING</div>

      <h3 data-en="Gaming & Esports"
          data-bn="গেমিং ও ই-স্পোর্টস">
        Gaming & Esports
      </h3>

      <p data-en="Competitive gaming and esports community."
         data-bn="প্রতিযোগিতামূলক গেমিং ও ই-স্পোর্টস কমিউনিটি।">
        Competitive gaming and esports community.
      </p>

    </div>

    <div class="card">

      <div class="number">02 / CREATIVE</div>

      <h3 data-en="Video Editing"
          data-bn="ভিডিও এডিটিং">
        Video Editing
      </h3>

      <p data-en="Creative editing, design and digital content."
         data-bn="সৃজনশীল এডিটিং, ডিজাইন ও ডিজিটাল কনটেন্ট।">
        Creative editing, design and digital content.
      </p>

    </div>

    <div class="card">

      <div class="number">03 / TECHNOLOGY</div>

      <h3 data-en="Technology"
          data-bn="প্রযুক্তি">
        Technology
      </h3>

      <p data-en="Computers, coding and modern technology."
         data-bn="কম্পিউটার, কোডিং ও আধুনিক প্রযুক্তি।">
        Computers, coding and modern technology.
      </p>

    </div>

  </div>

</section>

<!-- PROJECTS -->

<section id="projects" class="reveal">

  <h2 class="section-title">
    <span data-en="My" data-bn="আমার">My</span>
    <span data-en="Projects" data-bn="প্রজেক্ট">Projects</span>
  </h2>

  <div class="cards">

    <div class="card">

      <div class="number">PROJECT 01</div>

      <h3>Personal Portfolio</h3>

      <p data-en="My own digital identity and portfolio."
         data-bn="আমার নিজস্ব ডিজিটাল পরিচয় ও পোর্টফোলিও।">
        My own digital identity and portfolio.
      </p>

    </div>

    <div class="card">

      <div class="number">PROJECT 02</div>

      <h3>TEAM SLAYERS</h3>

      <p data-en="My esports team and gaming community."
         data-bn="আমার ই-স্পোর্টস টিম ও গেমিং কমিউনিটি।">
        My esports team and gaming community.
      </p>

    </div>

    <div class="card">

      <div class="number">PROJECT 03</div>

      <h3>Creative Works</h3>

      <p data-en="Experiments with design and technology."
         data-bn="ডিজাইন ও প্রযুক্তি নিয়ে বিভিন্ন সৃজনশীল কাজ।">
        Experiments with design and technology.
      </p>

    </div>

  </div>

</section>

<!-- CONTACT -->

<section class="contact reveal" id="contact">

  <h2 class="section-title"
      data-en="Let's Connect"
      data-bn="যোগাযোগ করুন">
    Let's Connect
  </h2>

  <p data-en="Follow me on social media."
     data-bn="সোশ্যাল মিডিয়ায় আমার সঙ্গে যুক্ত থাকুন।">
    Follow me on social media.
  </p>

  <div class="socials">

    <a class="youtube"
       href="https://youtube.com/@shihab5747"
       target="_blank"
       rel="noopener noreferrer">
      ▶ YouTube
    </a>

    <a class="facebook"
       href="https://www.facebook.com/share/1Dv9EyBxV7/"
       target="_blank"
       rel="noopener noreferrer">
      f Facebook
    </a>

  </div>

</section>

<!-- FOOTER -->

<footer>

  © 2026 <span>SHIHAB</span>.

  <span data-en="All Rights Reserved."
        data-bn="সর্বস্বত্ব সংরক্ষিত।">
    All Rights Reserved.
  </span>

</footer>

<button id="topBtn">↑</button>

<!-- JAVASCRIPT -->

<script>

// LANGUAGE SWITCHER

let language = "en";

document.getElementById("langBtn").onclick = function() {

  language = language === "en" ? "bn" : "en";

  document.querySelectorAll("[data-en]").forEach(element => {

    element.textContent = element.dataset[language];

  });

  document.documentElement.lang = language;

  this.textContent = language === "en" ? "বাংলা" : "English";

};

// TYPING ANIMATION

const words = {

  en:["Gamer","Creator","Tech Enthusiast"],

  bn:["গেমার","ক্রিয়েটর","প্রযুক্তিপ্রেমী"]

};

let wordIndex = 0;

setInterval(() => {

  const list = words[language];

  document.getElementById("typing").textContent =
    list[wordIndex % list.length];

  wordIndex++;

},2200);

// MOBILE MENU

document.getElementById("menuBtn").onclick = () => {

  document.getElementById("navLinks").classList.toggle("active");

};

document.querySelectorAll(".nav-links a").forEach(link => {

  link.onclick = () => {

    document.getElementById("navLinks").classList.remove("active");

  };

});

// SCROLL REVEAL

const observer = new IntersectionObserver(entries => {

  entries.forEach(entry => {

    if(entry.isIntersecting) {

      entry.target.classList.add("show");

    }

  });

},{threshold:0.12});

document.querySelectorAll(".reveal").forEach(el => {

  observer.observe(el);

});

// BACK TO TOP

const topBtn = document.getElementById("topBtn");

window.onscroll = () => {

  topBtn.style.display =
    window.scrollY > 400 ? "block" : "none";

};

topBtn.onclick = () => {

  window.scrollTo({
    top:0,
    behavior:"smooth"
  });

};

</script>

</body>
</html>
