<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Igor Resume - ServiceNow Developer</title>

        h1:contains("servicenowresume") {
            display: none;
        } 
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
       
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f5f5f5;
            color: #333;
        }

        /* Header */
        .header {
            background-color: #2c3e50;
            height: 54px;
            display: flex;
            align-items: center;
            padding: 0 16px;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        .logo {
            color: white;
            font-size: 18px;
            font-weight: bold;
            margin-right: 32px;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 24px;
        }

        .nav-menu li {
            color: #bdc3c7;
            font-size: 14px;
            cursor: pointer;
            padding: 8px 12px;
            border-radius: 4px;
            transition: all 0.3s ease;
        }

        .nav-menu li:hover, .nav-menu li.active {
            background-color: #34495e;
            color: white;
        }

        .header-right {
            margin-left: auto;
            display: flex;
            align-items: center;
            gap: 16px;
        }

        .search-container {
            position: relative;
        }

        .search-box {
            background-color: #34495e;
            border: 1px solid #4a5a6b;
            border-radius: 4px;
            padding: 6px 12px;
            color: white;
            width: 200px;
            font-size: 14px;
        }

        .search-box::placeholder {
            color: #95a5a6;
        }

        .user-info {
            display: flex;
            align-items: center;
            gap: 8px;
            color: #bdc3c7;
        }

        .user-avatar {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            background-color: #3498db;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }



        

        /* Main Container */
        .main-container {
            margin-top: 36px;
            padding: 0;
        }

        /* Breadcrumb */
        .breadcrumb {
            background-color: #ecf0f1;
            border-bottom: 1px solid #ddd;
            padding: 8px 16px;
            font-size: 14px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .breadcrumb-item {
            color: #3498db;
            text-decoration: none;
        }

        .breadcrumb-separator {
            color: #7f8c8d;
        }

        /* Content Area */
        .content-area {
            display: flex;
            background-color: white;
            min-height: calc(100vh - 88px);
        }

        /* Left Panel */
        .left-panel {
            width: 300px;
            background-color: #fafbfc;
            border-right: 1px solid #ddd;
            padding: 20px;
        }

        .profile-section {
            text-align: center;
            margin-bottom: 24px;
        }

        .profile-avatar {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            background: linear-gradient(135deg, #3498db, #2980b9);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 36px;
            font-weight: bold;
            margin: 0 auto 12px;
            overflow: hidden;
        }

        .profile-avatar img {
            width: 100%;
            height: 100%;
            object-fit: cover; /* Maintains aspect ratio while filling container */
             border-radius: inherit; /* Inherits any border-radius from parent */
        }




        

        .profile-name {
            font-size: 20px;
            font-weight: bold;
            color: #2c3e50;
            margin-bottom: 4px;
        }

        .profile-title {
            font-size: 14px;
            color: #7f8c8d;
            margin-bottom: 16px;
        }

        .section {
            margin-bottom: 24px;
        }

        .section-title {
            font-size: 16px;
            font-weight: bold;
            color: #2c3e50;
            margin-bottom: 12px;
            padding-bottom: 8px;
            border-bottom: 2px solid #3498db;
        }

        .info-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            font-size: 14px;
        }

        .info-label {
            color: #7f8c8d;
            font-weight: 500;
        }

        .info-value {
            color: #2c3e50;
        }

        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 6px;
        }

        .skill-tag {
            background-color: #e8f4f8;
            color: #2980b9;
            padding: 4px 8px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: 500;
        }

        /* Main Content */
        .main-content {
            flex: 1;
            padding: 24px;
        }

        .record-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 24px;
        }

        .record-title {
            font-size: 24px;
            font-weight: bold;
            color: #2c3e50;
        }

        .record-actions {
            display: flex;
            gap: 12px;
        }

        .btn {
            padding: 8px 16px;
            border: 1px solid #ddd;
            border-radius: 4px;
            background-color: white;
            color: #333;
            cursor: pointer;
            font-size: 14px;
            transition: all 0.3s ease;
        }

        .btn:hover {
            background-color: #f8f9fa;
        }

        .btn-primary {
            background-color: #3498db;
            color: white;
            border-color: #3498db;
        }

        .btn-primary:hover {
            background-color: #2980b9;
        }

        .tabs {
            display: flex;
            border-bottom: 1px solid #ddd;
            margin-bottom: 24px;
        }

        .tab {
            padding: 12px 24px;
            cursor: pointer;
            border-bottom: 2px solid transparent;
            color: #7f8c8d;
            font-size: 14px;
            transition: all 0.3s ease;
        }

        .tab.active {
            color: #3498db;
            border-bottom-color: #3498db;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        .form-section {
            background-color: white;
            border: 1px solid #ddd;
            border-radius: 4px;
            margin-bottom: 24px;
        }

        .form-section-header {
            background-color: #f8f9fa;
            padding: 12px 16px;
            border-bottom: 1px solid #ddd;
            font-weight: bold;
            color: #2c3e50;
        }

        .form-section-content {
            padding: 16px;
        }

        .form-row {
            display: flex;
            gap: 24px;
            margin-bottom: 16px;
        }

        .form-group {
            flex: 1;
        }

        .form-label {
            display: block;
            margin-bottom: 4px;
            font-weight: 500;
            color: #2c3e50;
            font-size: 14px;
        }

        .form-input {
            width: 100%;
            padding: 8px 12px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 14px;
            background-color: #f9f9f9;
            color: #333;
        }

        .form-textarea {
            width: 100%;
            padding: 8px 12px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 14px;
            background-color: #f9f9f9;
            color: #333;
            min-height: 100px;
            resize: vertical;
        }

        .experience-item {
            border-left: 3px solid #3498db;
            padding-left: 16px;
            margin-bottom: 20px;
        }

        .experience-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 8px;
        }

        .experience-title {
            font-size: 18px;
            font-weight: bold;
            color: #2c3e50;
        }

        .experience-company {
            font-size: 16px;
            color: #3498db;
            margin-bottom: 4px;
        }

        .experience-date {
            font-size: 14px;
            color: #7f8c8d;
            font-weight: 500;
        }

        .experience-description {
            color: #555;
            line-height: 1.5;
        }

        .experience-description ul {
            margin-left: 20px;
            margin-top: 8px;
        }

        .experience-description li {
            margin-bottom: 4px;
        }

        .certification-item {
            display: flex;
            align-items: center;
            padding: 12px;
            background-color: #f8f9fa;
            border-radius: 4px;
            margin-bottom: 8px;
        }

        .certification-icon {
            width: 40px;
            height: 40px;
            background-color: #27ae60;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            margin-right: 12px;
        }

        .certification-info {
            flex: 1;
        }

        .certification-name {
            font-weight: bold;
            color: #2c3e50;
        }

        .certification-issuer {
            font-size: 12px;
            color: #7f8c8d;
        }

        .project-card {
            background-color: white;
            border: 1px solid #ddd;
            border-radius: 4px;
            padding: 16px;
            margin-bottom: 16px;
            transition: all 0.3s ease;
        }

        .project-card:hover {
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }

        .project-title {
            font-size: 16px;
            font-weight: bold;
            color: #2c3e50;
            margin-bottom: 8px;
        }

        .project-description {
            color: #555;
            line-height: 1.5;
            margin-bottom: 12px;
        }

        .project-technologies {
            display: flex;
            flex-wrap: wrap;
            gap: 6px;
        }

        .tech-tag {
            background-color: #e8f4f8;
            color: #2980b9;
            padding: 4px 8px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: 500;
        }

        @media (max-width: 768px) {
            .content-area {
                flex-direction: column;
            }
            
            .left-panel {
                width: 100%;
            }
            
            .nav-menu {
                display: none;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <div class="header">
        <div class="logo">Igor Resume</div>
        <ul class="nav-menu">
            <li class="active" onclick="showTab('overview')">Overview</li>
            <li onclick="showTab('experience')">Experience</li>
            <li onclick="showTab('skills')">Skills</li>
            <li onclick="showTab('education')">Education</li>
            <li onclick="showTab('contact')">Contact</li>
            <li onclick="showTab('personal')">Personal</li>
        </ul>
        <div class="header-right">
            <div class="search-container">
                <input type="text" class="search-box" placeholder="There's no need to search...">
            </div>
            <div class="user-info">
                <div class="user-avatar">CR</div>
                <span>Recruiter</span>
            </div>
        </div>
    </div>

    <!-- Main Container -->
    <div class="main-container">
        <!-- Breadcrumb -->
        <div class="breadcrumb">
            <a href="#" class="breadcrumb-item">Home</a>
            <span class="breadcrumb-separator">></span>
            <a href="#" class="breadcrumb-item">Profiles</a>
            <span class="breadcrumb-separator">></span>
            <span>Igor K - ServiceNow Developer</span>
        </div>

        <!-- Content Area -->
        <div class="content-area">
            <!-- Left Panel -->
            <div class="left-panel">
                <div class="profile-section">
                    <div class="profile-avatar">
                        <img src="image/avatar.JPG" alt="Igor's profile photo">
                    </div>
                                        </div>

                    <div class="profile-name">Igor</div>
                    <div class="profile-title">ServiceNow Developer</div>

                <div class="section">
                    <div class="section-title">Personal Information</div>
                    <div class="info-item">
                        <span class="info-label">Location:</span>
                        <span class="info-value">Florida, USA</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">Email:</span>
                        <span class="info-value">khalfin.igor95@gmail.com</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">Phone:</span>
                        <span class="info-value">+1 (718) 775-8415</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">LinkedIn:</span>
                        <span class="info-value">linkedin.com/in/igor-kh</span>
                    </div>
                </div>

                <div class="section">
                    <div class="section-title">Core Skills</div>
                    <div class="skills-list">
                        <span class="skill-tag">ServiceNow</span>
                        <span class="skill-tag">JavaScript</span>
                        <span class="skill-tag">GlideRecord</span>
                        <span class="skill-tag">Business Rules</span>
                        <span class="skill-tag">UI Policies</span>
                        <span class="skill-tag">Workflows</span>
                        <span class="skill-tag">REST APIs</span>
                        <span class="skill-tag">ITIL</span>
                        <span class="skill-tag">Scripting</span>
                        <span class="skill-tag">Integration</span>
                    </div>
                </div>

                <div class="section">
                    <div class="section-title">Status</div>
                    <div class="info-item">
                        <span class="info-label">Availability:</span>
                        <span class="info-value" style="color: #27ae60;">Available</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">Remote Work:</span>
                        <span class="info-value">Yes</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">Notice Period:</span>
                        <span class="info-value">2 weeks</span>
                    </div>
                </div>
            </div>

            <!-- Main Content -->
            <div class="main-content">
                <div class="record-header">
                    <div class="record-title">ServiceNow Developer Profile</div>
                    <div class="record-actions">
                        <button class="btn">Download Resume</button>
                        <button class="btn btn-primary">Contact Me</button>
                    </div>
                </div>

                <div class="tabs">
                    <div class="tab active" onclick="showTab('overview')">Overview</div>
                    <div class="tab" onclick="showTab('experience')">Experience</div>
                    <div class="tab" onclick="showTab('skills')">Skills</div>
                    <div class="tab" onclick="showTab('education')">Education</div>
                    <div class="tab" onclick="showTab('contact')">Contact</div>
                    <div class="tab" onclick="showTab('projects')">Personal</div>
                </div>

                <!-- Overview Tab -->
                <div id="overview" class="tab-content active">
                    <div class="form-section">
                        <div class="form-section-header">About this Resume</div>
                        <div class="form-section-content">
                            <div class="form-group">
                                <textarea class="form-textarea" readonly>This resume web-site I developed with ServiceNow platform in mind. I've used some design elements from the platform to make it recognizable, however I have simplified the concept since format requires much less functionality. </textarea>
                            </div>
                        </div>
                    </div>
                    <div class="form-section">
                        <div class="form-section-header">Professional Summary</div>
                        <div class="form-section-content">
                            <div class="form-group">
                                <textarea class="form-textarea" readonly>Experienced ServiceNow Developer with 5+ years of expertise in designing, developing, and implementing ServiceNow solutions. Proven track record in ITSM, ITOM, and custom application development. Strong knowledge of ServiceNow platform capabilities, JavaScript, and integration technologies. Committed to delivering high-quality solutions that improve business processes and user experience.</textarea>
                            </div>
                        </div>
                    </div>

                    <div class="form-section">
                        <div class="form-section-header">Key Achievements</div>
                        <div class="form-section-content">
                            <ul>
                                <li>Led implementation of ServiceNow ITSM for 10,000+ user organization</li>
                                <li>Developed custom ServiceNow applications improving workflow efficiency by 40%</li>
                                <li>Achieved ServiceNow CSA and CAD certifications</li>
                                <li>Reduced incident resolution time by 30% through automated workflows</li>
                            </ul>
                        </div>
                    </div>

                    <div class="form-section">
                        <div class="form-section-header">Certifications</div>
                        <div class="form-section-content">
                            <div class="certification-item">
                                <div class="certification-icon">CSA</div>
                                <div class="certification-info">
                                    <div class="certification-name">Certified System Administrator</div>
                                    <div class="certification-issuer">ServiceNow • Valid until 2025</div>
                                </div>
                            </div>
                            <div class="certification-item">
                                <div class="certification-icon">CAD</div>
                                <div class="certification-info">
                                    <div class="certification-name">Certified Application Developer</div>
                                    <div class="certification-issuer">ServiceNow • Valid until 2025</div>
                                </div>
                            </div>
                            
                        </div>
                    </div>
                </div>

                <!-- Experience Tab -->
                <div id="experience" class="tab-content">
                    <div class="form-section">
                        <div class="form-section-header">Work Experience</div>
                        <div class="form-section-content">
                            <div class="experience-item">
                                <div class="experience-header">
                                    <div>
                                        <div class="experience-title"> ServiceNow Developer</div>
                                        <div class="experience-company">SQA Solution</div>
                                    </div>
                                    <div class="experience-date">Feb 2020 - Present</div>
                                </div>
                                <div class="experience-description">
                                    Contract developer for ServiceNow implementations across multiple clients.
                                    <ul>
                                        <li>Built custom workflows and automated business processes</li>
                                        <li>Configured and customized ITSM modules (Incident, Problem, Change)</li>
                                        <li>Performed system upgrades and maintained platform health</li>
                                        <li>Designed and developed custom ServiceNow applications using best practices</li>
                                        <li>Implemented ITSM, ITOM, and HR Service Delivery modules</li>
                                        <li>Created complex business rules, UI policies, and client scripts</li>
                                        <li>Integrated ServiceNow with external systems using REST/SOAP APIs</li>
                                        <li>Mentored junior developers and conducted code reviews</li>
                                    </ul>
                                </div>
                            </div>

                            

                            
                        </div>
                    </div>
                </div>

                <!-- Skills Tab -->
                <div id="skills" class="tab-content">
                    <div class="form-section">
                        <div class="form-section-header">Technical Skills</div>
                        <div class="form-section-content">
                            <div class="form-row">
                                <div class="form-group">
                                    <label class="form-label">ServiceNow Platform</label>
                                    <div class="skills-list">
                                        <span class="skill-tag">Platform Architecture</span>
                                        <span class="skill-tag">Application Development</span>
                                        <span class="skill-tag">System Administration</span>
                                        <span class="skill-tag">Upgrades & Patches</span>
                                    </div>
                                </div>
                                <div class="form-group">
                                    <label class="form-label">Development</label>
                                    <div class="skills-list">
                                        <span class="skill-tag">JavaScript (basic) </span>
                                        <span class="skill-tag">GlideRecord</span>
                                        <span class="skill-tag">GlideAjax</span>
                                        <span class="skill-tag">Business Rules</span>
                                        <span class="skill-tag">Script Includes</span>
                                    </div>
                                </div>
                            </div>
                            <div class="form-row">
                                <div class="form-group">
                                    <label class="form-label">ITSM Modules</label>
                                    <div class="skills-list">
                                        <span class="skill-tag">Incident Management</span>
                                        <span class="skill-tag">Problem Management</span>
                                        <span class="skill-tag">Change Management</span>
                                        <span class="skill-tag">Service Catalog</span>
                                        <span class="skill-tag">Knowledge Management</span>
                                    </div>
                                </div>
                                <div class="form-group">
                                    <label class="form-label">Integration</label>
                                    <div class="skills-list">
                                        <span class="skill-tag">REST APIs</span>
                                        <span class="skill-tag">SOAP Web Services</span>
                                        <span class="skill-tag">Import Sets</span>
                                        <span class="skill-tag">Transform Maps</span>
                                        <span class="skill-tag">MID Server</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="form-section">
                        <div class="form-section-header">Soft Skills</div>
                        <div class="form-section-content">
                            <div class="skills-list">
                                <span class="skill-tag">Problem Solving</span>
                                <span class="skill-tag">Team Leadership</span>
                                <span class="skill-tag">Client Communication</span>
                                <span class="skill-tag">Requirements Analysis</span>
                                <span class="skill-tag">Project Management</span>
                                <span class="skill-tag">B2C, B2B Sales</span>
                                <span class="skill-tag">Documentation</span>
                                <span class="skill-tag">Training & Mentoring</span>
                            </div>
                        </div>
                    </div>
                </div>

            

                <!-- Education Tab -->
                <div id="education" class="tab-content">
                    <div class="form-section">
                        <div class="form-section-header">Education</div>
                        <div class="form-section-content">
                            <div class="experience-item">
                                <div class="experience-header">
                                    <div>
                                        <div class="experience-title">Bachelor's degree, Automation Engineer Technology/Technician</div>
                                        <div class="experience-company">ITMO University</div>
                                    </div>
                                    <div class="experience-date">2012 - 2016</div>
                                </div>
                                <div class="experience-description">
                                    Graduated. Relevant coursework: Software Engineering, Database Systems, Web Development, Systems Analysis and Design.
                                </div>
                            </div>
                        </div>
                    </div>


                    <div class="form-section">
                        <div class="form-section-header">Professional Development</div>
                        <div class="form-section-content">
                            <ul>
                                <li>ServiceNow Developer  Program </li>
                                <li>ServiceNow AI Essentials </li>
                                <li>ServiceNow System Administrator </li>
                                <li>ServiceNow App Engine Studio</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <!-- Contact Tab -->
                <div id="contact" class="tab-content">
                    <div class="form-section">
                        <div class="form-section-header">Contact Information</div>
                        <div class="form-section-content">
                            <div class="form-row">
                                <div class="form-group">
                                    <label class="form-label">Full Name</label>
                                    <input type="text" class="form-input" value="Igor Khalfin" readonly>
                                </div>
                                <div class="form-group">
                                    <label class="form-label">Job Title</label>
                                    <input type="text" class="form-input" value="ServiceNow Developer" readonly>
                                </div>
                            </div>
                            <div class="form-row">
                                <div class="form-group">
                                    <label class="form-label">Email Address</label>
                                    <input type="email" class="form-input" value="khalfin.igor95@gmail.com" readonly>
                                </div>
                                <div class="form-group">
                                    <label class="form-label">Phone Number</label>
                                    <input type="tel" class="form-input" value="+1 (718) 775-8415" readonly>
                                </div>
                            </div>
                            <div class="form-row">
                                <div class="form-group">
                                    <label class="form-label">LinkedIn Profile</label>
                                    <input type="url" class="form-input" value="https://www.linkedin.com/in/igor-kh/" readonly>
                                </div>
                                <div class="form-group">
                                    <label class="form-label">GitHub Profile</label>
                                    <input type="url" class="form-input" value="https://github.com/badhalfy" readonly>
                                </div>
                            </div>
                            <div class="form-row">
                                <div class="form-group">
                                    <label class="form-label">Location</label>
                                    <input type="text" class="form-input" value="Pembroke Pines, FL" readonly>
                                </div>
                                <div class="form-group">
                                    <label class="form-label">Time Zone</label>
                                    <input type="text" class="form-input" value="UTC-5 (EST)" readonly>
                                </div>
                            </div>
                        </div>
                    </div>


  <!-- Personal Tab -->
                <div id="projects" class="tab-content">
                    <div class="form-section">
                        <div class="form-section-header">Personal Projects & Hobbies</div>
                        <div class="form-section-content">
                            <div class="project-card">
                                <div class="project-title">Car Rental Agency</div>
                                <div class="project-description">
                                    Passively running small car rental agency
                                </div>
                                <div class="project-technologies">
                                    <span class="tech-tag">Business Managemement</span>
                                    <span class="tech-tag">Financial Managemement</span>
                                    <span class="tech-tag">Stress Management</span>
                                    <span class="tech-tag">Marketing</span>
                                </div>
                            </div>

                            <div class="project-card">
                                <div class="project-title">Custom HR Service Portal</div>
                                <div class="project-description">
                                    Developed a comprehensive HR service portal with automated onboarding, offboarding, and employee lifecycle management. Reduced HR processing time by 60% and improved employee satisfaction scores.
                                </div>
                                <div class="project-technologies">
                                    <span class="tech-tag">Service Portal</span>
                                    <span class="tech-tag">HR Service Delivery</span>
                                    <span class="tech-tag">AngularJS</span>
                                    <span class="tech-tag">Workflow Automation</span>
                                </div>
                            </div>

                            <div class="project-card">
                                <div class="project-title">Multi-System Integration Platform</div>
                                <div class="project-description">
                                    Created a centralized integration platform connecting ServiceNow with 8 different enterprise systems including ERP, CRM, and monitoring tools. Implemented real-time data synchronization and automated incident creation.
                                </div>
                                <div class="project-technologies">
                                    <span class="tech-tag">REST/SOAP APIs</span>
                                    <span class="tech-tag">Integration Hub</span>
                                    <span class="tech-tag">MID Server</span>
                                    <span class="tech-tag">Data Synchronization</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                    

                    <div class="form-section">
                        <div class="form-section-header">Send a Message</div>
                        <div class="form-section-content">
                            <div class="form-row">
                                <div class="form-group">
                                    <label class="form-label">Your Name</label>
                                    <input type="text" class="form-input" placeholder="Enter your name">
                                </div>
                                <div class="form-group">
                                    <label class="form-label">Your Email</label>
                                    <input type="email" class="form-input" placeholder="Enter your email">
                                </div>
                            </div>
                            <div class="form-row">
                                <div class="form-group">
                                    <label class="form-label">Subject</label>
                                    <input type="text" class="form-input" placeholder="Enter subject">
                                </div>
                            </div>
                            <div class="form-row">
                                <div class="form-group">
                                    <label class="form-label">Message</label>
                                    <textarea class="form-textarea" placeholder="Enter your message here..."></textarea>
                                </div>
                            </div>
                            <div class="form-row">
                                <div class="form-group">
                                    <button class="btn btn-primary">Send Message</button>
                                    <button class="btn" style="margin-left: 12px;">Clear Form</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        function showTab(tabName) {
            // Hide all tab contents
            const tabContents = document.querySelectorAll('.tab-content');
            tabContents.forEach(content => {
                content.classList.remove('active');
            });

            // Remove active class from all tabs
            const tabs = document.querySelectorAll('.tab');
            tabs.forEach(tab => {
                tab.classList.remove('active');
            });

            // Show selected tab content
            document.getElementById(tabName).classList.add('active');

            // Add active class to clicked tab
            event.target.classList.add('active');

            // Update navigation menu
            const navItems = document.querySelectorAll('.nav-menu li');
            navItems.forEach(item => {
                item.classList.remove('active');
            });
            
            // Find and activate corresponding nav item
            const navItem = Array.from(navItems).find(item => 
                item.textContent.toLowerCase() === tabName.toLowerCase()
            );
            if (navItem) {
                navItem.classList.add('active');
            }
        }

        // Search functionality
        document.querySelector('.search-box').addEventListener('input', function(e) {
            const searchTerm = e.target.value.toLowerCase();
            const skillTags = document.querySelectorAll('.skill-tag, .tech-tag');
            
            skillTags.forEach(tag => {
                const text = tag.textContent.toLowerCase();
                if (text.includes(searchTerm)) {
                    tag.style.backgroundColor = '#fff3cd';
                    tag.style.color = '#856404';
                } else {
                    tag.style.backgroundColor = '';
                    tag.style.color = '';
                }
            });
        });

        // Contact form functionality
        document.querySelector('.btn-primary').addEventListener('click', function() {
            alert('Thank you for your message! I will get back to you soon.');
        });

        // Clear form functionality
        document.querySelector('.btn:not(.btn-primary)').addEventListener('click', function() {
            if (this.textContent === 'Clear Form') {
                const form = this.closest('.form-section-content');
                const inputs = form.querySelectorAll('input, textarea');
                inputs.forEach(input => {
                    if (!input.readOnly) {
                        input.value = '';
                    }
                });
            }
        });

        // Download resume functionality
        document.querySelector('.record-actions .btn').addEventListener('click', function() {
            alert('Resume download would start here. Connect this to your actual resume file.');
        });

        // Contact me button functionality
        document.querySelector('.btn-primary').addEventListener('click', function() {
            if (this.textContent === 'Contact Me') {
                showTab('contact');
            }
        });

        // Add smooth scrolling effect
        document.querySelectorAll('.nav-menu li, .tab').forEach(item => {
            item.addEventListener('click', function() {
                document.querySelector('.main-content').scrollTop = 0;
            });
        });

        // Initialize page
        document.addEventListener('DOMContentLoaded', function() {
            // Set default active states
            showTab('overview');
        });
    </script>
</body>
</html>
