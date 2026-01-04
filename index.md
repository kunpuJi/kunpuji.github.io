---
permalink: /
title: "About Me"
excerpt: "About Me"
author_profile: false
classes: wide
redirect_from: 
  - /about/
  - /about.html
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">

<style>
  /* ==========================================================================
     【关键修复】针对 Cayman 主题的暴力隐藏补丁
     ========================================================================== */
  /* 隐藏 Cayman 主题默认的顶部大标题栏 */
  .page-header {
    display: none !important;
    height: 0 !important;
    padding: 0 !important;
    margin: 0 !important;
    overflow: hidden !important;
  }
  
  /* 移除 Cayman 默认的主体内容边距，防止顶部留白 */
  .main-content {
    padding-top: 0 !important;
    margin-top: 0 !important;
    /* 在宽屏模式下允许内容更宽 */
    max-width: 100% !important; 
    padding: 0 !important;
  }

  /* ==========================================================================
     全局字体与布局重置
     ========================================================================== */
  body {
    font-family: 'Roboto', "Helvetica Neue", Helvetica, Arial, sans-serif !important;
    background-color: #fdfdfd; /* 极淡的灰白背景，不刺眼 */
    color: #333;
  }
  
  /* 链接颜色 */
  a { color: #005AB5; text-decoration: none; }
  a:hover { text-decoration: none; }

  /* ==========================================================================
     1. 顶部全屏背景图 (Full Width Hero)
     ========================================================================== */
  .hero-wrapper {
    width: 100vw;
    position: relative;
    left: 50%; 
    right: 50%;
    margin-left: -50vw;
    margin-right: -50vw;
    
    /* 【背景图设置】请确保 images 文件夹下有 polyu.jpg */
    background-image: url('polyu.jpg'); 
    background-size: cover;
    background-position: center;
    padding: 80px 20px;
    margin-bottom: 0; /* 下方紧接导航栏 */
    
    /* 叠加深色遮罩，让卡片更突出 */
    box-shadow: inset 0 0 0 1000px rgba(13, 44, 84, 0.4); 
    
    display: flex;
    justify-content: center;
    align-items: center;
  }

  /* ==========================================================================
     2. 个人信息卡片 (Glassmorphism 风格)
     ========================================================================== */
  .profile-card {
    background: rgba(255, 255, 255, 0.96); /* 高不透明度白色 */
    backdrop-filter: blur(10px);
    padding: 45px;
    border-radius: 12px;
    box-shadow: 0 15px 40px rgba(0,0,0,0.15); /* 柔和的高级阴影 */
    max-width: 900px;
    width: 95%;
    display: flex; /* 启用 Flexbox 左右布局 */
    gap: 50px;
    align-items: flex-start;
  }

  /* 左侧：头像 */
  .card-left {
    flex: 0 0 auto;
  }
  .avatar-img {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
    border: 6px solid #fff;
    box-shadow: 0 8px 20px rgba(0,0,0,0.12);
  }

  /* 右侧：信息 */
  .card-right {
    flex: 1;
    text-align: left; /* 强制左对齐 */
    padding-top: 10px;
  }

  .my-name {
    font-size: 2.2rem;
    font-weight: 700;
    color: #005AB5; /* PolyU Blue */
    margin: 0 0 5px 0;
    line-height: 1.2;
  }
  
  .my-role {
    font-size: 1.1rem;
    font-weight: 500;
    color: #444;
    margin-bottom: 15px;
    padding-bottom: 15px;
    border-bottom: 2px solid #f0f0f0; /* 细分割线 */
  }

  .my-info p {
    margin: 5px 0;
    color: #555;
    font-size: 0.95rem;
    line-height: 1.5;
    display: flex;
    align-items: center;
  }
  
  .my-info i {
    width: 25px;
    color: #005AB5;
    text-align: center;
    margin-right: 8px;
  }

  /* 社交按钮组 */
  .social-group {
    margin-top: 25px;
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
  }
  
  .social-btn {
    background-color: #f2f7fc;
    color: #005AB5 !important;
    padding: 8px 16px;
    border-radius: 6px;
    font-size: 0.9rem;
    font-weight: 600;
    border: 1px solid transparent;
    transition: all 0.2s;
  }
  
  .social-btn:hover {
    background-color: #005AB5;
    color: #fff !important;
    transform: translateY(-2px);
    box-shadow: 0 4px 12px rgba(0, 90, 181, 0.2);
  }

  /* ==========================================================================
     3. 导航栏 (现代化胶囊样式)
     ========================================================================== */
  .nav-wrapper {
    background: #fff;
    border-bottom: 1px solid #eaeaea;
    padding: 15px 0;
    position: sticky; /* 吸顶效果 (可选) */
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 10px rgba(0,0,0,0.03);
    
    /* 强制全宽背景 */
    width: 100vw;
    margin-left: -50vw;
    left: 50%;
    position: relative;
    margin-bottom: 40px;
    display: flex;
    justify-content: center;
  }

  .nav-links {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 8px;
    max-width: 1200px;
  }

  .nav-item {
    color: #555 !important;
    font-size: 0.95rem;
    font-weight: 500;
    padding: 8px 16px;
    border-radius: 20px; /* 胶囊圆角 */
    transition: all 0.2s ease;
  }

  .nav-item:hover {
    background-color: #eef4fa;
    color: #005AB5 !important;
  }

  /* ==========================================================================
     4. 正文内容区域布局
     ========================================================================== */
  .content-container {
    max-width: 1000px; /* 限制正文宽度，防止太宽难看 */
    margin: 0 auto;
    padding: 0 20px;
  }

  h3 {
    font-size: 1.6rem;
    color: #222;
    border-left: 5px solid #005AB5; /* 左侧蓝色竖线 */
    padding-left: 15px;
    margin-top: 50px;
    margin-bottom: 25px;
  }

  /* 列表优化 */
  ul.styled-list {
    padding-left: 20px;
  }
  ul.styled-list li {
    margin-bottom: 12px;
    line-height: 1.6;
  }

  /* 论文列表项 */
  .pub-item {
    margin-bottom: 16px;
    text-align: justify;
    line-height: 1.6;
    padding-left: 1.5em;
    text-indent: -1.5em; /* 悬挂缩进 */
    color: #333;
  }

  /* ==========================================================================
     响应式适配 (手机端)
     ========================================================================== */
  @media (max-width: 768px) {
    .profile-card {
      flex-direction: column;
      align-items: center;
      text-align: center;
      padding: 30px 20px;
      gap: 20px;
    }
    .card-right {
      text-align: center;
      padding-top: 0;
    }
    .avatar-img {
      width: 150px;
      height: 150px;
    }
    .my-role {
      border-bottom: none;
      margin-bottom: 10px;
    }
    .my-info p {
      justify-content: center;
    }
    .social-group {
      justify-content: center;
    }
    /* 导航栏手机端微调 */
    .nav-item {
      padding: 6px 12px;
      font-size: 0.85rem;
      background-color: #f5f5f5; /* 手机端加个底色区分 */
    }
  }
</style>

<div class="hero-wrapper">
  <div class="profile-card">
    <div class="card-left">
      <img src="kunpuji.jpg" alt="Kunpu Ji" class="avatar-img">
    </div>
    
    <div class="card-right">
      <div class="my-name">Kunpu Ji (嵇昆浦)</div>
      <div class="my-role">Postdoctoral Researcher</div>
      
      <div class="my-info">
        <p><i class="fas fa-university"></i> Department of Land Surveying and Geo-Informatics (LSGI)</p>
        <p><i class="fas fa-graduation-cap"></i> The Hong Kong Polytechnic University (PolyU)</p>
        <p><i class="fas fa-map-marker-alt"></i> 11 Yuk Choi Road, Hung Hom, Kowloon, Hong Kong</p>
        <p><i class="fas fa-envelope"></i> kunpu.ji@polyu.edu.hk</p>
      </div>

      <div class="social-group">
        <a href="mailto:kunpu.ji@polyu.edu.hk" class="social-btn"><i class="fas fa-paper-plane"></i> Email</a>
        <a href="https://scholar.google.com/citations?user=y5foruMAAAAJ&hl=en" target="_blank" class="social-btn"><i class="fas fa-book"></i> Google Scholar</a>
        <a href="https://www.researchgate.net/profile/Qunming_Wang" target="_blank" class="social-btn"><i class="fab fa-researchgate"></i> ResearchGate</a>
        <a href="#" class="social-btn"><i class="fab fa-github"></i> GitHub</a>
      </div>
    </div>
  </div>
</div>

<div class="nav-wrapper">
  <div class="nav-links">
    <a href="#News" class="nav-item">News</a>
    <a href="#Research" class="nav-item">Research Interests</a>
    <a href="#Education" class="nav-item">Education</a>
    <a href="#Experience" class="nav-item">Experience</a>
    <a href="#Publications" class="nav-item">Publications</a>
    <a href="#Codes" class="nav-item">Codes</a>
    <a href="#Datasets" class="nav-item">Datasets</a>
    <a href="#Professional" class="nav-item">Services</a>
    <a href="#Awards" class="nav-item">Awards</a>
  </div>
</div>

<div class="content-container">

  <a name="News"></a>
  <h3>News</h3>
  <ul class="styled-list">
    <li><b>10/2025:</b> A paper on soil moisture data reconstruction is published in <b>RSE</b>. <a href="https://www.sciencedirect.com/science/article/pii/S0034425725002457" target="_blank">[Link]</a></li>
    <li><b>03/2025:</b> A paper on subpixel mapping is published in <b>RSE</b>. <a href="https://www.sciencedirect.com/science/article/abs/pii/S0034425724005406" target="_blank">[Link]</a></li>
    <li><b>05/2024:</b> A paper on Landsat LST gap filling is published in <b>RSE</b>. <a href="https://www.sciencedirect.com/science/article/pii/S0034425724001536" target="_blank">[Link]</a></li>
    <li><b>06/2023:</b> A paper on 30 m young forest age in China is accepted by <b>ESSD</b>.</li>
    <li><b>03/2022:</b> A paper on haze removal is published in <b>RSE</b>. <a href="https://www.sciencedirect.com/science/article/pii/S0034425722001262" target="_blank">[Link]</a></li>
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
  <p style="color: #777; font-style: italic; padding: 20px; background: #f9f9f9; border-radius: 8px; text-align: center;">Codes will be uploaded soon...</p>

  <a name="Datasets"></a>
  <h3>Datasets</h3>
  <p>
    <b>A set of seamless 0.05-degree, daily SIF product data (FGSIF)</b> <a href="https://doi.org/10.5281/zenodo.11918785" target="_blank" class="social-btn" style="padding: 4px 10px; font-size: 0.8rem; background:#fff; border:1px solid #ccc;"><i class="fas fa-database"></i> Data Link</a><br>
    <span style="font-size: 0.95em; color: #555; display: block; margin-top: 5px;">J. Li, Q. Wang*, P. M. Atkinson. Filling gaps in global daily TROPOMI solar-induced chlorophyll fluorescence data from 2018 to 2021. IEEE Transactions on Geoscience and Remote Sensing, 2025, 63: 4413515.</span>
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

</div> ```
