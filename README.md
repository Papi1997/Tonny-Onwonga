# Tonny-Onwonga
Tonny Onwonga


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tonny Onwonga - Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    /* Base styles */
    :root {
      --portfolio-accent: #F59E0B;
      --portfolio-800: #1E3A8A;
      --portfolio-700: #4338ca;
      --portfolio-600: #4f46e5;
      --portfolio-500: #6366f1;
      --portfolio-400: #818cf8;
      --portfolio-300: #a5b4fc;
      --portfolio-200: #c7d2fe;
      --portfolio-100: #e0e7ff;
      --portfolio-50: #eef2ff;
    }
    
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    body {
      font-family: 'Inter', sans-serif;
      color: #333;
      line-height: 1.6;
      overflow-x: hidden;
    }
    
    h1, h2, h3, h4, h5, h6 {
      font-family: 'Playfair Display', serif;
      color: var(--portfolio-800);
    }
    
    a {
      text-decoration: none;
      color: inherit;
    }
    
    ul {
      list-style: none;
    }
    
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 2rem;
    }
    
    .section {
      padding: 4rem 0;
    }
    
    .section-title {
      font-size: 2rem;
      font-weight: bold;
      margin-bottom: 2rem;
      position: relative;
    }
    
    .section-title::after {
      content: '';
      position: absolute;
      left: 0;
      bottom: -0.75rem;
      width: 5rem;
      height: 0.25rem;
      background-color: var(--portfolio-accent);
    }
    
    .btn {
      display: inline-block;
      padding: 0.75rem 1.5rem;
      border-radius: 0.375rem;
      font-weight: 500;
      cursor: pointer;
      transition: all 0.3s ease;
    }
    
    .btn-primary {
      background-color: var(--portfolio-800);
      color: white;
    }
    
    .btn-primary:hover {
      background-color: var(--portfolio-700);
    }
    
    .btn-secondary {
      background-color: white;
      color: var(--portfolio-800);
      border: 1px solid #e5e7eb;
    }
    
    .btn-secondary:hover {
      background-color: #f9fafb;
    }
    
    .skill-tag {
      display: inline-block;
      padding: 0.25rem 0.75rem;
      background-color: var(--portfolio-100);
      color: var(--portfolio-800);
      border-radius: 9999px;
      font-size: 0.875rem;
      margin-right: 0.5rem;
      margin-bottom: 0.5rem;
    }
    
    .timeline-item {
      position: relative;
      padding-left: 2rem;
      padding-bottom: 2rem;
      border-left: 1px solid var(--portfolio-200);
    }
    
    .timeline-item::before {
      content: '';
      position: absolute;
      left: -0.5rem;
      top: 0;
      width: 1rem;
      height: 1rem;
      border-radius: 50%;
      background-color: var(--portfolio-accent);
    }
    
    .timeline-item:last-child {
      border-left: none;
    }
    
    .gradient-bg {
      background: linear-gradient(135deg, #ffffff 0%, #f0f4ff 100%);
    }
    
    /* Header styles */
    header {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      z-index: 1000;
      padding: 1.25rem 0;
      background-color: rgba(255, 255, 255, 0.9);
      backdrop-filter: blur(5px);
      transition: all 0.3s ease;
    }
    
    header.scrolled {
      padding: 0.75rem 0;
      box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
    }
    
    .header-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    
    .logo {
      font-family: 'Playfair Display', serif;
      font-size: 1.25rem;
      font-weight: bold;
      color: var(--portfolio-800);
    }
    
    .nav-desktop {
      display: flex;
      gap: 2rem;
    }
    
    .nav-link {
      position: relative;
      padding: 0.25rem 0.5rem;
      color: #4b5563;
      transition: color 0.3s ease;
    }
    
    .nav-link::after {
      content: '';
      position: absolute;
      left: 0;
      bottom: -0.25rem;
      width: 0;
      height: 0.125rem;
      background-color: var(--portfolio-accent);
      transition: width 0.3s ease;
    }
    
    .nav-link:hover {
      color: var(--portfolio-800);
    }
    
    .nav-link:hover::after {
      width: 100%;
    }
    
    .mobile-menu-btn {
      display: none;
      background: none;
      border: none;
      cursor: pointer;
      font-size: 1.5rem;
      color: #4b5563;
    }
    
    .mobile-menu {
      display: none;
      position: absolute;
      top: 100%;
      left: 0;
      right: 0;
      background-color: white;
      padding: 1rem 0;
      box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
    }
    
    .mobile-menu a {
      display: block;
      padding: 0.75rem 2rem;
      color: #4b5563;
    }
    
    /* Hero styles */
    #hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding-top: 4rem;
    }
    
    .hero-content {
      max-width: 48rem;
    }
    
    .hero-title {
      font-size: 3.5rem;
      font-weight: bold;
      margin-bottom: 1.5rem;
    }
    
    .hero-subtitle {
      font-size: 1.5rem;
      color: #4b5563;
      margin-bottom: 2rem;
    }
    
    .hero-text {
      font-size: 1.125rem;
      color: #4b5563;
      margin-bottom: 2.5rem;
      max-width: 36rem;
    }
    
    .hero-btns {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
    }
    
    /* About styles */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2.5rem;
    }
    
    .competencies-list li {
      display: flex;
      align-items: flex-start;
      margin-bottom: 0.75rem;
    }
    
    .competencies-list li::before {
      content: '•';
      color: var(--portfolio-accent);
      margin-right: 0.5rem;
    }
    
    .language-bar {
      height: 0.5rem;
      width: 100%;
      background-color: #e5e7eb;
      border-radius: 9999px;
      margin-bottom: 1rem;
    }
    
    .language-progress {
      height: 100%;
      background-color: var(--portfolio-accent);
      border-radius: 9999px;
    }
    
    /* Experience styles */
    .experience-list {
      padding-left: 0;
    }
    
    .experience-item h3 {
      font-size: 1.25rem;
      margin-bottom: 0.5rem;
    }
    
    .experience-item-header {
      margin-bottom: 0.75rem;
    }
    
    .experience-company {
      font-weight: 500;
      color: var(--portfolio-700);
    }
    
    .experience-date {
      color: #6b7280;
    }
    
    .experience-duties li {
      display: flex;
      align-items: flex-start;
      margin-bottom: 0.5rem;
    }
    
    .experience-duties li::before {
      content: '•';
      color: var(--portfolio-accent);
      margin-right: 0.5rem;
    }
    
    /* Education styles */
    .education-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
      gap: 2rem;
    }
    
    .education-card {
      background-color: white;
      padding: 1.5rem;
      border-radius: 0.5rem;
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
      border: 1px solid #f3f4f6;
      transition: all 0.3s ease;
    }
    
    .education-card:hover {
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      border-color: var(--portfolio-200);
    }
    
    .education-card-header {
      display: flex;
      justify-content: space-between;
      margin-bottom: 1rem;
    }
    
    /* Skills styles */
    .skills-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2rem;
    }
    
    .skills-card {
      background-color: white;
      padding: 1.5rem;
      border-radius: 0.5rem;
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
    }
    
    .skills-card h3 {
      font-size: 1.25rem;
      margin-bottom: 1rem;
      padding-bottom: 0.5rem;
      border-bottom: 1px solid #e5e7eb;
    }
    
    /* Contact styles */
    .contact-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2.5rem;
    }
    
    .contact-info-item {
      display: flex;
      align-items: center;
      margin-bottom: 1rem;
    }
    
    .contact-icon {
      width: 3rem;
      height: 3rem;
      background-color: var(--portfolio-100);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-right: 1rem;
    }
    
    .contact-form {
      background-color: white;
      padding: 1.5rem;
      border-radius: 0.5rem;
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
    }
    
    .form-group {
      margin-bottom: 1rem;
    }
    
    .form-label {
      display: block;
      font-size: 0.875rem;
      font-weight: 500;
      color: #4b5563;
      margin-bottom: 0.25rem;
    }
    
    .form-input, .form-textarea {
      width: 100%;
      padding: 0.5rem 0.75rem;
      border: 1px solid #d1d5db;
      border-radius: 0.375rem;
      outline: none;
      transition: border-color 0.3s ease;
    }
    
    .form-input:focus, .form-textarea:focus {
      border-color: var(--portfolio-500);
      box-shadow: 0 0 0 3px rgba(99, 102, 241, 0.1);
    }
    
    .form-textarea {
      min-height: 6rem;
      resize: vertical;
    }
    
    /* Footer styles */
    footer {
      background-color: var(--portfolio-800);
      color: white;
      padding: 2.5rem 0;
    }
    
    .footer-title {
      font-size: 1.5rem;
      font-weight: bold;
      margin-bottom: 1rem;
    }
    
    .footer-subtitle {
      color: var(--portfolio-200);
      margin-bottom: 1.5rem;
    }
    
    .footer-links {
      display: flex;
      justify-content: center;
      gap: 2rem;
      margin-bottom: 2rem;
    }
    
    .footer-links a {
      color: #d1d5db;
      transition: color 0.3s ease;
    }
    
    .footer-links a:hover {
      color: white;
    }
    
    .footer-copyright {
      text-align: center;
      color: #9ca3af;
      padding-top: 1.5rem;
      border-top: 1px solid #4b5563;
    }
    
    /* Responsive styles */
    @media (max-width: 768px) {
      .section-title {
        font-size: 1.75rem;
      }
      
      .hero-title {
        font-size: 2.5rem;
      }
      
      .hero-subtitle {
        font-size: 1.25rem;
      }
      
      .nav-desktop {
        display: none;
      }
      
      .mobile-menu-btn {
        display: block;
      }
      
      .mobile-menu.active {
        display: block;
      }
      
      .about-grid, .skills-grid, .contact-grid {
        grid-template-columns: 1fr;
      }
      
      .education-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <!-- Header -->
  <header id="header">
    <div class="container header-container">
      <a href="#" class="logo">Tonny Onwonga</a>
      
      <nav class="nav-desktop">
        <a href="#about" class="nav-link">About</a>
        <a href="#experience" class="nav-link">Experience</a>
        <a href="#education" class="nav-link">Education</a>
        <a href="#skills" class="nav-link">Skills</a>
        <a href="#contact" class="nav-link">Contact</a>
      </nav>
      
      <button class="mobile-menu-btn" aria-label="Toggle menu">
        ☰
      </button>
    </div>
    
    <div class="mobile-menu" id="mobileMenu">
      <a href="#about">About</a>
      <a href="#experience">Experience</a>
      <a href="#education">Education</a>
      <a href="#skills">Skills</a>
      <a href="#contact">Contact</a>
    </div>
  </header>

  <!-- Hero Section -->
  <section id="hero" class="section gradient-bg">
    <div class="container">
      <div class="hero-content">
        <h1 class="hero-title">Tonny Onwonga</h1>
        <h2 class="hero-subtitle">Customer Experience & Operations Specialist</h2>
        <p class="hero-text">
          Dedicated professional with expertise in customer relationship management, 
          complaint resolution, and operational excellence in the financial sector.
        </p>
        <div class="hero-btns">
          <a href="#contact" class="btn btn-primary">Contact Me</a>
          <a href="#experience" class="btn btn-secondary">View Experience</a>
        </div>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="section">
    <div class="container">
      <h2 class="section-title">About Me</h2>
      
      <div class="about-grid">
        <div>
          <h3 style="font-size: 1.5rem; margin-bottom: 1rem;">Career Objectives</h3>
          <ul class="competencies-list">
            <li>To utilize my strong communication, analytical, and organizational skills to ensure timely and effective resolution of customer complaints.</li>
            <li>To foster excellent customer experiences by adhering to industry standards, ensuring compliance, and enhancing processes for continuous improvement.</li>
            <li>To contribute to the organization's customer service delivery goals through ethical and efficient handling of customer concerns.</li>
          </ul>

          <h3 style="font-size: 1.5rem; margin-top: 2rem; margin-bottom: 1rem;">Key Competencies</h3>
          <ul class="competencies-list">
            <li><strong>Customer Relationship Management:</strong> Extensive experience resolving customer issues promptly and enhancing satisfaction.</li>
            <li><strong>Analytical & Problem-Solving Skills:</strong> Adept at analyzing complaints data to identify root causes and develop effective resolutions.</li>
            <li><strong>Compliance & Standards:</strong> Skilled in ensuring adherence to regulatory guidelines and internal complaint handling procedures.</li>
            <li><strong>Communication Excellence:</strong> Strong verbal and written communication abilities for clear, empathetic, and professional interactions.</li>
            <li><strong>Stakeholder Management:</strong> Proficient in collaborating with cross-functional teams to address and resolve customer concerns.</li>
          </ul>
        </div>

        <div>
          <div style="background-color: var(--portfolio-50); padding: 2rem; border-radius: 0.5rem; border: 1px solid var(--portfolio-100); box-shadow: 0 1px 3px rgba(0,0,0,0.1);">
            <h3 style="font-size: 1.5rem; margin-bottom: 1.5rem;">Languages</h3>
            
            <div style="margin-bottom: 1rem;">
              <div style="display: flex; justify-content: space-between; margin-bottom: 0.5rem;">
                <span style="font-weight: 500;">Swahili</span>
                <span>Native</span>
              </div>
              <div class="language-bar">
                <div class="language-progress" style="width: 100%;"></div>
              </div>
            </div>
            
            <div style="margin-bottom: 1rem;">
              <div style="display: flex; justify-content: space-between; margin-bottom: 0.5rem;">
                <span style="font-weight: 500;">English</span>
                <span>Fluent</span>
              </div>
              <div class="language-bar">
                <div class="language-progress" style="width: 95%;"></div>
              </div>
            </div>
            
            <div>
              <div style="display: flex; justify-content: space-between; margin-bottom: 0.5rem;">
                <span style="font-weight: 500;">German</span>
                <span>Basic</span>
              </div>
              <div class="language-bar">
                <div class="language-progress" style="width: 30%;"></div>
              </div>
            </div>

            <h3 style="font-size: 1.5rem; margin-top: 2.5rem; margin-bottom: 1.5rem;">Achievements</h3>
            <ul class="competencies-list">
              <li>Strengthened customer satisfaction metrics by resolving service requests within agreed timelines.</li>
              <li>Enhanced customer issue resolution processes, ensuring timely communication and compliance with risk and audit standards.</li>
              <li>Successfully managed escalations, achieving resolution while maintaining high ethical standards.</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Experience Section -->
  <section id="experience" class="section" style="background-color: var(--portfolio-50);">
    <div class="container">
      <h2 class="section-title">Professional Experience</h2>
      
      <div class="experience-list">
        <div class="timeline-item experience-item">
          <div class="experience-item-header">
            <h3>Card and ATM Operations Specialist</h3>
            <div style="display: flex; flex-direction: column; margin-bottom: 0.75rem;">
              <span class="experience-company">NCBA Group</span>
              <span class="experience-date">Oct 2022 – Present</span>
            </div>
          </div>
          <ul class="experience-duties">
            <li>Resolved customer service requests, including card issuance and PIN migrations, ensuring satisfaction and compliance with SLAs.</li>
            <li>Communicated effectively with customers on resolutions and escalated complex issues to appropriate teams.</li>
            <li>Analyzed operational gaps and implemented improvements to enhance customer experiences.</li>
            <li>Ensured compliance with audit standards and enterprise risk frameworks in all customer interactions.</li>
          </ul>
        </div>

        <div class="timeline-item experience-item">
          <div class="experience-item-header">
            <h3>Contact Centre Customer Experience Associate</h3>
            <div style="display: flex; flex-direction: column; margin-bottom: 0.75rem;">
              <span class="experience-company">NCBA Group</span>
              <span class="experience-date">Jul 2022 – Sep 2022</span>
            </div>
          </div>
          <ul class="experience-duties">
            <li>Handled customer inquiries, complaints, and escalations with a focus on resolving issues at first contact.</li>
            <li>Conducted surveys to gather customer feedback, analyzed trends, and recommended service improvements.</li>
            <li>Collaborated with teams to address fraud prevention and compliance with regulatory frameworks.</li>
          </ul>
        </div>

        <div class="timeline-item experience-item">
          <div class="experience-item-header">
            <h3>Economist Intern</h3>
            <div style="display: flex; flex-direction: column; margin-bottom: 0.75rem;">
              <span class="experience-company">Ministry of Sports, Culture, and Heritage</span>
              <span class="experience-date">May 2019 – Sep 2019</span>
            </div>
          </div>
          <ul class="experience-duties">
            <li>Assisted in analyzing feedback and resolving stakeholder concerns related to budget allocations and project impacts.</li>
            <li>Developed reports highlighting improvement areas for program efficiency.</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- Education Section -->
  <section id="education" class="section">
    <div class="container">
      <h2 class="section-title">Education</h2>
      
      <div class="education-grid">
        <div class="education-card">
          <div class="education-card-header">
            <div>
              <h3 style="font-size: 1.25rem;">WorldQuant University</h3>
              <p style="color: #6b7280;">Applied Data Science Lab</p>
            </div>
            <span style="font-size: 0.875rem; color: #6b7280;">Nov 2024 – Ongoing</span>
          </div>
          <p style="color: #4b5563;">
            Focused on Data Visualization, Predictive Models, and Machine Learning Ethics.
          </p>
        </div>

        <div class="education-card">
          <div class="education-card-header">
            <div>
              <h3 style="font-size: 1.25rem;">Amazon Web Services (AWS)</h3>
              <p style="color: #6b7280;">Cloud Computing & Data Science</p>
            </div>
            <span style="font-size: 0.875rem; color: #6b7280;">Oct 2024 – Ongoing</span>
          </div>
          <p style="color: #4b5563;">
            Learning Data Warehousing, Technical Essentials, and Practical Data Science with Amazon SageMaker.
          </p>
        </div>

        <div class="education-card">
          <div class="education-card-header">
            <div>
              <h3 style="font-size: 1.25rem;">Power Learn Project</h3>
              <p style="color: #6b7280;">Software Development & Data Analysis</p>
            </div>
            <span style="font-size: 0.875rem; color: #6b7280;">Feb 2024 – Aug 2024</span>
          </div>
          <p style="color: #4b5563;">
            Studied Python Programming, Machine Learning, SQL, and Advanced Excel.
          </p>
        </div>

        <div class="education-card">
          <div class="education-card-header">
            <div>
              <h3 style="font-size: 1.25rem;">Moi University</h3>
              <p style="color: #6b7280;">Bachelor of Arts in Economics</p>
            </div>
            <span style="font-size: 0.875rem; color: #6b7280;">Sep 2016 – Sep 2020</span>
          </div>
          <p style="color: #4b5563;">
            Focused on Financial Planning, Taxation, and Statistical Analysis.
          </p>
        </div>
      </div>

      <div style="margin-top: 2.5rem;">
        <h3 style="font-size: 1.5rem; margin-bottom: 1.5rem;">Certifications</h3>
        <div style="background-color: white; padding: 1.5rem; border-radius: 0.5rem; box-shadow: 0 1px 3px rgba(0,0,0,0.1); border: 1px solid #f3f4f6;">
          <ul class="competencies-list">
            <li>Customer Experience Certification (in progress)</li>
            <li>Quality Assurance Certification (in progress)</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- Skills Section -->
  <section id="skills" class="section" style="background-color: var(--portfolio-50);">
    <div class="container">
      <h2 class="section-title">Skills</h2>
      
      <div class="skills-grid">
        <div class="skills-card">
          <h3>Technical Skills</h3>
          <div style="margin-top: 1rem;">
            <span class="skill-tag">Data Analysis (SQL)</span>
            <span class="skill-tag">Python Programming</span>
            <span class="skill-tag">Advanced Excel</span>
            <span class="skill-tag">Report Writing & Documentation</span>
            <span class="skill-tag">Complaint Tracking & Resolution Tools</span>
            <span class="skill-tag">Statistical Analysis</span>
            <span class="skill-tag">Data Visualization</span>
            <span class="skill-tag">Financial Planning</span>
          </div>
        </div>
        
        <div class="skills-card">
          <h3>Soft Skills</h3>
          <div style="margin-top: 1rem;">
            <span class="skill-tag">Customer Service Excellence</span>
            <span class="skill-tag">Problem Solving</span>
            <span class="skill-tag">Communication</span>
            <span class="skill-tag">Stakeholder Management</span>
            <span class="skill-tag">Compliance & Standards</span>
            <span class="skill-tag">Analytical Thinking</span>
            <span class="skill-tag">Team Collaboration</span>
            <span class="skill-tag">Process Improvement</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="section">
    <div class="container">
      <h2 class="section-title">Contact Me</h2>
      
      <div class="contact-grid">
        <div>
          <h3 style="font-size: 1.5rem; margin-bottom: 1.5rem;">Get In Touch</h3>
          <p style="color: #4b5563; margin-bottom: 1.5rem;">
            Feel free to contact me for any work or suggestions below.
          </p>
          
          <div style="margin-bottom: 2rem;">
            <div class="contact-info-item">
              <div class="contact-icon">
                ✉️
              </div>
              <div>
                <h4 style="font-size: 0.875rem; color: #6b7280;">Email</h4>
                <a href="mailto:tonnyjarvis4@gmail.com" style="color: var(--portfolio-800); transition: color 0.3s ease;">
                  tonnyjarvis4@gmail.com
                </a>
              </div>
            </div>
            
            <div class="contact-info-item">
              <div class="contact-icon">
                📱
              </div>
              <div>
                <h4 style="font-size: 0.875rem; color: #6b7280;">Phone</h4>
                <a href="tel:+254799374150" style="color: var(--portfolio-800); transition: color 0.3s ease;">
                  +254 799 374 150
                </a>
              </div>
            </div>
          </div>
        </div>
        
        <div>
          <form class="contact-form">
            <div class="form-group">
              <label for="name" class="form-label">Name</label>
              <input type="text" id="name" class="form-input" required>
            </div>
            
            <div class="form-group">
              <label for="email" class="form-label">Email</label>
              <input type="email" id="email" class="form-input" required>
            </div>
            
            <div class="form-group">
              <label for="subject" class="form-label">Subject</label>
              <input type="text" id="subject" class="form-input" required>
            </div>
            
            <div class="form-group">
              <label for="message" class="form-label">Message</label>
              <textarea id="message" class="form-textarea" required></textarea>
            </div>
            
            <button type="submit" class="btn btn-primary" style="width: 100%; display: flex; align-items: center; justify-content: center;">
              Send Message
              <span style="margin-left: 0.5rem;">📤</span>
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="container" style="text-align: center;">
      <h2 class="footer-title">Tonny Onwonga</h2>
      <p class="footer-subtitle">Customer Experience & Operations Specialist</p>
      
      <div class="footer-links">
        <a href="#about">About</a>
        <a href="#experience">Experience</a>
        <a href="#education">Education</a>
        <a href="#skills">Skills</a>
        <a href="#contact">Contact</a>
      </div>
      
      <div class="footer-copyright">
        <p>
          &copy; 2025 Tonny Onwonga. All rights reserved.
        </p>
      </div>
    </div>
  </footer>

  <script>
    // Simple JavaScript for the header scroll effect and mobile menu
    const header = document.getElementById('header');
    const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
    const mobileMenu = document.getElementById('mobileMenu');
    
    // Header scroll effect
    window.addEventListener('scroll', () => {
      if (window.scrollY > 20) {
        header.classList.add('scrolled');
      } else {
        header.classList.remove('scrolled');
      }
    });
    
    // Mobile menu toggle
    mobileMenuBtn.addEventListener('click', () => {
      mobileMenu.classList.toggle('active');
    });
    
    // Close mobile menu when clicking a link
    const mobileLinks = mobileMenu.querySelectorAll('a');
    mobileLinks.forEach(link => {
      link.addEventListener('click', () => {
        mobileMenu.classList.remove('active');
      });
    });
    
    // Form submission
    const contactForm = document.querySelector('.contact-form');
    contactForm.addEventListener('submit', (e) => {
      e.preventDefault();
      alert('Thank you for your message! I will get back to you soon.');
      contactForm.reset();
    });
  </script>
</body>
</html>
