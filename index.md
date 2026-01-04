<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kunpu Ji - Home</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
        /* --- 全局设置 --- */
        :root {
            --primary-color: #005AB5; /* 你喜欢的深蓝色 */
            --text-color: #333;
            --bg-grey: #f9f9f9;
            --card-bg: rgba(255, 255, 255, 0.95); /* 卡片半透明背景 */
        }

        body {
            font-family: 'Roboto', Arial, sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            margin: 0;
            padding: 0;
            background-color: var(--bg-grey);
        }

        a {
            text-decoration: none;
            color: var(--primary-color);
            transition: color 0.3s;
        }

        a:hover {
            color: #003d7a;
        }

        /* --- 顶部 Banner 和个人信息卡片区域 --- */
        .hero-banner {
            /* 【重要】请在这里替换成香港理工大学的背景图路径 */
            background-image: url('polyu_bg.jpg'); 
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            padding: 60px 20px; /* 上下留白，给卡片空间 */
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 350px; /* 保证最小高度 */
        }

        .profile-card {
            background: var(--card-bg);
            padding: 40px;
            border-radius: 20px; /* 圆角 */
            box-shadow: 0 10px 30px rgba(0,0,0,0.15); /* 柔和的阴影 */
            text-align: center;
            max-width: 700px;
            width: 100%;
            backdrop-filter: blur(5px); /* 可选：背景毛玻璃效果，增加高级感 */
        }

        .profile-avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%; /* 圆形头像 */
            object-fit: cover;
            border: 4px solid #fff; /* 头像白边 */
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            margin-bottom: 20px;
            /* 如果想让头像突破卡片上边缘，可以取消下面两行的注释 */
            /* margin-top: -90px; */
            /* z-index: 10; */
        }

        .profile-name {
            color: var(--primary-color);
            margin: 10px 0;
            font-size: 2.2em;
            font-weight: 700;
        }

        .profile-info {
            font-size: 1.1em;
            color: #555;
            margin-bottom: 15px;
        }

        .profile-contact {
            font-size: 0.95em;
            color: #777;
            border-top: 1px solid #eee;
            padding-top: 15px;
            margin-top: 15px;
        }

        /* --- 导航栏 --- */
        .nav-bar-container {
            background: #fff;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            padding: 15px 0;
            position: sticky; /* 可选：让导航栏吸顶 */
            top: 0;
            z-index: 100;
        }

        .nav-bar {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 25px;
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .nav-bar a {
            font-weight: 500;
            font-size: 1.05em;
            padding: 5px 10px;
            border-radius: 5px;
        }

        .nav-bar a:hover {
            background-color: #f0f5ff; /* 鼠标悬停时的浅蓝色背景 */
        }

        /* --- 主体内容区域 --- */
        .container {
            max-width: 1000px; /* 控制下方内容的最大宽度，实现对齐 */
            margin: 40px auto; /* 居中且上下留白 */
            background: #fff;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 2px 15px rgba(0,0,0,0.03);
        }

        /* --- 内容样式优化 --- */
        h3 {
            color: #222;
            border-bottom: 2px solid var(--primary-color);
            padding-bottom: 10px;
            margin-top: 40px;
            font-size: 1.5em;
        }
        /* 让第一个标题顶部没有间距 */
        h3:first-of-type {
            margin-top: 0;
        }

        h4 {
            color: #555;
            margin-top: 25px;
            margin-bottom: 15px;
            font-size: 1.2em;
        }

        ul {
            padding-left: 20px;
        }

        li {
            margin-bottom: 10px;
        }
        
        /* 专门针对 News 列表的样式优化，让日期和内容对齐更好看 */
        .news-list li {
            display: grid;
            grid-template-columns: 90px 1fr;
            gap: 10px;
            align-items: baseline;
        }
        .news-date {
            font-weight: bold;
            color: var(--primary-color);
        }

        .publication-item {
            margin-bottom: 15px;
            text-align: justify;
        }
        
        /* 占位符样式 */
        .placeholder {
            color: #999;
            font-style: italic;
            padding: 20px;
            background: #f4f4f4;
            border-radius: 8px;
            text-align: center;
        }

    </style>
</head>
<body>

    <header class="hero-banner">
        <div class="profile-card">
            <img src="kunpuji.jpg" alt="Kunpu Ji" class="profile-avatar">
            <h1 class="profile-name">Kunpu Ji (嵇昆浦)</h1>
            <div class="profile-info">
                <b>Postdoctoral Researcher</b><br/>
                Department of Land Surveying and Geo-Informatics (LSGI)<br/>
                The Hong Kong Polytechnic University (PolyU)<br/>
            </div>
            <div class="profile-contact">
                <b>Email:</b> kunpu.ji@polyu.edu.hk | kunpuji@tongji.edu.cn | jkptongji@163.com<br/>
                <b>Address:</b> 11 Yuk Choi Road, Hung Hom, Kowloon, Hong Kong
            </div>
        </div>
    </header>

    <nav class="nav-bar-container">
        <div class="nav-bar">
            <a href="#News">News</a>
            <a href="#Research">Research Interests</a>
            <a href="#Education">Education</a>
            <a href="#Experience">Professional Experience</a>
            <a href="#Publications">Publications</a>
            <a href="#Codes">Codes</a>
            <a href="#Datasets">Datasets</a>
            <a href="#Professional">Professional Service</a>
            <a href="#Awards">Awards & Honors</a>
        </div>
    </nav>

    <main class="container">

        <a name="News"></a>
        <h3>News</h3>
        <ul class="news-list">
            <li>
                <span class="news-date">10/2025</span>
                <span>A paper on soil moisture data reconstruction is published in <b>RSE</b>. <a href="https://www.sciencedirect.com/science/article/pii/S0034425725002457">[Link]</a></span>
            </li>
            <li>
                <span class="news-date">03/2025</span>
                <span>A paper on subpixel mapping is published in <b>RSE</b>. <a href="https://www.sciencedirect.com/science/article/abs/pii/S0034425724005406">[Link]</a></span>
            </li>
            <li>
                <span class="news-date">05/2024</span>
                <span>A paper on Landsat LST gap filling is published in <b>RSE</b>. <a href="https://www.sciencedirect.com/science/article/pii/S0034425724001536">[Link]</a></span>
            </li>
            <li>
                <span class="news-date">06/2023</span>
                <span>A paper on 30 m young forest age in China is accepted by <b>ESSD</b>.</span>
            </li>
            <li>
                <span class="news-date">03/2022</span>
                <span>A paper on haze removal is published in <b>RSE</b>. <a href="https://www.sciencedirect.com/science/article/pii/S0034425722001262">[Link]</a></span>
            </li>
        </ul>

        <a name="Research"></a>
        <h3>Research Interests</h3>
        <ul>
            <li>Geodetic data processing theory, including parameter estimation, variance component estimation (VCE), quality control, and time series analysis</li>
            <li>GNSS-based hydrogeodesy</li>
            <li>Filtering of GRACE time-variable gravity field solutions and related applications</li>
        </ul>

        <a name="Education"></a>
        <h3>Education</h3>
        <ul>
            <li>09/2021 – 05/2025 &nbsp;&nbsp; <b>Ph.D.</b> in Geodesy, Tongji University, China</li>
            <li>09/2017 – 06/2020 &nbsp;&nbsp; <b>M.S.</b> in Surveying Engineering, Tongji University, China</li>
            <li>09/2013 – 06/2017 &nbsp;&nbsp; <b>B.S.</b> in Surveying Engineering, Nanjing Tech University, China</li>
        </ul>

        <a name="Experience"></a>
        <h3>Professional Experience</h3>
        <ul>
            <li>10/2025 – Present &nbsp;&nbsp; Postdoctoral Research Fellow, Department of Land Surveying and Geo-Informatics, The Hong Kong Polytechnic University, Hong Kong, China</li>
            <li>06/2025 – 09/2025 &nbsp;&nbsp; Research Assistant, College of Surveying and Geo-informatics, Tongji University, Shanghai, China</li>
            <li>07/2020 – 07/2021 &nbsp;&nbsp; Senior GNSS Algorithm Engineer, Qianxun Spatial Intelligence Inc., Shanghai, China</li>
        </ul>

        <a name="Publications"></a>
        <h3>Publications</h3>
        <p>
            Google Scholar: <a href="https://scholar.google.com/citations?user=y5foruMAAAAJ&hl=en" target="_blank">[Link]</a> &nbsp;|&nbsp; 
            ResearchGate: <a href="https://www.researchgate.net/profile/Qunming_Wang" target="_blank">[Link]</a>
        </p>

        <h4>2025</h4>
        <div class="publication-item">[6] <b>K. Ji</b>, Y. Shen, F. Wang. Minimum Norm Least Squares Wavelet Filtering for Processing Incomplete Geodetic Time Series. ***IEEE Transactions on Geoscience and Remote Sensing***, 2025, 63: 1-19.</div>
        <div class="publication-item">[5] <b>K. Ji</b>, Y. Shen, N. Sneeuw, et al. Least Squares Fourier Filter for Processing Incomplete and Heterogeneous GNSS Position Time Series. ***GPS Solutions***, 2025, 29: 130.</div>
        <div class="publication-item">[1] <b>K. Ji</b>, F. Wang. Some New Insights into Efficient ISSA for Processing Incomplete Geodetic Time Series. ***Acta Geodynamica et Geomaterialia***, 2025, 22(4): 531-544.</div>

        <h4>2024</h4>
        <div class="publication-item">[2] <b>K. Ji</b>, Y. Shen, F. Wang, Q. Chen, L. Zhang. Extended Multiresolution Analysis for Filtering Incomplete Heterogeneous Geophysical Time Series. ***IEEE Transactions on Geoscience and Remote Sensing***, 2024, 62: 1-13.</div>
        <div class="publication-item">[1] <b>嵇昆浦</b>, 沈云中, 陈秋杰. GRACE时变重力场模型的自适应正则化滤波方法. ***武汉大学学报(信息科学版)***, 2024, 49(11): 2101-2112.</div>
        
        <a name="Codes"></a>
        <h3>Codes</h3>
        <div class="placeholder">
            Content coming soon...
        </div>

        <a name="Datasets"></a>
        <h3>Datasets</h3>
        <p>
            <b>A set of seamless 0.05-degree, daily SIF product data (FGSIF)</b> &nbsp;(<a href="https://doi.org/10.5281/zenodo.11918785" target="_blank">https://doi.org/10.5281/zenodo.11918785</a>)<br/>
            J. Li, Q. Wang*, P. M. Atkinson. Filling gaps in global daily TROPOMI solar-induced chlorophyll fluorescence data from 2018 to 2021. IEEE Transactions on Geoscience and Remote Sensing, 2025, 63: 4413515.
        </p>

        <a name="Professional"></a>
        <h3>Professional Service</h3>
        <h4>Journal Reviewer</h4>
        <ul>
            <li>Advances in Space Research</li>
            <li>Journal of Geodesy</li>
        </ul>

        <a name="Awards"></a>
        <h3>Awards & Honors</h3>
        <ul>
            <li>2025: Excellent Doctoral Dissertation of Tongji University (Top 2 in the major)</li>
            <li>2025: Outstanding Graduate of Tongji University</li>
            <li>2024: China Scholarship Council (CSC) Scholarship</li>
            <li>2023: National Scholarship for Doctoral Students (Ministry of Education of China)</li>
            <li>2023: Outstanding Student of Tongji University</li>
            <li>2020: Excellent Master's Dissertation of Tongji University (Top 2 in the major)</li>
            <li>2018: Second Prize, The 15th "Huawei Cup" China Postgraduate Mathematical Contest in Modeling</li>
        </ul>

    </main>

</body>
</html>
