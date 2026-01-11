---
layout: page
title: Portfolio
---
<style>
  /* 1. ปรับ Container ให้กว้างขึ้นและกางออก */
  .project-item {
    display: flex;
    align-items: center;
    justify-content: center; /* เปลี่ยนเป็น center เพื่อความบาลานซ์ */
    margin-bottom: 120px;
    gap: 80px; /* เพิ่มช่องว่างระหว่างรูปกับข้อความ */
    width: 100%;
    max-width: 1100px; /* บังคับความกว้างสูงสุด */
    margin-left: auto;
    margin-right: auto;
  }
  
  /* บังคับสลับฝั่งฟันปลา */
  .project-item:nth-child(even) { 
    flex-direction: row-reverse !important; 
  }
  
  /* 2. สัดส่วนรูปภาพ */
  .project-image { 
    flex: 1; /* สัดส่วน 1 ต่อ 1.2 */
    min-width: 400px; /* กันไม่ให้รูปเล็กเกินไป */
  }
  .project-image img {
    width: 100%;
    border-radius: 20px;
    box-shadow: 0 20px 40px rgba(0,0,0,0.1);
    transition: 0.4s;
    display: block;
  }

  /* 3. สัดส่วนข้อความ - ปรับให้กางออก (Balanced) */
  .project-info { 
    flex: 1.2; 
    text-align: left; /* บังคับชิดซ้ายไม่ว่าธีมจะตั้งมายังไง */
  }

  /* 4. Typography & Badges */
  .project-info h2 {
    font-size: 2.2rem !important; /* ใหญ่ขึ้นนิดนึงให้ดูเป็นหัวข้อ */
    line-height: 1.2;
  }
  
  .project-info p {
    font-size: 1.1rem;
    line-height: 1.8; /* เพิ่มระยะห่างบรรทัดให้อ่านง่าย */
    color: #4b5563;
    margin-top: 15px;
    width: 100%; /* กางข้อความให้เต็มพื้นที่ flex */
  }

  .tech-badge {
    background: #f0f4f8;
    color: #3f51b5;
    padding: 5px 15px;
    border-radius: 50px;
    font-size: 0.8rem;
    font-weight: 600;
    border: 1px solid #dbeafe;
    display: inline-block;
    margin-bottom: 5px;
  }

  .btn-code {
    display: inline-flex;
    align-items: center;
    margin-top: 30px;
    padding: 12px 28px;
    background: #ffffff;
    color: #3f51b5;
    border: 2px solid #3f51b5;
    border-radius: 50px;
    text-decoration: none;
    font-weight: bold;
    transition: 0.3s;
  }
  .btn-code:hover { background: #3f51b5; color: white; }

  /* 5. Responsive Design (มือถือ) */
  @media (max-width: 900px) {
    .project-item, .project-item:nth-child(even) { 
      flex-direction: column !important; 
      text-align: center !important; 
      gap: 40px;
    }
    .project-info { text-align: center; }
    .project-image { min-width: 100%; }
    .tech-stack-container { justify-content: center; }
  }
</style>

<div id="projects" style="padding: 60px 5%;">

  <div class="project-item">
    <div class="project-image">
      <img src="/assets/img/airport.png" alt="Project 1">
    </div>
    <div class="project-info">
      <h2 style="color: #1a237e; margin-bottom: 8px; font-size: 1.8rem; font-weight: 800;">✈️ Flight Ticket Price Analysis</h2>
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