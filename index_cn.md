---
permalink: /cn/
title: "关于我"
excerpt: "关于我"
author_profile: false
layout: default
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">

<style>
  /* 样式与英文版保持一致 */
  .page-header { display: none !important; height: 0 !important; padding: 0 !important; margin: 0 !important; overflow: hidden !important; }
  .main-content { padding-top: 0 !important; margin-top: 0 !important; max-width: 100% !important; padding: 0 !important; }
  body { font-family: 'Roboto', "Microsoft YaHei", Arial, sans-serif !important; background-color: #fcfcfc; color: #333; scroll-behavior: smooth; }
  a { color: #005AB5; text-decoration: none; }
  a:hover { text-decoration: none; }

  .hero-wrapper {
    width: 100vw; position: relative; left: 50%; right: 50%; margin-left: -50vw; margin-right: -50vw;
    background-image: url('../polyu.jpg'); /* 适配 /cn/ 路径 */
    background-size: cover; background-position: center 30%;
    padding: 100px 20px; margin-bottom: 0;
    box-shadow: inset 0 0 0 1000px rgba(10, 35, 70, 0.5);
    display: flex; justify-content: center; align-items: center;
  }

  .lang-switch { position: absolute; top: 30px; right: 30px; z-index: 1002; }
  .lang-btn {
    text-decoration: none; background: rgba(255, 255, 255, 0.9); backdrop-filter: blur(5px);
    border: 1px solid rgba(255,255,255,0.5); padding: 8px 18px; border-radius: 30px;
    font-size: 0.9rem; font-weight: bold; color: #333; box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    transition: all 0.3s ease; display: inline-flex; align-items: center; gap: 6px;
  }
  .lang-btn:hover { background-color: #005AB5; color: #fff !important; transform: translateY(-2px); }

  .profile-card {
    background: rgba(255, 255, 255, 0.98); backdrop-filter: blur(15px); padding: 50px; border-radius: 16px;
    box-shadow: 0 20px 50px rgba(0,0,0,0.2); max-width: 950px; width: 95%;
    display: flex; gap: 60px; align-items: center;
  }
  .card-left { flex: 0 0 auto; display: flex; justify-content: center; align-items: center; }
  .avatar-img {
    width: 160px; height: 220px; border-radius: 50% / 50%; 
    object-fit: cover; object-position: center 20%; 
    border: 5px solid #fff; box-shadow: 0 10px 25px rgba(0,0,0,0.15);
  }
  .card-right { flex: 1; text-align: left; }
  .my-name { font-size: 2.4rem; font-weight: 700; color: #005AB5; margin: 0 0 8px 0; line-height: 1.1; }
  .my-role { font-size: 1.2rem; font-weight: 500; color: #555; margin-bottom: 20px; padding-bottom: 15px; border-bottom: 2px solid #eee; }
  .my-info p { margin: 6px 0; color: #444; font-size: 1rem; line-height: 1.6; display: flex; align-items: center; }
  .my-info i { width: 28px; color: #005AB5; text-align: center; margin-right: 10px; font-size: 1.1em; }
  
  .social-group { margin-top: 25px; display: flex; gap: 15px; flex-wrap: wrap; }
  .social-btn { 
    background-color: #f0f5fa; color: #005AB5 !important; padding: 10px 20px; border-radius: 8px; 
    font-size: 0.95rem; font-weight: 600; border: 1px solid transparent; transition: all 0.2s ease; 
  }
  .social-btn:hover { background-color: #005AB5; color: #fff !important; transform: translateY(-3px); box-shadow: 0 5px 15px rgba(0, 90, 181, 0.3); }

  .nav-wrapper { 
    background: #fff; border-bottom: 1px solid #eee; padding: 15px 0; position: sticky; top: 0; z-index: 999; 
    box-shadow: 0 4px 12px rgba(0,0,0,0.05); width: 100vw; margin-left: -50vw; left: 50%; 
    position: relative; margin-bottom: 50px; display: flex; justify-content: center; 
  }
  .nav-links { display: flex; flex-wrap: wrap; justify-content: center; gap: 5px; max-width: 1200px; }
  .nav-item { color: #444 !important; font-size: 0.95rem; font-weight: 600; padding: 10px 18px; border-radius: 6px; transition: all 0.2s ease; }
  .nav-item:hover { background-color: #eef4fb; color: #005AB5 !important; transform: translateY(-1px); }

  .content-container { max-width: 1050px; margin: 0 auto; padding: 0 20px 60px 20px; }
  h3 { font-size: 1.7rem; color: #222; border-left: 6px solid #005AB5; padding-left: 15px; margin-top: 60px; margin-bottom: 30px; font-weight: 700; }
  h4 { margin-top: 30px; margin-bottom: 15px; font-weight: 600; color: #555; border-bottom: 1px solid #eee; padding-bottom: 5px; }

  ul.styled-list { padding-left: 0; list-style: none; }
  ul.styled-list li { margin-bottom: 12px; line-height: 1.7; color: #444; display: flex; align-items: baseline; gap: 12px; }
  ul.styled-list li::before { content: "•"; color: #005AB5; font-weight: bold; display: inline-block; flex-shrink: 0; }

  /* 修复：移除 font-size，统一颜色为 #444 */
  .pub-item { 
    display: flex; 
    align-items: baseline; 
    gap: 12px; 
    margin-bottom: 16px; 
    line-height: 1.7; 
    color: #444; 
    text-align: justify; 
  }
  .pub-num { 
    flex-shrink: 0; 
    font-weight: bold; 
    color: #444; 
  }
  .pub-content { flex: 1; }

  #back-to-top { display: none; position: fixed; bottom: 30px; right: 30px; z-index: 1000; width: 50px; height: 50px; border: none; outline: none; background-color: #005AB5; color: white; cursor: pointer; border-radius: 50%; box-shadow: 0 4px 15px rgba(0,0,0,0.3); font-size: 20px; transition: all 0.3s ease; align-items: center; justify-content: center; }
  #back-to-top:hover { background-color: #003d7a; transform: translateY(-5px); box-shadow: 0 6px 20px rgba(0,0,0,0.4); }

  @media (max-width: 800px) {
    .profile-card { flex-direction: column; text-align: center; padding: 40px 20px; gap: 30px; }
    .card-right { text-align: center; }
    .my-info p { justify-content: center; }
    .social-group { justify-content: center; }
    .nav-item { padding: 8px 12px; font-size: 0.85rem; }
    .lang-switch { top: 15px; right: 15px; } 
    .lang-btn { padding: 6px 12px; font-size: 0.8rem; }
    #back-to-top { width: 45px; height: 45px; bottom: 20px; right: 20px; font-size: 18px; }
  }
</style>

<div class="hero-wrapper">
  <div class="lang-switch">
    <a href="/" class="lang-btn">
      <i class="fas fa-language"></i> English
    </a>
  </div>

  <div class="profile-card">
    <div class="card-left">
      <img src="../kunpuji.jpg" alt="Kunpu Ji" class="avatar-img">
    </div>
    
    <div class="card-right">
      <div class="my-name">嵇昆浦</div>
      <div class="my-role">博士后研究员</div>
      
      <div class="my-info">
        <p><i class="fas fa-university"></i> 土地测量及地理资讯学系 (LSGI)</p>
        <p><i class="fas fa-graduation-cap"></i> 香港理工大学 (PolyU)</p>
        <p><i class="fas fa-map-marker-alt"></i> 香港九龙红磡育才道11号</p>
      </div>

      <div class="social-group">
        <a href="mailto:kunpu.ji@polyu.edu.hk" class="social-btn"><i class="fas fa-paper-plane"></i> 邮箱</a>
        <a href="https://www.researchgate.net/profile/Kunpu-Ji-2" target="_blank" class="social-btn"><i class="fas fa-book-open"></i> 谷歌学术</a>
        <a href="https://www.researchgate.net/profile/Kunpu-Ji-2" target="_blank" class="social-btn"><i class="fab fa-researchgate"></i> ResearchGate</a>
        <a href="#" class="social-btn"><i class="fab fa-github"></i> GitHub</a>
      </div>
    </div>
  </div>
</div>

<div class="nav-wrapper">
  <div class="nav-links">
    <a href="#News" class="nav-item">新闻动态</a>
    <a href="#Research" class="nav-item">研究方向</a>
    <a href="#Education" class="nav-item">教育经历</a>
    <a href="#Experience" class="nav-item">工作经历</a>
    <a href="#Publications" class="nav-item">发表论文</a>
    <a href="#Codes" class="nav-item">代码</a>
    <a href="#Datasets" class="nav-item">数据集</a>
    <a href="#Professional" class="nav-item">学术服务</a>
    <a href="#Awards" class="nav-item">荣誉奖项</a>
  </div>
</div>

<div class="content-container">

  <a name="News"></a>
  <h3>新闻动态</h3>
  <ul class="styled-list">
    <li><span><b>12/2025:</b> 关于地球物理时间序列滤波的论文被 <b>Surveys in Geophysics</b> 接收。</span></li>
    <li><span><b>11/2025:</b> 关于改进SSA方法的论文发表于 <b>Acta Geodynamica et Geomaterialia</b>。 <a href="https://www2.irsm.cas.cz/index_en.php?page=acta_detail_doi&id=557" target="_blank">[链接]</a></span></li>
    <li><span><b>10/2025:</b> 关于小波滤波的论文发表于 <b>IEEE TGRS</b>。 <a href="https://ieeexplore.ieee.org/document/11218160/" target="_blank">[链接]</a></span></li>
    <li><span><b>10/2025:</b> 关于傅里叶滤波的论文发表于 <b>GPS Solutions</b>。 <a href="https://link.springer.com/article/10.1007/s10291-025-01885-x" target="_blank">[链接]</a></span></li>
    <li><span><b>01/2025:</b> 关于病态模型正则化的论文发表于 <b>IEEE TGRS</b>。 <a href="https://ieeexplore.ieee.org/document/10836814" target="_blank">[链接]</a></span></li>
  </ul>

  <a name="Research"></a>
  <h3>研究方向</h3>
  <ul class="styled-list">
    <li><span>大地测量数据处理理论（参数估计、方差分量估计、质量控制、时间序列分析）</span></li>
    <li><span>基于GNSS的水文大地测量学</span></li>
    <li><span>GRACE时变重力场滤波及相关应用</span></li>
  </ul>

  <a name="Education"></a>
  <h3>教育经历</h3>
  <ul class="styled-list">
    <li><span><b>03/2024 – 03/2025:</b> 联合培养博士 (大地测量学), 德国斯图加特大学</span></li>
    <li><span><b>09/2021 – 05/2025:</b> 博士 (大地测量学), 同济大学</span></li>
    <li><span><b>09/2017 – 06/2020:</b> 硕士 (测绘工程), 同济大学</span></li>
    <li><span><b>09/2013 – 06/2017:</b> 学士 (测绘工程), 南京工业大学</span></li>
  </ul>

  <a name="Experience"></a>
  <h3>工作经历</h3>
  <ul class="styled-list">
    <li><span><b>10/2025 – 至今:</b> 博士后研究员, 香港理工大学 (PolyU)</span></li>
    <li><span><b>06/2025 – 09/2025:</b> 研究助理, 同济大学</span></li>
    <li><span><b>07/2020 – 07/2021:</b> 高级 GNSS 算法工程师, 千寻位置网络有限公司</span></li>
  </ul>

  <a name="Publications"></a>
  <h3>发表论文</h3>

  <h4>2025</h4>
  <div class="pub-item">
    <div class="pub-num">[6]</div>
    <div class="pub-content"><b>K. Ji</b>, Y. Shen, F. Wang. Minimum Norm Least Squares Wavelet Filtering for Processing Incomplete Geodetic Time Series. <b><i>IEEE Transactions on Geoscience and Remote Sensing</i></b>, 2025, 63: 1-19.</div>
  </div>

  <div class="pub-item">
    <div class="pub-num">[5]</div>
    <div class="pub-content"><b>K. Ji</b>, Y. Shen, N. Sneeuw, et al. Least Squares Fourier Filter for Processing Incomplete and Heterogeneous GNSS Position Time Series. <b><i>GPS Solutions</i></b>, 2025, 29: 130.</div>
  </div>

  <div class="pub-item">
    <div class="pub-num">[4]</div>
    <div class="pub-content"><b>K. Ji</b>, L. Zhang, F. Wang. Filtering Unevenly Spaced Geophysical Time Series as an Ill-Posed Problem. <b><i>Surveys in Geophysics</i></b>, 2025. (Accepted)</div>
  </div>

  <div class="pub-item">
    <div class="pub-num">[3]</div>
    <div class="pub-content"><b>K. Ji</b>, Y. Shen, F. Wang, et al. An Efficient Improved Singular Spectrum Analysis for Processing GNSS Position Time Series with Missing Data. <b><i>Geophysical Journal International</i></b>, 2025, 240(1): 189-200.</div>
  </div>

  <div class="pub-item">
    <div class="pub-num">[2]</div>
    <div class="pub-content"><b>K. Ji</b>, Y. Shen, N. Sneeuw, et al. A Recursive Regularized Solution to Geophysical Linear Ill-Posed Inverse Problems. <b><i>IEEE Transactions on Geoscience and Remote Sensing</i></b>, 2025, 63: 1-14.</div>
  </div>

  <div class="pub-item">
    <div class="pub-num">[1]</div>
    <div class="pub-content"><b>K. Ji</b>, F. Wang. Some New Insights into Efficient ISSA for Processing Incomplete Geodetic Time Series. <b><i>Acta Geodynamica et Geomaterialia</i></b>, 2025, 22(4): 531-544.</div>
  </div>

  <h4>2024</h4>
  <div class="pub-item">
    <div class="pub-num">[2]</div>
    <div class="pub-content"><b>K. Ji</b>, Y. Shen, F. Wang, Q. Chen, L. Zhang. Extended Multiresolution Analysis for Filtering Incomplete Heterogeneous Geophysical Time Series. <b><i>IEEE Transactions on Geoscience and Remote Sensing</i></b>, 2024, 62: 1-13.</div>
  </div>

  <div class="pub-item">
    <div class="pub-num">[1]</div>
    <div class="pub-content"><b>嵇昆浦</b>, 沈云中, 陈秋杰. GRACE时变重力场模型的自适应正则化滤波方法. <b><i>武汉大学学报(信息科学版)</i></b>, 2024, 49(11): 2101-2112.</div>
  </div>

  <h4>2023</h4>
  <div class="pub-item">
    <div class="pub-num">[2]</div>
    <div class="pub-content"><b>K. Ji</b>, Y. Shen, Q. Chen, F. Wang. Extended Singular Spectrum Analysis for Processing Incomplete Heterogeneous Geodetic Time Series. <b><i>Journal of Geodesy</i></b>, 2023, 97(8): 74.</div>
  </div>

  <div class="pub-item">
    <div class="pub-num">[1]</div>
    <div class="pub-content"><b>K. Ji</b>, Y. Shen, Q. Chen, T. Feng. Extended Principal Component Analysis for Spatiotemporal Filtering of Incomplete Heterogeneous GNSS Position Time Series. <b><i>IEEE Transactions on Geoscience and Remote Sensing</i></b>, 2023, 61: 1-19.</div>
  </div>

  <h4>2022</h4>
  <div class="pub-item">
    <div class="pub-num">[1]</div>
    <div class="pub-content"><b>K. Ji</b>, Y. Shen, Q. Chen, B. Li, W. Wang. An Adaptive Regularized Solution to Inverse Ill-posed Models. <b><i>IEEE Transactions on Geoscience and Remote Sensing</i></b>, 2022, 60: 1-15.</div>
  </div>

  <h4>2020</h4>
  <div class="pub-item">
    <div class="pub-num">[3]</div>
    <div class="pub-content"><b>K. Ji</b>, Y. Shen, F. Wang. Signal Extraction from GNSS Position Time Series Using Weighted Wavelet Analysis. <b><i>Remote Sensing</i></b>, 2020, 12.</div>
  </div>

  <div class="pub-item">
    <div class="pub-num">[2]</div>
    <div class="pub-content"><b>嵇昆浦</b>, 沈云中. 含缺值GNSS基准站坐标序列的非插值小波分析与信号提取. <b><i>测绘学报</i></b>, 2020, 49(05).</div>
  </div>

  <div class="pub-item">
    <div class="pub-num">[1]</div>
    <div class="pub-content"><b>嵇昆浦</b>, 沈云中. TSVD正则化解法的单位权方差无偏估计. <b><i>武汉大学学报(信息科学版)</i></b>, 2020, 45(04).</div>
  </div>

  <a name="Codes"></a>
  <h3>代码</h3>
  <p style="color: #777; font-style: italic; padding: 30px; background: #f9f9f9; border-radius: 8px; text-align: center; border: 1px dashed #ddd;">代码即将上传...</p>

  <a name="Datasets"></a>
  <h3>数据集</h3>
  <p style="color: #777; font-style: italic; padding: 30px; background: #f9f9f9; border-radius: 8px; text-align: center; border: 1px dashed #ddd;">数据集即将上传...</p>

  <a name="Professional"></a>
  <h3>学术服务</h3>
  <p><b>期刊审稿人:</b></p>
  <ul class="styled-list">
    <li><span>Advances in Space Research</span></li>
    <li><span>Journal of Geodesy</span></li>
  </ul>

  <a name="Awards"></a>
  <h3>荣誉奖项</h3>
  <ul class="styled-list">
    <li><span><b>2025:</b> 同济大学优秀博士学位论文 (专业前2名)</span></li>
    <li><span><b>2025:</b> 同济大学优秀毕业生</span></li>
    <li><span><b>2024:</b> 国家留学基金委 (CSC) 奖学金</span></li>
    <li><span><b>2023:</b> 博士研究生国家奖学金</span></li>
    <li><span><b>2023:</b> 同济大学优秀学生</span></li>
    <li><span><b>2020:</b> 同济大学优秀硕士学位论文 (专业前2名)</span></li>
    <li><span><b>2018:</b> 第十五届“华为杯”中国研究生数学建模竞赛二等奖</span></li>
  </ul>

</div>

<button id="back-to-top" title="回到顶部">
  <i class="fas fa-arrow-up"></i>
</button>

<script>
  var mybutton = document.getElementById("back-to-top");
  window.onscroll = function() {scrollFunction()};
  function scrollFunction() {
    if (document.body.scrollTop > 300 || document.documentElement.scrollTop > 300) {
      mybutton.style.display = "flex";
    } else {
      mybutton.style.display = "none";
    }
  }
  mybutton.onclick = function() {
    window.scrollTo({top: 0, behavior: 'smooth'});
  }
</script>
