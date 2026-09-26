# Josh-Webbs-Website-
MEITE Project/Website 2
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
  .about-grid p{max-width:62ch;}
  .quote{
    font-family:"Lora",serif;font-style:italic;font-size:1.4rem;line-height:1.4;color:var(--charcoal);
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
  .contact p{max-width:54ch;margin:1.25rem auto 2rem;}
  .contact-links{display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;}

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

<!-- ============ HERO ============ -->
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
    <p class="hero-meta">Based in North Carolina. Community School Site Director at Chapel Hill-Carrboro City Schools and graduate student at UNC Chapel Hill.</p>
  </div>
</section>

<!-- ============ ABOUT ============ -->
<section class="band" id="about">
  <div class="wrap">
    <div class="sec-head">
      <p class="sec-kicker">About</p>
      <h2>An equity leveler across the whole system</h2>
    </div>
    <div class="about-grid">
      <div>
        <p>
          I work at the intersection of the classroom, extended learning, and educational access. I have
          taught middle grades English and social studies, led out-of-school-time programs, and now design
          learning experiences that reach students in school, in the hours around it, and in the communities
          where opportunity is thinnest. I believe every one of those settings is a lever, and I am not
          content to pull just one.
        </p>
        <p>
          My commitment to equity is rooted in real-world experience. I have student-taught in classrooms
          across Edgecombe and Wake County, coordinated enrichment at the Alexander Family YMCA, and directed
          youth programming at the John Chavis Community Center. Today I serve as a Community School Site
          Director in Chapel Hill-Carrboro City Schools and, as a graduate Education Innovation intern with
          Goodwill Industries of Eastern North Carolina, I am designing literacy tools that put hands-on
          reading support into high-need communities. Alongside that direct work, I have contributed to major
          policy briefs and published on education access, teacher training, and equity.
        </p>
        <p>
          I hold a B.S. in Middle Grades Education from NC State University, and I am a graduate student in the
          Master of Arts in Educational Innovation, Technology, and Entrepreneurship program at UNC Chapel Hill.
        </p>
      </div>
      <div>
        <blockquote class="quote">
          A zip code should never determine the trajectory of a child's life.
          The belief driving everything I am building toward.
        </blockquote>
        <dl class="fastfacts">
          <div><dt>Based in</dt><dd>North Carolina</dd></div>
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

      <a class="writing-item" href="#" rel="noopener">
        <div>
          <h3>Undergraduate Commencement Address, Class of 2026</h3>
          <div class="desc">Delivered the commencement address for the NC State College of Education, reflecting on the work it takes to become an educator worth investing in.</div>
        </div>
        <div class="src">NC State</div>
      </a>

      <a class="writing-item" href="#" rel="noopener">
        <div>
          <h3>Developing global perspectives for future teachers and their students</h3>
          <div class="desc">A perspective on how international teacher-training experiences shape more inclusive, culturally responsive classrooms back home.</div>
        </div>
        <div class="src">EducationNC · 2024</div>
      </a>

      <a class="writing-item" href="#" rel="noopener">
        <div>
          <h3>Gen Z Educators on the Teaching Profession</h3>
          <div class="desc">Panel contribution on the challenges facing new teachers and how to support first-year educators entering the field.</div>
        </div>
        <div class="src">News &amp; Observer · 2023</div>
      </a>

      <a class="writing-item" href="#" rel="noopener">
        <div>
          <h3>Perspective Articles on North Carolina Education</h3>
          <div class="desc">Ongoing author covering shifts in NC public education, from teacher retention and training to the school-to-prison pipeline and early childhood programs.</div>
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
      <a href="mailto:your-email@example.com" class="btn btn-primary">Email me</a>
      <a href="https://www.linkedin.com/in/YOUR-HANDLE" class="btn btn-ghost" rel="noopener">LinkedIn</a>
    </div>
  </div>
</section>

<footer>
  <div class="wrap">
    Joshua Webb, Educator &amp; Program Designer · North Carolina
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
