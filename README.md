<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>देश और विदेश का विशेष न्यूज</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Hind Siliguri', 'Nirmala UI', Arial, sans-serif;
        }
        
        :root {
            --primary: #c62828;
            --primary-dark: #8e0000;
            --secondary: #1a237e;
            --accent: #ff6f00;
            --light: #f5f5f5;
            --dark: #212121;
            --gray: #757575;
            --card-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            --transition: all 0.3s ease;
        }
        
        body {
            background-color: #f0f2f5;
            color: var(--dark);
            line-height: 1.6;
        }
        
        /* Header Styles */
        header {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            padding: 1rem 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        .header-container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
            flex-wrap: wrap;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo i {
            font-size: 2.5rem;
            color: #ffeb3b;
        }
        
        .logo h1 {
            font-size: 1.8rem;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
        }
        
        .date-display {
            background: rgba(255, 255, 255, 0.15);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
            gap: 15px;
            flex-wrap: wrap;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            padding: 8px 16px;
            border-radius: 4px;
            transition: background 0.3s;
            font-size: 1.1rem;
        }
        
        .nav-links a:hover {
            background: rgba(255, 255, 255, 0.2);
        }
        
        .nav-links a.active {
            background: rgba(255, 255, 255, 0.3);
        }
        
        /* Breaking News */
        .breaking-news {
            background: var(--accent);
            color: white;
            padding: 12px 0;
            position: sticky;
            top: 80px;
            z-index: 90;
            box-shadow: 0 3px 6px rgba(0,0,0,0.1);
        }
        
        .breaking-container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            align-items: center;
            padding: 0 2rem;
        }
        
        .breaking-tag {
            background: #d32f2f;
            padding: 5px 15px;
            border-radius: 4px;
            font-weight: bold;
            margin-right: 20px;
            white-space: nowrap;
        }
        
        .breaking-content {
            flex-grow: 1;
            overflow: hidden;
            position: relative;
            height: 30px;
        }
        
        .breaking-text {
            position: absolute;
            white-space: nowrap;
            animation: scrollText 25s linear infinite;
            font-size: 1.1rem;
            font-weight: 500;
        }
        
        @keyframes scrollText {
            0% { transform: translateX(100%); }
            100% { transform: translateX(-100%); }
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1586339949916-3e9457bef6d3?ixlib=rb-4.0.3') center/cover;
            height: 450px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-bottom: 2rem;
            position: relative;
        }
        
        .hero-content {
            max-width: 800px;
            padding: 0 2rem;
            z-index: 2;
        }
        
        .hero h2 {
            font-size: 3.2rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 6px rgba(0, 0, 0, 0.7);
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 1.3rem;
            margin-bottom: 1.8rem;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.5);
        }
        
        .btn {
            display: inline-block;
            background: var(--primary);
            color: white;
            padding: 12px 25px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 1.1rem;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        
        .btn:hover {
            background: var(--primary-dark);
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.3);
        }
        
        .btn i {
            margin-right: 8px;
        }
        
        .auto-update {
            background: rgba(255, 255, 255, 0.2);
            padding: 10px 20px;
            border-radius: 30px;
            margin-top: 20px;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            font-size: 1rem;
            backdrop-filter: blur(5px);
        }
        
        /* Main Content */
        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 2rem 3rem;
        }
        
        .section-title {
            font-size: 2rem;
            color: var(--secondary);
            margin: 2.5rem 0 1.8rem;
            padding-bottom: 0.8rem;
            border-bottom: 4px solid var(--primary);
            display: inline-block;
            font-weight: 700;
        }
        
        .full-news-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(600px, 1fr));
            gap: 30px;
            margin-bottom: 3rem;
        }
        
        .full-news-article {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: var(--card-shadow);
            transition: var(--transition);
        }
        
        .full-news-article:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 25px rgba(0, 0, 0, 0.15);
        }
        
        .article-header {
            background: linear-gradient(to right, var(--secondary), var(--primary));
            color: white;
            padding: 1.3rem;
            font-size: 1.5rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .article-content {
            padding: 2rem;
        }
        
        .article-title {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: var(--dark);
            line-height: 1.3;
        }
        
        .article-meta {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid #eee;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .article-date {
            display: flex;
            align-items: center;
            gap: 8px;
            font-weight: 500;
            color: var(--primary);
        }
        
        .article-author {
            display: flex;
            align-items: center;
            gap: 8px;
            color: var(--gray);
        }
        
        .article-category {
            background: var(--primary);
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-weight: 500;
        }
        
        .article-image {
            width: 100%;
            max-height: 450px;
            object-fit: cover;
            border-radius: 10px;
            margin: 1.5rem 0;
        }
        
        .article-text {
            font-size: 1.15rem;
            line-height: 1.8;
            margin-bottom: 1.5rem;
            text-align: justify;
        }
        
        .article-text p {
            margin-bottom: 1.5rem;
        }
        
        .article-text h3 {
            color: var(--secondary);
            margin: 1.8rem 0 1rem;
            font-size: 1.5rem;
        }
        
        .article-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 2rem;
        }
        
        .article-tag {
            background: #e3f2fd;
            color: var(--secondary);
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
        }
        
        /* Ad Space */
        .ad-space {
            background: #f9f9f9;
            border: 2px dashed #ccc;
            border-radius: 8px;
            height: 250px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            margin: 2rem 0;
            color: var(--gray);
            text-align: center;
            padding: 20px;
        }
        
        .ad-space i {
            font-size: 3rem;
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        .ad-space h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }
        
        /* Contact Section */
        .contact-section {
            background: white;
            border-radius: 12px;
            padding: 2.5rem;
            box-shadow: var(--card-shadow);
            margin-top: 2rem;
        }
        
        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 1.8rem;
        }
        
        .contact-card {
            background: #f5f7ff;
            border-radius: 10px;
            padding: 1.8rem;
            border-left: 4px solid var(--primary);
            box-shadow: 0 3px 8px rgba(0,0,0,0.05);
        }
        
        .contact-card h3 {
            color: var(--secondary);
            margin-bottom: 1.2rem;
            font-size: 1.5rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .contact-card p {
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 1.1rem;
        }
        
        .contact-card i {
            color: var(--primary);
            width: 24px;
            text-align: center;
            font-size: 1.2rem;
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
            width: 45px;
            height: 45px;
            background: var(--secondary);
            color: white;
            border-radius: 50%;
            font-size: 1.3rem;
            transition: var(--transition);
        }
        
        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 3rem 0 1rem;
            margin-top: 3rem;
        }
        
        .footer-content {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 2rem;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
        }
        
        .footer-logo {
            display: flex;
            flex-direction: column;
        }
        
        .footer-logo h3 {
            font-size: 1.8rem;
            margin-bottom: 1.2rem;
            color: #ffeb3b;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .footer-logo p {
            color: #e0e0e0;
            line-height: 1.8;
        }
        
        .footer-links h4 {
            font-size: 1.3rem;
            margin-bottom: 1.3rem;
            color: #ffeb3b;
            padding-bottom: 5px;
            border-bottom: 2px solid var(--primary);
            display: inline-block;
        }
        
        .footer-links ul {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.9rem;
        }
        
        .footer-links a {
            color: #e0e0e0;
            text-decoration: none;
            transition: color 0.3s;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .footer-links a:hover {
            color: #ffeb3b;
        }
        
        .footer-links a i {
            width: 20px;
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            margin-top: 3rem;
            border-top: 1px solid #424242;
            color: #bdbdbd;
            font-size: 1.05rem;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .hero h2 {
                font-size: 2.6rem;
            }
            
            .full-news-container {
                grid-template-columns: 1fr;
            }
        }
        
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                gap: 15px;
            }
            
            .nav-links {
                justify-content: center;
            }
            
            .hero {
                height: 400px;
            }
            
            .hero h2 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .breaking-container {
                flex-direction: column;
                gap: 10px;
                text-align: center;
            }
            
            .breaking-tag {
                margin-right: 0;
            }
            
            .breaking-content {
                height: auto;
            }
            
            .breaking-text {
                position: static;
                animation: none;
                white-space: normal;
            }
        }
        
        @media (max-width: 480px) {
            .hero {
                height: 350px;
            }
            
            .hero h2 {
                font-size: 1.8rem;
            }
            
            .section-title {
                font-size: 1.6rem;
            }
            
            .article-header {
                font-size: 1.3rem;
            }
            
            .article-title {
                font-size: 1.5rem;
            }
            
            .contact-section {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-container">
            <div class="logo">
                <i class="fas fa-newspaper"></i>
                <h1>देश और विदेश का विशेष न्यूज</h1>
            </div>
            
            <div class="date-display">
                <i class="fas fa-calendar-alt"></i>
                <span id="current-date">13 जुलाई 2025, रविवार</span>
            </div>
            
            <ul class="nav-links">
                <li><a href="#" class="active">होम</a></li>
                <li><a href="#politics">राजनीति</a></li>
                <li><a href="#sports">खेल</a></li>
                <li><a href="#entertainment">मनोरंजन</a></li>
                <li><a href="#business">व्यापार</a></li>
                <li><a href="#technology">तकनीक</a></li>
                <li><a href="#contact">संपर्क</a></li>
            </ul>
        </div>
    </header>
    
    <!-- Breaking News -->
    <div class="breaking-news">
        <div class="breaking-container">
            <div class="breaking-tag">
                <i class="fas fa-bolt"></i> ब्रेकिंग न्यूज
            </div>
            <div class="breaking-content">
                <div class="breaking-text">
                    भारत ने विश्व कप क्रिकेट जीता! विराट कोहली ने शतक बनाकर देश को गौरवान्वित किया। पूरा देश जश्न में डूबा हुआ है। देखें विशेष रिपोर्ट।
                </div>
            </div>
        </div>
    </div>
    
    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h2>विश्वसनीय और ताज़ा खबरें</h2>
            <p>देश और दुनिया की सभी महत्वपूर्ण खबरें हिंदी में। विभिन्न भाषाओं के समाचारों का स्वचालित अनुवाद।</p>
            <a href="#news" class="btn"><i class="fas fa-newspaper"></i> ताज़ा खबरें पढ़ें</a>
            <div class="auto-update">
                <i class="fas fa-sync-alt"></i> यह वेबसाइट प्रतिदिन स्वचालित रूप से अपडेट होती है
            </div>
        </div>
    </section>
    
    <!-- Main Content -->
    <main class="container">
        <h2 class="section-title" id="news">आज की ताज़ा खबरें <small>(13 जुलाई 2025)</small></h2>
        
        <!-- Ad Space -->
        <div class="ad-space">
            <i class="fas fa-ad"></i>
            <h3>विज्ञापन स्थान</h3>
            <p>यहाँ आपका विज्ञापन प्रदर्शित किया जाएगा</p>
        </div>
        
        <!-- राजनीति -->
        <div class="full-news-article" id="politics">
            <div class="article-header">
                <i class="fas fa-landmark"></i> राजनीति
            </div>
            <div class="article-content">
                <h2 class="article-title">केंद्रीय मंत्रिमंडल ने नई शिक्षा नीति को मंजूरी दी</h2>
                
                <div class="article-meta">
                    <div class="article-date">
                        <i class="far fa-calendar"></i> 13 जुलाई 2025
                    </div>
                    <div class="article-author">
                        <i class="fas fa-user-edit"></i> रिपोर्टर: राहुल शर्मा
                    </div>
                    <div class="article-category">
                        <i class="fas fa-tag"></i> शिक्षा नीति
                    </div>
                </div>
                
                <img src="https://images.unsplash.com/photo-1584622650111-993a426fbf0a?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80" alt="Education Policy" class="article-image">
                
                <div class="article-text">
                    <p>केंद्र सरकार ने आज नई शिक्षा नीति को मंजूरी दे दी है जिसमें 10+2 प्रणाली को खत्म कर 5+3+3+4 प्रणाली लागू की जाएगी। इस नई नीति का उद्देश्य शिक्षा प्रणाली को और अधिक समावेशी, लचीला और भविष्योन्मुखी बनाना है।</p>
                    
                    <h3>मुख्य बदलाव</h3>
                    <p>नई शिक्षा नीति में कई महत्वपूर्ण बदलाव किए गए हैं:</p>
                    <p>1. शिक्षा संरचना: 10+2 प्रणाली को बदलकर 5+3+3+4 प्रणाली लागू की जाएगी। इसके तहत पहले पाँच वर्ष फाउंडेशन स्टेज 
