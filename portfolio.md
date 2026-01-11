---
layout: page
title: Portfolio
---
<style>
  /* 1. Header & Title ส่วนกลางหน้า */
  .portfolio-header {
    text-align: center;
    padding: 60px 0 30px 0;
  }

  .portfolio-header h1 {
    font-size: 3.5rem !important;
    font-weight: 900 !important;
    color: #3f51b5 !important;
    margin: 0 !important;
    text-transform: uppercase;
    letter-spacing: -1.5px;
  }

  .portfolio-header .divider {
    width: 60px;
    height: 4px;
    background: #3f51b5;
    margin: 20px auto;
    border-radius: 10px;
  }

  /* 2. Grid 2x2 Layout */
  .project-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 25px;
    margin-top: 20px;
  }

  /* 3. การ์ดโปร่งแสง เน้นเส้นกรอบ */
  .project-card {
    background: rgba(255, 255, 255, 0.02);
    border: 1px solid rgba(63, 81, 181, 0.3);
    border-radius: 20px;
    padding: 35px 25px;
    text-align: center;
    transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    display: flex;
    flex-direction: column;
    align-items: center;
    text-decoration: none !important;
  }

  .project-card:hover {
    transform: translateY(-10px);
    border-color: #3f51b5;
    background: rgba(63, 81, 181, 0.05);
    box-shadow: 0 15px 30px rgba(63, 81, 181, 0.2);
  }

  .project-emoji {
    font-size: 45px;
    margin-bottom: 20px;
  }

 .project-card h2 {
    font-size: 1.5rem !important; /* ปรับลดจาก 1.8 ให้พอดีกับชื่อยาว */
    font-weight: 800 !important;
    color: #e8eaf6 !important; /* สีขาวอมม่วง สว่างเด่น */
    margin: 0 0 5px 0 !important;
    line-height: 1.2 !important;
    min-height: 3.6rem; /* บังคับความสูง 2 บรรทัด เพื่อให้การ์ดเท่ากัน */
    display: flex;
    align-items: center;
    justify-content: center;
  }

  /* ปรับแต่งหัวข้อรอง (H3) ให้เล็กลงและดูเป็นระเบียบ */
  .project-card h3 {
    font-size: 0.95rem !important; /* เล็กกว่า H2 ชัดเจน */
    font-weight: 500 !important;
    color: #9fa8da !important; /* สีม่วงจางลงมาหน่อย */
    margin: 0 0 15px 0 !important;
    text-transform: uppercase; /* ทำเป็นตัวพิมพ์ใหญ่เล็กๆ จะดูโปรขึ้น */
    letter-spacing: 1px;
  }

 /* ปรับเนื้อหาให้อ่านง่าย สบายตา */
  .project-card p {
    font-size: 1.15rem !important; /* ขนาดใหญ่ขึ้นแบบกำลังดี */
    color: #cfd8dc !important;    /* ปรับสีให้สว่างขึ้นอีกนิดเพื่อตัดกับพื้นหลัง */
    line-height: 1.7 !important;   /* เพิ่มระยะห่างระหว่างบรรทัด ไม่ให้ดูเบียด */
    margin-bottom: 25px !important;
    font-weight: 400;
    max-width: 90% ;              /* เว้นขอบซ้ายขวานิดหน่อยให้อ่านง่าย */
    min-height: 4.5rem;           /* ปรับความสูงขั้นต่ำตามขนาดฟอนต์ที่ใหญ่ขึ้น */
  }

/* ก้อนรวม Tech Stack */
  .tech-stack {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    justify-content: center;
    margin-bottom: 25px;
  }

  /* สไตล์แต่ละ Tag (แคปซูล) */
  .tech-badge {
    background: rgba(63, 81, 181, 0.15); /* พื้นหลังม่วงโปร่งแสง */
    color: #c5cae9; /* สีตัวอักษรม่วงอ่อน */
    border: 1px solid rgba(63, 81, 181, 0.4); /* เส้นกรอบม่วง Indigo */
    padding: 4px 12px;
    border-radius: 50px; /* ทรงแคปซูล */
    font-size: 0.75rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    transition: all 0.3s ease;
  }

  /* เอฟเฟกต์เวลาเมาส์ชี้ที่การ์ด ให้ Tag เรืองแสงตาม */
  .project-card:hover .tech-badge {
    border-color: #5c6bc0;
    background: rgba(63, 81, 181, 0.25);
    box-shadow: 0 0 10px rgba(92, 107, 192, 0.3); /* เรืองแสงอ่อนๆ */
    color: #ffffff;
  }
  
  /* 4. ปุ่ม Action */
  .project-actions {
    display: flex;
    gap: 12px;
  }

  .btn-view, .btn-demo {
    padding: 8px 18px;
    border-radius: 50px;
    font-size: 0.85rem;
    font-weight: 700;
    text-decoration: none !important;
  }

  .btn-view {
    border: 1px solid rgba(63, 81, 181, 0.5);
    color: #9fa8da !important;
  }

  .btn-demo {
    background: #3f51b5;
    color: white !important;
  }

  /* มือถือเหลือ 1 คอลัมน์ */
  @media (max-width: 768px) {
    .project-grid { grid-template-columns: 1fr; }
  }
</style>

<div class="project-grid">

  <div class="project-card">
    <span class="project-emoji">✈️</span>
    <h2>Flight Ticket Price Analysis</h2>
     <h3>Market Insights & Pricing Patterns</h3>
    <p>
        Explores the distribution and variability of flight ticket prices. Applies data cleaning and visualization to uncover actionable market insights.
    </p>
    <div class="tech-stack-container" style="display: flex; flex-wrap: wrap; gap: 6px; margin-top: 15px;">
        <span class="tech-badge">Python</span> 
        <span class="tech-badge">Pandas</span> 
        <span class="tech-badge">NumPy</span>
        <span class="tech-badge">Matplotlib</span> 
        <span class="tech-badge">Seaborn</span>
    </div>
    <a href="https://github.com/Thutsaneeya/flight_pricing" target="_blank" class="btn-view">Code</a>
  </div>

  <div class="project-card">
    <span class="project-emoji">📚</span>
    <h2>Reading Behavior Analysis: Mystery, Thriller & Crime</h2>
    <h3>Sentiment Analysis of Goodreads Dataset</h3>
    <p>
      Investigates reader preferences in the Mystery & Crime genre using the Goodreads dataset. Analyzes factors like ratings and publication years through EDA, Sentiment Analysis, and WordCloud visualization.
    </p>
    <div class="tech-stack-container" style="display: flex; flex-wrap: wrap; gap: 6px; margin-top: 15px;">
      <span class="tech-badge">Python</span> 
      <span class="tech-badge">Pandas</span> 
      <span class="tech-badge">NumPy</span>
      <span class="tech-badge">Matplotlib</span> 
      <span class="tech-badge">Seaborn</span>
      <span class="tech-badge">Plotly</span>
      <span class="tech-badge">WordCloud</span> 
      <span class="tech-badge">TextBlob</span>
    </div>
    <a href="https://github.com/Thutsaneeya/flight_pricing" class="btn-view">Code</a>
  </div>

  <div class="project-card">
    <span class="project-emoji">🍃</span>
    <h2>Thailand Mental Health</h2>
    <h3>Interactive Geospatial Visualization</h3>
    <p>
      An interactive Streamlit dashboard visualizing provincial-level mental health data in Thailand. Features year-over-year (YoY) trends, choropleth maps, heatmaps, and disease-ranking KPI cards.
    </p>
    <div class="tech-stack-container" style="display: flex; flex-wrap: wrap; gap: 6px; margin-top: 15px;">
      <span class="tech-badge">Python</span> 
      <span class="tech-badge">Pandas</span> 
      <span class="tech-badge">Plotly</span>
      <span class="tech-badge">Altair</span> 
      <span class="tech-badge">Streamlit</span>
      <span class="tech-badge">GeoJson</span>
    </div>
    <a href="https://github.com/Thutsaneeya/mental_health_dashboard" class="btn-view">Code</a>
    <a href="#" class="btn-view">Demo</a>
  </div>

  <div class="project-card">
    <span class="project-emoji">🛠️</span>
    <h2>Exploring ETL: German Credit Risk</h2>
    <h3>End-to-End Pipeline & Predictive Modeling</h3>
    <p>
      Builds a complete ETL pipeline using the German Credit Dataset. Utilizes DuckDB and SQL for high-performance data transformation, followed by a Logistic Regression model to predict customer credit risk.
    </p>
    <div class="tech-stack-container" style="display: flex; flex-wrap: wrap; gap: 6px; margin-top: 15px;">
      <span class="tech-badge">Python</span> 
      <span class="tech-badge">Pandas</span> 
      <span class="tech-badge">NumPy</span>
      <span class="tech-badge">Matplotlib</span> 
      <span class="tech-badge">Seaborn</span>
      <span class="tech-badge">DuckDB</span> 
      <span class="tech-badge">Scikit-learn</span>
    </div>
    <a href="https://github.com/Thutsaneeya/german_credit_risk" class="btn-view">Code</a>
  </div>
</div>


<!--<div id="projects" style="padding: 60px 5%;">

  <div class="project-item">
    <div class="project-image">
      <img src="/assets/img/airport.png" alt="Project 1">
    </div>
    <div class="project-info">
      <h2 style="margin-bottom: 8px; font-size: 1.8rem; font-weight: 800;">✈️ Flight Ticket Price Analysis</h2>
      <h3 style="display: inline-block; background: #e8eaf6; color: #3f51b5; padding: 5px 12px; border-radius: 8px; font-size: 1rem; font-weight: 700; margin-bottom: 15px; border-left: 5px solid #3f51b5;">Market Insights & Pricing Patterns</h3>
      <p class="project-desc">
      Explores the distribution and variability of flight ticket prices. Applies data cleaning and visualization to uncover actionable market insights.
      </p>
      <div class="tech-stack-container" style="display: flex; flex-wrap: wrap; gap: 6px; margin-top: 15px;">
        <span class="tech-badge">Python</span> 
        <span class="tech-badge">Pandas</span> 
        <span class="tech-badge">NumPy</span>
        <span class="tech-badge">Matplotlib</span> 
        <span class="tech-badge">Seaborn</span>
      </div>
      <a href="https://github.com/Thutsaneeya/flight_pricing" target="_blank" class="btn-code">Code 🚀</a>
    </div>
  </div>

  <div class="project-item">
    <div class="project-image">
      <img src="/assets/img/reading.png" alt="Project 2">
    </div>
    <div class="project-info">
      <h2 style="color: #1a237e; margin-bottom: 8px; font-size: 1.8rem; font-weight: 800;">📚 Reading Behavior Analysis: Mystery, Thriller & Crime</h2>
      <h3 style="display: inline-block; background: #e8eaf6; color: #3f51b5; padding: 5px 12px; border-radius: 8px; font-size: 1rem; font-weight: 700; margin-bottom: 15px; border-left: 5px solid #3f51b5;">Sentiment Analysis of Goodreads Dataset</h3>
      <p style="color: #4b5563; line-height: 1.6; font-size: 1rem;">
      Investigates reader preferences in the Mystery & Crime genre using the Goodreads dataset. Analyzes factors like ratings and publication years through EDA, Sentiment Analysis, and WordCloud visualization.
      </p>
      <div class="tech-stack-container" style="display: flex; flex-wrap: wrap; gap: 6px; margin-top: 15px;">
        <span class="tech-badge">Python</span> 
        <span class="tech-badge">Pandas</span> 
        <span class="tech-badge">NumPy</span>
        <span class="tech-badge">Matplotlib</span> 
        <span class="tech-badge">Seaborn</span>
        <span class="tech-badge">Plotly</span>
        <span class="tech-badge">WordCloud</span> 
        <span class="tech-badge">TextBlob</span>
      </div>
      <a href="https://github.com/Thutsaneeya/goodreads_by_genre" target="_blank" class="btn-code">Code 🚀</a>
    </div>
  </div>

  <div class="project-item">
    <div class="project-image">
      <img src="/assets/img/contemplating.png" alt="Project 3">
    </div>
    <div class="project-info">
      <h2 style="color: #1a237e; margin-bottom: 8px; font-size: 1.8rem; font-weight: 800;">
      🍃 Thailand Mental Health
      </h2>
      <h3 style="display: inline-block; background: #e8eaf6; color: #3f51b5; padding: 5px 12px; border-radius: 8px; font-size: 1rem; font-weight: 700; margin-bottom: 15px; border-left: 5px solid #3f51b5;">
      Interactive Geospatial Visualization
      </h3>
      <p style="color: #4b5563; line-height: 1.6; font-size: 1rem;">
      An interactive Streamlit dashboard visualizing provincial-level mental health data in Thailand. Features year-over-year (YoY) trends, choropleth maps, heatmaps, and disease-ranking KPI cards.
      </p>
      <div class="tech-stack-container" style="display: flex; flex-wrap: wrap; gap: 6px; margin-top: 15px;">
        <span class="tech-badge">Python</span> 
        <span class="tech-badge">Pandas</span> 
        <span class="tech-badge">Plotly</span>
        <span class="tech-badge">Altair</span> 
        <span class="tech-badge">Streamlit</span>
        <span class="tech-badge">GeoJson</span>
      </div>
      <a href="https://github.com/Thutsaneeya/mental_health_dashboard" target="_blank" class="btn-code">Code 🚀</a>
      <a href="#" target="_blank" class="btn-code">Demo 🌐</a>
    </div>
  </div>

  <div class="project-item">
    <div class="project-image">
      <img src="/assets/img/server.png" alt="Project 4">
    </div>
    <div class="project-info">
      <h2 style="color: #1a237e; margin-bottom: 8px; font-size: 1.8rem; font-weight: 800;">
      🛠️ Exploring ETL: German Credit Risk
      </h2>
      <h3 style="display: inline-block; background: #e8eaf6; color: #3f51b5; padding: 5px 12px; border-radius: 8px; font-size: 1rem; font-weight: 700; margin-bottom: 15px; border-left: 5px solid #3f51b5;">
      End-to-End Pipeline & Predictive Modeling
      </h3>
      <p style="color: #4b5563; line-height: 1.6; font-size: 1rem;">
        Builds a complete ETL pipeline using the German Credit Dataset. Utilizes DuckDB and SQL for high-performance data transformation, followed by a Logistic Regression model to predict customer credit risk.
      </p>
      <div class="tech-stack-container" style="display: flex; flex-wrap: wrap; gap: 6px; margin-top: 15px;">
        <span class="tech-badge">Python</span> 
        <span class="tech-badge">Pandas</span> 
        <span class="tech-badge">NumPy</span>
        <span class="tech-badge">Matplotlib</span> 
        <span class="tech-badge">Seaborn</span>
        <span class="tech-badge">DuckDB</span> 
        <span class="tech-badge">Scikit-learn</span>
      </div>
      <a href="https://github.com/Thutsaneeya/german_credit_risk" target="_blank" class="btn-code">Code 🚀</a>
    </div>
  </div>
</div>
-->