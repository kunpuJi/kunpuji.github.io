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
     0. 强制隐藏 Cayman 主题默认顶部
     ========================================================================== */
  .page-header { display: none !important; height: 0 !important; padding: 0 !important; margin: 0 !important; overflow: hidden !important; }
  .main-content { padding-top: 0 !important; margin-top: 0 !important; max-width: 100% !important; padding: 0 !important; }

  /* ==========================================================================
     1. 全局样式重置
     ========================================================================== */
  body { font-family: 'Roboto', "Helvetica Neue", Arial, sans-serif !important; background-color: #fcfcfc; color: #333; scroll-behavior: smooth; }
  a { color: #005AB5; text-decoration: none; }
  a:hover { text-decoration: none; }

  /* ==========================================================================
     2. 顶部 Hero 区域 (全屏背景)
     ========================================================================== */
  .hero-wrapper {
    width: 100vw; position: relative; left: 50%; right: 50%; margin-left: -50vw; margin-right: -50vw;
    background-image: url('polyu.jpg'); background-size: cover; background-position: center 30%;
    padding: 100px 20px; margin-bottom: 0;
    box-shadow: inset 0 0 0 1000px rgba(10, 35, 70, 0.5);
    display: flex; justify-content: center; align-items: center;
  }

  /* ==========================================================================
     3. 个人信息卡片
     ========================================================================== */
  .profile-card {
    background: rgba(255, 255, 255, 0.98); backdrop-filter: blur(15px); padding: 50px; border-radius: 16px;
    box-shadow: 0 20px 50px rgba(0,0,0,0.2); max-width: 950px; width: 95%;
    display: flex; gap: 60px; align-items: center;
  }

  /* 左侧头像容器 */
  .card-left { flex: 0 0 auto; display: flex; justify-content: center; align-items: center; }

  /* 头像：瘦长椭圆 */
  .avatar-img {
    width: 160px; height: 220px; 
    border-radius: 50% / 50%; 
    object-fit: cover; object-position: center 20%; 
    border: 5px solid #fff; 
    box-shadow: 0 10px 25px rgba(0,0,0,0.15);
  }

  /* 右侧信息 */
  .card-right { flex: 1; text-align: left; }
  .my-name { font-size: 2.4rem; font-weight: 700; color: #005AB5; margin: 0 0 8px 0; line-height: 1.1; }
  .my-role { font-size: 1.2rem; font-weight: 500; color: #555; margin-bottom: 20px; padding-bottom: 15px; border-bottom: 2px solid #eee; }
  .my-info p { margin: 6px 0; color: #444; font-size: 1rem; line-height: 1.6; display: flex; align-items: center; }
  .my-info i { width: 28px; color: #005AB5; text-align: center; margin-right: 10px; font-size: 1.1em; }
  .social-group { margin-top: 25px; display: flex; gap: 15px; flex-wrap: wrap; }
  .social-btn { background-color: #f0f5fa; color: #005AB5 !important; padding: 10px 20px; border-radius: 8px; font-size: 0.95rem; font-weight: 600; border: 1px solid transparent; transition: all 0.2s ease; }
  .social-btn:hover { background-color: #005AB5; color: #fff !important; transform: translateY(-3px); box-shadow: 0 5px 15px rgba(0, 90, 181, 0.3); }

  /* ==========================================================================
     4. 导航栏
     ========================================================================== */
  .nav-wrapper { background: #fff; border-bottom: 1px solid #eee; padding: 15px 0; position: sticky; top: 0; z-index: 999; box-shadow: 0 4px 12px rgba(0,0,0,0.05); width: 100vw; margin-left: -50vw; left: 50%; position: relative; margin-bottom: 50px; display: flex; justify-content: center; }
  .nav-links { display: flex; flex-wrap: wrap; justify-content: center; gap: 5px; max-width: 1200px; }
  .nav-item { color: #444 !important; font-size: 0.95rem; font-weight: 600; padding: 10px 18px; border-radius: 6px; transition: all 0.2s ease; }
  .nav-item:hover { background-color: #eef4fb; color: #005AB5 !important; transform: translateY(-1px); }

  /* ==========================================================================
     5. 正文样式
     ========================================================================== */
  .content-container { max-width: 1050px; margin: 0 auto; padding: 0 20px 60px 20px; }
  h3 { font-size: 1.7rem; color: #222; border-left: 6px solid #005AB5; padding-left: 15px; margin-top: 60px; margin-bottom: 30px; font-weight: 700; }
  ul.styled-list { padding-left: 20px; }
  ul.styled-list li { margin-bottom: 12px; line-height: 1.7; color: #444; }
  .pub-item { margin-bottom: 18px; text-align: justify; line-height: 1.7; padding-left: 1.8em; text-indent: -1.8em; color: #333; font-size: 1rem; }
  h4 { margin-top: 30px; margin-bottom: 15px; font-weight: 600; color: #555; border-bottom: 1px solid #eee; padding-bottom: 5px; }

  /* ==========================================================================
     6. 回到顶部按钮 (Back To Top Button)
     ========================================================================== */
  #back-to-top {
    display: none; /* 默认隐藏 */
    position: fixed;
    bottom: 30px;
    right: 30px;
    z-index: 1000;
    width: 50px;
    height: 50px;
    border: none;
    outline: none;
    background-color: #005AB5; /* 你的主题蓝 */
    color: white;
    cursor: pointer;
    border-radius: 50%; /* 圆形 */
    box-shadow: 0 4px 15px rgba(0,0,0,0.3);
    font-size: 20px;
    transition: all 0.3s ease;
    align-items: center;
    justify-content: center;
  }
  
  #back-to-top:hover {
    background-color: #003d7a;
    transform: translateY(-5px); /* 悬停上浮 */
    box-shadow: 0 6px 20px rgba(0,0,0,0.4);
  }

  /* 移动端适配 */
  @media (max-width: 800px) {
    .profile-card { flex-direction: column; text-align: center; padding: 40px 20px; gap: 30px; }
    .card-right { text-align: center; }
    .my-info p { justify-content: center; }
    .social-group { justify-content: center; }
    .nav-item { padding: 8px 12px; font-size: 0.85rem; }
    /* 移动端按钮稍微小一点，位置靠边一点 */
    #back-to-top { width: 45px; height: 45px; bottom: 20px; right: 20px; font-size: 18px; }
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
      </div>

      <div class="social-group">
        <a href="mailto:kunpu.ji@polyu.edu.hk" class="social-btn"><i class="fas fa-paper-plane"></i> Email</a>
        <a href="https://scholar.google.com/citations?user=y5foruMAAAAJ&hl=en" target="_blank" class="social-btn"><i class="fas fa-book-open"></i> Google Scholar</a>
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
  <p style="color: #777; font-style: italic; padding: 30px; background: #f9f9f9; border-radius: 8px; text-align: center; border: 1px dashed #ddd;">Codes will be uploaded soon...</p>

  <a name="Datasets"></a>
  <h3>Datasets</h3>
  <p>
    <b>A set of seamless 0.05-degree, daily SIF product data (FGSIF)</b> <a href="https://doi.org/10.5281/zenodo.11918785" target="_blank" class="social-btn" style="padding: 4px 10px; font-size: 0.8rem; background:#fff; border:1px solid #ddd; color:#555 !important;"><i class="fas fa-database"></i> Data Link</a><br>
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

</div>

<button id="back-to-top" title="Go to top">
  <i class="fas fa-arrow-up"></i>
</button>

<script>
  // 获取按钮
  var mybutton = document.getElementById("back-to-top");

  // 监听滚动
  window.onscroll = function() {scrollFunction()};

  function scrollFunction() {
    // 滚动超过 300px 显示按钮
    if (document.body.scrollTop > 300 || document.documentElement.scrollTop > 300) {
      mybutton.style.display = "flex"; // 使用 flex 让图标居中
    } else {
      mybutton.style.display = "none";
    }
  }

  // 点击平滑滚动回顶部
  mybutton.onclick = function() {
    window.scrollTo({top: 0, behavior: 'smooth'});
  }
</script>
