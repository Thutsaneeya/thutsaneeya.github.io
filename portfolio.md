---
layout: page
title: Portfolio
---
<style>
  /* Container สำหรับจัดวางการ์ดเรียงต่อกัน */
  .project-list {
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin-top: 40px;
    width: 100%;
  }

  /* สไตล์การ์ดยาวโปร่งแสง */
  .project-row {
    display: flex;
    align-items: center;
    background: rgba(255, 255, 255, 0.02); /* โปร่งใสมาก */
    border: 1px solid rgba(63, 81, 181, 0.3); /* กรอบม่วงจางๆ */
    border-radius: 16px;
    padding: 25px 35px;
    transition: all 0.3s ease;
    text-decoration: none !important;
    gap: 25px;
  }

  /* เอฟเฟกต์ตอน Hover */
  .project-row:hover {
    background: rgba(63, 81, 181, 0.08);
    border-color: #3f51b5; /* กรอบม่วงชัดขึ้น */
    transform: translateX(10px); /* เลื่อนขวานิดๆ ดูมีมิติ */
    box-shadow: -5px 0 20px rgba(63, 81, 181, 0.2);
  }

  .row-emoji {
    font-size: 35px;
    flex-shrink: 0;
  }

  .row-content {
    flex-grow: 1;
  }

  .row-content h2 {
    margin: 0 0 5px 0 !important;
    font-size: 1.8rem !important;
    color: #c5cae9 !important; /* สีม่วงอ่อน */
    font-weight: 700;
  }

  .row-content p {
    margin: 0 !important;
    font-size: 1.1rem;
    color: #9fa8da; /* สีม่วงเทา สบายตา */
    line-height: 1.5;
  }

  /* ลูกศรชี้ขวาปิดท้าย */
  .row-arrow {
    color: #3f51b5;
    font-size: 20px;
    font-weight: bold;
    opacity: 0.5;
    transition: 0.3s;
  }

  .project-row:hover .row-arrow {
    opacity: 1;
    transform: translateX(5px);
  }

  @media (max-width: 600px) {
    .project-row { padding: 20px; gap: 15px; }
    .row-emoji { font-size: 28px; }
    .row-arrow { display: none; } /* ซ่อนลูกศรในมือถือเพื่อให้มีที่ว่าง */
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
    <a href="https://github.com/Thutsaneeya/flight_pricing" target="_blank" class="btn-view">Code 🚀</a>
  </div>

  <div class="project-card">
    <span class="project-emoji">📊</span>
    <h2>Sales Dashboard</h2>
    <p>Interactive sales performance tracking with Tableau.</p>
    <a href="#" class="btn-view">View Project</a>
  </div>

  <div class="project-card">
    <span class="project-emoji">🧪</span>
    <h2>A/B Testing</h2>
    <p>Statistical analysis for website conversion optimization.</p>
    <a href="#" class="btn-view">Read Case Study</a>
  </div>

  <div class="project-card">
    <span class="project-emoji">🧠</span>
    <h2>ML Model</h2>
    <p>Predicting customer churn using Random Forest algorithm.</p>
    <a href="#" class="btn-view">Explore GitHub</a>
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