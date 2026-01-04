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
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">

<style>
  /* ==========================================================================
     【需求1：隐藏顶部原有的大标题栏】
     针对常见 Jekyll 主题的顶部区域进行隐藏。
     如果你的网站仍显示顶部蓝绿渐变条，请告知你的主题名称，需调整选择器。
     ========================================================================== */
  .masthead, .site-header, .page__header {
      display: none !important;
  }
  
  /* 全局字体优化 */
  body {
    font-family: 'Roboto', -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
  }

  /* ==========================================================================
     布局核心：全屏背景 Header
     ========================================================================== */
  .full-width-header {
    width: 100vw;
    position: relative;
    left: 50%;
    right: 50%;
    margin-left: -50vw;
    margin-right: -50vw;
    /* 【请确认图片路径】 如果图片在 images 文件夹下，应为 url('/images/polyu.jpg') */
    background-image: url('polyu.jpg'); 
    background-size: cover;
    background-position: center 40%; /* 稍微调整背景图对齐位置 */
    padding: 80px 20px;
    margin-top: -30px; /* 抵消掉一些默认顶部边距，让它更贴顶 */
    margin-bottom: 40px;
    /* 叠加颜色遮罩，确保文字可读性，这里用了深蓝色半透明 */
    box-shadow: inset 0 0 0 1000px rgba(0, 40, 85, 0.5); 
    display: flex;
    justify-content: center;
    align-items: center;
  }

  /* ==========================================================================
     【需求2：个人信息卡片 - 左图右文布局】
     ========================================================================== */
  .profile-card {
    background: rgba(255, 255, 255, 0.95); /* 几乎不透明的白色背景 */
    backdrop-filter: blur(12px); /* 毛玻璃效果 */
    padding: 40px;
    border-radius: 16px;
    box-shadow: 0 20px 40px rgba(0,0,0,0.25); /* 更强的立体感阴影 */
    text-align: left; /* 整体文字左对齐 */
    max-width: 850px;
    width: 92%;
  }

  /* Flex 容器：负责左右排列 */
  .profile-flex {
    display: flex;
    align-items: flex-start; /* 顶部对齐 */
    justify-content: center;
    gap: 40px; /* 左右两侧的间距 */
  }

  /* 左侧：头像区域 */
  .profile-left {
    flex: 0 0 auto; /* 固定宽度，不伸缩 */
  }

  .profile-avatar {
    width: 180px;
    height: 180px;
    border-radius: 50%;
    object-fit: cover;
    border: 4px solid #fff; /* 白边 */
    box-shadow: 0 8px 20px rgba(0,0,0,0.2);
    display: block;
  }

  /* 右侧：信息区域 */
  .profile-right {
    flex: 1; /* 占据剩余空间 */
    padding-top: 10px; /* 稍微对齐一下头像的视觉中心 */
  }

  /* 姓名样式 */
  .profile-name-inside {
    font-size: 2.4rem;
    font-weight: 700;
    color: #005AB5; /* PolyU Blue */
    margin: 0 0 10px 0;
    line-height: 1.1;
  }

  /* 职位样式 */
  .profile-role-inside {
    font-size: 1.2rem;
    color: #444;
    font-weight: 500;
    margin-bottom: 15px;
    padding-bottom: 15px;
    border-bottom: 2px solid #f0f0f0; /* 添加一条细分割线 */
  }

  /* 部门和联系方式 */
  .profile-dept {
    font-size: 1rem;
    color: #555;
    margin-bottom: 15px;
    line-height: 1.6;
  }

  .profile-contact-item {
    font-size: 0.95rem;
    color: #666;
    margin-bottom: 8px;
    display: flex;
    align-items: center;
  }
  .profile-contact-item i {
    color: #005AB5;
    width: 24px; /* 图标固定宽度，保证文字对齐 */
    margin-right: 5px;
    text-align: center;
  }

  /* 社交链接按钮栏 */
  .social-buttons {
    display: flex;
    justify-content: flex-start; /* 左对齐按钮 */
    gap: 12px;
    margin-top: 25px;
    flex-wrap: wrap;
  }
  .social-btn {
    display: inline-flex;
    align-items: center;
    padding: 8px 16px;
    background-color: #eef2f6;
    color: #005AB5;
    border-radius: 8px;
    text-decoration: none !important;
    font-size: 0.9rem;
    font-weight: 600;
    transition: all 0.2s ease;
    border: 1px solid transparent;
  }
  .social-btn i { margin-right: 8px; }
  .social-btn:hover {
    background-color: #005AB5;
    color: #fff;
    transform: translateY(-3px); /* 悬浮上移效果 */
    box-shadow: 0 5px 15px rgba(0, 90, 181, 0.2);
    border-color: #004a94;
  }

  /* ==========================================================================
     【需求3：美化导航栏 - 胶囊式菜单风格】
     ========================================================================== */
  .nav-container {
      display: flex;
      justify-content: center;
      margin-bottom: 50px;
  }
  
  .custom-nav {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px; /* 按钮之间的间距 */
    padding: 10px;
    background: #fff;
    border-radius: 50px; /* 整个导航条的圆角 */
    box-shadow: 0 5px 20px rgba(0,0,0,0.06); /* 柔和的阴影 */
    border: 1px solid #f5f5f5;
  }
  
  .custom-nav a {
    color: #555;
    text-decoration: none !important;
    font-weight: 600;
    font-size: 0.95rem;
    padding: 10px 18px; /* 增加内边距，让它看起来像按钮 */
    border-radius: 30px; /* 单个链接的胶囊形状 */
    transition: all 0.3s ease;
    letter-spacing: 0.5px;
  }
  
  /* 导航链接悬停效果 */
  .custom-nav a:hover {
    background-color: #005AB5; /* PolyU Blue 背景 */
    color: #fff !important; /* 白色文字 */
    transform: translateY(-2px); /* 微微上浮 */
    box-shadow: 0 4px 10px rgba(0, 90, 181, 0.3);
  }

  /* ==========================================================================
     其他内容区域样式优化
     ========================================================================== */
  h3 {
    border-left: 6px solid #005AB5;
    padding-left: 15px;
    margin-top: 50px;
    margin-bottom: 25px;
    font-size: 1.6rem;
    font-weight: 700;
    color: #222;
  }
  
  /* 论文列表间距和对齐 */
  .pub-item {
    margin-bottom: 18px;
    text-align: justify;
    line-height: 1.6;
    padding-left: 2em;
    text-indent: -2em; /* 悬挂缩进，让序号突出 */
  }
  
  /* 列表样式优化 */
  ul.styled-list {
      padding-left: 25px;
  }
  ul.styled-list li {
    margin-bottom: 12px;
    line-height: 1.6;
  }

  /* 响应式适配：手机端恢复上下布局 */
  @media (max-width: 768px) {
    .profile-flex {
      flex-direction: column; /* 改为垂直排列 */
      align-items: center;
      text-align: center;
      gap: 25px;
    }
    .profile-right {
      text-align: center;
      padding-top: 0;
    }
    .profile-avatar {
      width: 150px;
      height: 150px;
    }
    .profile-name-inside { font-size: 2rem; }
    .profile-role-inside { 
        justify-content: center; 
        border-bottom: none;
    }
    .profile-contact-item { justify-content: center; }
    .social-buttons { justify-content: center; }
    
    /* 手机端导航栏调整 */
    .custom-nav {
        border-radius: 20px;
        gap: 5px;
    }
    .custom-nav a {
        padding: 8px 12px;
        font-size: 0.85rem;
    }
  }
</style>

<div class="full-width-header">
  <div class="profile-card">
    
    <div class="profile-flex">
      
      <div class="profile-left">
        <img src="kunpuji.jpg" alt="Kunpu Ji" class="profile-avatar">
      </div>

      <div class="profile-right">
        <div class="profile-name-inside">Kunpu Ji (嵇昆浦)</div>
        <div class="profile-role-inside">Postdoctoral Researcher</div>
        
        <div class="profile-dept">
          Department of Land Surveying and Geo-Informatics (LSGI)<br>
          The Hong Kong Polytechnic University (PolyU)
        </div>

        <div class="profile-contact-item">
          <i class="fas fa-map-marker-alt"></i> 
          <span>11 Yuk Choi Road, Hung Hom, Kowloon, Hong Kong</span>
        </div>
        <div class="profile-contact-item">
          <i class="fas fa-envelope"></i>
          <span>kunpu.ji@polyu.edu.hk</span>
        </div>

        <div class="social-buttons">
          <a href="mailto:kunpu.ji@polyu.edu.hk" class="social-btn"><i class="fas fa-paper-plane"></i> Email</a>
          <a href="https://scholar.google.com/citations?user=y5foruMAAAAJ&hl=en" target="_blank" class="social-btn"><i class="fas fa-graduation-cap"></i> Google Scholar</a>
          <a href="https://www.researchgate.net/profile/Qunming_Wang" target="_blank" class="social-btn"><i class="fab fa-researchgate"></i> ResearchGate</a>
        </div>
      </div>
    </div> </div>
</div>

<div class="nav-container">
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
</div>

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
  <b>A set of seamless 0.05-degree, daily SIF product data (FGSIF)</b> <a href="https://doi.org/10.5281/zenodo.11918785" target="_blank" class="social-btn" style="padding: 4px 10px; font-size: 0.8rem;"><i class="fas fa-database"></i> Data Link</a><br>
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
