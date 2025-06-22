<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>देश और विदेश का विशेष न्यूज</title>
    <link href="https://fonts.googleapis.com/css2?family=Hind:wght@400;500;700&family=Noto+Sans+Devanagari:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #d32f2f;
            --primary-dark: #b71c1c;
            --secondary: #1e88e5;
            --dark: #222;
            --light: #f5f5f5;
            --gray: #777;
            --border: #e0e0e0;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Hind', 'Noto Sans Devanagari', sans-serif;
            background-color: #f9f9f9;
            color: #333;
            line-height: 1.6;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: white;
            padding: 1rem 0;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        .header-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 5%;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo h1 {
            font-size: 1.8rem;
            margin-left: 12px;
        }
        
        .logo-icon {
            font-size: 2.5rem;
            color: #ffeb3b;
        }
        
        .date-display {
            background: rgba(0,0,0,0.2);
            padding: 8px 15px;
            border-radius: 30px;
            font-size: 0.9rem;
        }
        
        nav {
            background-color: var(--primary-dark);
            padding: 0.8rem 5%;
        }
        
        .nav-menu {
            display: flex;
            list-style: none;
            justify-content: center;
        }
        
        .nav-menu li {
            margin: 0 15px;
        }
        
        .nav-menu a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            font-size: 1.1rem;
            padding: 8px 0;
            position: relative;
        }
        
        .nav-menu a:hover::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background: white;
        }
        
        /* Hero Section */
        .hero {
            position: relative;
            height: 500px;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1586339949916-3e9457bef6d3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            padding: 0 5%;
        }
        
        .hero-content {
            max-width: 800px;
        }
        
        .hero h2 {
            font-size: 2.8rem;
            margin-bottom: 1.5rem;
            text-shadow: 0 2px 4px rgba(0,0,0,0.5);
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .search-box {
            display: flex;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .search-box input {
            flex: 1;
            padding: 15px 20px;
            border: none;
            border-radius: 50px 0 0 50px;
            font-size: 1.1rem;
        }
        
        .search-box button {
            background: var(--primary);
            color: white;
            border: none;
            padding: 0 25px;
            border-radius: 0 50px 50px 0;
            cursor: pointer;
            font-size: 1.1rem;
            transition: all 0.3s;
        }
        
        .search-box button:hover {
            background: var(--primary-dark);
        }
        
        /* News Sections */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 5%;
        }
        
        .section-title {
            text-align: center;
            margin: 3rem 0 2rem;
            color: var(--primary-dark);
            font-size: 2rem;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--primary);
        }
        
        .news-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 3rem;
        }
        
        .news-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .news-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }
        
        .card-image {
            height: 200px;
            overflow: hidden;
        }
        
        .card-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .news-card:hover .card-image img {
            transform: scale(1.1);
        }
        
        .card-content {
            padding: 20px;
        }
        
        .card-content .category {
            display: inline-block;
            background: var(--secondary);
            color: white;
            padding: 5px 12px;
            border-radius: 30px;
            font-size: 0.8rem;
            margin-bottom: 12px;
        }
        
        .card-content h3 {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--dark);
        }
        
        .card-content p {
            color: var(--gray);
            margin-bottom: 15px;
            font-size: 0.95rem;
        }
        
        .card-meta {
            display: flex;
            justify-content: space-between;
            color: var(--gray);
            font-size: 0.85rem;
            border-top: 1px solid var(--border);
            padding-top: 15px;
        }
        
        /* Video Section */
        .video-section {
            background: linear-gradient(to right, #f5f5f5, #e0e0e0);
            padding: 3rem 0;
            margin: 3rem 0;
        }
        
        .video-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 25px;
        }
        
        .video-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
        }
        
        .video-thumb {
            position: relative;
            height: 200px;
        }
        
        .video-thumb img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .play-btn {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: rgba(211, 47, 47, 0.8);
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .play-btn:hover {
            background: rgba(183, 28, 28, 0.9);
            transform: translate(-50%, -50%) scale(1.1);
        }
        
        .video-content {
            padding: 20px;
        }
        
        .video-content h3 {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: var(--dark);
        }
        
        /* Contact Section */
        .contact-section {
            background: white;
            padding: 4rem 0;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }
        
        .contact-info {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: white;
            padding: 40px;
            border-radius: 10px;
        }
        
        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 15px;
        }
        
        .contact-info h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 3px;
            background: white;
        }
        
        .contact-details {
            margin-top: 30px;
        }
        
        .contact-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 25px;
        }
        
        .contact-icon {
            font-size: 1.2rem;
            margin-right: 15px;
            min-width: 30px;
            text-align: center;
        }
        
        .contact-text {
            line-height: 1.6;
        }
        
        .contact-text h4 {
            font-size: 1.1rem;
            margin-bottom: 5px;
        }
        
        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 12px 15px;
            margin-bottom: 20px;
            border: 1px solid var(--border);
            border-radius: 5px;
            font-family: inherit;
            font-size: 1rem;
        }
        
        .contact-form textarea {
            height: 150px;
            resize: vertical;
        }
        
        .submit-btn {
            background: var(--primary);
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 50px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .submit-btn:hover {
            background: var(--primary-dark);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 4rem 0 2rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 30px;
            margin-bottom: 3rem;
        }
        
        .footer-col h4 {
            font-size: 1.2rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-col h4::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 2px;
            background: var(--primary);
        }
        
        .footer-col ul {
            list-style: none;
        }
        
        .footer-col ul li {
            margin-bottom: 12px;
        }
        
        .footer-col ul li a {
            color: #aaa;
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .footer-col ul li a:hover {
            color: white;
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: #333;
            color: white;
            border-radius: 50%;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-5px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #444;
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Language Selector */
        .lang-selector {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 1000;
        }
        
        .lang-btn {
            background: var(--primary);
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 50px;
            font-size: 1rem;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s;
        }
        
        .lang-btn:hover {
            background: var(--primary-dark);
            transform: translateY(-3px);
        }
        
        /* Breaking News Ticker */
        .breaking-news {
            background: var(--secondary);
            color: white;
            padding: 10px 0;
            overflow: hidden;
        }
        
        .ticker-container {
            display: flex;
            align-items: center;
            white-space: nowrap;
        }
        
        .ticker-label {
            background: var(--primary);
            padding: 5px 15px;
            font-weight: bold;
            margin-right: 20px;
        }
        
        .ticker-content {
            display: inline-block;
            animation: ticker 20s linear infinite;
            padding-left: 100%;
        }
        
        @keyframes ticker {
            0% { transform: translateX(0); }
            100% { transform: translateX(-100%); }
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .footer-content {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .contact-container {
                grid-template-columns: 1fr;
            }
        }
        
        @media (max-width: 768px) {
            .nav-menu {
                flex-wrap: wrap;
            }
            
            .header-top {
                flex-direction: column;
                gap: 15px;
            }
            
            .hero h2 {
                font-size: 2.2rem;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
            }
            
            .news-grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    </style>
</head>
<body>
    <!-- Header Section -->
    <header>
        <div class="header-top">
            <div class="logo">
                <i class="fas fa-newspaper logo-icon"></i>
                <h1>देश और विदेश का विशेष न्यूज</h1>
            </div>
            <div class="date-display">
                <i class="fas fa-calendar-alt"></i> <span id="currentDate">22 जून, 2025</span>
            </div>
        </div>
        
        <nav>
            <ul class="nav-menu">
                <li><a href="#"><i class="fas fa-home"></i> होम</a></li>
                <li><a href="#"><i class="fas fa-globe-asia"></i> भारत</a></li>
                <li><a href="#"><i class="fas fa-globe-americas"></i> विदेश</a></li>
                <li><a href="#"><i class="fas fa-business-time"></i> व्यापार</a></li>
                <li><a href="#"><i class="fas fa-basketball-ball"></i> खेल</a></li>
                <li><a href="#"><i class="fas fa-film"></i> मनोरंजन</a></li>
                <li><a href="#"><i class="fas fa-video"></i> वीडियो</a></li>
            </ul>
        </nav>
        
        <div class="breaking-news">
            <div class="ticker-container">
                <div class="ticker-label">ब्रेकिंग न्यूज</div>
                <div class="ticker-content">
                    भारत और अमेरिका ने नई रक्षा संधि पर हस्ताक्षर किए • ओलंपिक 2028 के लिए लॉस एंजिल्स को मेजबानी मिली • विश्व बैंक ने भारत की विकास दर 8.2% रहने का अनुमान लगाया • बिहार में नई सिंचाई परियोजना का शुभारंभ • आईपीएल 2026 के लिए नीलामी दिसंबर में होगी
                </div>
            </div>
        </div>
    </header>
    
    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h2>विश्व भर की ताजा खबरें, आपकी भाषा में</h2>
            <p>स्वचालित अनुवाद और हिंदी डबिंग के साथ विश्व भर की खबरों का सबसे विश्वसनीय स्रोत</p>
            
            <div class="search-box">
                <input type="text" placeholder="आज की ताजा खबरें खोजें...">
                <button><i class="fas fa-search"></i> खोजें</button>
            </div>
        </div>
    </section>
    
    <!-- Latest News Section -->
    <section class="container">
        <h2 class="section-title">आज की ताजा खबरें</h2>
        
        <div class="news-grid">
            <!-- News Card 1 -->
            <div class="news-card">
                <div class="card-image">
                    <img src="https://images.unsplash.com/photo-1588681664899-f142ff2dc9b1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1074&q=80" alt="News Image">
                </div>
                <div class="card-content">
                    <span class="category">राजनीति</span>
                    <h3>प्रधानमंत्री ने लॉन्च की नई युवा रोजगार योजना</h3>
                    <p>केंद्र सरकार ने आज नई युवा रोजगार योजना का शुभारंभ किया जिससे 5 लाख युवाओं को रोजगार मिलने की उम्मीद है।</p>
                    <div class="card-meta">
                        <span><i class="far fa-clock"></i> 2 घंटे पहले</span>
                        <span><i class="far fa-eye"></i> 12K दृश्य</span>
                    </div>
                </div>
            </div>
            
            <!-- News Card 2 -->
            <div class="news-card">
                <div class="card-image">
                    <img src="https://images.unsplash.com/photo-1611162617474-5b21e879e113?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1074&q=80" alt="News Image">
                </div>
                <div class="card-content">
                    <span class="category">विज्ञान</span>
                    <h3>ISRO ने सफलतापूर्वक लॉन्च किया नया उपग्रह</h3>
                    <p>भारतीय अंतरिक्ष अनुसंधान संगठन (ISRO) ने आज सतीश धवन अंतरिक्ष केंद्र से नए संचार उपग्रह का सफल प्रक्षेपण किया।</p>
                    <div class="card-meta">
                        <span><i class="far fa-clock"></i> 4 घंटे पहले</span>
                        <span><i class="far fa-eye"></i> 8.5K दृश्य</span>
                    </div>
                </div>
            </div>
            
            <!-- News Card 3 -->
            <div class="news-card">
                <div class="card-image">
                    <img src="https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="News Image">
                </div>
                <div class="card-content">
                    <span class="category">खेल</span
