<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

<style>
  /* ==========================================================================
     核心布局：全屏背景
     ========================================================================== */
  .full-width-header {
    width: 100vw;
    position: relative;
    left: 50%;
    right: 50%;
    margin-left: -50vw;
    margin-right: -50vw;
    background-image: url('polyu.jpg'); /* 【背景图片路径】 */
    background-size: cover;
    background-position: center;
    padding: 80px 20px;
    margin-bottom: 40px;
    box-shadow: inset 0 0 0 1000px rgba(0, 40, 85, 0.4); /* 加深一点遮罩，突出卡片 */
    display: flex;
    justify-content: center;
    align-items: center;
  }

  /* ==========================================================================
     个人信息悬浮卡片 (左右布局)
     ========================================================================== */
  .profile-card {
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    padding: 40px;
    border-radius: 12px;
    box-shadow: 0 15px 35px rgba(0,0,0,0.2);
    max-width: 900px;
    width: 95%;
    
    /* 关键：启用 Flexbox 实现左右布局 */
    display: flex;
    align-items: center; /* 垂直居中 */
    justify-content: center;
    gap: 50px; /* 左右两栏的间距 */
  }

  /* --- 左侧：头像区域 --- */
  .profile-left {
    flex: 0 0 auto; /* 不缩放 */
  }

  .profile-avatar {
    width: 220px;       /* 稍微加大一点头像 */
    height: 220px;
    border-radius: 50%;
    object-fit: cover;
    border: 5px solid #fff;
    box-shadow: 0 8px 20px rgba(0,0,0,0.15);
    display: block;
  }

  /* --- 右侧：信息区域 --- */
  .profile-right {
    text-align: left; /* 文字左对齐 */
    flex: 1;
  }

  .profile-name {
    font-size: 2.2rem;
    font-weight: 700;
    color: #005AB5;
    margin-bottom: 8px;
    line-height: 1.2;
  }

  .profile-role {
    font-size: 1.2rem;
    color: #444;
    font-weight: 600;
    margin-bottom: 15px;
  }

  .profile-dept {
    font-size: 1rem;
    color: #666;
    margin-bottom: 15px;
    line-height: 1.5;
  }

  .profile-info-item {
    font-size: 0.95rem;
    color: #555;
    margin-bottom: 8px;
    display: flex;
    align-items: center;
  }
  .profile-info-item i {
    color: #005AB5;
    width: 20px;     /* 固定宽度对齐图标 */
    margin-right: 8px;
    text-align: center;
  }

  /* 社交链接按钮 */
  .social-buttons {
    display: flex;
    gap: 12px;
    margin-top: 25px;
    flex-wrap: wrap;
  }
  .social-btn {
    display: inline-flex;
    align-items: center;
    padding: 6px 14px;
    background-color: #f0f4f8;
    color: #005AB5;
    border-radius: 6px;
    text-decoration: none !important;
    font-size: 0.9rem;
    font-weight: 500;
    transition: all 0.2s ease;
  }
  .social-btn:hover {
    background-color: #005AB5;
    color: #fff;
    transform: translateY(-2px);
  }

  /* --- 响应式适配：手机端变为上下布局 --- */
  @media (max-width: 768px) {
    .profile-card {
      flex-direction: column; /* 改为垂直排列 */
      text-align: center;
      padding: 30px 20px;
      gap: 20px;
    }
    .profile-right {
      text-align: center; /* 手机端居中对齐 */
    }
    .profile-avatar {
      width: 160px;
      height: 160px;
    }
    .profile-info-item {
      justify-content: center; /* 手机端图标文字居中 */
    }
    .social-buttons {
      justify-content: center;
    }
  }

  /* ==========================================================================
     导航栏与正文样式 (保持不变)
     ========================================================================== */
  .custom-nav {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 15px;
    margin-bottom: 40px;
    padding-bottom: 20px;
    border-bottom: 1px solid #eee;
  }
  .custom-nav a {
    color: #555;
    text-decoration: none !important;
    font-weight: 500;
    padding: 8px 12px;
    border-radius: 4px;
    transition: all 0.2s;
  }
  .custom-nav a:hover {
    background-color: #eef2f6;
    color: #005AB5;
  }

  h3 {
    border-left: 5px solid #005AB5;
    padding-left: 12px;
    margin-top: 40px;
    font-size: 1.4rem;
    color: #333;
  }
  
  .pub-item {
    margin-bottom: 15px;
    text-align: justify;
  }
  ul.styled-list li {
    margin-bottom: 10px;
  }
</style>

<div class="full-width-header">
  <div class="profile-card">
    
    <div class="profile-left">
      <img src="kunpuji.jpg" alt="Kunpu Ji" class="profile-avatar">
    </div>

    <div class="profile-right">
      <div class="profile-name">Kunpu Ji (嵇昆浦)</div>
      <div class="profile-role">Postdoctoral Researcher</div>
      
      <div class="profile-dept">
        Department of Land Surveying and Geo-Informatics (LSGI)<br>
        The Hong Kong Polytechnic University (PolyU)
      </div>

      <div class="profile-info-item">
        <i class="fas fa-map-marker-alt"></i> 
        <span>11 Yuk Choi Road, Hung Hom, Kowloon, Hong Kong</span>
      </div>
      <div class="profile-info-item">
        <i class="fas fa-envelope"></i>
        <span>kunpu.ji@polyu.edu.hk</span>
      </div>

      <div class="social-buttons">
        <a href="mailto:kunpu.ji@polyu.edu.hk" class="social-btn"><i class="fas fa-paper-plane"></i> Email</a>
        <a href="https://scholar.google.com/citations?user=y5foruMAAAAJ&hl=en" class="social-btn"><i class="fas fa-graduation-cap"></i> Google Scholar</a>
        <a href="https://www.researchgate.net/profile/Qunming_Wang" class="social-btn"><i class="fab fa-researchgate"></i> ResearchGate</a>
        <a href="https://github.com/your-github-id" class="social-btn"><i class="fab fa-github"></i> GitHub</a>
      </div>
    </div>

  </div>
</div>

<nav class="custom-nav">
  <a href="#News">News</a>
  <a href="#Research">Research Interests</a>
  <a href="#Education">Education</a>
  <a href="#Experience">Experience</a>
  <a href="#Publications">Publications</a>
  <a href="#Codes">Codes</a>
  <a href="#Datasets">Datasets</a>
  <a href="#Professional">Services</a>
  <a href="#Awards">Awards</a>
</nav>

<a name="News"></a>
<h3>News</h3>
<ul class="styled-list">
  <li><b>10/2025:</b> A paper on soil moisture data reconstruction is published in <b>RSE</b>. <a href="https://www.sciencedirect.com/science/article/pii/S0034425725002457">[Link]</a></li>
  <li><b>03/2025:</b> A paper on subpixel mapping is published in <b>RSE</b>. <a href="https://www.sciencedirect.com/science/article/abs/pii/S0034425724005406">[Link]</a></li>
  <li><b>05/2024:</b> A paper on Landsat LST gap filling is published in <b>RSE</b>. <a href="https://www.sciencedirect.com/science/article/pii/S0034425724001536">[Link]</a></li>
  <li><b>06/2023:</b> A paper on 30 m young forest age in China is accepted by <b>ESSD</b>.</li>
  <li><b>03/2022:</b> A paper on haze removal is published in <b>RSE</b>. <a href="https://www.sciencedirect.com/science/article/pii/S0034425722001262">[Link]</a></li>
</ul>

<a name="Research"></a>
<h3>Research Interests</h3>
<ul class="styled-list">
  <li>Geodetic data processing theory (Parameter estimation, VCE, Quality control, Time series analysis)</li>
  <li>GNSS-based Hydrogeodesy</li>
  <li>Filtering of GRACE time-variable gravity field solutions and related applications</li>
</ul>

<a name="Education"></a>
<h3>Education</h3>
<ul class="styled-list">
  <li><b>09/2021 – 05/2025:</b> Ph.D. in Geodesy, Tongji University, China</li>
  <li><b>09/2017 – 06/2020:</b> M.S. in Surveying Engineering, Tongji University, China</li>
  <li><b>09/2013 – 06/2017:</b> B.S. in Surveying Engineering, Nanjing Tech University, China</li>
</ul>

<a name="Experience"></a>
<h3>Professional Experience</h3>
<ul class="styled-list">
  <li><b>10/2025 – Present:</b> Postdoctoral Research Fellow, The Hong Kong Polytechnic University (PolyU)</li>
  <li><b>06/2025 – 09/2025:</b> Research Assistant, Tongji University, Shanghai</li>
  <li><b>07/2020 – 07/2021:</b> Senior GNSS Algorithm Engineer, Qianxun Spatial Intelligence Inc.</li>
</ul>

<a name="Publications"></a>
<h3>Publications</h3>

<h4>2025</h4>
<div class="pub-item">[6] <b>K. Ji</b>, Y. Shen, F. Wang. Minimum Norm Least Squares Wavelet Filtering for Processing Incomplete Geodetic Time Series. <i>IEEE Transactions on Geoscience and Remote Sensing</i>, 2025, 63: 1-19.</div>
<div class="pub-item">[5] <b>K. Ji</b>, Y. Shen, N. Sneeuw, et al. Least Squares Fourier Filter for Processing Incomplete and Heterogeneous GNSS Position Time Series. <i>GPS Solutions</i>, 2025, 29: 130.</div>
<div class="pub-item">[4] <b>K. Ji</b>, L. Zhang, F. Wang. Filtering Unevenly Spaced Geophysical Time Series as an Ill-Posed Problem. <i>Surveys in Geophysics</i>, 2025. (Accepted)</div>
<div class="pub-item">[3] <b>K. Ji</b>, Y. Shen, F. Wang, et al. An Efficient Improved Singular Spectrum Analysis for Processing GNSS Position Time Series with Missing Data. <i>Geophysical Journal International</i>, 2025, 240(1): 189-200.</div>
<div class="pub-item">[2] <b>K. Ji</b>, Y. Shen, N. Sneeuw, et al. A Recursive Regularized Solution to Geophysical Linear Ill-Posed Inverse Problems. <i>IEEE Transactions on Geoscience and Remote Sensing</i>, 2025, 63: 1-14.</div>
<div class="pub-item">[1] <b>K. Ji</b>, F. Wang. Some New Insights into Efficient ISSA for Processing Incomplete Geodetic Time Series. <i>Acta Geodynamica et Geomaterialia</i>, 2025, 22(4): 531-544.</div>

<h4>2024</h4>
<div class="pub-item">[2] <b>K. Ji</b>, Y. Shen, F. Wang, Q. Chen, L. Zhang. Extended Multiresolution Analysis for Filtering Incomplete Heterogeneous Geophysical Time Series. <i>IEEE Transactions on Geoscience and Remote Sensing</i>, 2024, 62: 1-13.</div>
<div class="pub-item">[1] <b>嵇昆浦</b>, 沈云中, 陈秋杰. GRACE时变重力场模型的自适应正则化滤波方法. <i>武汉大学学报(信息科学版)</i>, 2024, 49(11): 2101-2112.</div>

<h4>2023</h4>
<div class="pub-item">[2] <b>K. Ji</b>, Y. Shen, Q. Chen, F. Wang. Extended Singular Spectrum Analysis for Processing Incomplete Heterogeneous Geodetic Time Series. <i>Journal of Geodesy</i>, 2023, 97(8): 74.</div>
<div class="pub-item">[1] <b>K. Ji</b>, Y. Shen, Q. Chen, T. Feng. Extended Principal Component Analysis for Spatiotemporal Filtering of Incomplete Heterogeneous GNSS Position Time Series. <i>IEEE Transactions on Geoscience and Remote Sensing</i>, 2023, 61: 1-19.</div>

<h4>2022</h4>
<div class="pub-item">[1] <b>K. Ji</b>, Y. Shen, Q. Chen, B. Li, W. Wang. An Adaptive Regularized Solution to Inverse Ill-posed Models. <i>IEEE Transactions on Geoscience and Remote Sensing</i>, 2022, 60: 1-15.</div>

<h4>2020</h4>
<div class="pub-item">[3] <b>K. Ji</b>, Y. Shen, F. Wang. Signal Extraction from GNSS Position Time Series Using Weighted Wavelet Analysis. <i>Remote Sensing</i>, 2020, 12.</div>
<div class="pub-item">[2] <b>嵇昆浦</b>, 沈云中. 含缺值GNSS基准站坐标序列的非插值小波分析与信号提取. <i>测绘学报</i>, 2020, 49(05).</div>
<div class="pub-item">[1] <b>嵇昆浦</b>, 沈云中. TSVD正则化解法的单位权方差无偏估计. <i>武汉大学学报(信息科学版)</i>, 2020, 45(04).</div>

<a name="Codes"></a>
<h3>Codes</h3>
<p style="color: #666; font-style: italic;">Codes will be uploaded soon...</p>

<a name="Datasets"></a>
<h3>Datasets</h3>
<p>
  <b>A set of seamless 0.05-degree, daily SIF product data (FGSIF)</b> <a href="https://doi.org/10.5281/zenodo.11918785">[Data Link]</a><br>
  <span style="font-size: 0.9em; color: #555;">J. Li, Q. Wang*, P. M. Atkinson. Filling gaps in global daily TROPOMI solar-induced chlorophyll fluorescence data from 2018 to 2021. IEEE Transactions on Geoscience and Remote Sensing, 2025, 63: 4413515.</span>
</p>

<a name="Professional"></a>
<h3>Professional Service</h3>
<p><b>Journal Reviewer:</b></p>
<ul class="styled-list">
  <li>Advances in Space Research</li>
  <li>Journal of Geodesy</li>
</ul>

<a name="Awards"></a>
<h3>Awards & Honors</h3>
<ul class="styled-list">
  <li><b>2025:</b> Excellent Doctoral Dissertation of Tongji University (Top 2)</li>
  <li><b>2025:</b> Outstanding Graduate of Tongji University</li>
  <li><b>2024:</b> China Scholarship Council (CSC) Scholarship</li>
  <li><b>2023:</b> National Scholarship for Doctoral Students</li>
  <li><b>2023:</b> Outstanding Student of Tongji University</li>
  <li><b>2020:</b> Excellent Master's Dissertation of Tongji University (Top 2)</li>
  <li><b>2018:</b> Second Prize, The 15th "Huawei Cup" China Postgraduate Mathematical Contest in Modeling</li>
</ul>
