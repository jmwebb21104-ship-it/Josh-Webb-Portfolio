<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Joshua Webb — Educator, Community Schools Leader & Program Designer</title>
<meta name="description" content="Joshua Webb is an educator, community schools leader, and program designer in North Carolina working to close achievement gaps across the classroom, extended learning, and educational access.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --cream:#fffcf2;
    --parchment:#f7f1e4;
    --beige:#ccc5b9;
    --beige-soft:#e3ddd0;
    --ink:#403d39;
    --charcoal:#252422;
    --ember:#eb5e28;
    --ember-deep:#c14a1c;
    --maxw:1120px;
  }
 
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;scroll-padding-top:76px;}
  body{
    margin:0;
    background:var(--cream);
    color:var(--ink);
    font-family:"Inter",system-ui,-apple-system,"Segoe UI",Roboto,sans-serif;
    font-size:1.0625rem;
    line-height:1.7;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3,h4{font-family:"Lora",Georgia,"Times New Roman",serif;color:var(--charcoal);line-height:1.15;margin:0;}
  p{margin:0 0 1rem;}
  a{color:inherit;}
  img{max-width:100%;}
 
  .wrap{max-width:var(--maxw);margin:0 auto;padding:0 clamp(1.25rem,5vw,3rem);}
 
  /* ---------- Nav ---------- */
  .nav{
    position:sticky;top:0;z-index:50;
    background:rgba(255,252,242,0.9);
    backdrop-filter:saturate(180%) blur(8px);
    border-bottom:1px solid var(--beige-soft);
  }
  .nav-inner{display:flex;align-items:center;justify-content:space-between;height:64px;}
  .brand{font-family:"Lora",serif;font-weight:600;font-size:1.15rem;color:var(--charcoal);text-decoration:none;letter-spacing:.01em;}
  .brand span{color:var(--ember);}
  .nav-links{display:flex;gap:1.9rem;align-items:center;}
  .nav-links a{
    text-decoration:none;color:var(--ink);font-size:.95rem;font-weight:500;
    padding:.25rem 0;position:relative;transition:color .2s;
  }
  .nav-links a::after{
    content:"";position:absolute;left:0;bottom:-2px;height:2px;width:0;background:var(--ember);transition:width .25s ease;
  }
  .nav-links a:hover,.nav-links a.active{color:var(--charcoal);}
  .nav-links a:hover::after,.nav-links a.active::after{width:100%;}
  .nav-toggle{display:none;background:none;border:0;cursor:pointer;padding:.4rem;}
  .nav-toggle span{display:block;width:24px;height:2px;background:var(--charcoal);margin:5px 0;transition:.25s;}
 
  /* ---------- Hero ---------- */
  .hero{padding:clamp(4rem,10vw,7.5rem) 0 clamp(3rem,7vw,5rem);}
  .hero-name{
    display:inline-flex;align-items:baseline;gap:.6rem;flex-wrap:wrap;
    font-size:1.05rem;font-weight:600;color:var(--ember-deep);margin-bottom:1.5rem;
  }
  .hero-name .pron{font-weight:500;color:var(--ink);font-size:.9rem;opacity:.8;}
  .hero h1{
    font-size:clamp(2.4rem,6vw,4.4rem);font-weight:600;max-width:19ch;letter-spacing:-0.015em;
  }
  .hero-lead{
    max-width:62ch;margin-top:1.75rem;font-size:1.15rem;color:var(--ink);
  }
  .hero-lead .accent{color:var(--charcoal);font-weight:600;}
  .hero-cta{display:flex;gap:1rem;flex-wrap:wrap;margin-top:2.25rem;}
  .btn{
    display:inline-block;text-decoration:none;font-weight:600;font-size:.98rem;
    padding:.85rem 1.6rem;border-radius:2px;transition:transform .15s ease, background .2s, color .2s;
  }
  .btn-primary{background:var(--ember);color:#fff;}
  .btn-primary:hover{background:var(--ember-deep);}
  .btn-ghost{background:transparent;color:var(--charcoal);border:1.5px solid var(--beige);}
  .btn-ghost:hover{border-color:var(--charcoal);}
  .hero-meta{margin-top:2.75rem;font-size:.95rem;color:var(--ink);opacity:.75;}
 
  /* ---------- Section scaffolding ---------- */
  section{padding:clamp(3.5rem,8vw,6rem) 0;}
  .band{background:var(--parchment);border-top:1px solid var(--beige-soft);border-bottom:1px solid var(--beige-soft);}
  .sec-head{max-width:58ch;margin-bottom:2.75rem;}
  .sec-kicker{font-size:.9rem;font-weight:600;color:var(--ember-deep);margin-bottom:.6rem;}
  .sec-head h2{font-size:clamp(1.9rem,3.6vw,2.7rem);font-weight:600;letter-spacing:-0.01em;}
  .sec-head p{margin-top:1rem;color:var(--ink);}
 
  /* ---------- About ---------- */
  .about-grid{display:grid;grid-template-columns:1.55fr 1fr;gap:clamp(2rem,5vw,4rem);align-items:start;}
  .about-grid p{max-width:64ch;}
  .photo{
    position:relative;width:100%;max-width:340px;aspect-ratio:1/1;border-radius:4px;overflow:hidden;
    background:var(--beige);border:1px solid var(--beige-soft);margin-bottom:1.75rem;
    display:flex;align-items:center;justify-content:center;
  }
  .photo-fallback{font-family:"Lora",serif;font-size:3.5rem;font-weight:600;color:var(--cream);letter-spacing:.05em;}
  .photo img{position:absolute;inset:0;width:100%;height:100%;object-fit:cover;}
  .quote{
    font-family:"Lora",serif;font-style:italic;font-size:1.35rem;line-height:1.4;color:var(--charcoal);
    border-left:3px solid var(--ember);padding:.25rem 0 .25rem 1.5rem;margin:0;
  }
  .quote cite{display:block;font-style:normal;font-family:"Inter",sans-serif;font-size:.9rem;color:var(--ink);opacity:.7;margin-top:1rem;font-weight:500;}
  .fastfacts{margin-top:2rem;border-top:1px solid var(--beige-soft);}
  .fastfacts div{display:flex;justify-content:space-between;gap:1rem;padding:.75rem 0;border-bottom:1px solid var(--beige-soft);font-size:.95rem;}
  .fastfacts dt{color:var(--ink);opacity:.75;}
  .fastfacts dd{margin:0;font-weight:600;color:var(--charcoal);text-align:right;}
 
  /* ---------- Focus areas ---------- */
  .focus-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:1px;background:var(--beige-soft);border:1px solid var(--beige-soft);}
  .focus-item{background:var(--cream);padding:clamp(1.5rem,3vw,2.25rem);}
  .band .focus-item{background:var(--parchment);}
  .focus-item h3{font-size:1.3rem;font-weight:600;margin-bottom:.35rem;}
  .focus-item .bar{width:34px;height:3px;background:var(--ember);margin-bottom:1rem;}
  .focus-item p{margin:0;font-size:1rem;color:var(--ink);}
 
  /* ---------- Experience timeline ---------- */
  .timeline{position:relative;margin-left:.5rem;}
  .tl-item{position:relative;padding:0 0 2.75rem 2.25rem;border-left:2px solid var(--beige-soft);}
  .tl-item:last-child{padding-bottom:0;}
  .tl-item::before{
    content:"";position:absolute;left:-8px;top:.3rem;width:14px;height:14px;border-radius:50%;
    background:var(--cream);border:3px solid var(--ember);
  }
  .band .tl-item::before{background:var(--parchment);}
  .tl-date{font-size:.85rem;font-weight:600;color:var(--ember-deep);letter-spacing:.01em;}
  .tl-item h3{font-size:1.3rem;font-weight:600;margin:.35rem 0 .15rem;}
  .tl-org{font-weight:500;color:var(--ink);margin-bottom:.85rem;}
  .tl-item ul{margin:0;padding-left:1.1rem;color:var(--ink);}
  .tl-item li{margin-bottom:.45rem;}
 
  /* ---------- Building / EDGE ---------- */
  .edge{background:var(--charcoal);color:var(--cream);border-radius:4px;padding:clamp(2rem,5vw,3.5rem);}
  .edge .tag{
    display:inline-block;font-size:.8rem;font-weight:600;letter-spacing:.02em;
    color:var(--cream);background:var(--ember);padding:.3rem .8rem;border-radius:2px;margin-bottom:1.5rem;
  }
  .edge h3{color:var(--cream);font-size:clamp(1.7rem,3.5vw,2.4rem);font-weight:600;max-width:20ch;}
  .edge p{color:#e8e2d6;max-width:64ch;margin-top:1.25rem;}
  .edge-programs{display:grid;grid-template-columns:repeat(2,1fr);gap:1.5rem;margin-top:2.25rem;}
  .edge-card{border:1px solid rgba(255,252,242,.18);border-radius:3px;padding:1.5rem;}
  .edge-card h4{color:var(--ember);font-size:1.15rem;margin-bottom:.4rem;}
  .edge-card p{color:#e8e2d6;margin:0;font-size:.97rem;}
 
  /* ---------- Writing ---------- */
  .writing-list{border-top:1px solid var(--beige-soft);}
  .writing-item{
    display:grid;grid-template-columns:1fr auto;gap:1rem 2rem;align-items:baseline;
    padding:1.4rem 0;border-bottom:1px solid var(--beige-soft);text-decoration:none;
  }
  .writing-item h3{font-size:1.2rem;font-weight:600;transition:color .2s;}
  .writing-item:hover h3{color:var(--ember-deep);}
  .writing-item .desc{grid-column:1;font-size:.97rem;color:var(--ink);opacity:.85;margin-top:.35rem;max-width:70ch;}
  .writing-item .src{font-size:.9rem;font-weight:600;color:var(--ember-deep);white-space:nowrap;}
 
  /* ---------- Education ---------- */
  .edu-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:1.5rem;}
  .edu-card{border:1px solid var(--beige-soft);border-radius:3px;padding:1.75rem;background:var(--cream);}
  .band .edu-card{background:var(--parchment);}
  .edu-card .yr{font-size:.85rem;font-weight:600;color:var(--ember-deep);}
  .edu-card h3{font-size:1.2rem;font-weight:600;margin:.4rem 0 .3rem;}
  .edu-card .inst{font-weight:600;color:var(--charcoal);}
  .edu-card p{font-size:.95rem;color:var(--ink);margin:.5rem 0 0;}
 
  /* ---------- Contact ---------- */
  .contact{text-align:center;}
  .contact h2{font-size:clamp(2rem,4.5vw,3rem);font-weight:600;max-width:20ch;margin:0 auto;}
  .contact p{max-width:54ch;margin:1.25rem auto 1.5rem;}
  .contact-links{display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;}
  .contact-details{margin-top:1.75rem;font-size:.95rem;color:var(--ink);opacity:.8;}
  .contact-details a{color:var(--ember-deep);font-weight:600;text-decoration:none;}
  .contact-details a:hover{text-decoration:underline;}
 
  footer{padding:2.5rem 0 3rem;border-top:1px solid var(--beige-soft);color:var(--ink);opacity:.7;font-size:.9rem;text-align:center;}
 
  /* ---------- Responsive ---------- */
  @media (max-width:820px){
    .nav-links{
      position:absolute;top:64px;left:0;right:0;flex-direction:column;gap:0;
      background:var(--cream);border-bottom:1px solid var(--beige-soft);
      max-height:0;overflow:hidden;transition:max-height .3s ease;
    }
    .nav-links.open{max-height:400px;}
    .nav-links a{padding:.9rem clamp(1.25rem,5vw,3rem);width:100%;border-top:1px solid var(--beige-soft);}
    .nav-links a::after{display:none;}
    .nav-toggle{display:block;}
    .about-grid{grid-template-columns:1fr;}
    .focus-grid{grid-template-columns:1fr;}
    .edge-programs{grid-template-columns:1fr;}
    .edu-grid{grid-template-columns:1fr;}
    .writing-item{grid-template-columns:1fr;}
    .writing-item .src{grid-column:1;}
  }
 
  @media (prefers-reduced-motion:reduce){
    html{scroll-behavior:auto;}
    *{transition:none!important;}
  }
  :focus-visible{outline:2px solid var(--ember);outline-offset:3px;}
</style>
</head>
<body>
 
<!-- ============ NAV ============ -->
<header class="nav">
  <div class="wrap nav-inner">
    <a href="#top" class="brand">Joshua <span>Webb</span></a>
    <button class="nav-toggle" aria-label="Toggle menu" aria-expanded="false">
      <span></span><span></span><span></span>
    </button>
    <nav class="nav-links">
      <a href="#about">About</a>
      <a href="#focus">Focus</a>
      <a href="#experience">Experience</a>
      <a href="#building">Building</a>
      <a href="#writing">Writing</a>
      <a href="#contact">Contact</a>
    </nav>
  </div>
</header>
 
<!-- ============ HERO (HOME) ============ -->
<section class="hero" id="top">
  <div class="wrap">
    <div class="hero-name">
      Joshua Webb <span class="pron">(he/him)</span>
    </div>
    <h1>A child's zip code should never decide how far their education can take them.</h1>
    <p class="hero-lead">
      I am an educator, community schools leader, and program designer working to change that across
      every place learning happens: <span class="accent">in the classroom, in the extended hours around it,
      and in the hands-on experiences that expand what students believe is possible.</span> Afterschool is
      one lever I pull to change the face of education. It is not the only one.
    </p>
    <div class="hero-cta">
      <a href="#experience" class="btn btn-primary">See my work</a>
      <a href="#contact" class="btn btn-ghost">Get in touch</a>
    </div>
    <p class="hero-meta">Based in Raleigh, North Carolina. Community School Site Director at Chapel Hill-Carrboro City Schools and graduate student at UNC Chapel Hill.</p>
  </div>
</section>
 
<!-- ============ ABOUT (PROFESSIONAL STATEMENT) ============ -->
<section class="band" id="about">
  <div class="wrap">
    <div class="sec-head">
      <p class="sec-kicker">About</p>
      <h2>Who I am, and how I work</h2>
    </div>
    <div class="about-grid">
      <div>
        <p>
          I am an educator, community schools leader, and program designer, and across more than seven years
          in classrooms and youth programs I have worked to make public education more equitable, one student
          and one program at a time. My work lives at the intersection of three settings that too often operate
          in isolation: the classroom, the extended hours that surround it, and the community spaces where
          students first encounter what is possible for their lives. I do not see these as separate worlds. I
          see them as connected levers, and I have built my career learning how to pull them together.
        </p>
        <p>
          In practice, that means I teach, I design, and I lead. I have taught middle grades English and social
          studies in Wake and Edgecombe County classrooms, coordinated year-round enrichment at the Alexander
          Family YMCA, and directed a municipal summer camp for the City of Raleigh. Today I lead a K&ndash;5
          community schools site for Chapel Hill-Carrboro City Schools, where I build programming that bridges
          the school day and the home, and as a graduate Education Innovation intern with Goodwill Industries of
          Eastern North Carolina, I design hands-on literacy tools that put high-quality reading support into
          the communities that need it most. Earlier, as a policy research assistant with the Public School
          Forum of North Carolina, I helped advocate for over a million dollars in funding and contributed to
          briefs that inform reform at the state level.
        </p>
        <p>
          I approach every one of these roles through an equity-centered, data-informed, and justice-driven
          lens. I start by listening: sitting in classrooms, learning what teachers want to see grow in their
          students, and letting real needs shape what I build rather than the other way around. I design
          programs that add genuine learning time rather than simply filling hours, I measure what I do so that
          I can improve it, and I hold myself and my teams accountable to outcomes, not just intentions. Above
          all, I work to create spaces where every student is known, supported, and given a real reason to
          believe in their own future.
        </p>
        <p>
          I am building toward a career at the systems level of education, where I can shape how out-of-school
          learning and in-school instruction reinforce one another to close achievement gaps. My graduate
          research explores how high-quality curriculum for extended learning can raise outcomes for the
          students who are furthest from opportunity, and it is laying the groundwork for a model I am
          developing to serve K&ndash;8 students in the community where I grew up. This is the throughline of
          everything I do: I want to help build an education system where a student's possibilities are defined
          by their potential, not by their circumstances, and I am pursuing that goal from every angle the work
          allows.
        </p>
      </div>
      <div>
        <div class="photo">
          <span class="photo-fallback">JW</span>
          <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5Ojf/2wBDAQoKCg0MDRoPDxo3JR8lNzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzf/wAARCAEsASwDASIAAhEBAxEB/8QAGwAAAgMBAQEAAAAAAAAAAAAAAwQBAgUGAAf/xAA6EAACAgEDAwMCBAQGAgEFAQABAgADEQQSIQUxQRMiUWFxBhQygSORodEzQlKxwfBi4XIVJTRDU/H/xAAaAQACAwEBAAAAAAAAAAAAAAABAwACBAUG/8QAKREAAgICAgICAwACAgMAAAAAAAECEQMhEjEEQRMiBVFhMkIUI3Gx0f/aAAwDAQACEQMRAD8AyvzLPgcgfeQcg55l6NG1lYYFj9hxDHTt6ZyCSPOe0ZJxXQqmLVak1Z7wFj+tYWIlX4Y4g+RLqC7BYev2tnxNFbR6GVwX7zNqOTg4h1YVggngzPljZdMbq1OV2OeftLWVlMP2ihrLsrrniH1xst0o2Aj5meUUmqLDOk1dbk7mBx4hq7FS4MvCnxMFqb6ApUZJ8fE0On12uP4oPPbmKy44pckyyb6NR9trkFvbMnWuaLcI3tjvoWAk7iYKzT+ofdxiIi1F/wAC9oL065WT9R3fePNaxABGR8zCUrVadseGuIqAI5lMkN2iJmgtKAewcmI3owLDyIXSPYXDA5zDWaawksR3lIz4OmX7RmUraWOe0YqBWwbu0tYWpGCIP1T3Ij+TewHRdK1ldLgMOJ1entS1AUInzdb8DcD2nRfh3XXWDaQ23PE6PieTJv42jPlxqrOs8z0HWr5yxhZ0mZCJ6TIgIekSZ6QJE9JxPSEInpMjI8mEhMiTPQEPT09iekIenp6TCQiBv/UPtDQN/wCofaAiPnlNYrrA45HbMDqk3IQoXJ8AyvrWbQCAFx4HeeqvVBmxe85VSWzc2jM1OidF3Ac/ETNZJ7Ym9fqVs4WvAx3zM6xkqfcQcfWPhkk1sW0heuoqCWHEqUZ24h9RZur3YOJTS3Iv6/5SNurJRo6GrCYPP2jyoldTMy4x8zKr1oW3aqYEa/MCzgjg+DMOSMrtjE0L06gX6liVGB2zC3awINq4EU1j10/oxkwGmJvJAELgn9vRLNfQajLneciE11qg+3tM9dLYq4rY7oDWJqKADacj4+InhFy0w26DNszvB5lL7C7oqfviIVXFrNvPM1tDWrNjHMtOPDbJ2aNTinTgjuBGKdcXqAByYtsDkVxunS01cZ5mGfH2MVi+rfeORzB1aVrRjHEeY11N7lyJA1qK2FAllkaVRQaXsGNEmmH8TkToOjMhUbAABMe9ntqyRkQei1llANaZEb42d4p82UnHkqO7puVjtB7Q84jQa22nU77XJBPzOs0muqvUbWGZ3/H8hZ1a0zHkx8GNz0rvXHeIarq1GnO1jzHvW2KSNHE9M/R9Tq1Ck5xj5iHUOvV6ZmQEEj4ktVd6DxfRtm1A20sMxfX61NJSbGIwBOJv6tqL7xYrFcSep6y2/TDdZn6TM/Lx7rtDFiZ0Gk/ENV7MvY+JnarrOor1vH+HOYousrsDDPE0LdZ66gbefmJXluUabpjPiSZ1XTeuJqLRW3Bm6pDAEGfO6R6G2zdz34mrT1nU0lSylq/maceVtffsXPHvR2E9FtLqhbSrnjIzGAyt2OY+hRM9PT0BD0DcPcPtDQN/6h9pAnzVbAagWIzjjEBqFLoQlXuPky6BaQHQDt5jKF7lz8+cTlN8do2pWY9RNbFGwCO8V1l3qPgcgRvqtK1Hdk5J5iCqCPbNMGmuRR/ou14ara3AEFURuBlrE/h9oKtckYPMOqDQ+jrWC7DnxCUubP4hGB4gXqJoOTzjtKo7LTtJEzTS9F+gusWtkLZGYLRj0gXYYU9jmJWOd5y3EIXe9Qg4EDg0qAdBpWQrvB5+CYvrq31fAMz9PbZW4pBBB+ZqpXaB7e5mOUeErsstgdBo6q/bYMsfM0U03pPvQYBl6NMxTdj3ywrvFmbD7fiZpzcndl0gTOgcswIP1iQ6gX1JTPA8mO6rT+v+niJDp5RiT/QQwUa2VdsZbWqTg8iVttqwGB7TL1B9E5V9wJ4GOZdWDVnnP0EcsGrQTb0nUltxUgyAJFr7LeRjMQ6eUqGeAfEbNyXPgkcYzzKLFUtIK62Wcue3MZo1VlGCrEGDpZHVXQ+0z16KD8GBtxf10Ro1dF10o2Lmz+89f1XR3WHIGfrOauqPqZDcReyh1JYOZ08HmyjGp7M8sSb0bmp6mleRQcfaI2WhzuY5MQKs1f1EmhjnDxWbJKT5F1Ch1Lh4Eux3rErSa1JQQulS+6vd4ivh5q4hCCsDvJVRiEs0t6Vh2HECW2jmUljnHsgZbh6WxgSfEe0Vz0qDcuUEzFsVuB3hPWtsIr/y/M14s769lXE19b1zdWEoypEno3XbVuxqCSvjMytRUKlDHGD3gmZdmVwI2WfKpcmV4Rqj6BouqVamwqrCaA5ny2jV203BqbDkTtukdXWyhfWPumrBn+XTVMTPHx6N2Av/AFD7QlVqWjKkGUv/AFD7R7FnyF3cldzHE0KtSPR2VMT8zKTV5qwyDOO8P01mySVOPmc3Ivrv0bUB6k5cY2nA8mK6Z60B9TOYx1TVM1mwJgCZj2ZbmMhbhQOmPXXB6zxxFULBht7yUsBwJ53CH24g60R7G/UbhTJurIUE9vM9p1rKb7H5EYAS6ohGyRM0p0y9CF1asMjsIKoMTkZjTaG41tgy/TNqMUcZYQudRbWyUAp313hnBA+s19PqyWAyAJa5UsG0qBAtoRXXuVplnOM1siRq/nFpXG7mCGvy21zwZgvb/E2uxG2Dv1WCuGxwewyfpKx8bkHZvarVDAFbBfuZlXdUssVRSSF888t9oh67uCfVUlQWyeBj4+8AgYVbq0GTj+IG7TZi8aMNvYRl9TuVrK3NlmcnIxxiTp2t3bQmWc9y2Rn/AKJmbihJKjH04PeHoub0iqEhv1KD/wB+80UCxh7N6ks7MM+1kbOO3HEMuqavB4JPtPgxGp/UI2B1XsQp89oO1nUsGXPJByeQYaJZu0dXsoPoOhyAOMYx/wBMOOqc2LchDA4DA5yZzlOpZCGdgzgYy+W4+IdScgJZmwc57845+xlHji/QbOmfmvebF75Cjk//AOQSEuoBGSeeJh/mdRVXWy7GwQysxDMB4mrouoV1Vq9tbkMMAoc4x9PMW8SXZHXobBAzkYEEzV7jjvDF0tsc18gec9/rKmqse4d5lcqdMHJgwXdSMQmm1FlS7ewEsjgCVwLQQO8vGVdA7HreoG6pasxewEeMwFeK+D3+Z42OLOOQY5zjJfZg6KI2XPGI2tu1YtaSvOO8mo7q8nvEN3tMjC3XNam0mLuSlZHOIG+0owwDiES4OnMMHK17JSI0qrvBzzmdQukKaEXI+TjOJywUI42Akk+JrevfRSEdm2nxNuL63yQuSvo0+kdVtruCMSVJnWlw6q2e4nz3SWObwUXPnInUUa9RSgsbDAc5mjBJuNSF5I70cInTQiBrLM8DtDU1shyjeyRpg1yhGbgCeo3V6o15yJypTbu2aUA1+hNwNgOJhGpwW9pxnuZ2lu0Jhxj6TL6lpXtr20qAvzLYvIa0wuJzbgJjnMr6niTqKHpYhgcwKEbxu7Zm1NNWLHKN1iFQCTNLSaazSVhu7HxHejaOhqwykE4jjtWHIK/pnPyeRbcUhiWrB6dHakmwcnxFPyvp6gNnbH/zIcfwx2lHza43D+UTzf8A4LaYO6ympCWbJ8QlDJdVljhRzzA6rS12YB7CJX2kMaKzhQMkjwJFBTVIDBdT9FrA1TjvjI8xEacXVGyy4KpOAHPcY7/8QGrsZrsAnk/pE86vt2Aq2Rxk8CdKEOEUgA73CqqIDjAJzIqcqCG3AfHeSijfswLHxjcO0pY2xn3IUsB/TjgS4A4RWYPb+nGcecYnmalRtQEng4Px9IkbC7cNgE5xCkL6iBAC5ODzwftJYSA4fvkEdgR3jANeVUbeByzDz/aUupUNhSWf/wAew+mYL03dXZQdqDLZkB0WsAZ/4ZTgdhxmWNjoCCMHyIXS1ULU9+otxjsg/U5+mePiU1tS0emwyy2KHBHHeSw1qy2lvQOhI2kEjKnj6cfGe8NVZYhYbwGYYPkHPxM+vG5cgjBzgeYxTZW+/wBV2D8bD/f/AHkIjX0WqSp0qfIyTk57H7TT9XdUOCCe6t3BmDqEVSjpf61pzuY9xiMaTWMrBXOasd2OSPrE5MaktEaNBGcvg9oyNoX2nmKq+5SVwcjxPUWFCfUmSUWVoIpJY74Ws5HErvBJ9sGLkrYwU2iUMMpIyYJHIJGJL6pdmYjfqiCFHGZeEOSog622wYIEEhRcqRiVpBChiZvdC6ZVrS4sHOI7BjfPgvYJPirM7p16C3IQuQY5qrbNW6qaWVRxmMabpT6LXPQiZDHIP0nSW6SnSdPLWhd2J1I46jTYhz3ZzFSHRsCnIIgr72ss3DiMu6X1NtPuiAouYZwZklGcv8doZa9gXxQRsGBjmB06+tqyyPzGNQv5hgqkdovVpLdLaXz3nLUo1vs0UrNKyjevL+6eFFhTbn957TgHBcnJh72VMYaJk2tIt6MPrPTgK94Pbmcq4JswPmdnrnaxCCDt/wB5yl1B9ZthwPrNvizdUxTVjvSdU9LlFPceZuaV3t3eoowfOJznTNPadQSBn6zqKeK8A8mU8hJOyyWtgEX07iF7S1960nI8xha1XJbzK/l6bASTzMvJXsgnqDa9W9TiY2t1BVAosww74P8A3E2dVYa/4S4xObuK26i1yvsTkibfFSeyMihWsbap3WudvP8AeV1LKAlKH3ofcTxz/wCoubvScNUdrA59vgytWbbsjJJ+fJmyyLehjUXis7dOAFKjk8kHHP8AWDq99T7yd2Pb94907pWo1pb0UO1e7ePtOt6T+Dxea/zSiusfqVDlm+5/tEzzxjo1Y/GlJX6OT6Z0a7VqW4rUj2mwEBv3jFv4c1yVoUqYrZ2Crk5+J9d0+i09VS1BFCKAFH0HaOVaRM7igJ8H4mb58jdof8WGKpo+T0/hLU1InquVsdd2VGdv0x/zM/V9L1fTOoJUis5x7cpkNkeB5n2r8mNxOBznv4kXdOrcKxqQkDgleRDHJk7A44Hqj4tqvw9r3oNlOndqawSWIwfr/wB+kBoNPqNfUNJVS1jV8rYWwEBPJP0n2htGlVbBVAU8bQOMTmx+FNJRqzbXW+Scqd3C/tLLyJLsn/Hxyf1Pm3Uem3aL07LqwUcYXB/75iuprK1paQo9Qdl4A8Yn0j8U9AtuC6zSB7La0KbB3+4E4bWdI1Gm0YvurYBG2lWGOY3FmUlvsTm8dptx6EKTtAY7z5G09xGAV9qG0jeASe+B/eIkFsY7jwfAjVjKq0qxDWKSCQ+Y+zKjT0F7DIbAAJAJIGcTQ/UwbxMTSozsm4+wHcY9ZewrJETkjb0Rmp69YXxAakVvWGER07bkO894wVzQRE8eLKbLOA1QCxDWMSPb3Ed0t1YU1sefrEtbS9TF1OVMbik42gNEU6q3ABHAnQdN6tdokFqYPyJy6WOeAJo6ItaVrc4XPMatS5AavR2FHWLtQReKjkfSC1nW314NJyPGJs9GTSJ07b7d2OZgaqhfzJehRnceZsyRnxu7FRauh7oPTH/MhriCmO06S2jSoQoVeBONTrN2ls2k5Ik39YvtcNyMiLx58eOPGKZHjbdmJ0nUFrMk8TYsK3DIbtOX/j0nfWPafEYOovVQUySe4E42THydo1J0a9eqRXZT4hDarHeRkTLqcCos4w3mPdM1Fdi7CO0XOFKyJh2uW1WXZgYnJ6zS3fniQrCsnxOyBqR+RB2LVa+AoIhxZeDtIs1Zjfm6dDpwtaZcj4iNfVba9xKkmbPUqKkq3hBkfSYNre0vs4+01Y+ORbRJNsNZ1y63CiuOaG++4nHH7zIoeu1wm3BmlobDpdQFLe1v6SuTHFKooCRHVy9FLXscEnAE5u1xlirEBvGc5+hnV9efTHT+73nH8jORbbvPcLmO8ZtwBIoOTNbQ6QMiEKS7dgJmImW7zt/w3p12I7DJjckqVjvGhykdH0TQJo9HVWg+rE+SZvUggYGIppUOwcfyj9aAczmO3KzrSpKhmlQcbhn7xxDgDOYvSBjjmN1r2+sdFGPIxlDgfp7+ZWx9qkbTxmR6gAxySJ6whuCQMiPozJbE7TvGVAHxFiFzyMH4jj7RxuBIg2APxESiaYuhO0Y7fPM5/wDE+kF/Tb9qHdjIA8zpL0weBM/WKTS4x4i6p2aIbVHxLU1ejeUP78S9C1uyh22Y847za69o1NjMigMpx+0ytNpxZcoKsQDyJ0oyTjZyskXCTRp06dKkbDFs+SYF7ff6YHGZrU0DZ2AHYRVtD/GyDEc0+yjLFKV05ckAxSvV7srBdQFiPsGdsWSt2cBePrLRiuNtlGwloYWFlaPpbvoHqRC/T2Iw2nJjWk09li4fIhcoqNkTI9gOVHMd0ecF2GJavQqmCTB227X2AcCKc+fQVodS29CTS7AHwDPJqdUhMWTUMiggcQ9OrD5BHMCy5YrvRWkCJsezc/JMcDkKuV8QBBwWE8XY4+0nyO7RdRTM3peq9QFNRwR8zT6XSr6pj3WY405swU43fE6rp9VWn0wBPvx5iPIaiteywm2ia/VMAMJHNF02vT2liRAXaiykkouYWhrLE9SxsZmeTm496Imhq+hbGJWI5Glchu57ZhX1dajCvzEdf/FCsre4wQT6fQW/0OMPzGnYEDntObvqurY1lcrmdFRp7FqDM/cRTW1bffmPxSp0ibZnaKhHO1q/cIt1FXWzAU8eZq0Akhl7yL621DFduT9o1TalslaoxtDU+qsZbcsh75ntb+H76w1lA9RO4A7zQOjs0gJU94qeraug7G5X6xinNyuAKS7MfT1lrQuOc4nedGQBkTsqgEnxOM0g360PjgsTidNq3s216PTkqXALv8COy7WzX4urZ0Os/FOh0BNSA2FRyV7TMs/Hbmz+FpyB9e09o9J03S7Taquw7tZ/aa9Wn0GqTdXp0b/ySn+wmTnBerNjx5HvlQrofxs7uoNa/BKidboOqHUVq+Rn6TitTpNPXYy0bVcd024P8jHOi6hzZ6a5GPEq8ntIusKa+x27ar25HBmHr9Tq97lD3UjOfMeTT3PUHIIHzmZ2rrsVuT7RJLJJFcWOF0c+1HXrbi1NgAzzh8ExqjT/AIoqOWsrev8A0taMwr9TFL7UKKAeWsfaoj1PVNJdUAnVdC13+jP/ALhjlm10SeKMX2CTqev0LE62pmrb+k0U1FWsqLVHIzgj4mbb1Cyl9uooJrPAev3oR/uI5oa9Oc2UKELd9vaVc77LuFbON/E2h9HVu6KxDjOBOf0SKLDuJ/hkcduZ3P4soLVIQcYM5KrTs9l7bWOH52jOOJphL/rOf5Ud2hivUA+wRiuvdzmZ6ogfAbEbVzXwGzEy/hiQR005yrgZmfqKVRvZL6gWcsf5xbTO9jFWOSDLRTSuwPsuUKlSwz9Y2G24KieUEjBAOJW0lR7VlbsgQWgnBg3oDZIETc3PZ7BgfWaNTFKcN+qWrj0QWw6Hke2Wa6tcYEMzh1w3EXfSEng8S1r2EZR8jInnzkc+Ip76ByZRrXYg58SnDeitmppqERMkSEFl+pABIAjNhVKsgeIlTq2W3cq4AmeNytjWbNdIVcOMyuqqArwpwD8RXUdVRaOP1zndX1jUM5AbAHxBjwzmVugnUEei/h+D9ZodPUPSHd8kTnS+o113GTNLTaPVU1nDYGO01zx1FJvYEdBpNQLGKE8QWrRCdrHAMytMNVXZlu30k9S1hZkUHseYlQqf1Lp0hms+mSE90b0ZCIXYcmB0CBsOol8uxcE4xK5Nlv6HurFozj9phdTStnKY9w7zTo1ewMH7jiYfWkY6g6hM7WP9YzAmpbGYoxnKpC+iqK65FnU6jRW21i7T1szEAECc70wmzWUlhyCeZ9F6DtesIR9T9Zozt8VRqwQUJNHFka3S27jpDZb/AJd5BAP2jLv+KLrE9HU2KuAdqMFA+nefQbej6a47/SG7wR3lK/w7Tu3MzY+8Qptf6jWoPuTObTovUr+no+q6j6msWwnbYwddv0I5BmnotF6N6vj3Fv6Y5m8NPTpq9ta/vFRXm4MOeZV3Jl4SSWjY0278r7sRdqltO0qDj58xmpsUgfSC/SxJ4jJpNIyxbTZz+t/Cmk97pp3sNoIYk7iM/Ge055vwLoUdCp1m4HOGrGPtxPpVNzMAFZW/eGxnuvMKuvqwPLv7qzgdH+FWrYFdRqgme2/A/lNyjRro6mC7s4z7jOielQu7AmXrD/KLnjfbGwzc9Lo5f8TEnREjkxW7qFXR9FTpq6/V1Jx6ip4Y/Ma67ltPhSM71Az9xD6Loen0t9mpZi9hwXZvpzmFP60PVRlbOF66G/8AqNliVmtSAWXtg45l9N76N3nxNnX1pq7XdwPcxMVVKqQEBGJV57VUcjIrm2vYkXN1RU8EReiv0iTjmaGqowPUqmU2sw+zHPaWxvkvqLarscW7IxnmGY5q7AmZtde5i5bEMbxWh92ZZwXoFFbNQ1bZxiN0WJZhiZh3aljbk9szR04S1AVbmMnjSRX2PXhHXj+kCjlSAGzAuzadCXORA02i0lg2M+ItQ0Qa1lXq17g2MTJa6xDt+JrcFSC0y9QmLTjtGY/0yG/6jWPsxgCAvcI2K158zR1KpWgZcbsTntfa1dm9WHPiZca5svLQ5X6dmd/6j4nr+n6fZ7gAT5ifTrjZfubsI/1CxXT25yPiMpxnRI7K6bTflR/BUMTCvdbgi1dg+syqtXqtJZvUll/0mOjqJ6krVsuxsRksV7LVFh9Jb6jkL7gPMV6npP4q2IPOYPpzW9P1DpYpKE5BmuLqryAR7TFS5Y52ugVZTp9qqm0d4xf6dal7GAzLV6esgtUPrMzqFd+rxUF2r8xdKctDN0eSyq27bWwOTGep9NLdONij9JyR9Itoukfl7lc2YI+PM6JXrar0ywIIwRLTvG04vQYNxds4nQt6errHkEzvvw9cCBg+eZwepq9DXYHYMROl/DeqxYATjmasv+Fm7C7mz6LpnGwE/wAoS63av2mZRqRjgybdagO3OW8CI5qizxNyFNfffbelKP6SseW8xjTMEXbu3EHvOZ/FnUbtLbpbKe/uzjz2mFX+LNSLsupEkU2rRofBLi3R9g0daPpyzkZA7Zil7pu2gjvONo/GVXoBmPOOR5mVb13rXVLwvTaSqZxkLu/me0Y5WujOsHGVtnY9RV1y2l/xAM+0wvR/xE1hNVuQ68Mr9xFOj6fU06Qfm3L3vy58D6CZ3XtF/E/P07xdWPcqnG8f3ieTjK0P4wmuEtncHWi1MDEztWwIJBmL0jqaanTI6WbuPnmPvYHQhTjPaSU7WxKwcHowOvWFKmIGSuDj95rdVf0ul2MgIaxEH2z3mB+IiVrsII5AHM2+to9fR6NTsc1WKnJXHO2WSfx2iuaaTaOZe1AvuMRtetwSDDW7bj7VxPflFNfH6pmVLbOY7FbXsFB2nPExrEYkt5Ma1H5qq0of0fMhbkVCj/qmzGnFWij2KPvCYziLXM6juYayws+2Gcp6IDjmaU6KilI9TvH9GrVNkHiDpFYXI7yzOUGR2kb5aCtov1O4soWJLuVcrmWINp3E9o9pqgwAYcSuoRoAkltjqeTBtac895oavTAECruYuenucEmRSjVgo2tZY6DddxuHE5jVOWsbByMzpNa46gwVCOPExNZ02+l8svB7RPj8Ut9jJK9onp7EMFUZJM6rQ6OoVhmG4kTnul6W2pxZZWQvjM6LT3AldviL8iVv6hjrsyer6GytmtUAL/pxENHcrMMDa86jqH8UAH9MzU6bSCbAB9pMWX6fYNbtGfq7LtwCruJkaJr/AFxVYAFmsNHxuHjtmJpptQNWXzkdsSzypp0R3ZqVWpS61qcA95bqwZNPu0xBOMxDqNi6esEj3HHaF0d7WoA3Ix5mb7amHk+gGguNy4vc7vMeqZKWIBzmJflSbm28ZjVGl2nLnMZNprslmH1S5fXr3J797Etn+kb6VfssVhzGOv6Ou3SF61xbX7gR5mFotS1Lqw7ZmpS+WGjThnGMj6BRq7rKv4fiKrqXrsDW2brGGSPgfEZ/DrU62of+Q8HzC6joqavTXVq/p6hQQHx58Z+kxrumdRy1oDfboNVSE15T5XJ5ExNT+H9He27S6l1B8MuQItpOi6/S9Q/+5rig8i0EFP5+P3n0zpXQOjbLD+ZFjAjBFw9o44/eaIwaemInlhV5Ecf0L8K9NW0HW26jUD/SvsX9/M6Z7dNokFWkqqqqTsB4nVJ0rpdZQrVWOfLZzLvT0utmxVp8uu0gKDn6S7xtrbM//Kx39Ys4nUder0/+Ki7T5XiCfq+i1lZOnuVif8pM67XHpttBW+pNvpgYKjIGe30M43QfhDQva1hV8h2fcGIHJ4GPgCKljpD8eWMlfGjK02gfSdaFmmXOmvUttJ/Q3n/edDYxROeIRNItLqw//WpA/c/+pndR1QRSd2Avn6RD+zH8tGP+I9SgqCH9TtNTVdVfUaCvSAuyoiglznsPichqbW1/UlYD+HUcgTb09yuAB3l80nCCijm5s1yaRUlaydwAEJWlZG8GTqNIbVzniAT+H7BzMiaa0ZXa7K6xK7FwePrMHqWi9Jwy/p+Y/wBSsuxhVIHyIumsruX0bh7h8ibMKnFJopJpmOhVGJPMu9otE9r6xXd7BxBacqWO/tNypqygRSB2hbnBrxKVoHtATkZmlbpUZAMYlZSSaAkY9Rw4mvUcgAHER1lIpG5PEHTqyxGTiSS5K0Q1rCgGc8iJXa0B8ZgbHyD7jM9yS3eCGNeyWdLZUvSnrtySpxnMF1TraXhRUoJED1jUtZQtR54HMyETaRn+UXjxKSU59jG60jotH1BtUiqUC4mh6YRQymc5pbVR/ia2j1It3KW7ROXHX+PRE77NVmzR4zLaDSWWIWJG3xFKGzlW55l7NbdUy1V8Ke8z1LpFk12ab0oteCcETL1AcPtq7/MOHLEb2z+8lgi+5jiCP17IkYXU9Pq2KljlczT6dRV+XXLYbHzC2MuoTg5xMPVWav1ClCnaPMcryR49A6OgKItvtYEGBsuZL/apInOafWalbNrMSc9p02l3GkOwGZWeN4+9kWyXuzX7qyfuJx+or9DU2V9kzuAnZLebAVKYA8zneu0Ev6yKCF4OPiX8aVSpjItJjf4b1zaTULg+3IzO602sru1b4P6qgT958s0WoFdg+/edHpOqhGGCWOOePrz/AEjsmNuVo6GPIuNM662tg5FZ790P/Etp3trb31JgjGNoEX0erTWKBnB/qJqUpZgDdmUjOUdGvmmhmnVZQKdLWw4xxiG1FrtUEpoVOPAxiDqruBGMR303A5b+saskv0ZJOKejOo0Ts++5sZ7zQUrWmFwoEEzY4zmY3XOpjTVisMNzZBI8DGYuUnJklc+wfUtdioKrYZhuz9JyPUNW+1lcn3cHHxLanqysyt5VMf3mLq9SdVqPTRsl2xJDG7LTyJRHej0sUuuxw7cfYRlAVsJziM6aj0aVrQ8ATzKinDd4ic7k2ciTbdharWYbd0o9Rqy+c5lVwGHxLajO0YPBilFWS77AO5cYZRBLpqiSdo3Qq1WD3HtJXCnOY5OloBm63RF8ngTGu0zISR2nQazeAxz/ACnOtqH3sh7fWa8Dk0VYbp52sT5myAbavgzApLV2BhzNvT6jcmcYhzJ3aIhbUUu1TKVyZjWVtWcEYM6NdRuYhhxFNbpRedy8cQ4506YWr6MMuw7mQTC30tWeRAkTRplDc1WlsdUC8kyq9O9Nd1zcjxNGtrDdsRSQPM9q1zZmzMw/JJaHcfZlPXSP08mE0zAXADIyZodP0dRd3IGJ67QJdYTUcMD4keRXTKtGkorroDAjOIjdbY7AhcjMpqa9T+XCoCWENoRaNqXLzjuYhJRV9luw1fsr9V27eIm/Va72NfbwIfqFShWXfwR8znqdM9lpCAnB7y+KEZpyYGdDoU2ktklZfW7GQ+ngMYpozbp1/iHiD1eo9VSK+CIFBuVoK6M6yttLdvsbJPMer6myV4JO2I6t/VADE+2H0tSanTkKORNEkmk5FV/Bheohgdr7cyg1JRbC7bgV7HzMdkNVpTOTmFbIQ5PfiF4orodhh8klEW34YrxjPH0hq7ipHfEEiCxnU98cQZBQ7W4+seh0k110dT0LrLVahVsYEMTO60PUEtOA30nxxLCjAjg/Im70zrllNn8Rj2+YnLivaHePl/1kfZNM6hQxPfsZfV2oFJDfcDxOG0f4oqNahnGMSmq/E1SI6pZklSMj/v1iU5dUOeKN8rN/qHV69LWSTz2/9zgerdZOqbex47D6RHqfWbdTafIzjkzLa1WBzuJ8Y8mOhirbEZMl6QZ9SSmAw/aaXQNNuua2wZ2jg/Eyqaza+WHH1nW9P0vo9KNgAySD+2YZyUdGjxMXLInLoObPTI3SSa7RnzB6hd9QMWrV04Y8TPlxpPRl8/xvgya6Y4SoHMFY7NWdg7RTXMa696ngSvT9bXaCpaK+NpcjAMU6xdpW1gCIGvV12WlFMxuok1ap9rcH4hemoqZusMesMePIl+jSvcK53czI12kBzavAM2kNNy7gcybdPW1W0+YIT4MD2c9psDAPeadGQDiKailKLcA94xRkjKmOk+SsKKZcWNntE7tewfb2mr6TNkzE11FgvOFJGe8ONxbA9BbrBcn1ibKfiGryuMjEcSlSgLDmMtRKmx0q4DII5+ZrDQJqamZyO0w9LaoC+MCHbWXHIrbAnOnCTlrQ6LpbM7V2X6HUMqnckNotaeXIIaM00i5ybDuMh6kQsNmAO/EY5RaprZWilnW0rB4BaLr1d7m9q4MTtoS+7bWMHtHtLTVoVJvIJMu4Y4rrYLbJuW+2rc55PiNdOq/L1DIBJ8wmm1VOoqJXG0dooNU7WOFGFHYxVyknGqLMb1dfqkHwfiJ36YivCd4xTc78NGDXtXcTmGEnHQUcvrKjV7STkwGm1dmmDKp4M3tboPzLBhAJ0bCltpJ+JpWWHGpFad6MhS72Gw8kxixT6Kk9zD3VGohGABHfmXKb9P8AaGc9JnU/H+O3yk/0ZSNstP1EJYoccyl6EHI7ieR8iX7VoW/pNxfsC6MO2SJ5SPjmMHmeNat4k5/sHwp7iCFrAYUtz3l62buQWP1MsKOO8ItIA5PeBzXovDBL2Lk5IAyTC005Pu4EKKwpO3AhaxnjviVc/wBDY4UnbD6Oo2WqqjucCdmwWvpPbGUA7RL8OdLCKLrl/UMj6RvqlwexaK/0py338CZ2+ckkbvHg3NCVhxVj6RG6yztGb3zxPKqtjIzxHZFyehn5HxJZ8S4doUZvXqKMp/eKafpzVsSOD4mnqVKEGsDEJXaMc4JHxM/NxWjyri06Zhajptr2bnY/aN1UIKfTaaWEuJ3f1imu0rpSzV5zLrI5JJgozA35a8orErma1PvQMTkTKr0jGhrGyXltG+pKYzwJacVLaZEM6/RrfypwRFtNTdp8g5IjtAYHdaYdnrYYA5lVNpcSIGBwGkMqMMkAwdpZQQIt67I4DeZFG+iMO+jquwdoBlHoCEKD4jSnK8RDVG31eDxiGNvQaId6zcBSeccya7SGKmJ6GxVYg/qMZNYJLKefMu41oKD6O6xdUG/yHiaTN6lmMZBmdXnYABnHmaAcoocLniZ8m2WWhXUaWqhvUb2/WYXUbGsu9rllnR6nbrKGD8YnNWL6bsO+DH+P+32UkP8ASa2cbN2BNKz8vQRWCNxmXotXXWozwYzUa79QG7yuSL5NvoK6o0qaEPIbAjllVfpZU5IiyGtaiOc/EoHZRtB7zPxlJnR8f8bnzbql+2C1GsXTcAgt8RDU9V1Fq7EIrX/x7n95rDTqTlkXPyRFtb09LhlDtcfyM1xhFbaOlH8VHGrTtmLXk5J7xyjG3bBflbaWZWQ8ierbDQZNmnCnjq0C1dOCSBM11KHI7TftQWV5Ey7q8EyYp+jN5vjJ7QsrZEIp8yjIVOR2llEc6ZzI8oOmFU5lic9oNe8J3i2jQpOiVnQ/h7pYvH5m4e0EhVI/rFOh9Ht6hcDjFYPuJnZ2pT0zTbiBgcKB5PwJny5P9Yj8UW2C1uoGj06rWMWN+lf+ZjE7VJJJJ5J+ZZ3e61rrTlj/AEHxAWvmNxw+ONvs6+LEoqijHJhq/wDaBUZMOi4Qn5l4bdj5dE2EEbscGL36d0U2UZYf6f7RtRlCPpIDlRtVf5mXcE+zHn8bFnVSW/37EBbmsMp5B5Es2rZ8IBx5jL0q2TtGTzxE7hYi4orLE/AiJY6PP+T+NzYftH7L+f8AwaqrXABHfxB2pXU/tgGtuqp3OjZ88RROpK7EP3lFCTOfLHKOpKjQdkdfrKsiIoYHmI1eo+6xf0y6FraipyD9YeNFOi1tygjkGestoChjjMy7QUchmJ5nijWkAdo5Y0kSx5tcg7GJ2atnbIHED6BRjuziV9ULwAIxQXolhtDS3q5wfvNO2o7cp3lNYw0yoEHfuYbSOLay3mInJtciyXoC1x01Hu5JjGkvfU1BWwoMGdLvffZyue0bOlRgAmVH0lHT0ux+Dx8uaVQQprVekhVOVbjiKWdOuu/w1xnuWm4tQGPp88mECDzzHQi0djF+Gh3llf8AEYtHRVGDdYzH4XgTQp0tdIxUgX/eObR8D+UjGJdpvs6mHxsGH/CKQL08fP8AKXrq9wJ8S88JOKH2y8hlyDPAycwlNoBYp2kEZxyDF9RokuTcgCt3yPMfIB7yqgKSng8iV4plm01TMYV2VNtZcj5Epdpd59s2bK8+Iq9ZBzEThKLtBUISVMzB0wsP1gfTEDf022gbsbl+QO02FJBjKWBhhu0vCTfbEZvCxSjVHLrUc8TU6P0bUdQ1KoqEJn3NjgCbGi0OgbVqdXuWknlk8Tt7bOm9J0S2VlPTYfw1r5Nn2lcjktJHJnhlikotW30IpRR0vR7m211Vjvjkn/kzmtXqLNbebbMhRwif6R/eH6lr7uo2h7cJWv6Kl7L/AHMSd+MCTFh4faXZ0/GwOCuXf/opa4HAglUscy4QseYwlYAjVFyezZaiildcu/AAhAuIN+Tn+UbVIXdsvX2lGEunAlH7yPoC7JWUZArHgy6SbBzxJWg3sGrAD9Qx9TBXU6a79dSufkLz/OF2g9xPDHYCDZJRjJU1YumkrRcIrAHxumR1cX6Vs1n2EZzOhbgRLqumOq0ZSsD1O4+srxV2c3zfBxzxN44/b+HKpcWO5zkxijUENPWaF6a82LtYeIA1kDMbSaPMTg4umNam4sMLFGDZlqWy2DGGTMtGNLQEk12aF9LvgP3+sY0mlasYLYB8TQSgPatjYKAZ+5klQGOO2ZjgnKP8O9+N8GGSPyZVa9A0QKPP7wqj4k4l0X25jYxSO4lGEaiqRUDMkjzJWWx4l6JZUcyCJ7GDJ7yEKyJJnpUJ4SRIkiQjLYBEq6kjK9xyJYSwhorZAIdMyj15Mh29JvUHKn9Y+PrDjDAEHIPYiFb0yXQm1XM8teIy5UEjOT8CCuVjWxHt4/eUcUiym2SpO5UwBk4yxwB94G8WuuEOccqyjGI06b1xnmXS10rasKiq+N23ziRwbdWV5foyqupKLPR1iml/DEcH+0eFe7BHIPYiTdTVeuLUVx9RA16P8v8A/i2tWP8A+be5YUmu9lU5IZVMSwEoljD/ABEwflTkS+5SMqwI84MumiOyCePvBsO0sDk5+e32kHvIyyLr2g37Qg7QbyPoi7JTtLNxKp2l27SLoj7BsZ5BIPeXUcQewvorZPDG3kZkP3lh2kXZPQHUaeq9Nti5H18RI9O06goeR9ZqbcnEuABxjgyybXRmz+Lgzr7x3+/Zh1/hfqGosV9Fp3etvPxHbPwZ1tCB6CnjPefSOl/iLp2k6JVZqGWt6l2OPqP7z1X4w6dq09RDgDj3YBl45GjyWXD8c3F+jgtOhTTqD3AkOvu/aEz7QPtKt+sfaJSSVHsscVCKiukVYYH3hAPb+0qw/SPrL+DCizZQcgGWxK181iXkXRH2UYSM8y5HEriQKZB7yMS+J6QllQJ7EtieEhLIAkgfynhJkAR3gloCZAd9uc7M8CFnh3gaTJZ5VA4AkWfob7SwkWfpMj6J7JJxIHaSF3OASBz5OBCOoQ7dyN/8GyJYFoH5kz2OZ6QhBlGRTyQCYTEgyUFMrI8yZ6AJbsMwR5MIeZXb8QsiJXtLN2kASWhB7BGEHAlMe6EbhYEFgjy0IolFGTCLwZIkke/zSQZXPJlhCApdUtyhX5AORINdAwOOBCTL6ho77NRvpu2KRyp+YnLj5O0zl/kPEeWpwWzQJ/QP/L/ie/zj95V+Cn/zH+0kf4g/f/eWs6vouf8AEWT4kf5s/SW7gSwClXKY+pl5Sn9Lfc/7y8i6I+yJM9PeJAEeZM8OwkwkInpMjxIQ9I8yZ75kIRIky2OTIQrK2cITLmRZ+gwPoi7LqTW6uEV8ZyrdiJa20WHCVLVWpO1R3/cyD3Mg+JaitK7IMgy3iRIE8RK8y2JGeIAlTIEtPACQNnvE9JAnvMIDwkGSRKOeJAo8g5lrDxPJ2kNB6J7IQeZeQOAJMKIwecCXUwb91lkPBgTC1osIO39Q+0JB2DkfaEqz/9k=" alt="Joshua Webb" onerror="this.remove()">
        </div>
        <blockquote class="quote">
          A zip code should never determine the trajectory of a child's life.
          <cite>The belief driving everything I am building toward.</cite>
        </blockquote>
        <dl class="fastfacts">
          <div><dt>Based in</dt><dd>Raleigh, NC</dd></div>
          <div><dt>Current role</dt><dd>Site Director, CHCCS</dd></div>
          <div><dt>Studying</dt><dd>M.A., UNC Chapel Hill</dd></div>
          <div><dt>Working across</dt><dd>Schools, enrichment, access</dd></div>
        </dl>
      </div>
    </div>
  </div>
</section>
 
<!-- ============ FOCUS ============ -->
<section id="focus">
  <div class="wrap">
    <div class="sec-head">
      <p class="sec-kicker">What I do</p>
      <h2>The levers I pull to change the face of education</h2>
      <p>Areas where I have built depth across classrooms, community centers, education-innovation work, and policy.</p>
    </div>
    <div class="focus-grid">
      <div class="focus-item">
        <div class="bar"></div>
        <h3>Classroom Teaching &amp; Instruction</h3>
        <p>Designing and delivering standards-aligned, responsive instruction, from a justice-and-perspectives unit for 120 eighth-graders to Universal Design for Learning that reaches every kind of learner.</p>
      </div>
      <div class="focus-item">
        <div class="bar"></div>
        <h3>Extended &amp; Out-of-School Learning</h3>
        <p>Building enrichment in the hours around the school day as one lever for closing gaps, structured to add real learning time rather than simply fill hours.</p>
      </div>
      <div class="focus-item">
        <div class="bar"></div>
        <h3>Educational Access &amp; Exposure</h3>
        <p>Getting hands-on STEAM and literacy support into high-need communities, so a student's access to opportunity is not decided by where they happen to live.</p>
      </div>
      <div class="focus-item">
        <div class="bar"></div>
        <h3>Equity &amp; Education Policy</h3>
        <p>Synthesizing data across programs and districts to advocate for funding, inform state-level reform, and keep equity at the center of the conversation.</p>
      </div>
      <div class="focus-item">
        <div class="bar"></div>
        <h3>Curriculum &amp; Program Design</h3>
        <p>Building the curricula, schedules, staffing models, and systems that let strong programs hold their weight for kids, day after day.</p>
      </div>
      <div class="focus-item">
        <div class="bar"></div>
        <h3>Family &amp; Community Engagement</h3>
        <p>Connecting schools, families, and community partners so learning is reinforced everywhere a student spends their time.</p>
      </div>
    </div>
  </div>
</section>
 
<!-- ============ EXPERIENCE ============ -->
<section class="band" id="experience">
  <div class="wrap">
    <div class="sec-head">
      <p class="sec-kicker">Experience</p>
      <h2>A record of building across every setting</h2>
    </div>
    <div class="timeline">
 
      <div class="tl-item">
        <div class="tl-date">Aug 2026 &ndash; Present</div>
        <h3>Community School Site Director</h3>
        <div class="tl-org">Chapel Hill-Carrboro City Schools · Rashkis Elementary</div>
        <ul>
          <li>Lead all operations of a K&ndash;5 enrichment program serving 40+ students, scaling to 80+ on teacher workdays.</li>
          <li>Designed a weekly model with two targeted-instruction days, two active-programming days, and one hands-on project, adding six hours of targeted learning per week.</li>
          <li>Hire, train, supervise, and evaluate assistant directors, group leaders, substitutes, and volunteers using district-aligned assessments.</li>
          <li>Coordinate daily with 20+ educators and 40+ guardians to align programming with student needs and bridge the school day.</li>
        </ul>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">Fall 2026 &ndash; Present</div>
        <h3>Education Innovation Intern (UNC MEITE)</h3>
        <div class="tl-org">Goodwill Industries of Eastern North Carolina</div>
        <ul>
          <li>Support Goodwill's STEAM education programs serving high-need communities across eastern North Carolina.</li>
          <li>Designing a free, multisensory literacy toolkit aligned to the science of reading, built to support both classrooms and out-of-school programs serving students with reading-based learning needs.</li>
          <li>Conducted an eastern North Carolina educational-landscape analysis, mapping funding gaps, literacy and STEM proficiency, and partner needs to inform grant strategy.</li>
          <li>Represented Goodwill's STEAM program in community STEM outreach, connecting students and families to hands-on learning.</li>
        </ul>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">Apr 2026 &ndash; Aug 2026</div>
        <h3>Program Director, Youth Camp</h3>
        <div class="tl-org">City of Raleigh · John Chavis Community Center</div>
        <ul>
          <li>Directed daily operations for a 55-hour-per-week municipal youth camp serving 45+ campers.</li>
          <li>Supervised, coached, and evaluated eight seasonal staff, delivering 495 hours of STEM, literacy, creative, and physical programming.</li>
          <li>Developed and analyzed beginning, midpoint, and end-of-program assessments to measure quality and inform leadership decisions.</li>
          <li>Designed inclusive adaptations and individualized support plans for campers with diverse learning and behavioral needs.</li>
        </ul>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">Aug 2024 &ndash; May 2026</div>
        <h3>Teacher Candidate, Middle Grades English</h3>
        <div class="tl-org">Wake County &amp; Edgecombe County Public Schools</div>
        <ul>
          <li>Designed and delivered a unit on justice and perspectives in American literature for 120 eighth-graders, using scaffolded, responsive instruction.</li>
          <li>Applied Universal Design for Learning frameworks to differentiate instruction and support diverse learners.</li>
          <li>Integrated digital literacies, inquiry-based learning, and citizenship across English and social studies content.</li>
        </ul>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">Feb 2024 &ndash; Apr 2026</div>
        <h3>Youth Enrichment Site Coordinator</h3>
        <div class="tl-org">YMCA of the Triangle · Alexander Family YMCA</div>
        <ul>
          <li>Managed year-round operations serving 70+ students and led office operations for 300+ campers during the summer.</li>
          <li>Mentored and co-supervised 8 academic-year counselors and 40 summer counselors, plus three Youth Club Supervisors.</li>
          <li>Designed a data-driven curriculum integrating literacy, social studies, STEM, and social-emotional learning.</li>
        </ul>
      </div>
 
      <div class="tl-item">
        <div class="tl-date">Feb 2023 &ndash; Mar 2024</div>
        <h3>Education Policy Research Assistant</h3>
        <div class="tl-org">Public School Forum of North Carolina</div>
        <ul>
          <li>Collaborated with Dogwood Health Trust to advocate for over $1 million in funding through data synthesis and policy presentations.</li>
          <li>Performed analytical research on 80+ after-school programs and coded interview transcripts to identify key equity themes.</li>
          <li>Increased program visibility by 25% through strategic communications and stakeholder engagement.</li>
        </ul>
      </div>
 
    </div>
  </div>
</section>
 
<!-- ============ BUILDING TOWARD ============ -->
<section id="building">
  <div class="wrap">
    <div class="sec-head">
      <p class="sec-kicker">Building toward</p>
      <h2>A research and design initiative in development</h2>
      <p>Beyond my day-to-day work, I am developing and researching a model for what high-quality out-of-school learning can be.</p>
    </div>
    <div class="edge">
      <span class="tag">In development · Research initiative</span>
      <h3>Expanded E.D.G.E. Learning</h3>
      <p>
        Expanded E.D.G.E. Learning is a concept I am designing and a research project I am pursuing: an
        investigation into how high-quality curriculum for out-of-school-time programs can raise learning
        outcomes and close achievement gaps. The model is being built for K&ndash;8 students in Edgecombe County,
        North Carolina, one of the communities where I first learned what a zip code can cost a child. It is a
        vision under active development, not yet a launched organization.
      </p>
      <div class="edge-programs">
        <div class="edge-card">
          <h4>ELEVATE · Grades K&ndash;5</h4>
          <p>An elementary track built around early literacy, foundational skills, and the social-emotional habits that help young learners feel they belong.</p>
        </div>
        <div class="edge-card">
          <h4>ASCEND · Grades 6&ndash;8</h4>
          <p>A middle-grades track focused on academic momentum, identity, and the agency young adolescents need to author their own futures.</p>
        </div>
      </div>
    </div>
  </div>
</section>
 
<!-- ============ WRITING ============ -->
<section class="band" id="writing">
  <div class="wrap">
    <div class="sec-head">
      <p class="sec-kicker">Writing &amp; speaking</p>
      <h2>Contributing to the conversation on education equity</h2>
    </div>
    <div class="writing-list">
 
      <a class="writing-item" href="https://ced.ncsu.edu/news/2026/04/23/josh-webb-26-the-college-of-education-didnt-just-teach-me-how-to-educate-it-taught-me-how-to-lead/" target="_blank" rel="noopener">
        <div>
          <h3>The College of Education Taught Me How to Lead</h3>
          <div class="desc">An NC State College of Education feature on my path from Rocky Mount to graduate study, and what studying abroad and teaching taught me about leading in education.</div>
        </div>
        <div class="src">NC State · 2026</div>
      </a>
 
      <a class="writing-item" href="https://ced.ncsu.edu/news/2023/09/19/teaching-is-the-backbone-of-humanity-gen-z-on-the-teaching-profession/" target="_blank" rel="noopener">
        <div>
          <h3>Teaching Is the Backbone of Humanity: Gen Z on the Teaching Profession</h3>
          <div class="desc">An NC State College of Education panel feature on why my generation is choosing to teach and how to support new educators entering the field.</div>
        </div>
        <div class="src">NC State · 2023</div>
      </a>
 
      <a class="writing-item" href="https://www.ednc.org/developing-global-perspectives-for-future-teachers-and-their-students/" target="_blank" rel="noopener">
        <div>
          <h3>Developing global perspectives for future teachers and their students</h3>
          <div class="desc">A perspective on how international teacher-training experiences shape more inclusive, culturally responsive classrooms back home.</div>
        </div>
        <div class="src">EdNC · 2024</div>
      </a>
 
      <a class="writing-item" href="https://www.ednc.org/author/joshua-webb/" target="_blank" rel="noopener">
        <div>
          <h3>Perspective articles on North Carolina education</h3>
          <div class="desc">My full author archive at EdNC, covering equity, teacher training, critical literacy, and access across NC public schools.</div>
        </div>
        <div class="src">EdNC · 2022&ndash;Present</div>
      </a>
 
    </div>
  </div>
</section>
 
<!-- ============ EDUCATION ============ -->
<section id="education">
  <div class="wrap">
    <div class="sec-head">
      <p class="sec-kicker">Education</p>
      <h2>Grounded in research and practice</h2>
    </div>
    <div class="edu-grid">
      <div class="edu-card">
        <div class="yr">Aug 2026 &ndash; May 2027</div>
        <h3>Master of Arts in Educational Innovation, Technology, and Entrepreneurship</h3>
        <div class="inst">The University of North Carolina at Chapel Hill</div>
        <p>Innovative Specialist concentration, focused on leadership, research, and innovation within educational organizations, districts, and nonprofits.</p>
      </div>
      <div class="edu-card">
        <div class="yr">Aug 2023 &ndash; May 2026</div>
        <h3>B.S., Middle Grades Education: English &amp; Social Studies</h3>
        <div class="inst">North Carolina State University</div>
        <p>Summa Cum Laude, 3.93 GPA. Transformational Scholar, Honors College, Kappa Delta Pi, Queer Educators Alliance Chair. Study abroad in New Zealand and Costa Rica.</p>
      </div>
    </div>
  </div>
</section>
 
<!-- ============ CONTACT ============ -->
<section class="band contact" id="contact">
  <div class="wrap">
    <p class="sec-kicker">Contact</p>
    <h2>Let's build something that holds its weight for kids.</h2>
    <p>Whether you are working in schools, extended learning, education innovation, or policy, I would love to connect.</p>
    <div class="contact-links">
      <a class="btn btn-primary" href="mailto:joshwebb@unc.edu">Email me</a>
      <a class="btn btn-ghost" href="https://www.linkedin.com/in/joshua-webb-1332201b7/" target="_blank" rel="noopener">LinkedIn</a>
      <a class="btn btn-ghost" href="tel:+12524587504">Call or text</a>
    </div>
    <p class="contact-details">
      <a href="mailto:joshwebb@unc.edu">joshwebb@unc.edu</a> &nbsp;·&nbsp; <a href="tel:+12524587504">252-458-7504</a>
    </p>
  </div>
</section>
 
<footer>
  <div class="wrap">
    Joshua Webb, Educator &amp; Program Designer · Raleigh, North Carolina
  </div>
</footer>
 
<script>
  // Mobile menu toggle
  const toggle = document.querySelector('.nav-toggle');
  const links = document.querySelector('.nav-links');
  toggle.addEventListener('click', () => {
    const open = links.classList.toggle('open');
    toggle.setAttribute('aria-expanded', open);
  });
  links.querySelectorAll('a').forEach(a =>
    a.addEventListener('click', () => {
      links.classList.remove('open');
      toggle.setAttribute('aria-expanded', 'false');
    })
  );
 
  // Scrollspy: highlight active nav link
  const navLinks = [...document.querySelectorAll('.nav-links a')];
  const sections = navLinks
    .map(a => document.querySelector(a.getAttribute('href')))
    .filter(Boolean);
  const spy = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        const id = '#' + e.target.id;
        navLinks.forEach(a => a.classList.toggle('active', a.getAttribute('href') === id));
      }
    });
  }, { rootMargin: '-45% 0px -50% 0px' });
  sections.forEach(s => spy.observe(s));
</script>
 
</body>
</html>
