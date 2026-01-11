---
layout: page
title: Portfolio
---
<style>
  /* 1. Layout หลัก - กางออกเต็มพื้นที่ใหม่ */
  .project-item {
    display: flex;
    align-items: center; /* เปลี่ยนเป็น center เพื่อความสมดุลของรูปและข้อความ */
    justify-content: space-between;
    margin-bottom: 120px;
    gap: 60px; /* เพิ่มระยะห่างให้ดูโปร่งขึ้น */
    width: 100%;
  }
  
  /* ท่าฟันปลา สลับซ้าย-ขวา */
  .project-item:nth-child(even) { 
    flex-direction: row-reverse !important; 
  }
  
  /* 2. ฝั่งรูปภาพ */
  .project-image { 
    flex: 1; 
    max-width: 500px;
  }
  .project-image img {
    width: 100%;
    border-radius: 15px; /* ปรับให้ล้อไปกับไฟล์ Sass ที่แก้ใหม่ */
    box-shadow: 0 15px 35px rgba(0,0,0,0.1);
    transition: 0.4s;
    display: block;
  }
  .project-image img:hover { transform: scale(1.03); }

  /* 3. ฝั่งข้อความ - เลิกเป็นแนวตั้งแน่นอน */
  .project-info { 
    flex: 1; 
    text-align: left;
  }

  .project-info h2 {
    margin-top: 0;
    font-size: 2.2rem !important; /* ปรับขนาดให้เข้ากับ Wrapper ใหม่ */
    color: #1a237e;
    line-height: 1.2;
  }

  .project-info p {
    font-size: 1.1rem;
    line-height: 1.8;
    color: #4b5563;
  }

  /* 4. Badges & Buttons */
  .tech-badge {
    background: #f0f4f8;
    color: #3f51b5;
    padding: 5px 15px;
    border-radius: 50px;
    font-size: 0.8rem;
    font-weight: 600;
    border: 1px solid #dbeafe;
    display: inline-block;
    margin-bottom: 8px;
    margin-right: 5px;
  }

  .btn-code {
    display: inline-flex;
    align-items: center;
    margin-top: 25px;
    padding: 12px 28px;
    background: #ffffff;
    color: #3f51b5;
    border: 2px solid #3f51b5;
    border-radius: 50px;
    text-decoration: none;
    font-weight: bold;
    transition: 0.3s;
  }
  .btn-code:hover {
    background: #3f51b5;
    color: white;
    box-shadow: 0 5px 15px rgba(63, 81, 181, 0.3);
  }

  /* 5. รองรับมือถือ */
  @media (max-width: 850px) {
    .project-item, .project-item:nth-child(even) { 
      flex-direction: column !important; 
      text-align: center; 
      gap: 30px;
    }
    .project-image { max-width: 100%; }
    .project-info { text-align: center; }
  }
</style>

<div id="projects" style="padding: 60px 5%;">

  <div class="project-item">
    <div class="project-image">
      <img src="/assets/img/airport.png" alt="Project 1">
    </div>
    <div class="project-info">
      <h2 style="margin-bottom: 8px; font-size: 1.8rem; font-weight: 800;">✈️ Flight Ticket Price Analysis</h2>
      <h3 style="display: inline-block; background: #e8eaf6; color: #3f51b5; padding: 5px 12px; border-radius: 8px; font-size: 1rem; font-weight: 700; margin-bottom: 15px; border-left: 5px solid #3f51b5;">Market Insights & Pricing Patterns</h3>
      <p style="color: #4b5563; line-height: 1.6; font-size: 1rem;">
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