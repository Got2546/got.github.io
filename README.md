<!--
Cinematic Portfolio — Thanet "Got" Chomsri
- วางไฟล์นี้เป็น README.md / เพจ Markdown ที่อนุญาต <style> และ HTML
- ใส่รูปในโฟลเดอร์ assets/ ตามชื่อไฟล์ที่อ้างอิงด้านล่าง
-->

<style>
:root{
  --ink:#F3F4F6;      /* ข้อความหลัก (ขาวนุ่ม) */
  --ink-soft:#C9CDD4; /* ข้อความรอง */
  --bg:#0C0F13;       /* ดำอมฟ้า */
  --deep:#0A2A36;     /* น้ำเงินเข้ม */
  --gold:#BFA77A;     /* ทองหม่น */
  --card:#111417;     /* สีพื้นการ์ด */
  --muted:#8B929B;    /* ตัวหนังสือรอง */
  --line:rgba(255,255,255,.08);
}

html,body{margin:0;padding:0;background:var(--bg);color:var(--ink);font-family:Inter,Prompt,system-ui,-apple-system,"Segoe UI",Roboto,"Helvetica Neue",Arial,"Noto Sans",sans-serif;line-height:1.8;}
*{box-sizing:border-box}
a{color:var(--ink);text-decoration:none}
a:hover{opacity:.9}

/* NAV */
.nav{
  position:fixed;z-index:20;top:0;left:0;right:0;
  display:flex;align-items:center;justify-content:space-between;
  padding:18px 32px;background:linear-gradient(180deg, rgba(0,0,0,.55), rgba(0,0,0,0));
  backdrop-filter:saturate(150%) blur(6px);
}
.brand{display:flex;gap:12px;align-items:center}
.logo{width:36px;height:36px;border-radius:50%;border:2px solid var(--gold);position:relative}
.logo:before,.logo:after{content:"";position:absolute;inset:8px;border:1.5px solid var(--gold);border-radius:50%;clip-path:polygon(0 0,100% 0,100% 50%,0 50%);opacity:.9}
.brand-name{letter-spacing:.28em;color:var(--gold);font-weight:600;font-size:.95rem;}
.menu{display:flex;gap:28px;font-size:.95rem;letter-spacing:.12em}
.menu a{color:var(--ink);opacity:.9}
.menu a.active{color:var(--gold)}
@media (max-width:860px){.menu{gap:18px;font-size:.9rem}.brand-name{display:none}}

/* HERO */
.hero{
  min-height:88vh;display:grid;place-items:center;text-align:center;position:relative;overflow:hidden;
  background:
    radial-gradient(1200px 600px at 50% 20%, rgba(255,255,255,.05), transparent),
    linear-gradient(180deg, rgba(0,0,0,.35), rgba(0,0,0,.75)),
    url(assets/hero.jpg) center/cover no-repeat;
}
.hero .title-sm{color:var(--ink-soft);font-weight:600;letter-spacing:.2em;margin:10px 0 6px}
.hero h1{font-size:clamp(28px,6vw,64px);margin:.2rem 0 1.2rem;font-weight:800;text-shadow:0 4px 28px rgba(0,0,0,.6);}
.play{display:inline-flex;align-items:center;gap:12px;border:2px solid var(--ink);padding:10px 16px;border-radius:999px;background:rgba(0,0,0,.25)}
.play .dot{width:36px;height:36px;border-radius:50%;border:2px solid var(--ink);display:grid;place-items:center}
.play:hover{transform:translateY(-1px);border-color:var(--gold)}
.cta-outline{margin:42px auto 0;display:inline-block;border:2px solid var(--ink);padding:14px 22px;border-radius:6px}
.cta-outline:hover{border-color:var(--gold);color:var(--gold)}
.arrow{position:absolute;left:4%;top:50%;translate:0 -50%;width:40px;height:40px;border-left:3px solid var(--ink-soft);border-bottom:3px solid var(--ink-soft);rotate:45deg;opacity:.8}

/* SECTION */
.section{padding:84px 6vw;background:var(--bg)}
.section.black{background:linear-gradient(180deg,#0B0E11,#0A0D10)}
.section h2{font-size:clamp(24px,4vw,44px);margin:0 0 10px;font-weight:800;color:#fff;text-wrap:balance}
.section p.lead{color:var(--ink-soft);font-size:clamp(16px,2.1vw,22px);max-width:900px}

/* GRID & CARD */
.grid{display:grid;gap:20px;margin-top:28px;grid-template-columns:repeat(12,1fr)}
.card{grid-column:span 6;background:var(--card);border:1px solid var(--line);border-radius:14px;overflow:hidden}
.card .thumb{aspect-ratio:16/9;background:#0e1820 center/cover no-repeat}
.card .body{padding:18px 18px 22px}
.card h3{margin:0 0 6px;font-size:1.15rem}
.card .meta{color:var(--muted);font-size:.95rem}
.card .meta b{color:var(--gold)}
@media (max-width:960px){.card{grid-column:span 12}}

/* TAGS */
.tag{display:inline-block;background:rgba(191,167,122,.15);color:var(--gold);border:1px solid rgba(191,167,122,.35);border-radius:999px;padding:4px 10px;font-size:.85rem;margin:2px}

/* CONTACT */
.contact{padding:84px 6vw;background:#0A0D10;border-top:1px solid var(--line)}
.contact h2{margin:0 0 6px}
.contact .row{display:grid;gap:28px;grid-template-columns:1.2fr .8fr;align-items:start}
@media (max-width:960px){.contact .row{grid-template-columns:1fr}}
.input{background:transparent;border:1.5px solid var(--ink);color:var(--ink);padding:14px 16px;border-radius:4px;width:100%}
.btn{background:linear-gradient(135deg, rgba(191,167,122,.9), rgba(191,167,122,.7));color:#111;font-weight:700;padding:14px 16px;border-radius:4px;border:0;cursor:pointer}
.footer{color:var(--muted);text-align:center;padding:28px 0 64px}
.icon-row{display:flex;gap:18px;margin-top:10px}
.icon{width:22px;height:22px;border:1.5px solid var(--ink);border-radius:50%;display:inline-block;opacity:.8}
</style>

<!-- NAV -->
<div class="nav">
  <div class="brand">
    <div class="logo"></div>
    <div class="brand-name">ธเนศ.ชอมศรี</div>
  </div>
  <div class="menu">
    <a href="#stories" class="active">เล่าเรื่อง</a>
    <a href="#projects">โปรเจกต์</a>
    <a href="#ux">UX/UI</a>
    <a href="#bio">ประวัติ</a>
    <a href="#contact">ติดต่อ</a>
  </div>
</div>

<!-- HERO -->
<section class="hero" id="top">
  <div class="arrow" aria-hidden="true"></div>
  <div>
    <div class="title-sm">Thanet “Got” Chomsri</div>
    <h1>“ร้านสมปรารถนา” — Short Film</h1>
    <a class="play" href="[ลิงก์ทีเซอร์หรือไฟล์วิดีโอ]">
      <span class="dot">▶</span> เล่นวิดีโอ
    </a>
    <div>
      <a class="cta-outline" href="#stories">ดูวิดีโอ/สื่อทั้งหมด ＋</a>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section class="section black" id="bio">
  <h2>นักศึกษา IT | UX/UI & Frontend | ผู้สร้างหนังสั้น | คอนเทนต์สวนมะนาว</h2>
  <p class="lead">
    ผมก็อต ปี 4 สายเทคโนโลยีสารสนเทศ ชอบแปลงเรื่องยากให้เข้าใจง่ายผ่าน
    <b>UX/UI</b> ที่ใช้สะดวก และ <b>ภาพยนตร์สั้น</b> ที่สื่ออารมณ์ชัดเจน
    ช่วงนี้โฟกัสงาน <span class="tag">Full-Stack (Kotlin + Spring Boot + React)</span>
    <span class="tag">Tourism UX</span> และ <span class="tag">Short Film</span>
  </p>
  <p>จุดแข็ง: ออกแบบ flow ที่คนทำงานสำเร็จใน 3 คลิก, จัดวางเนื้อหาอ่านสบายตา, ภาพใหญ่ชัด CTA เด่น</p>
</section>

<!-- WORKS: STORY / FILM -->
<section class="section" id="stories">
  <h2>เล่าเรื่อง — งานภาพเคลื่อนไหว</h2>
  <div class="grid">
    <article class="card">
      <div class="thumb" style='background-image:url("assets/film-sompra.jpg")'></div>
      <div class="body">
        <h3>ร้านสมปรารถนา (Short Film)</h3>
        <div class="meta">บท/กำกับ/ตัดต่อ · <b>ดราม่า-จิตวิทยา</b> · Logline: “ทุกความปรารถนา มีราคาที่ต้องจ่าย”</div>
      </div>
    </article>
    <article class="card">
      <div class="thumb" style='background-image:url("assets/garden-doc.jpg")'></div>
      <div class="body">
        <h3>สวนมะนาวบ้านแพ้ว (Micro Doc)</h3>
        <div class="meta">กำกับภาพ/ตัดต่อ · <b>สารคดีสั้น</b> · คอนเทนต์การปลูก/ขาย + ไลฟ์</div>
      </div>
    </article>
  </div>
</section>

<!-- PROJECTS (DEV) -->
<section class="section" id="projects">
  <h2>โปรเจกต์เด่น — สายพัฒนาเว็บ</h2>
  <div class="grid">
    <article class="card">
      <div class="thumb" style='background-image:url("assets/productmaster.png")'></div>
      <div class="body">
        <h3>ProductMaster (Full-stack CRUD)</h3>
        <div class="meta">Kotlin + Spring Boot · React · SQL · Docker</div>
        <p>ระบบจัดการสินค้า: Create/Read/Update/Delete, ค้นหา, ฟอร์ม Validate, การ์ดสินค้า</p>
        <p><a href="[ลิงก์โค้ด]">โค้ด</a> · <a href="[ลิงก์สาธิต]">สาธิต</a></p>
      </div>
    </article>

    <article class="card">
      <div class="thumb" style='background-image:url("assets/student-course.png")'></div>
      <div class="body">
        <h3>Student–Course Management</h3>
        <div class="meta">ตาราง: students, courses, enrollments, attendance</div>
        <p>REST API 3 จุดหลัก + UI ฟอร์ม CRUD + ตารางค้นหา/เช็กชื่อ</p>
        <p><a href="[ลิงก์โค้ด]">โค้ด</a> · <a href="[ลิงก์ API Spec]">API Spec</a></p>
      </div>
    </article>

    <article class="card">
      <div class="thumb" style='background-image:url("assets/tourism-ux.jpg")'></div>
      <div class="body">
        <h3>Tourism UX Website</h3>
        <div class="meta">โฟลวจอง 3 ขั้นตอน · ภาพใหญ่ · CTA ชัด</div>
        <p>Case study สำหรับธุรกิจท่องเที่ยว: ลดขั้นตอน, เปรียบเทียบแพ็กเกจ, เนื้อหาสั้นครบ</p>
        <p><a href="[ลิงก์เคสสตัดดี้]">อ่านเคส</a> · <a href="[ลิงก์โปรโตไทป์]">Prototype</a></p>
      </div>
    </article>
  </div>
</section>

<!-- UX -->
<section class="section black" id="ux">
  <h2>แนวคิด UX/UI</h2>
  <p class="lead">
    เน้นการค้นหาง่าย อ่านรู้เรื่องในไม่กี่บรรทัด ใช้ภาพใหญ่ + bullet สั้น + CTA เด่น,
    สายตาไหลตามโครงพร็อกซิมิตี้, คุมคอนทราสต์แบบไม่ฉูดฉาด (ดำ-ทอง-น้ำเงินเข้ม)
  </p>
  <p>
    เครื่องมือ: Figma, Design System, Accessibility (พื้นฐาน WCAG), Usability Testing ·
    Frontend: HTML/CSS/JS/React · Backend: Kotlin/Spring Boot/REST · DB: SQL/DBeaver
  </p>
  <p>
    <span class="tag">Wireframe → Prototype → Test</span>
    <span class="tag">Iterative Delivery</span>
    <span class="tag">Measure & Improve</span>
  </p>
</section>

<!-- CONTACT -->
<section class="contact" id="contact">
  <div class="row">
    <div>
      <h2>ติดต่อ</h2>
      <p class="lead">อยากร่วมงานหรือให้ช่วยออกแบบ/พัฒนา แจ้งมาได้เลยครับ</p>
      <p><b>อีเมล:</b> <a href="mailto:thanet.got@example.com">thanet.got@example.com</a>  |  <b>โซเชียล:</b> TikTok/Facebook/GitHub/LinkedIn</p>
      <div class="icon-row">
        <span class="icon" title="Twitter/X"></span>
        <span class="icon" title="Facebook"></span>
        <span class="icon" title="YouTube"></span>
        <span class="icon" title="Instagram"></span>
        <span class="icon" title="GitHub"></span>
      </div>
    </div>
    <form onsubmit="return false">
      <label>สมัครรับอัปเดตจากผม</label><br/>
      <input class="input" type="email" placeholder="กรอกอีเมลของคุณที่นี่*"/><br/><br/>
      <button class="btn">สมัครรับข้อมูลเลย</button>
    </form>
  </div>
</section>

<p class="footer">© 2025 Thanet “Got” Chomsri — สร้างด้วย Markdown</p>
