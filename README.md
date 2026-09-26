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
          <img src="data:image/jpeg;base64,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
