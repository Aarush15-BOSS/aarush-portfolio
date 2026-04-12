<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Aurexis Labs — AI Product Studio</title>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

<link rel="icon" href="https://i.postimg.cc/ZnvffBCg/1dcdb7f7-de7b-48ae-920e-9869e990031b-7C361840-19A8-47AC-B944-81763F2E43D9.jpg">

<style>
:root{
--bg:#05070a;
--card:#0f1318;
--text:#f5f7fa;
--muted:#8b949e;
--border:#1f2630;
--accent:#5b7cff;
--glow:#5b7cff55;
}

*{margin:0;padding:0;box-sizing:border-box;font-family:'Inter',sans-serif;}

body{
background:radial-gradient(circle at 20% 20%, #111827, #05070a);
color:var(--text);
scroll-behavior:smooth;
}

/* NAV */
nav{
display:flex;
justify-content:space-between;
align-items:center;
padding:18px 50px;
background:rgba(5,7,10,0.7);
backdrop-filter:blur(10px);
border-bottom:1px solid var(--border);
position:sticky;
top:0;
z-index:1000;
}

.logo{
display:flex;
align-items:center;
gap:10px;
font-weight:600;
}

.logo img{
height:34px;
border-radius:10px;
}

.nav-links a{
margin-left:30px;
text-decoration:none;
color:var(--muted);
font-size:14px;
position:relative;
}

.nav-links a:hover{color:white}

/* HERO */
.hero{
text-align:center;
margin:120px auto;
max-width:900px;
animation:fadeUp 1s ease;
}

.hero-logo{
height:80px;
border-radius:16px;
margin-bottom:20px;
box-shadow:0 0 40px var(--glow);
animation:float 3s ease-in-out infinite;
}

.hero h1{
font-size:56px;
line-height:1.1;
}

.hero p{
margin-top:20px;
color:var(--muted);
font-size:18px;
}

/* BUTTON */
.btn{
display:inline-block;
margin-top:30px;
padding:14px 30px;
border-radius:10px;
background:var(--accent);
color:white;
text-decoration:none;
transition:0.3s;
}

.btn:hover{
transform:translateY(-4px);
box-shadow:0 10px 30px var(--glow);
}

/* SECTION */
section{
max-width:1000px;
margin:100px auto;
padding:0 20px;
opacity:0;
transform:translateY(50px);
transition:0.8s;
}

section.show{
opacity:1;
transform:translateY(0);
}

h2{
font-size:32px;
margin-bottom:10px;
}

.sub{
color:var(--muted);
margin-bottom:30px;
}

/* GRID */
.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
gap:20px;
}

/* CARD */
.card{
background:var(--card);
border:1px solid var(--border);
border-radius:14px;
padding:30px;
transition:0.3s;
}

.card:hover{
transform:translateY(-8px);
}

/* CASE STUDY */
.case{
display:grid;
grid-template-columns:1fr 1fr;
gap:30px;
margin-bottom:50px;
align-items:center;
}

.case img{
width:100%;
border-radius:14px;
}

.case-content p{
margin-top:10px;
color:var(--muted);
}

/* CTA */
.cta{
padding:60px;
border-radius:16px;
background:linear-gradient(135deg,#5b7cff,#3a5bff);
text-align:center;
}

/* GLASS */
.glass{
background:rgba(255,255,255,0.05);
border:1px solid rgba(255,255,255,0.1);
backdrop-filter:blur(14px);
border-radius:16px;
padding:30px;
}

/* FORM */
.contact input,.contact textarea{
width:100%;
padding:14px;
margin-top:12px;
border-radius:8px;
border:1px solid var(--border);
background:#0b0f14;
color:white;
}

/* FOOTER */
footer{
text-align:center;
padding:50px;
color:var(--muted);
border-top:1px solid var(--border);
margin-top:80px;
}

/* ANIMATIONS */
@keyframes fadeUp
from{opacity:0; transform:translateY(40px);}
to{opacity:1; transform:translateY(0);}
}

@keyframes float{
0%,100%{transform:translateY(0);}
50%{transform:translateY(-10px);}
}

/* MOBILE */
@media(max-width:768px){
.case{
grid-template-columns:1fr;
}
}
</style>
</head>

<body>

<nav>
<div class="logo">
<img src="https://i.postimg.cc/ZnvffBCg/1dcdb7f7-de7b-48ae-920e-9869e990031b-7C361840-19A8-47AC-B944-81763F2E43D9.jpg">
<span>Aurexis Labs</span>
</div>

<div class="nav-links">
<a href="#home">Home</a>
<a href="#about">About</a>
<a href="#portfolio">Work</a>
<a href="#pricing">Pricing</a>
<a href="#contact">Contact</a>
</div>
</nav>

<!-- HERO -->
<div class="hero" id="home">
<img class="hero-logo" src="https://i.postimg.cc/ZnvffBCg/1dcdb7f7-de7b-48ae-920e-9869e990031b-7C361840-19A8-47AC-B944-81763F2E43D9.jpg">
<h1>Build AI & Software That Wins</h1>
<p>We design and engineer high-performance digital systems.</p>
<a href="#contact" class="btn">Start Project</a>
</div>

<!-- ABOUT -->
<section id="about">
<h2>About</h2>
<div class="card">
Innovating the future of webs for a Connected World.<br>
Welcome to Innovating Aurexis Labs for a Connected World.<br>
Welcome to AurexisLabs. We are a forward-thinking technology company dedicated to building intelligent, scalable solutions for modern businesses. In a world where digital transformation is no longer optional, we provide the technical foundation that helps our partners thrive, scale, and lead in their respective industries.
<h2>Our Mission</h2>h2>
At AurexisLabs, our mission is simple: to empower businesses by turning complex technological challenges into intuitive, high-performance solutions. We believe that whether we are developing enterprise software, AI integrations, cloud infrastructure, the end result should always be seamless, secure, and built  scale.
<h2>The AurexisLabs Story</h2>
We started AurexisLabs in 2025 with a shared frustration: We were not able to attract companies and customers for tech reforming and were in a huge loss between the global giants like Microsoft, Google etc.<br>
We knew there had to be a smarter way. What began as a small team of passionate engineers has grown into a dedicated lab of innovators, developers, and problem-solvers. Today, we are proud to be the trusted technical engine behind  over 50+ startups, global enterprise clients and cutting-edge digital platforms. We are a forward-thinking technology company dedicated to building intelligent, scalable solutions for modern businesses. In a world where digital transformation is no longer optional, we provide the technical foundation that helps our partners thrive, scale, and lead in their respective industries.
</div>
</section>

<!-- SERVICES -->
<section>
<h2>Services</h2>
<div class="grid">
<div class="card">AI Systems</div>
<div class="card">Game Development</div>
<div class="card">Software Engineering</div>
</div>
</section>

<!-- CASE STUDIES -->
<section id="portfolio">
<h2>Case Studies</h2>
<p class="sub">Real systems. Real impact.</p>

<div class="case">
<img src="https://images.unsplash.com/photo-1677442136019-21780ecad995">
<div class="case-content">
<h3>AI Automation Platform</h3>
<p><strong>Problem:</strong> Manual workflows were slow.</p>
<p><strong>Solution:</strong> Built AI automation system.</p>
<p><strong>Result:</strong> 60% efficiency boost.</p>
</div>
</div>

<div class="case">
<img src="https://images.unsplash.com/photo-1606813907291-d86efa9b94db">
<div class="case-content">
<h3>3D Cricket Engine</h3>
<p><strong>Problem:</strong> Unrealistic gameplay.</p>
<p><strong>Solution:</strong> Custom physics engine.</p>
<p><strong>Result:</strong> Realistic gameplay.</p>
</div>
</div>

</section>

<!-- PRICING -->
<section id="pricing">
<h2>Pricing</h2>
<div class="grid">
<div class="card">Starter — ₹10,000+</div>
<div class="card">Professional — ₹50,000+</div>
<div class="card">Enterprise — Custom</div>
</div>
</section>

<!-- HIRE -->
<section>
<div class="cta">
<h2>Hire Us For Your Next Project</h2>
<a href="#contact" class="btn">Get Started</a>
</div>
</section>

<!-- CONTACT -->
<section id="contact">
<h2>Contact</h2>

<div class="glass">
<form class="contact" action="https://formspree.io/f/xjgepqwn" method="POST">
<input name="name" placeholder="Name" required>
<input name="email" placeholder="Email" required>
<textarea name="message" placeholder="Your idea" required></textarea>
<button class="btn">Send Message</button>
</form>

<p style="margin-top:20px;">
📱 <a href="tel:+917415072867" style="color:white;">+91 7415072867</a><br>
📸 <a href="https://instagram.com/aurexislabs" style="color:white;">@aurexislabs</a>
</p>
</div>
</section>

<footer>© 2026 Aurexis Labs</footer>

<script>
let sections=document.querySelectorAll("section");
window.addEventListener("scroll",()=>{
sections.forEach(sec=>{
if(sec.getBoundingClientRect().top < window.innerHeight-100){
sec.classList.add("show");
}
});
});
</script>

</body>
</html>
