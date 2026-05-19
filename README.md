# HTML-Project
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Abhishek Kumar | Data Analyst Portfolio</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap');

:root{
  --bg:#07111f;
  --bg2:#0d1b2a;
  --card:#10253d;
  --card2:#132b45;
  --text:#ffffff;
  --sub:#a6b6cc;
  --line:#1f3b5a;

  --blue:#38bdf8;
  --purple:#8b5cf6;
  --green:#22c55e;
  --orange:#f59e0b;
  --pink:#ec4899;
  --cyan:#06b6d4;
}

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

body{
  font-family:'Poppins',sans-serif;
  background:linear-gradient(180deg,#07111f,#0a1628,#07111f);
  color:var(--text);
  overflow-x:hidden;
}

/* ================= HERO ================= */

.hero{
  padding:70px 8%;
  position:relative;
  background:
  radial-gradient(circle at top left,rgba(56,189,248,.18),transparent 30%),
  radial-gradient(circle at bottom right,rgba(139,92,246,.18),transparent 30%),
  linear-gradient(135deg,#07111f,#10253d);
}

.hero::before{
  content:'';
  position:absolute;
  inset:0;
  background-image:
  linear-gradient(rgba(255,255,255,.04) 1px,transparent 1px),
  linear-gradient(90deg,rgba(255,255,255,.04) 1px,transparent 1px);
  background-size:40px 40px;
}

.hero-content{
  position:relative;
  z-index:2;
}

.badges{
  display:flex;
  flex-wrap:wrap;
  gap:10px;
  margin-bottom:25px;
}

.badge{
  padding:8px 14px;
  border-radius:30px;
  font-size:12px;
  font-weight:600;
  letter-spacing:.5px;
}

.b1{background:rgba(56,189,248,.18);color:#7dd3fc;}
.b2{background:rgba(139,92,246,.18);color:#c4b5fd;}
.b3{background:rgba(34,197,94,.18);color:#86efac;}
.b4{background:rgba(236,72,153,.18);color:#f9a8d4;}

.hero h1{
  font-size:60px;
  line-height:1.1;
  margin-bottom:18px;
  font-weight:800;
}

.hero h1 span{
  background:linear-gradient(90deg,var(--blue),var(--purple),var(--pink));
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

.hero p{
  color:var(--sub);
  max-width:850px;
  line-height:1.8;
  margin-bottom:35px;
  font-size:16px;
}

.hero-stats{
  display:flex;
  flex-wrap:wrap;
  gap:25px;
}

.stat{
  background:rgba(255,255,255,.05);
  padding:20px;
  border-radius:18px;
  min-width:170px;
  border:1px solid rgba(255,255,255,.08);
  backdrop-filter:blur(10px);
}

.stat h2{
  font-size:34px;
  margin-bottom:8px;
}

.stat p{
  margin:0;
  font-size:13px;
  color:#d1d5db;
}

/* ================= SECTIONS ================= */

.section{
  padding:70px 8%;
}

.section-title{
  font-size:34px;
  margin-bottom:40px;
  position:relative;
  display:inline-block;
}

.section-title::after{
  content:'';
  position:absolute;
  left:0;
  bottom:-12px;
  width:70%;
  height:4px;
  border-radius:20px;
  background:linear-gradient(90deg,var(--blue),var(--purple));
}

/* ================= KPI ================= */

.kpi-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:20px;
}

.kpi-card{
  background:linear-gradient(145deg,var(--card),var(--card2));
  border:1px solid rgba(255,255,255,.06);
  border-radius:22px;
  padding:28px;
  transition:.3s;
}

.kpi-card:hover{
  transform:translateY(-6px);
}

.kpi-card h2{
  font-size:38px;
  margin-bottom:10px;
}

.kpi-card p{
  color:var(--sub);
  margin-bottom:8px;
}

.kpi-card span{
  color:#4ade80;
  font-size:13px;
  font-weight:600;
}

/* ================= SKILLS ================= */

.skills-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(230px,1fr));
  gap:22px;
}

.skill-card{
  background:linear-gradient(145deg,var(--card),#0f2137);
  padding:28px;
  border-radius:20px;
  border:1px solid rgba(255,255,255,.06);
  transition:.3s;
}

.skill-card:hover{
  transform:translateY(-8px);
  border-color:rgba(56,189,248,.4);
}

.skill-card h3{
  margin:14px 0 8px;
  font-size:22px;
}

.skill-card p{
  color:var(--sub);
  margin-bottom:15px;
}

.progress{
  width:100%;
  height:8px;
  border-radius:20px;
  background:#1f3b5a;
}

.progress span{
  display:block;
  height:100%;
  border-radius:20px;
  background:linear-gradient(90deg,var(--blue),var(--purple));
}

/* ================= PROJECTS ================= */

.projects{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
  gap:25px;
}

.project-card{
  background:linear-gradient(145deg,#10253d,#0f2137);
  padding:30px;
  border-radius:24px;
  border:1px solid rgba(255,255,255,.06);
  transition:.3s;
}

.project-card:hover{
  transform:translateY(-8px);
}

.project-tag{
  display:inline-block;
  padding:6px 12px;
  border-radius:30px;
  font-size:11px;
  margin-bottom:16px;
  font-weight:600;
}

.t1{background:#0f3d2d;color:#86efac;}
.t2{background:#402f00;color:#fde047;}
.t3{background:#401c1c;color:#fca5a5;}
.t4{background:#2b1745;color:#d8b4fe;}

.project-card h3{
  margin-bottom:12px;
  font-size:22px;
}

.project-card p{
  color:var(--sub);
  line-height:1.7;
  margin-bottom:20px;
}

.metrics{
  display:flex;
  justify-content:space-between;
}

.metrics div h4{
  font-size:24px;
}

.metrics div span{
  font-size:12px;
  color:var(--sub);
}

/* ================= POWER PLATFORM ================= */

.tools{
  display:flex;
  flex-wrap:wrap;
  gap:14px;
}

.tool{
  padding:12px 20px;
  border-radius:40px;
  background:rgba(255,255,255,.05);
  border:1px solid rgba(255,255,255,.08);
  font-size:14px;
}

/* ================= CODE SECTION ================= */

.code-wrap{
  background:#06111d;
  padding:30px;
  border-radius:20px;
  overflow:auto;
  border:1px solid rgba(255,255,255,.06);
}

.code-wrap pre{
  color:#d1d5db;
  line-height:1.8;
  font-size:14px;
}

/* ================= CONTACT ================= */

.contact-grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
  gap:20px;
}

.contact-card{
  background:linear-gradient(145deg,var(--card),#10253d);
  padding:24px;
  border-radius:20px;
  border:1px solid rgba(255,255,255,.06);
}

.contact-card h3{
  margin-bottom:10px;
}

.contact-card p,
.contact-card a{
  color:var(--sub);
  text-decoration:none;
}

/* ================= FORM ================= */

.form-grid{
  margin-top:50px;
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:20px;
}

.form-group{
  display:flex;
  flex-direction:column;
}

.form-group.full{
  grid-column:1/-1;
}

.form-group label{
  margin-bottom:10px;
  font-size:14px;
}

.form-group input,
.form-group textarea,
.form-group select{
  padding:14px;
  border-radius:14px;
  border:1px solid #23415f;
  background:#0b1727;
  color:#fff;
  outline:none;
}

.form-group textarea{
  min-height:120px;
}

button{
  background:linear-gradient(90deg,var(--blue),var(--purple));
  border:none;
  padding:16px;
  border-radius:16px;
  color:#fff;
  font-size:16px;
  font-weight:600;
  cursor:pointer;
  transition:.3s;
}

button:hover{
  transform:translateY(-3px);
}

/* ================= FOOTER ================= */

footer{
  padding:35px 8%;
  text-align:center;
  color:#94a3b8;
  border-top:1px solid rgba(255,255,255,.06);
}

/* ================= RESPONSIVE ================= */

@media(max-width:768px){

  .hero h1{
    font-size:42px;
  }

  .form-grid{
    grid-template-columns:1fr;
  }

}
</style>
</head>

<body>

<!-- HERO -->

<section class="hero">
  <div class="hero-content">

    <div class="badges">
      <div class="badge b1">Power BI Developer</div>
      <div class="badge b2">SQL Developer</div>
      <div class="badge b3">Excel Automation</div>
      <div class="badge b4">Power Query Expert</div>
    </div>

    <h1>
      Abhishek Kumar <br>
      <span>Data Analyst & BI Developer</span>
    </h1>

    <p>
      Data Analyst specializing in Power BI, SQL, Excel Automation,
      Power Query, Power Pivot, VBA Macros, and dashboard development.
      Passionate about transforming raw business data into meaningful insights
      using modern analytics and automation tools.
    </p>

    <div class="hero-stats">

      <div class="stat">
        <h2>50+</h2>
        <p>Dashboards Built</p>
      </div>

      <div class="stat">
        <h2>5+</h2>
        <p>Years Experience</p>
      </div>

      <div class="stat">
        <h2>200K+</h2>
        <p>Rows Automated</p>
      </div>

      <div class="stat">
        <h2>30%</h2>
        <p>Time Saved</p>
      </div>

    </div>
  </div>
</section>

<!-- KPI -->

<section class="section">

  <h2 class="section-title">Business KPI Dashboard</h2>

  <div class="kpi-grid">

    <div class="kpi-card">
      <h2>₹2.4M</h2>
      <p>Revenue YTD</p>
      <span>▲ 18.3% Growth</span>
    </div>

    <div class="kpi-card">
      <h2>94%</h2>
      <p>Data Accuracy</p>
      <span>▲ Improved Quality</span>
    </div>

    <div class="kpi-card">
      <h2>1,247</h2>
      <p>Reports Automated</p>
      <span>▲ Automation Success</span>
    </div>

    <div class="kpi-card">
      <h2>68h</h2>
      <p>Hours Saved / Month</p>
      <span>▲ Productivity Increase</span>
    </div>

  </div>
</section>

<!-- SKILLS -->

<section class="section">

  <h2 class="section-title">Technology Stack</h2>

  <div class="skills-grid">

    <div class="skill-card">
      <h1>📊</h1>
      <h3>Excel Automation</h3>
      <p>Advanced formulas, VBA, dashboards, macros</p>
      <div class="progress"><span style="width:95%"></span></div>
    </div>

    <div class="skill-card">
      <h1>📈</h1>
      <h3>Power BI</h3>
      <p>DAX, dashboards, drill-through reports</p>
      <div class="progress"><span style="width:92%"></span></div>
    </div>

    <div class="skill-card">
      <h1>🗄️</h1>
      <h3>SQL</h3>
      <p>MySQL, SQL Server, PostgreSQL</p>
      <div class="progress"><span style="width:90%"></span></div>
    </div>

    <div class="skill-card">
      <h1>⚡</h1>
      <h3>Power Query</h3>
      <p>Data cleaning & ETL transformation</p>
      <div class="progress"><span style="width:93%"></span></div>
    </div>

    <div class="skill-card">
      <h1>📘</h1>
      <h3>Power Pivot</h3>
      <p>Data modeling & relationships</p>
      <div class="progress"><span style="width:88%"></span></div>
    </div>

    <div class="skill-card">
      <h1>🐍</h1>
      <h3>Python</h3>
      <p>Pandas, NumPy, Matplotlib</p>
      <div class="progress"><span style="width:78%"></span></div>
    </div>

  </div>
</section>

<!-- CODE -->

<section class="section">

  <h2 class="section-title">SQL Sample Code</h2>

  <div class="code-wrap">

<pre>
SELECT pizza_category,
SUM(total_price) * 100 /
CAST(
(
SELECT SUM(total_price)
FROM pizza_sales
WHERE MONTH(order_date) = 1
) AS DECIMAL(10,2)
) AS PCT
FROM pizza_sales
WHERE MONTH(order_date) = 1
GROUP BY pizza_category;
</pre>

  </div>

</section>

<!-- PROJECTS -->

<section class="section">

  <h2 class="section-title">Featured Projects</h2>

  <div class="projects">

    <div class="project-card">

      <div class="project-tag t1">Excel + VBA</div>

      <h3>Inventory Automation Tracker</h3>

      <p>
        Automated stock management system with VBA macros,
        Power Query integration, and Pivot analysis dashboards.
      </p>

      <div class="metrics">

        <div>
          <h4>85%</h4>
          <span>Time Saved</span>
        </div>

        <div>
          <h4>10K+</h4>
          <span>SKUs</span>
        </div>

        <div>
          <h4>0</h4>
          <span>Manual Errors</span>
        </div>

      </div>

    </div>

    <div class="project-card">

      <div class="project-tag t2">Power BI</div>

      <h3>Executive Sales Dashboard</h3>

      <p>
        Interactive Power BI dashboard with DAX calculations,
        KPI tracking, drill-through analysis and RLS security.
      </p>

      <div class="metrics">

        <div>
          <h4>50+</h4>
          <span>DAX Measures</span>
        </div>

        <div>
          <h4>15</h4>
          <span>Pages</span>
        </div>

        <div>
          <h4>Daily</h4>
          <span>Refresh</span>
        </div>

      </div>

    </div>

    <div class="project-card">

      <div class="project-tag t3">SQL + Python</div>

      <h3>Data Warehouse Pipeline</h3>

      <p>
        ETL solution integrating multiple systems into SQL Server
        using Python automation and Power Query transformations.
      </p>

      <div class="metrics">

        <div>
          <h4>2M+</h4>
          <span>Rows/Day</span>
        </div>

        <div>
          <h4>99.8%</h4>
          <span>Uptime</span>
        </div>

        <div>
          <h4>5 Min</h4>
          <span>Latency</span>
        </div>

      </div>

    </div>

  </div>
</section>

<!-- POWER PLATFORM -->

<section class="section">

  <h2 class="section-title">Microsoft Power Platform</h2>

  <div class="tools">

    <div class="tool">Power BI Desktop</div>
    <div class="tool">Power BI Service</div>
    <div class="tool">Power Query</div>
    <div class="tool">Power Pivot</div>
    <div class="tool">Excel VBA</div>
    <div class="tool">Power Apps</div>
    <div class="tool">Power Automate</div>
    <div class="tool">SQL Server</div>
    <div class="tool">Python Pandas</div>
    <div class="tool">Azure Data Studio</div>

  </div>

</section>

<!-- CONTACT -->

<section class="section">

  <h2 class="section-title">Contact Information</h2>

  <div class="contact-grid">

    <div class="contact-card">
      <h3>Email</h3>
      <p>Abhishek10487@gmail.com</p>
    </div>

    <div class="contact-card">
      <h3>Phone</h3>
      <p>+91 8340549570</p>
    </div>

    <div class="contact-card">
      <h3>GitHub</h3>
      <a href="https://github.com/Abhishek10487" target="_blank">
        github.com/Abhishek10487
      </a>
    </div>

    <div class="contact-card">
      <h3>LinkedIn</h3>
      <a href="https://www.linkedin.com/in/abhishek-kumar-3b350923" target="_blank">
        linkedin.com/in/abhishek-kumar-3b350923
      </a>
    </div>

  </div>

  <!-- FORM -->

  <div class="form-grid">

    <div class="form-group">
      <label>Name</label>
      <input type="text" placeholder="Enter your name">
    </div>

    <div class="form-group">
      <label>Email</label>
      <input type="email" placeholder="Enter your email">
    </div>

    <div class="form-group">
      <label>Phone</label>
      <input type="text" placeholder="+91 XXXXX XXXXX">
    </div>

    <div class="form-group">
      <label>Service</label>
      <select>
        <option>Power BI Dashboard</option>
        <option>Excel Automation</option>
        <option>Power Query</option>
        <option>Power Pivot</option>
        <option>SQL Reporting</option>
      </select>
    </div>

    <div class="form-group full">
      <label>Message</label>
      <textarea placeholder="Write your project requirement..."></textarea>
    </div>

    <div class="form-group full">
      <button>Send Enquiry</button>
    </div>

  </div>

</section>

<footer>
  © 2026 Abhishek Kumar | Data Analyst Portfolio | Built for GitHub
</footer>

</body>
</html>
