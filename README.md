[Uploading 3t<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The 3TR Care Series - 시간(Time)을 리젠하다</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700&display=swap');
        
        :root {
            --primary: #2c3e50;
            --secondary: #34495e;
            --accent: #16a085;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --text: #333;
            --text-light: #7f8c8d;
            --background: #fff;
            --section-bg: #f9fafb;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Noto Sans KR', sans-serif;
            color: var(--text);
            line-height: 1.6;
            background-color: var(--background);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background-color: var(--background);
            position: fixed;
            width: 100%;
            padding: 20px 0;
            box-shadow: 0 1px 10px rgba(0,0,0,0.05);
            z-index: 1000;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--primary);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            color: var(--dark);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--accent);
        }
        
        /* Hero Section */
        .hero {
            padding: 180px 0 100px;
            background: linear-gradient(135deg, #f6f6f6 0%, #ffffff 100%);
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 50%;
            height: 100%;
            background: url('/api/placeholder/600/400') no-repeat center center / cover;
            opacity: 0.9;
            border-radius: 0 0 0 100px;
        }
        
        .hero-content {
            width: 50%;
            position: relative;
            z-index: 1;
        }
        
        .hero h1 {
            font-size: 48px;
            font-weight: 700;
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .hero h2 {
            font-size: 28px;
            font-weight: 300;
            margin-bottom: 20px;
            color: var(--accent);
        }
        
        .hero p {
            font-size: 18px;
            margin-bottom: 30px;
            line-height: 1.8;
            color: var(--text);
        }
        
        .cta-buttons {
            display: flex;
            gap: 20px;
            margin-top: 40px;
        }
        
        .btn {
            display: inline-block;
            padding: 15px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 500;
            font-size: 16px;
            transition: all 0.3s;
            cursor: pointer;
        }
        
        .btn-primary {
            background-color: var(--accent);
            color: white;
            border: 2px solid var(--accent);
        }
        
        .btn-primary:hover {
            background-color: transparent;
            color: var(--accent);
        }
        
        .btn-secondary {
            background-color: transparent;
            color: var(--primary);
            border: 2px solid var(--primary);
        }
        
        .btn-secondary:hover {
            background-color: var(--primary);
            color: white;
        }
        
        /* Steps Section */
        .steps {
            padding: 100px 0;
            background-color: var(--section-bg);
        }
        
        .steps-title {
            text-align: center;
            margin-bottom: 80px;
        }
        
        .steps-title h2 {
            font-size: 36px;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .steps-container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 40px;
        }
        
        .step-card {
            background-color: white;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
            padding: 40px;
            transition: transform 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .step-card:hover {
            transform: translateY(-10px);
        }
        
        .step-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            height: 5px;
            width: 100%;
            background-color: var(--accent);
        }
        
        .step-number {
            font-size: 16px;
            font-weight: 700;
            color: var(--accent);
            margin-bottom: 15px;
        }
        
        .step-card h3 {
            font-size: 24px;
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        .step-quote {
            font-style: italic;
            color: var(--text-light);
            margin-bottom: 25px;
            font-size: 18px;
        }
        
        .step-features {
            margin-top: 20px;
        }
        
        .step-feature {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .step-feature svg {
            margin-right: 15px;
            color: var(--accent);
        }
        
        /* Trust Section */
        .trust {
            padding: 100px 0;
            background-color: white;
        }
        
        .trust-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .trust-title h2 {
            font-size: 36px;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .gallery {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-bottom: 60px;
        }
        
        .gallery-item {
            border-radius: 10px;
            overflow: hidden;
            position: relative;
            height: 250px;
            cursor: pointer;
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s;
        }
        
        .gallery-item:hover img {
            transform: scale(1.1);
        }
        
        .testimonials {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            margin-top: 60px;
        }
        
        .testimonial {
            background-color: var(--section-bg);
            padding: 30px;
            border-radius: 15px;
            position: relative;
        }
        
        .testimonial::before {
            content: '"';
            position: absolute;
            top: 15px;
            left: 15px;
            font-size: 60px;
            color: var(--accent);
            opacity: 0.2;
        }
        
        .testimonial p {
            font-style: italic;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .testimonial-author img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            margin-right: 15px;
        }
        
        .testimonial-info h4 {
            font-size: 18px;
            margin-bottom: 5px;
        }
        
        .testimonial-info span {
            font-size: 14px;
            color: var(--text-light);
        }
        
        /* Booking Section */
        .booking {
            padding: 100px 0;
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            text-align: center;
        }
        
        .booking h2 {
            font-size: 36px;
            margin-bottom: 30px;
        }
        
        .booking-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
            margin-bottom: 60px;
        }
        
        .trust-elements {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin-top: 50px;
        }
        
        .trust-element {
            text-align: center;
        }
        
        .trust-element svg {
            font-size: 40px;
            margin-bottom: 15px;
            color: var(--light);
        }
        
        .trust-element h3 {
            font-size: 18px;
            margin-bottom: 10px;
        }
        
        .trust-element p {
            font-size: 14px;
            color: rgba(255, 255, 255, 0.8);
        }
        
        /* FAQ Section */
        .faq {
            padding: 100px 0;
            background-color: var(--section-bg);
        }
        
        .faq-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .faq-title h2 {
            font-size: 36px;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .faq-container {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .faq-item {
            background-color: white;
            border-radius: 10px;
            margin-bottom: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            overflow: hidden;
        }
        
        .faq-question {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 30px;
            cursor: pointer;
            font-weight: 500;
            font-size: 18px;
            color: var(--primary);
        }
        
        .faq-answer {
            padding: 0 30px 20px;
            color: var(--text-light);
        }
        
        .reviews {
            margin-top: 80px;
        }
        
        .reviews-title {
            text-align: center;
            margin-bottom: 40px;
        }
        
        .reviews-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }
        
        .review {
            background-color: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
        .review-header {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .review-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            margin-right: 15px;
            background-color: #ddd;
        }
        
        .review-info h4 {
            font-size: 18px;
            margin-bottom: 5px;
        }
        
        .review-stars {
            color: gold;
        }
        
        .review-content {
            margin-top: 15px;
            color: var(--text);
        }
        
        /* Footer */
        footer {
            padding: 60px 0;
            background-color: var(--dark);
            color: white;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 40px;
        }
        
        .footer-logo {
            font-size: 24px;
            font-weight: 700;
            margin-bottom: 20px;
        }
        
        .footer-about p {
            color: rgba(255, 255, 255, 0.7);
            margin-bottom: 20px;
        }
        
        .footer-heading {
            font-size: 18px;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-heading::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 2px;
            background-color: var(--accent);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: rgba(255, 255, 255, 0.7);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--accent);
        }
        
        .footer-contact-item {
            display: flex;
            margin-bottom: 15px;
        }
        
        .footer-contact-item svg {
            margin-right: 15px;
            color: var(--accent);
        }
        
        .footer-social {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .footer-social a {
            display: inline-flex;
            justify-content: center;
            align-items: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            transition: all 0.3s;
        }
        
        .footer-social a:hover {
            background-color: var(--accent);
        }
        
        .footer-form input {
            width: 100%;
            padding: 12px;
            border-radius: 5px;
            border: none;
            margin-bottom: 15px;
        }
        
        .footer-bottom {
            margin-top: 40px;
            padding-top: 20px;
            text-align: center;
            color: rgba(255, 255, 255, 0.5);
            font-size: 14px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Mobile Responsive */
        @media (max-width: 1024px) {
            .steps-container,
            .testimonials,
            .gallery,
            .reviews-grid,
            .footer-container {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .hero::before {
                width: 40%;
            }
            
            .hero-content {
                width: 60%;
            }
        }
        
        @media (max-width: 768px) {
            .hero {
                padding: 150px 0 80px;
            }
            
            .hero::before {
                display: none;
            }
            
            .hero-content {
                width: 100%;
            }
            
            .steps-container,
            .testimonials,
            .gallery,
            .reviews-grid,
            .footer-container {
                grid-template-columns: 1fr;
            }
            
            .trust-elements {
                flex-direction: column;
                gap: 20px;
            }
            
            .nav-menu {
                display: none;
            }
            
            .cta-buttons {
                flex-direction: column;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero h2 {
                font-size: 24px;
            }
        }
        
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }
        
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">3TR Care</div>
            <nav>
                <ul class="nav-menu">
                    <li><a href="#solution">솔루션</a></li>
                    <li><a href="#trust">전문성</a></li>
                    <li><a href="#faq">FAQ</a></li>
                    <li><a href="#contact">상담예약</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content fade-in">
                <h1>The 3TR Care Series</h1>
                <h2>시간(Time)을 리젠하다</h2>
                <p>당신의 얼굴, 표정, 라이프스타일까지 반영한<br>완전히 새로운 안티에이징 디자인 솔루션</p>
                <div class="cta-buttons">
                    <a href="#booking" class="btn btn-primary">무료 상담 예약하기</a>
                    <a href="#gallery" class="btn btn-secondary">포트폴리오 보기</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Steps Section -->
    <section class="steps" id="solution">
        <div class="container">
            <div class="steps-title fade-in">
                <h2>단계별 맞춤 안티에이징 솔루션</h2>
                <p>당신만의 얼굴을 위한 정교한 4단계 시술 과정</p>
            </div>
            <div class="steps-container">
                <div class="step-card fade-in">
                    <div class="step-number">STEP 01</div>
                    <h3>Tailored Design</h3>
                    <p class="step-quote">"단순한 진단을 넘어, 당신만의 실루엣을 설계합니다."</p>
                    <div class="step-features">
                        <div class="step-feature">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9 16.17L4.83 12L3.41 13.41L9 19L21 7L19.59 5.59L9 16.17Z" fill="#16a085"/>
                            </svg>
                            <p>1:1 맞춤 디자인</p>
                        </div>
                        <div class="step-feature">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9 16.17L4.83 12L3.41 13.41L9 19L21 7L19.59 5.59L9 16.17Z" fill="#16a085"/>
                            </svg>
                            <p>라이프스타일과 표정까지 고려한 프리디자인</p>
                        </div>
                        <div class="step-feature">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9 16.17L4.83 12L3.41 13.41L9 19L21 7L19.59 5.59L9 16.17Z" fill="#16a085"/>
                            </svg>
                            <p>상담 & 촬영 & 분석 기반 설계</p>
                        </div>
                    </div>
                </div>
                <div class="step-card fade-in">
                    <div class="step-number">STEP 02</div>
                    <h3>Tone / Texture / Tension</h3>
                    <p class="step-quote">"피부의 3T를 정교하게 되살립니다."</p>
                    <div class="step-features">
                        <div class="step-feature">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9 16.17L4.83 12L3.41 13.41L9 19L21 7L19.59 5.59L9 16.17Z" fill="#16a085"/>
                            </svg>
                            <p>Tone: 균일한 피부톤</p>
                        </div>
                        <div class="step-feature">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9 16.17L4.83 12L3.41 13.41L9 19L21 7L19.59 5.59L9 16.17Z" fill="#16a085"/>
                            </svg>
                            <p>Texture: 밀도 있고 매끈한 결</p>
                        </div>
                        <div class="step-feature">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9 16.17L4.83 12L3.41 13.41L9 19L21 7L19.59 5.59L9 16.17Z" fill="#16a085"/>
                            </svg>
                            <p>Tension: 탄탄한 리프팅</p>
                        </div>
                    </div>
                </div>
                <div class="step-card fade-in">
                    <div class="step-number">STEP 03</div>
                    <h3>지속적 케어 & 리파인</h3>
                    <p class="step-quote">"진짜 동안은, 지속적인 동행에서 시작됩니다."</p>
                    <div class="step-features">
                        <div class="step-feature">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9 16.17L4.83 12L3.41 13.41L9 19L21 7L19.59 5.59L9 16.17Z" fill="#16a085"/>
                            </svg>
                            <p>리터치 및 리디자인 관리</p>
                        </div>
                        <div class="step-feature">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9 16.17L4.83 12L3.41 13.41L9 19L21 7L19.59 5.59L9 16.17Z" fill="#16a085"/>
                            </svg>
                            <p>주기적 모니터링 및 포인트 케어</p>
                        </div>
                        <div class="step-feature">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9 16.17L4.83 12L3.41 13.41L9 19L21 7L19.59 5.59L9 16.17Z" fill="#16a085"/>
                            </svg>
                            <p>고객 피부 변화 기반 지속적 보완</p>
                        </div>
                    </div>
                </div>
                <div class="step-card fade-in">
                    <div class="step-number">STEP 04</div>
                    <h3>줄기세포 기반 완성</h3>
                    <p class="step-quote">"가장 정교하고 안전한 회복 솔루션"</p>
                    <div class="step-features">
                        <div class="step-feature">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9 16.17L4.83 12L3.41 13.41L9 19L21 7L19.59 5.59L9 16.17Z" fill="#16a085"/>
                            </svg>
                            <p>자가 줄기세포 활용</p>
                        </div>
                        <div class="step-feature">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9 16.17L4.83 12L3.41 13.41L9 19L21 7L19.59 5.59L9 16.17Z" fill="#16a085"/>
                            </svg>
                            <p>고유한 회복력으로 자연스럽고 나다운 완성</p>
                        </div>
                        <div class="step-feature">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M9 16.17L4.83 12L3.41 13.41L9 19L21 7L19.59 5.59L9 16.17Z" fill="#16a085"/>
                            </svg>
                            <p>시술이 아닌, 재생 기반 디자인</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Trust Section -->
    <section class="trust" id="trust">
        <div class="container">
            <div class="trust-title fade-in">
                <h2>신뢰할 수 있는 결과</h2>
                <p>실제 고객 사례와 전문가의 기술력</p>
            </div>
            <div class="gallery" id="gallery">
                <div class="gallery-item fade-in">
                    <img src="/api/placeholder/400/300" alt="Before and After 1">
                </div>
                <div class="gallery-item fade-in">
                    <img src="/api/placeholder/400/300" alt="Before and After 2">
                </div>
                <div class="gallery-item fade-in">
                    <img src="/api/placeholder/400/300" alt="Before and After 3">
                </div>
                <div class="gallery-item fade-in">
                    <img src="/api/placeholder/400/300" alt="시술 과정 1">
                </div>
                <div class="gallery-item fade-in">
                    <img src="/api/placeholder/400/300" alt="시술 과정 2">
                </div>
                <div class="gallery-item fade-in">
                    <img src="/api/placeholder/400/300" alt="시술 과정 3">
                </div>
            </div>
            <div class="testimonials">
                <div class="testimonial fade-in">
                    <p>"어느 병원을 가도 어색한 필러 자국이 있었는데, 3TR 케어로 완전히 자연스러워졌어요. 특히 라이프스타일까지 고려한 디자인이 정말 달랐습니다."</p>
                    <div class="testimonial-author">
                        <img src="/api/placeholder/50/50" alt="Customer 1">
                        <div class="testimonial-info">
                            <h4>김지수</h4>
                            <span>38세, 직장인</span>
                        </div>
                    </div>
                </div>
                <div class="testimonial fade-in">
                    <p>"회복 기간이 놀라울 정도로 짧았습니다. 줄기세포 활용 덕분인지 붓기도 거의 없었고, 결과물도 매우 만족스럽습니다. 무엇보다 자연스러운 표정이 유지된다는 점이 최고예요."</p>
                    <div class="testimonial-author">
                        <img src="/api/placeholder/50/50" alt="Customer 2">
                        <div class="testimonial-info">
                            <h4>이승민</h4>
                            <span>45세, 사업가</span>
                        </div>
                    </div>
                </div>
                <div class="testimonial fade-in">
                    <p>"단순히 주름만 펴지는 것이 아니라 피부의 질감과 탄력이 함께 개선되는 느낌입니다. 1년이 지났는데도 효과가 꾸준히 유지되고 있어요. 지속적인 관리 시스템도 정말 좋습니다."</p>
                    <div class="testimonial-author">
                        <img src="/api/placeholder/50/50" alt="Customer 3">
                        <div class="testimonial-info">
                            <h4>박현주</h4>
                            <span>52세, 교수</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Booking Section -->
    <section class="booking" id="booking">
        <div class="container">
            <h2 class="fade-in">지금, 당신만의 젊음을 설계하세요</h2>
            <p class="fade-in">단 한 번의 상담으로 완전히 새로운 변화를 경험하세요</p>
            <div class="booking-buttons fade-in">
                <a href="#contact" class="btn btn-primary">1:1 무료 상담 신청</a>
                <a href="#gallery" class="btn btn-secondary">케이스 보기</a>
            </div>
            <div class="trust-elements fade-in">
                <div class="trust-element">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 2C6.48 2 2 6.48 2 12C2 17.52 6.48 22 12 22C17.52 22 22 17.52 22 12C22 6.48 17.52 2 12 2ZM12 20C7.59 20 4 16.41 4 12C4 7.59 7.59 4 12 4C16.41 4 20 7.59 20 12C20 16.41 16.41 20 12 20ZM16.59 7.58L10 14.17L7.41 11.59L6 13L10 17L18 9L16.59 7.58Z" fill="white"/>
                    </svg>
                    <h3>상담 시 비용 없음</h3>
                    <p>초기 상담은 완전 무료로 진행됩니다</p>
                </div>
                <div class="trust-element">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 2C6.48 2 2 6.48 2 12C2 17.52 6.48 22 12 22C17.52 22 22 17.52 22 12C22 6.48 17.52 2 12 2ZM12 20C7.59 20 4 16.41 4 12C4 7.59 7.59 4 12 4C16.41 4 20 7.59 20 12C20 16.41 16.41 20 12 20ZM16.59 7.58L10 14.17L7.41 11.59L6 13L10 17L18 9L16.59 7.58Z" fill="white"/>
                    </svg>
                    <h3>비수술적 접근</h3>
                    <p>최소한의 개입으로 최대의 효과</p>
                </div>
                <div class="trust-element">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 2C6.48 2 2 6.48 2 12C2 17.52 6.48 22 12 22C17.52 22 22 17.52 22 12C22 6.48 17.52 2 12 2ZM12 20C7.59 20 4 16.41 4 12C4 7.59 7.59 4 12 4C16.41 4 20 7.59 20 12C20 16.41 16.41 20 12 20ZM16.59 7.58L10 14.17L7.41 11.59L6 13L10 17L18 9L16.59 7.58Z" fill="white"/>
                    </svg>
                    <h3>100% 커스터마이징</h3>
                    <p>당신만을 위한 맞춤형 디자인</p>
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ Section -->
    <section class="faq" id="faq">
        <div class="container">
            <div class="faq-title fade-in">
                <h2>자주 묻는 질문</h2>
                <p>궁금한 점을 미리 확인하세요</p>
            </div>
            <div class="faq-container">
                <div class="faq-item fade-in">
                    <div class="faq-question">
                        시술 소요 시간은 얼마나 되나요?
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M16.59 8.59L12 13.17L7.41 8.59L6 10L12 16L18 10L16.59 8.59Z" fill="#2c3e50"/>
                        </svg>
                    </div>
                    <div class="faq-answer">
                        개인별 맞춤 설계에 따라 다르지만, 일반적으로 첫 방문 시 약 2-3시간 정도 소요됩니다. 상담, 진단, 설계까지 포함된 시간이며, 실제 시술은 단계별로 진행됩니다.
                    </div>
                </div>
                <div class="faq-item fade-in">
                    <div class="faq-question">
                        회복 기간은 어느 정도인가요?
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M16.59 8.59L12 13.17L7.41 8.59L6 10L12 16L18 10L16.59 8.59Z" fill="#2c3e50"/>
                        </svg>
                    </div>
                    <div class="faq-answer">
                        줄기세포 기반 3TR 케어는 일반적인 시술보다 회복이 빠른 편입니다. 가벼운 붓기는 1-3일 내로 가라앉으며, 대부분 5-7일 이내에 일상생활로 복귀 가능합니다.
                    </div>
                </div>
                <div class="faq-item fade-in">
                    <div class="faq-question">
                        줄기세포는 어떻게 사용되나요?
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M16.59 8.59L12 13.17L7.41 8.59L6 10L12 16L18 10L16.59 8.59Z" fill="#2c3e50"/>
                        </svg>
                    </div>
                    <div class="faq-answer">
                        자가 줄기세포를 추출하여 안전하게 배양한 후 시술 과정에서 활용합니다. 피부의 자연 재생을 촉진하고 콜라겐 생성을 활성화하여 지속적인 피부 개선 효과를 제공합니다. 모든 과정은 GMP 인증 시설에서 진행됩니다.
                    </div>
                </div>
                <div class="faq-item fade-in">
                    <div class="faq-question">
                        효과는 얼마나 오래 지속되나요?
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M16.59 8.59L12 13.17L7.41 8.59L6 10L12 16L18 10L16.59 8.59Z" fill="#2c3e50"/>
                        </svg>
                    </div>
                    <div class="faq-answer">
                        일반적으로 1-2년 동안 효과가 유지됩니다. 3TR 케어의 장점은 지속적인 관리 시스템을 통해 효과를 계속 유지하고 강화할 수 있다는 점입니다. 3개월마다 진행되는 포인트 케어를 통해 더 오랜 기간 효과를 유지할 수 있습니다.
                    </div>
                </div>
            </div>
            <div class="reviews">
                <div class="reviews-title fade-in">
                    <h3>실제 고객 후기</h3>
                </div>
                <div class="reviews-grid">
                    <div class="review fade-in">
                        <div class="review-header">
                            <div class="review-avatar"></div>
                            <div class="review-info">
                                <h4>장미영</h4>
                                <div class="review-stars">★★★★★</div>
                            </div>
                        </div>
                        <div class="review-content">
                            <p>재생 기술에 관심이 많았는데, 여기서 받은 3TR 케어는 정말 획기적이었습니다. 줄기세포의 힘인지 피부가 속부터 차오르는 느낌이에요. 무엇보다 자연스러움이 큰 장점입니다.</p>
                        </div>
                    </div>
                    <div class="review fade-in">
                        <div class="review-header">
                            <div class="review-avatar"></div>
                            <div class="review-info">
                                <h4>최준호</h4>
                                <div class="review-stars">★★★★★</div>
                            </div>
                        </div>
                        <div class="review-content">
                            <p>남자 입장에서도 매우 만족스러웠습니다. 티 나지 않으면서도 확실히 젊어 보이는 효과가 있었어요. 특히 표정 근육까지 고려한 맞춤 디자인이 인상적이었습니다.</p>
                        </div>
                    </div>
                    <div class="review fade-in">
                        <div class="review-header">
                            <div class="review-avatar"></div>
                            <div class="review-info">
                                <h4>한소연</h4>
                                <div class="review-stars">★★★★★</div>
                            </div>
                        </div>
                        <div class="review-content">
                            <p>일반 필러는 항상 어색했는데, 3TR 케어는 정말 자연스러워요. 6개월이 지난 지금도 효과가 그대로입니다. 특히 지속적인 관리 시스템이 마음에 들어요.</p>
                        </div>
                    </div>
                    <div class="review fade-in">
                        <div class="review-header">
                            <div class="review-avatar"></div>
                            <div class="review-info">
                                <h4>정태영</h4>
                                <div class="review-stars">★★★★★</div>
                            </div>
                        </div>
                        <div class="review-content">
                            <p>피부 질감이 확연히 개선되었어요. 다른 시술들은 일시적인 효과였는데, 3TR는 시간이 지날수록 더 좋아지는 느낌입니다. 정말 추천합니다!</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="footer-container">
                <div class="footer-about fade-in">
                    <div class="footer-logo">3TR Care</div>
                    <p>The 3TR Care Series는 Tone, Texture, Tension을 리젠하는 맞춤형 안티에이징 솔루션입니다. 당신만의 시간을 되찾아 드립니다.</p>
                    <div class="footer-social">
                        <a href="#">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                                <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                            </svg>
                        </a>
                        <a href="#">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                                <path d="M22.675 0h-21.35c-.732 0-1.325.593-1.325 1.325v21.351c0 .731.593 1.324 1.325 1.324h11.495v-9.294h-3.128v-3.622h3.128v-2.671c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12v9.293h6.116c.73 0 1.323-.593 1.323-1.325v-21.35c0-.732-.593-1.325-1.325-1.325z"/>
                            </svg>
                        </a>
                        <a href="#">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                                <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/>
                            </svg>
                        </a>
                        <a href="#">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                                <path d="M19.615 3.184c-3.604-.246-11.631-.245-15.23 0-3.897.266-4.356 2.62-4.385 8.816.029 6.185.484 8.549 4.385 8.816 3.6.245 11.626.246 15.23 0 3.897-.266 4.356-2.62 4.385-8.816-.029-6.185-.484-8.549-4.385-8.816zm-10.615 12.816v-8l8 3.993-8 4.007z"/>
                            </svg>
                        </a>
                    </div>
                </div>
                <div class="footer-links-section fade-in">
                    <h3 class="footer-heading">고객 지원</h3>
                    <ul class="footer-links">
                        <li><a href="#">자주 묻는 질문</a></li>
                        <li><a href="#">시술 가이드</a></li>
                        <li><a href="#">케어 제품</a></li>
                        <li><a href="#">예약 안내</a></li>
                    </ul>
                </div>
                <div class="footer-links-section fade-in">
                    <h3 class="footer-heading">진료 정보</h3>
                    <ul class="footer-links">
                        <li><a href="#">의료진 소개</a></li>
                        <li><a href="#">클리닉 투어</a></li>
                        <li><a href="#">시술 정보</a></li>
                        <li><a href="#">줄기세포 연구</a></li>
                    </ul>
                </div>
                <div class="footer-contact fade-in">
                    <h3 class="footer-heading">연락처</h3>
                    <div class="footer-contact-item">
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                            <path d="M12 2C8.13 2 5 5.13 5 9C5 14.25 12 22 12 22C12 22 19 14.25 19 9C19 5.13 15.87 2 12 2ZM12 11.5C10.62 11.5 9.5 10.38 9.5 9C9.5 7.62 10.62 6.5 12 6.5C13.38 6.5 14.5 7.62 14.5 9C14.5 10.38 13.38 11.5 12 11.5Z" fill="#16a085"/>
                        </svg>
                        <p>서울특별시 강남구 테헤란로 123<br>메디컬타워 7층</p>
                    </div>
                    <div class="footer-contact-item">
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                            <path d="M6.62 10.79C8.06 13.62 10.38 15.94 13.21 17.38L15.41 15.18C15.69 14.9 16.08 14.82 16.43 14.93C17.55 15.3 18.75 15.5 20 15.5C20.55 15.5 21 15.95 21 16.5V20C21 20.55 20.55 21 20 21C10.61 21 3 13.39 3 4C3 3.45 3.45 3 4 3H7.5C8.05 3 8.5 3.45 8.5 4C8.5 5.25 8.7 6.45 9.07 7.57C9.18 7.92 9.1 8.31 8.82 8.59L6.62 10.79Z" fill="#16a085"/>
                        </svg>
                        <p>02-123-4567</p>
                    </div>
                    <div class="footer-contact-item">
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                            <path d="M20 4H4C2.9 4 2.01 4.9 2.01 6L2 18C2 19.1 2.9 20 4 20H20C21.1 20 22 19.1 22 18V6C22 4.9 21.1 4 20 4ZM20 8L12 13L4 8V6L12 11L20 6V8Z" fill="#16a085"/>
                        </svg>
                        <p>info@3trcare.com</p>
                    </div>
                    <div class="footer-contact-item">
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                            <path d="M11.99 2C6.47 2 2 6.48 2 12C2 17.52 6.47 22 11.99 22C17.52 22 22 17.52 22 12C22 6.48 17.52 2 11.99 2ZM12 20C7.58 20 4 16.42 4 12C4 7.58 7.58 4 12 4C16.42 4 20 7.58 20 12C20 16.42 16.42 20 12 20ZM12.5 7H11V13L16.25 16.15L17 14.92L12.5 12.25V7Z" fill="#16a085"/>
                        </svg>
                        <p>평일 10:00 - 19:00<br>토요일 10:00 - 17:00<br>일요일 휴무</p>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p>© 2025 The 3TR Care Series. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Fade In Animation
        document.addEventListener('DOMContentLoaded', function() {
            const fadeElements = document.querySelectorAll('.fade-in');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('visible');
                    }
                });
            }, {
                threshold: 0.1
            });
            
            fadeElements.forEach(element => {
                observer.observe(element);
            });
            
            // FAQ Accordion
            const faqQuestions = document.querySelectorAll('.faq-question');
            
            faqQuestions.forEach(question => {
                question.addEventListener('click', () => {
                    const answer = question.nextElementSibling;
                    const isOpen = answer.style.maxHeight;
                    
                    // Close all answers
                    document.querySelectorAll('.faq-answer').forEach(item => {
                        item.style.maxHeight = null;
                    });
                    
                    // Toggle current answer
                    if (!isOpen) {
                        answer.style.maxHeight = answer.scrollHeight + 'px';
                    }
                });
            });
        });
    </script>
</body>
</html>r-landing-page.html…]()
