
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#080b18">
<meta name="description" content="الموقع الشخصي لمحمود أبو شنب، طالب برمجة حاسوب ومهتم بتطوير الويب وبايثون.">
<title>محمود أبو شنب | مبرمج ومطور</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;800;900&family=Inter:wght@400;600;700;800&display=swap');

:root{
  --bg:#080b18;
  --panel:rgba(18,26,51,.88);
  --text:#f1f5ff;
  --muted:#a4afcb;
  --border:#839bff35;
  --cyan:#36e3f5;
  --blue:#5b8cff;
  --purple:#a477ff;
  --shadow:0 20px 55px #0003;
}
body.light{
  --bg:#f3f6ff;
  --panel:rgba(255,255,255,.92);
  --text:#17213d;
  --muted:#5c6784;
  --border:#5b8cff38;
  --shadow:0 18px 45px #263b7012;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth;scroll-padding-top:85px}
body{
  font-family:'Cairo',sans-serif;
  background:var(--bg);color:var(--text);line-height:1.8;
  transition:background .3s,color .3s;overflow-x:hidden
}
body.en{font-family:'Inter',sans-serif}
a{color:inherit;text-decoration:none}
button,input,textarea{font:inherit}
button{cursor:pointer}
.container{width:min(1120px,91%);margin:auto}
#particles{position:fixed;inset:0;width:100%;height:100%;z-index:-2;pointer-events:none}
.glow{position:fixed;width:300px;height:300px;filter:blur(100px);opacity:.15;border-radius:50%;z-index:-1;pointer-events:none}
.glow.one{background:var(--blue);top:-100px;right:-100px}
.glow.two{background:var(--purple);bottom:0;left:-100px}

header{
  position:sticky;top:0;z-index:20;
  background:color-mix(in srgb,var(--bg) 88%,transparent);
  backdrop-filter:blur(18px);border-bottom:1px solid var(--border)
}
.nav{min-height:75px;display:flex;justify-content:space-between;align-items:center;gap:15px}
.logo{font-family:Inter,sans-serif;font-weight:900;font-size:20px;white-space:nowrap}
.logo span{color:var(--cyan)}
.nav-links{display:flex;gap:17px;align-items:center}
.nav-links a{font-size:12px;color:var(--muted);font-weight:700}
.nav-links a:hover{color:var(--cyan)}
.actions{display:flex;gap:7px}
.icon-btn{border:1px solid var(--border);background:var(--panel);color:var(--text);border-radius:12px;padding:7px 12px}
.icon-btn:hover{border-color:var(--cyan)}

.hero{
  min-height:610px;display:grid;grid-template-columns:1.2fr .8fr;
  align-items:center;gap:35px;padding-top:55px;padding-bottom:65px
}
.eyebrow{
  display:inline-flex;align-items:center;gap:9px;padding:7px 13px;
  border:1px solid var(--border);border-radius:30px;color:var(--cyan);
  background:var(--panel);font-size:12px;margin-bottom:22px
}
.status-dot{width:8px;height:8px;border-radius:50%;background:#4ce6a5;box-shadow:0 0 12px #4ce6a5}
h1{font-size:clamp(38px,5.5vw,65px);line-height:1.25;margin-bottom:17px}
body.en h1{font-family:Inter,sans-serif;letter-spacing:-2px;direction:ltr}
.gradient{
  display:block;background:linear-gradient(100deg,var(--cyan),var(--blue),var(--purple));
  background-size:200%;-webkit-background-clip:text;background-clip:text;
  color:transparent;animation:shine 5s linear infinite
}
@keyframes shine{to{background-position:200%}}
.hero h2{font-size:20px;margin-bottom:12px}
p{color:var(--muted);font-size:14px;line-height:2}
.hero p{max-width:580px}
.buttons{display:flex;gap:11px;flex-wrap:wrap;margin-top:24px}
.btn{
  display:inline-flex;align-items:center;justify-content:center;gap:8px;
  padding:11px 19px;border-radius:12px;border:1px solid var(--border);
  font-size:13px;font-weight:800;transition:.25s
}
.primary{background:linear-gradient(110deg,var(--cyan),#8caaff);color:#08111e;border:0}
.secondary{background:var(--panel)}
.btn:hover{transform:translateY(-4px)}
.tech-row{display:flex;gap:9px;flex-wrap:wrap;margin-top:25px}
.tech{display:grid;place-items:center;width:43px;height:43px;border:1px solid var(--border);border-radius:13px;background:var(--panel);font-size:19px}
.signature{font:11px Inter,sans-serif;letter-spacing:2px;color:var(--muted);margin-top:22px}

.visual{position:relative;display:grid;place-items:center;min-height:370px}
.orbit{position:absolute;width:290px;height:290px;border:1px solid #5b8cff55;border-radius:50%;animation:spin 24s linear infinite}
.orbit:before,.orbit:after{content:"";position:absolute;width:12px;height:12px;border-radius:50%;background:var(--cyan);box-shadow:0 0 20px var(--cyan)}
.orbit:before{top:35px;left:35px}
.orbit:after{bottom:30px;right:25px;background:var(--purple);box-shadow:0 0 20px var(--purple)}
.orbit.small{width:220px;height:220px;animation-direction:reverse;animation-duration:17s}
@keyframes spin{to{transform:rotate(360deg)}}
.profile-card{
  width:230px;padding:18px;border:1px solid var(--border);border-radius:24px;
  background:var(--panel);box-shadow:var(--shadow);z-index:2;
  animation:float 5s ease-in-out infinite;text-align:center
}
@keyframes float{50%{transform:translateY(-10px)}}
.avatar{
  width:185px;height:215px;margin:auto auto 15px;border-radius:18px;
  overflow:hidden;border:1px solid var(--border);background:linear-gradient(135deg,#14284b,#28214b);
  display:grid;place-items:center;color:var(--cyan);font:800 44px Inter,sans-serif
}
.avatar img{width:100%;height:100%;object-fit:cover;display:block}
.profile-caption{font-size:12px;color:var(--muted)}
.tag{position:absolute;padding:9px 12px;border:1px solid var(--border);background:var(--panel);border-radius:12px;font-size:11px;font-weight:800;z-index:3}
.tag.one{top:25px;right:0;color:var(--cyan)}
.tag.two{bottom:20px;left:0;color:var(--purple)}

section{padding:70px 0}
.heading{margin-bottom:28px}
.kicker{font-size:12px;font-weight:900;color:var(--cyan);letter-spacing:1px}
.heading h2{font-size:clamp(25px,4vw,36px);margin-top:7px;line-height:1.5}
.heading p{margin-top:8px;max-width:700px}
.grid{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:17px}
.panel{
  padding:23px;border:1px solid var(--border);border-radius:19px;
  background:var(--panel);box-shadow:var(--shadow);transition:.3s;min-width:0
}
.panel:hover{transform:translateY(-5px);border-color:#36e3f577}
.card-icon{width:46px;height:46px;display:grid;place-items:center;border:1px solid var(--border);border-radius:14px;background:linear-gradient(135deg,#36e3f51c,#a477ff20);font-size:22px;margin-bottom:15px}
.panel h3{font-size:17px;margin-bottom:8px}
.panel p{font-size:13px}
.chips{display:flex;flex-wrap:wrap;gap:7px;margin-top:15px}
.chip{font-size:10px;font-weight:800;padding:4px 9px;border:1px solid var(--border);border-radius:8px;color:var(--cyan)}
.project{display:flex;flex-direction:column;min-height:260px}
.project .bottom{display:flex;justify-content:space-between;align-items:center;margin-top:auto;padding-top:18px;font-size:11px;color:var(--purple)}
.skill-bar{height:6px;border-radius:20px;background:var(--border);overflow:hidden;margin-top:15px}
.skill-bar span{display:block;height:100%;background:linear-gradient(90deg,var(--cyan),var(--purple));border-radius:20px}
.learning{padding:27px;border:1px solid var(--border);border-radius:20px;background:linear-gradient(125deg,#5b8cff13,#a477ff10,#36e3f508)}
.learning h3{font-size:20px;margin-bottom:10px}
.goal-list{display:grid;gap:12px;margin-top:18px}
.goal{display:flex;gap:10px;color:var(--muted);font-size:13px}
.check{color:var(--cyan);font-weight:900}
.lab-tabs{display:flex;gap:8px;flex-wrap:wrap;margin:18px 0}
.lab-tab{border:1px solid var(--border);border-radius:10px;padding:8px 12px;color:var(--muted);background:transparent;font-size:12px}
.lab-tab.active{background:var(--cyan);color:#07111e;border-color:var(--cyan)}
.lab-screen{direction:ltr;text-align:left;white-space:pre-wrap;overflow-wrap:anywhere;background:#060a14;color:#d8e4ff;border:1px solid var(--border);border-radius:13px;padding:20px;font:13px/2 monospace;min-height:110px}
.certificate{display:flex;flex-direction:column}
.certificate img{width:100%;height:190px;object-fit:contain;background:#fff;border-radius:12px;margin-bottom:15px}
.certificate-placeholder{height:190px;display:grid;place-items:center;background:linear-gradient(135deg,#14284b,#28214b);border:1px dashed var(--border);border-radius:12px;margin-bottom:15px;font-size:45px}
.contact{display:grid;grid-template-columns:.85fr 1.15fr;gap:18px}
.email{display:inline-block;direction:ltr;color:var(--cyan);font:13px Inter,sans-serif;overflow-wrap:anywhere;margin-top:12px}
.form{display:grid;gap:12px}
.field{display:grid;gap:6px}
.field label{font-size:12px;font-weight:800}
.field input,.field textarea{width:100%;padding:12px;border:1px solid var(--border);border-radius:11px;background:var(--bg);color:var(--text);outline:none}
.field input:focus,.field textarea:focus{border-color:var(--cyan)}
.field textarea{min-height:110px;resize:vertical}
footer{padding:25px 0;border-top:1px solid var(--border);font-size:12px;color:var(--muted)}
.footer-inner{display:flex;justify-content:space-between;gap:12px;flex-wrap:wrap}
.reveal{opacity:0;transform:translateY(18px);transition:.7s}
.reveal.visible{opacity:1;transform:translateY(0)}
.back-top{position:fixed;bottom:18px;left:18px;width:42px;height:42px;display:grid;place-items:center;border:1px solid var(--border);border-radius:13px;background:var(--panel);color:var(--cyan);z-index:5}

@media(max-width:900px){
  .nav-links{gap:10px}
  .nav-links a{font-size:11px}
  .hero{grid-template-columns:1fr;gap:10px}
  .visual{min-height:360px}
  .contact{grid-template-columns:1fr}
  .grid{grid-template-columns:repeat(2,minmax(0,1fr))}
}
@media(max-width:650px){
  .nav{min-height:65px}
  .nav-links{display:none}
  .logo{font-size:16px}
  .hero{padding-top:40px;gap:10px}
  .hero h1{font-size:clamp(34px,10vw,47px)}
  .hero h2{font-size:17px}
  .hero p{font-size:13px}
  .visual{min-height:330px}
  .orbit{width:260px;height:260px}
  .orbit.small{width:205px;height:205px}
  section{padding:52px 0}
  .grid{grid-template-columns:1fr}
  .panel{padding:20px}
}
@media(prefers-reduced-motion:reduce){
  *,*:before,*:after{animation:none!important;scroll-behavior:auto!important;transition:none!important}
}
</style>
</head>

<body>
<canvas id="particles"></canvas>
<div class="glow one"></div>
<div class="glow two"></div>

<header>
  <div class="container nav">
    <a href="#home" class="logo">MAHMOUD<span>.</span></a>
    <nav class="nav-links">
      <a href="#about" data-ar="من أنا" data-en="About">من أنا</a>
      <a href="#skills" data-ar="مهاراتي" data-en="Skills">مهاراتي</a>
      <a href="#projects" data-ar="مشاريعي" data-en="Projects">مشاريعي</a>
      <a href="#certificates" data-ar="شهاداتي" data-en="Certificates">شهاداتي</a>
      <a href="#goals" data-ar="طموحي" data-en="Goals">طموحي</a>
      <a href="#contact" data-ar="تواصل" data-en="Contact">تواصل</a>
    </nav>
    <div class="actions">
      <button class="icon-btn" id="languageBtn" type="button">EN</button>
      <button class="icon-btn" id="themeBtn" type="button" aria-label="تغيير الإضاءة">☀</button>
    </div>
  </div>
</header>

<main>
<section class="container hero" id="home">
  <div class="reveal">
    <div class="eyebrow"><span class="status-dot"></span>
      <span data-ar="رحلة مستمرة نحو الاحتراف" data-en="On a journey to grow">رحلة مستمرة نحو الاحتراف</span>
    </div>
    <h1>
      <span class="gradient" data-ar="محمود" data-en="Mahmoud">محمود</span>
      <span data-ar="أبو شنب" data-en="Abu Shanab">أبو شنب</span>
    </h1>
    <h2 data-ar="طالب برمجة حاسوب | شغوف ببايثون" data-en="Computer Programming Student | Python Enthusiast">طالب برمجة حاسوب | شغوف ببايثون</h2>
    <p data-ar="أؤمن أن كل فكرة عظيمة تبدأ بسطر كود، وأن التعلم المستمر هو الطريق لبناء مستقبل أفضل. أتعلم البرمجة خطوة بخطوة، وأحوّل الأفكار إلى تجارب عملية."
       data-en="I believe every great idea starts with a line of code. I am learning programming step by step and turning ideas into practical experiences.">
      أؤمن أن كل فكرة عظيمة تبدأ بسطر كود، وأن التعلم المستمر هو الطريق لبناء مستقبل أفضل. أتعلم البرمجة خطوة بخطوة، وأحوّل الأفكار إلى تجارب عملية.
    </p>
    <div class="buttons">
      <a class="btn primary" href="#projects">✦ <span data-ar="استكشف مشاريعي" data-en="Explore My Work">استكشف مشاريعي</span></a>
      <a class="btn secondary" href="#contact">✉ <span data-ar="تواصل معي" data-en="Contact Me">تواصل معي</span></a>
    </div>
    <div class="tech-row">
      <div class="tech" title="Python">🐍</div>
      <div class="tech" title="HTML">🌐</div>
      <div class="tech" title="CSS">🎨</div>
      <div class="tech" title="JavaScript">⚡</div>
      <div class="tech" title="GitHub">⌘</div>
      <div class="tech" title="Learning">🧠</div>
    </div>
    <div class="signature">THINK. CODE. CREATE.</div>
  </div>

  <div class="visual reveal">
    <div class="orbit"></div><div class="orbit small"></div>
    <div class="tag one">✦ <span data-ar="عقل مبدع" data-en="Creative Mind">عقل مبدع</span></div>
    <div class="tag two">Python • Web • Ideas</div>
    <div class="profile-card">
      <div class="avatar" id="avatar">
        <img src="profile.jpg" alt="صورة محمود أبو شنب"
             onerror="this.style.display='none';this.parentElement.textContent='MA';">
      </div>
      <div class="profile-caption" data-ar="أتعلم وأجرّب وأتطور كل يوم" data-en="Learning, creating, and growing every day">أتعلم وأجرّب وأتطور كل يوم</div>
    </div>
  </div>
</section>

<section id="about">
<div class="container">
  <div class="heading reveal">
    <div class="kicker" data-ar="نبذة عني" data-en="WHO I AM">نبذة عني</div>
    <h2 data-ar="أتعلم اليوم، لأبني غدًا." data-en="Learning today. Building tomorrow.">أتعلم اليوم، لأبني غدًا.</h2>
    <p data-ar="لست هنا لأتوقف عند ما أعرفه، بل لأكتشف ما يمكنني تعلمه وصنعه." data-en="I am here to discover what I can learn and create.">لست هنا لأتوقف عند ما أعرفه، بل لأكتشف ما يمكنني تعلمه وصنعه.</p>
  </div>
  <div class="grid">
    <article class="panel reveal"><div class="card-icon">💻</div><h3 data-ar="البرمجة" data-en="Programming">البرمجة</h3><p data-ar="أهتم بفهم طريقة عمل البرامج وكتابة أكواد واضحة ومنظمة، وأطور مهاراتي بالممارسة." data-en="I enjoy understanding how software works and writing clear code while improving through practice.">أهتم بفهم طريقة عمل البرامج وكتابة أكواد واضحة ومنظمة، وأطور مهاراتي بالممارسة.</p></article>
    <article class="panel reveal"><div class="card-icon">🧩</div><h3 data-ar="حل المشكلات" data-en="Problem Solving">حل المشكلات</h3><p data-ar="أتعامل مع المشكلة خطوة بخطوة وأبحث عن حل منطقي بدلًا من الاستسلام عند أول خطأ." data-en="I approach problems step by step and look for logical solutions instead of giving up.">أتعامل مع المشكلة خطوة بخطوة وأبحث عن حل منطقي بدلًا من الاستسلام عند أول خطأ.</p></article>
    <article class="panel reveal"><div class="card-icon">🚀</div><h3 data-ar="التطور المستمر" data-en="Continuous Growth">التطور المستمر</h3><p data-ar="أؤمن أن الاحتراف يأتي من الاستمرار والتعلم والاستفادة من الأخطاء." data-en="I believe expertise grows through consistency, learning, and improving through mistakes.">أؤمن أن الاحتراف يأتي من الاستمرار والتعلم والاستفادة من الأخطاء.</p></article>
  </div>
</div>
</section>

<section id="skills">
<div class="container">
  <div class="heading reveal">
    <div class="kicker" data-ar="الأدوات والتقنيات" data-en="TOOLS & TECHNOLOGIES">الأدوات والتقنيات</div>
    <h2 data-ar="أبني أساسًا قويًا في البرمجة." data-en="Building a strong programming foundation.">أبني أساسًا قويًا في البرمجة.</h2>
    <p data-ar="تقنيات أتعلمها وأستخدمها في رحلتي لبناء مشاريع عملية." data-en="Technologies I am learning on my journey to build practical projects.">تقنيات أتعلمها وأستخدمها في رحلتي لبناء مشاريع عملية.</p>
  </div>
  <div class="grid">
    <article class="panel reveal"><div class="card-icon">🐍</div><h3>Python</h3><p data-ar="أركز على تعلم الأساسيات والمنطق البرمجي وبناء البرامج." data-en="Learning programming fundamentals, logic, and small programs.">أركز على تعلم الأساسيات والمنطق البرمجي وبناء البرامج.</p><div class="chips"><span class="chip">Variables</span><span class="chip">Functions</span><span class="chip">OOP</span></div><div class="skill-bar"><span style="width:70%"></span></div></article>
    <article class="panel reveal"><div class="card-icon">🌐</div><h3>HTML</h3><p data-ar="إنشاء هيكل صفحات الويب وتنظيم العناوين والنصوص والروابط." data-en="Creating web page structure and organizing text, headings, and links.">إنشاء هيكل صفحات الويب وتنظيم العناوين والنصوص والروابط.</p><div class="chips"><span class="chip">Structure</span><span class="chip">Semantic HTML</span></div><div class="skill-bar"><span style="width:75%"></span></div></article>
    <article class="panel reveal"><div class="card-icon">🎨</div><h3>CSS</h3><p data-ar="تصميم واجهات جذابة ومتجاوبة مع الألوان والتنسيقات والحركات." data-en="Designing attractive responsive interfaces with layouts and animations.">تصميم واجهات جذابة ومتجاوبة مع الألوان والتنسيقات والحركات.</p><div class="chips"><span class="chip">Flexbox</span><span class="chip">Grid</span></div><div class="skill-bar"><span style="width:60%"></span></div></article>
    <article class="panel reveal"><div class="card-icon">⚡</div><h3>JavaScript</h3><p data-ar="إضافة التفاعل إلى صفحات الويب والتعامل مع الأزرار والمحتوى." data-en="Adding interactivity to web pages and handling buttons and content.">إضافة التفاعل إلى صفحات الويب والتعامل مع الأزرار والمحتوى.</p><div class="chips"><span class="chip">DOM</span><span class="chip">Events</span></div><div class="skill-bar"><span style="width:45%"></span></div></article>
    <article class="panel reveal"><div class="card-icon">⌘</div><h3>GitHub</h3><p data-ar="التعرف على حفظ المشاريع ومشاركة الكود وبناء معرض للأعمال." data-en="Learning to store projects, share code, and build a portfolio.">التعرف على حفظ المشاريع ومشاركة الكود وبناء معرض للأعمال.</p><div class="chips"><span class="chip">Repositories</span><span class="chip">Pages</span></div><div class="skill-bar"><span style="width:45%"></span></div></article>
    <article class="panel reveal"><div class="card-icon">🧠</div><h3 data-ar="التفكير المنطقي" data-en="Logical Thinking">التفكير المنطقي</h3><p data-ar="تقسيم الأفكار الكبيرة إلى خطوات صغيرة يمكن فهمها وتنفيذها." data-en="Breaking big ideas into smaller steps that are easier to implement.">تقسيم الأفكار الكبيرة إلى خطوات صغيرة يمكن فهمها وتنفيذها.</p><div class="chips"><span class="chip">Logic</span><span class="chip">Practice</span></div><div class="skill-bar"><span style="width:65%"></span></div></article>
  </div>
  <p style="margin-top:14px" data-ar="مستويات المهارات تقديرية؛ عدّلها لتعكس مستواك الحقيقي." data-en="Skill levels are estimates; adjust them to reflect your actual experience.">مستويات المهارات تقديرية؛ عدّلها لتعكس مستواك الحقيقي.</p>
</div>
</section>

<section id="projects">
<div class="container">
  <div class="heading reveal">
    <div class="kicker" data-ar="مساحة الإبداع" data-en="CREATIVE SPACE">مساحة الإبداع</div>
    <h2 data-ar="أفكار أطمح إلى بنائها." data-en="Projects I aim to build.">أفكار أطمح إلى بنائها.</h2>
    <p data-ar="هذه أفكار مستقبلية؛ أضف روابط أعمالك الفعلية عندما تصبح جاهزة." data-en="These are project ideas. Add links to your real work when it is ready.">هذه أفكار مستقبلية؛ أضف روابط أعمالك الفعلية عندما تصبح جاهزة.</p>
  </div>
  <div class="grid">
    <article class="panel project reveal"><div class="card-icon">📊</div><div class="kicker" data-ar="فكرة مشروع" data-en="PROJECT IDEA">فكرة مشروع</div><h3 data-ar="مساعد الطلاب" data-en="Student Assistant">مساعد الطلاب</h3><p data-ar="برنامج لحساب العلامات والمعدلات وتنظيم ساعات الدراسة." data-en="A program to calculate grades and averages and organize study hours.">برنامج لحساب العلامات والمعدلات وتنظيم ساعات الدراسة.</p><div class="chips"><span class="chip">Python</span><span class="chip">Logic</span></div><div class="bottom"><span data-ar="قيد التخطيط" data-en="Planned idea">قيد التخطيط</span><span>01</span></div></article>
    <article class="panel project reveal"><div class="card-icon">🌌</div><div class="kicker" data-ar="فكرة مشروع" data-en="PROJECT IDEA">فكرة مشروع</div><h3 data-ar="موقع شخصي تفاعلي" data-en="Interactive Website">موقع شخصي تفاعلي</h3><p data-ar="واجهة عصرية تعرض المهارات والأفكار والمشاريع بأسلوب متجاوب." data-en="A modern responsive interface for skills, ideas, and projects.">واجهة عصرية تعرض المهارات والأفكار والمشاريع بأسلوب متجاوب.</p><div class="chips"><span class="chip">HTML</span><span class="chip">CSS</span><span class="chip">JS</span></div><div class="bottom"><span data-ar="مشروع تعلّم" data-en="Learning project">مشروع تعلّم</span><span>02</span></div></article>
    <article class="panel project reveal"><div class="card-icon">🤖</div><div class="kicker" data-ar="فكرة مشروع" data-en="PROJECT IDEA">فكرة مشروع</div><h3 data-ar="أدوات برمجية مفيدة" data-en="Useful Developer Tools">أدوات برمجية مفيدة</h3><p data-ar="أدوات صغيرة تساعد على تنفيذ المهام اليومية وتبسيط العمليات." data-en="Small tools to help with everyday tasks and repetitive operations.">أدوات صغيرة تساعد على تنفيذ المهام اليومية وتبسيط العمليات.</p><div class="chips"><span class="chip">Python</span><span class="chip">Automation</span></div><div class="bottom"><span data-ar="هدف مستقبلي" data-en="Future goal">هدف مستقبلي</span><span>03</span></div></article>
  </div>
</div>
</section>

<section id="lab">
<div class="container">
  <div class="heading reveal">
    <div class="kicker" data-ar="مختبر الكود" data-en="CODE LAB">مختبر الكود</div>
    <h2 data-ar="أفكار صغيرة، وإمكانيات كبيرة." data-en="Small ideas. Big possibilities.">أفكار صغيرة، وإمكانيات كبيرة.</h2>
    <p data-ar="اضغط على أحد الأمثلة لتتعرف على مفهوم برمجي." data-en="Choose an example to explore a programming concept.">اضغط على أحد الأمثلة لتتعرف على مفهوم برمجي.</p>
  </div>
  <div class="panel reveal">
    <h3 data-ar="جرّب أمثلة بايثون" data-en="Explore Python Examples">جرّب أمثلة بايثون</h3>
    <div class="lab-tabs">
      <button class="lab-tab active" data-example="hello" data-ar="الطباعة" data-en="Print">الطباعة</button>
      <button class="lab-tab" data-example="variables" data-ar="المتغيرات" data-en="Variables">المتغيرات</button>
      <button class="lab-tab" data-example="function" data-ar="الدوال" data-en="Functions">الدوال</button>
      <button class="lab-tab" data-example="loop" data-ar="التكرار" data-en="Loops">التكرار</button>
    </div>
    <div class="lab-screen" id="labScreen">print("Hello, World!")</div>
    <p id="labCaption" style="margin-top:12px">تعليمة الطباعة تعرض النص أو القيمة على الشاشة.</p>
  </div>
</div>
</section>

<section id="goals">
<div class="container">
  <div class="heading reveal">
    <div class="kicker" data-ar="الرؤية والطموح" data-en="VISION & AMBITION">الرؤية والطموح</div>
    <h2 data-ar="المستقبل يُبنى خطوة بخطوة." data-en="The future is built one step at a time.">المستقبل يُبنى خطوة بخطوة.</h2>
  </div>
  <div class="learning reveal">
    <h3 data-ar="هدفي أن أصبح مطورًا أفضل كل يوم." data-en="My goal is to become a better developer every day.">هدفي أن أصبح مطورًا أفضل كل يوم.</h3>
    <p data-ar="أعمل على بناء أساس قوي في البرمجة، وتطبيق ما أتعلمه في مشاريع عملية، وتطوير مهاراتي مع الوقت." data-en="I aim to build a strong programming foundation, apply what I learn in practical projects, and grow my skills over time.">أعمل على بناء أساس قوي في البرمجة، وتطبيق ما أتعلمه في مشاريع عملية، وتطوير مهاراتي مع الوقت.</p>
    <div class="goal-list">
      <div class="goal"><span class="check">✓</span><span data-ar="تطوير مهاراتي في Python ومفاهيم البرمجة الأساسية." data-en="Improve my Python and programming fundamentals.">تطوير مهاراتي في Python ومفاهيم البرمجة الأساسية.</span></div>
      <div class="goal"><span class="check">✓</span><span data-ar="إنشاء مواقع ويب باستخدام HTML وCSS وJavaScript." data-en="Build websites using HTML, CSS, and JavaScript.">إنشاء مواقع ويب باستخدام HTML وCSS وJavaScript.</span></div>
      <div class="goal"><span class="check">✓</span><span data-ar="بناء مشاريع عملية ومشاركتها على GitHub." data-en="Build practical projects and share them on GitHub.">بناء مشاريع عملية ومشاركتها على GitHub.</span></div>
      <div class="goal"><span class="check">✓</span><span data-ar="الاستمرار في التعلم وتطوير مهارات حل المشكلات." data-en="Keep learning and improve problem-solving skills.">الاستمرار في التعلم وتطوير مهارات حل المشكلات.</span></div>
    </div>
  </div>
</div>
</section>

<section id="certificates">
<div class="container">
  <div class="heading reveal">
    <div class="kicker" data-ar="إنجازاتي" data-en="MY ACHIEVEMENTS">إنجازاتي</div>
    <h2 data-ar="الشهادات والدورات" data-en="Certificates & Courses">الشهادات والدورات</h2>
    <p data-ar="ضع صور شهاداتك داخل مجلد images لتظهر هنا." data-en="Place your certificate images in the images folder to display them here.">ضع صور شهاداتك داخل مجلد images لتظهر هنا.</p>
  </div>
  <div class="grid">
    <article class="panel certificate reveal">
      <img src="images/certificate1.jpg" alt="الشهادة الأولى" onerror="this.style.display='none';this.nextElementSibling.style.display='grid'">
      <div class="certificate-placeholder" style="display:none">🏅</div>
      <h3 data-ar="الشهادة الأولى" data-en="Certificate One">الشهادة الأولى</h3>
      <p data-ar="استبدل الصورة بصورة شهادتك الأولى." data-en="Replace this image with your first certificate.">استبدل الصورة بصورة شهادتك الأولى.</p>
    </article>
    <article class="panel certificate reveal">
      <img src="images/certificate2.jpg" alt="الشهادة الثانية" onerror="this.style.display='none';this.nextElementSibling.style.display='grid'">
      <div class="certificate-placeholder" style="display:none">📜</div>
      <h3 data-ar="الشهادة الثانية" data-en="Certificate Two">الشهادة الثانية</h3>
      <p data-ar="استبدل الصورة بصورة شهادتك الثانية." data-en="Replace this image with your second certificate.">استبدل الصورة بصورة شهادتك الثانية.</p>
    </article>
    <article class="panel certificate reveal">
      <div class="certificate-placeholder">🎓</div>
      <h3 data-ar="إنجازات قادمة" data-en="Future Achievements">إنجازات قادمة</h3>
      <p data-ar="مساحة لإضافة دورات وشهادات جديدة مستقبلًا." data-en="Space for new courses and certificates in the future.">مساحة لإضافة دورات وشهادات جديدة مستقبلًا.</p>
    </article>
  </div>
</div>
</section>

<section id="contact">
<div class="container">
  <div class="heading reveal">
    <div class="kicker" data-ar="لنتواصل" data-en="LET'S CONNECT">لنتواصل</div>
    <h2 data-ar="كل فكرة عظيمة تبدأ بمحادثة." data-en="Every great idea starts with a conversation.">كل فكرة عظيمة تبدأ بمحادثة.</h2>
    <p data-ar="للتواصل أو تبادل الأفكار البرمجية، يمكنك مراسلتي عبر البريد الإلكتروني." data-en="For contact or programming discussions, feel free to email me.">للتواصل أو تبادل الأفكار البرمجية، يمكنك مراسلتي عبر البريد الإلكتروني.</p>
  </div>
  <div class="contact">
    <div class="panel reveal">
      <div class="card-icon">✉️</div>
      <h3 data-ar="بريدي الإلكتروني" data-en="My Email">بريدي الإلكتروني</h3>
      <p data-ar="يسعدني استقبال رسائلك وأفكارك." data-en="I welcome your messages and ideas.">يسعدني استقبال رسائلك وأفكارك.</p>
      <a class="email" href="mailto:mahmoud63862@gmail.com">mahmoud63862@gmail.com</a>
      <div style="margin-top:20px">
        <a class="btn primary" href="mailto:mahmoud63862@gmail.com">✉ <span data-ar="أرسل بريدًا إلكترونيًا" data-en="Send an Email">أرسل بريدًا إلكترونيًا</span></a>
      </div>
    </div>
    <div class="panel reveal">
      <h3 data-ar="اكتب رسالتك" data-en="Write a Message">اكتب رسالتك</h3>
      <p style="margin-bottom:15px" data-ar="سيتم فتح تطبيق البريد على جهازك لإرسال الرسالة." data-en="Your email app will open so you can send the message.">سيتم فتح تطبيق البريد على جهازك لإرسال الرسالة.</p>
      <form class="form" id="contactForm">
        <div class="field">
          <label for="senderName" data-ar="اسمك" data-en="Your Name">اسمك</label>
          <input id="senderName" required data-ar-placeholder="اكتب اسمك" data-en-placeholder="Enter your name" placeholder="اكتب اسمك">
        </div>
        <div class="field">
          <label for="senderEmail" data-ar="بريدك الإلكتروني (اختياري)" data-en="Your Email (optional)">بريدك الإلكتروني (اختياري)</label>
          <input id="senderEmail" type="email" data-ar-placeholder="example@email.com" data-en-placeholder="example@email.com" placeholder="example@email.com">
        </div>
        <div class="field">
          <label for="senderMessage" data-ar="الرسالة" data-en="Message">الرسالة</label>
          <textarea id="senderMessage" required data-ar-placeholder="اكتب رسالتك هنا..." data-en-placeholder="Write your message here..." placeholder="اكتب رسالتك هنا..."></textarea>
        </div>
        <button class="btn primary" type="submit"><span data-ar="تجهيز الرسالة للإرسال" data-en="Prepare Email">تجهيز الرسالة للإرسال</span></button>
      </form>
    </div>
  </div>
</div>
</section>
</main>

<footer>
  <div class="container footer-inner">
    <div><strong style="font-family:Inter,sans-serif;color:var(--text)">Mahmoud Abu Shanab</strong><div data-ar="أتعلم، أجرّب، وأتطور." data-en="Learning, experimenting, and growing.">أتعلم، أجرّب، وأتطور.</div></div>
    <div>© <span id="year"></span> Mahmoud. <span data-ar="صُنع بشغف 💙" data-en="Made with passion 💙">صُنع بشغف 💙</span></div>
  </div>
</footer>
<a class="back-top" href="#home" aria-label="العودة للأعلى">↑</a>

<script>
const CONFIG = { email: "mahmoud63862@gmail.com" };
let currentLanguage = "ar";

const languageBtn = document.getElementById("languageBtn");
const themeBtn = document.getElementById("themeBtn");

function setLanguage(language) {
  currentLanguage = language;
  const english = language === "en";

  document.documentElement.lang = language;
  document.documentElement.dir = english ? "ltr" : "rtl";
  document.body.classList.toggle("en", english);
  languageBtn.textContent = english ? "عربي" : "EN";

  document.querySelectorAll("[data-ar][data-en]").forEach(element => {
    element.textContent = english ? element.dataset.en : element.dataset.ar;
  });

  document.querySelectorAll("[data-ar-placeholder]").forEach(element => {
    element.placeholder = english
      ? element.dataset.enPlaceholder
      : element.dataset.arPlaceholder;
  });

  renderLab(document.querySelector(".lab-tab.active")?.dataset.example || "hello");
}

languageBtn.addEventListener("click", () => {
  setLanguage(currentLanguage === "ar" ? "en" : "ar");
});

themeBtn.addEventListener("click", () => {
  document.body.classList.toggle("light");
  const isLight = document.body.classList.contains("light");
  themeBtn.textContent = isLight ? "☾" : "☀";
  themeBtn.setAttribute("aria-label", isLight ? "تفعيل الوضع الداكن" : "تفعيل الوضع الفاتح");
});

const examples = {
  hello: {
    code: 'print("Hello, World!")',
    ar: "تعليمة الطباعة تعرض النص أو القيمة على الشاشة.",
    en: "The print statement displays text or a value on the screen."
  },
  variables: {
    code: 'name = "Mahmoud"\nage = 20\nprint(name)',
    ar: "المتغير يخزن قيمة يمكن استخدامها لاحقًا.",
    en: "A variable stores a value you can use later."
  },
  function: {
    code: 'def greet(name):\n    return "Hello, " + name\n\nprint(greet("Mahmoud"))',
    ar: "الدالة تجمع تعليمات يمكن استدعاؤها عند الحاجة وإرجاع نتيجة.",
    en: "A function groups instructions and can return a result."
  },
  loop: {
    code: "for number in range(1, 4):\n    print(number)",
    ar: "حلقة التكرار تنفذ التعليمات عدة مرات، وهذا المثال يطبع الأرقام من 1 إلى 3.",
    en: "A loop repeats instructions. This example prints numbers 1 through 3."
  }
};

const labScreen = document.getElementById("labScreen");
const labCaption = document.getElementById("labCaption");
const labTabs = document.querySelectorAll(".lab-tab");

function renderLab(name) {
  const item = examples[name] || examples.hello;
  labScreen.textContent = item.code;
  labCaption.textContent = currentLanguage === "en" ? item.en : item.ar;
  labTabs.forEach(tab => tab.classList.toggle("active", tab.dataset.example === name));
}

labTabs.forEach(tab => tab.addEventListener("click", () => renderLab(tab.dataset.example)));

document.getElementById("contactForm").addEventListener("submit", event => {
  event.preventDefault();

  const name = document.getElementById("senderName").value.trim();
  const email = document.getElementById("senderEmail").value.trim();
  const message = document.getElementById("senderMessage").value.trim();

  if (!name || !message) {
    alert(currentLanguage === "en" ? "Please enter your name and message." : "يرجى كتابة اسمك والرسالة.");
    return;
  }

  const subject = encodeURIComponent(
    currentLanguage === "en" ? "Portfolio message from " + name : "رسالة من موقع محمود أبو شنب - " + name
  );

  const body = encodeURIComponent(
    "Name: " + name + "\nEmail: " + (email || "Not provided") + "\n\nMessage:\n" + message
  );

  window.location.href = "mailto:" + CONFIG.email + "?subject=" + subject + "&body=" + body;
});

/* إظهار الأقسام عند التمرير */
if ("IntersectionObserver" in window) {
  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add("visible");
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.12 });

  document.querySelectorAll(".reveal").forEach(element => observer.observe(element));
} else {
  document.querySelectorAll(".reveal").forEach(element => element.classList.add("visible"));
}

/* خلفية متحركة خفيفة */
const canvas = document.getElementById("particles");
const ctx = canvas.getContext("2d");
let particles = [];
let width = 0;
let height = 0;
let frame;

function resizeCanvas() {
  const ratio = Math.min(window.devicePixelRatio || 1, 2);
  width = window.innerWidth;
  height = window.innerHeight;
  canvas.width = width * ratio;
  canvas.height = height * ratio;
  ctx.setTransform(ratio, 0, 0, ratio, 0, 0);

  const count = Math.min(45, Math.max(20, Math.floor(width / 22)));
  particles = Array.from({ length: count }, () => ({
    x: Math.random() * width,
    y: Math.random() * height,
    r: Math.random() * 1.5 + 0.5,
    vx: (Math.random() - 0.5) * 0.3,
    vy: (Math.random() - 0.5) * 0.3
  }));
}

function draw() {
  ctx.clearRect(0, 0, width, height);
  const light = document.body.classList.contains("light");

  particles.forEach((p, i) => {
    p.x += p.vx;
    p.y += p.vy;
    if (p.x < 0 || p.x > width) p.vx *= -1;
    if (p.y < 0 || p.y > height) p.vy *= -1;

    ctx.beginPath();
    ctx.arc(p.x, p.y, p.r, 0, Math.PI * 2);
    ctx.fillStyle = light ? "rgba(54,110,200,.3)" : "rgba(90,155,255,.48)";
    ctx.fill();

    for (let j = i + 1; j < particles.length; j++) {
      const q = particles[j];
      const dx = p.x - q.x;
      const dy = p.y - q.y;
      const distance = Math.sqrt(dx * dx + dy * dy);

      if (distance < 105) {
        ctx.beginPath();
        ctx.moveTo(p.x, p.y);
        ctx.lineTo(q.x, q.y);
        ctx.strokeStyle = light ? "rgba(80,120,200,.10)" : "rgba(75,130,255,.12)";
        ctx.lineWidth = 0.7;
        ctx.stroke();
      }
    }
  });

  frame = requestAnimationFrame(draw);
}

resizeCanvas();
draw();
window.addEventListener("resize", resizeCanvas);

document.addEventListener("visibilitychange", () => {
  cancelAnimationFrame(frame);
  if (!document.hidden) draw();
});

document.getElementById("year").textContent = new Date().getFullYear();
setLanguage("ar");
</script>
</body>
</html>

