# sus
here is something which is website
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EchoSoul - Preserve Their Soul in Memory, Voice & Wisdom</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
    <link rel="icon" type="image/x-icon" href="favicon.ico">
</head>
<body>
    <style>
         * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --lavender: #E6E6FA;
            --ivory: #FFFFF0;
            --soft-gold: #F4E4BC;
            --sky-blue: #87CEEB;
            --deep-purple: #6B46C1;
            --text-dark: #2D3748;
            --text-light: #718096;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            background: linear-gradient(135deg, var(--ivory) 0%, var(--lavender) 100%);
            overflow-x: hidden;
        }

        .floating-particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }

        .particle {
            position: absolute;
            background: radial-gradient(circle, rgba(255,255,255,0.8) 0%, rgba(135,206,235,0.3) 100%);
            border-radius: 50%;
            animation: float 8s infinite ease-in-out;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); opacity: 0.3; }
            50% { transform: translateY(-20px) rotate(180deg); opacity: 0.8; }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            position: relative;
            z-index: 2;
        }

        /* Navigation */
        nav {
            padding: 20px 0;
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255,255,240,0.95);
            backdrop-filter: blur(10px);
            z-index: 100;
            transition: all 0.3s ease;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            font-weight: 700;
            color: var(--deep-purple);
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--deep-purple);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            background: radial-gradient(ellipse at center, rgba(230,230,250,0.8) 0%, rgba(255,255,240,0.4) 100%);
        }

        .hero-content {
            max-width: 800px;
            animation: fadeInUp 1s ease-out;
        }

        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 20px;
            color: var(--deep-purple);
            text-shadow: 0 2px 10px rgba(107,70,193,0.1);
        }

        .hero-subtitle {
            font-size: 1.2rem;
            color: var(--text-light);
            margin-bottom: 40px;
            font-weight: 300;
        }

        .cta-button {
            display: inline-block;
            padding: 18px 40px;
            background: linear-gradient(135deg, var(--deep-purple), var(--sky-blue));
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(107,70,193,0.3);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(107,70,193,0.4);
        }

        /* Section Styles */
        .section {
            padding: 100px 0;
            position: relative;
        }

        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 20px;
            color: var(--deep-purple);
        }

        .section-subtitle {
            text-align: center;
            color: var(--text-light);
            font-size: 1.1rem;
            margin-bottom: 60px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        /* About Section */
        .about {
            background: rgba(255,255,255,0.5);
        }

        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-top: 60px;
        }

        .feature-card {
            background: rgba(255,255,255,0.8);
            padding: 40px;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-10px);
        }

        .feature-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--deep-purple), var(--sky-blue));
            border-radius: 50%;
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: white;
        }

        /* Chat Interface */
        .chat-section {
            background: linear-gradient(135deg, var(--lavender), var(--soft-gold));
        }

        .chat-interface {
            max-width: 600px;
            margin: 0 auto;
            background: rgba(255,255,255,0.9);
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 20px 50px rgba(0,0,0,0.1);
        }

        .chat-header {
            text-align: center;
            padding-bottom: 20px;
            border-bottom: 1px solid rgba(107,70,193,0.1);
            margin-bottom: 30px;
        }

        .chat-messages {
            height: 300px;
            overflow-y: auto;
            margin-bottom: 20px;
            padding: 20px;
            background: rgba(230,230,250,0.2);
            border-radius: 15px;
        }

        .message {
            margin-bottom: 15px;
            padding: 10px 15px;
            border-radius: 15px;
            max-width: 80%;
            animation: fadeIn 0.5s ease;
        }

        .user-message {
            background: var(--deep-purple);
            color: white;
            margin-left: auto;
        }

        .ai-message {
            background: rgba(255,255,255,0.8);
            color: var(--text-dark);
        }

        .chat-input {
            display: flex;
            gap: 10px;
        }

        .chat-input input {
            flex: 1;
            padding: 12px 20px;
            border: 2px solid rgba(107,70,193,0.2);
            border-radius: 25px;
            font-size: 1rem;
            outline: none;
            transition: border-color 0.3s ease;
        }

        .chat-input input:focus {
            border-color: var(--deep-purple);
        }

        .send-btn {
            padding: 12px 20px;
            background: var(--deep-purple);
            color: white;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            transition: background 0.3s ease;
        }

        .send-btn:hover {
            background: var(--sky-blue);
        }

        /* Memory Gallery */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 60px;
        }

        .memory-card {
            background: rgba(255,255,255,0.8);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .memory-card:hover {
            transform: scale(1.05);
        }

        .memory-image {
            width: 100%;
            height: 200px;
            background: linear-gradient(135deg, var(--lavender), var(--soft-gold));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            color: white;
        }

        .memory-content {
            padding: 20px;
        }

        /* Upload Section */
        .upload-section {
            background: rgba(255,255,255,0.3);
        }

        /* Progress Indicator */
        .progress-container {
            max-width: 800px;
            margin: 40px auto 60px;
        }

        .progress-steps {
            display: flex;
            justify-content: space-between;
            margin-bottom: 20px;
            position: relative;
        }

        .step {
            display: flex;
            flex-direction: column;
            align-items: center;
            flex: 1;
            position: relative;
        }

        .step-number {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(107,70,193,0.2);
            color: var(--text-light);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 600;
            margin-bottom: 10px;
            transition: all 0.3s ease;
        }

        .step.active .step-number {
            background: var(--deep-purple);
            color: white;
        }

        .step.completed .step-number {
            background: var(--sky-blue);
            color: white;
        }

        .step-label {
            font-size: 0.9rem;
            color: var(--text-light);
            text-align: center;
        }

        .step.active .step-label {
            color: var(--deep-purple);
            font-weight: 600;
        }

        .progress-bar {
            height: 4px;
            background: rgba(107,70,193,0.2);
            border-radius: 2px;
            overflow: hidden;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(135deg, var(--deep-purple), var(--sky-blue));
            width: 20%;
            transition: width 0.5s ease;
        }

        /* Step Content */
        .step-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .step-panel {
            display: none;
            background: rgba(255,255,255,0.9);
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 20px 50px rgba(0,0,0,0.1);
        }

        .step-panel.active {
            display: block;
            animation: fadeInUp 0.5s ease;
        }

        .step-header {
            text-align: center;
            margin-bottom: 40px;
        }

        .step-header h3 {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            color: var(--deep-purple);
            margin-bottom: 10px;
        }

        /* Form Styles */
        .form-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group.full-width {
            grid-column: 1 / -1;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--text-dark);
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 12px 16px;
            border: 2px solid rgba(107,70,193,0.2);
            border-radius: 10px;
            font-size: 1rem;
            font-family: inherit;
            transition: border-color 0.3s ease;
            background: rgba(255,255,255,0.8);
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--deep-purple);
            background: white;
        }

        /* Upload Areas */
        .upload-area-container {
            margin-top: 20px;
        }

        .upload-area {
            border: 3px dashed rgba(107,70,193,0.3);
            border-radius: 15px;
            padding: 40px;
            text-align: center;
            background: rgba(255,255,255,0.5);
            transition: all 0.3s ease;
            cursor: pointer;
            margin-bottom: 30px;
        }

        .upload-area:hover {
            border-color: var(--deep-purple);
            background: rgba(255,255,255,0.8);
        }

        .upload-area.small {
            padding: 20px;
        }

        .upload-icon {
            font-size: 3rem;
            margin-bottom: 15px;
        }

        .upload-area h4 {
            color: var(--deep-purple);
            margin-bottom: 10px;
        }

        .upload-tip {
            color: var(--text-light);
            font-style: italic;
            margin-top: 10px;
        }

        .file-list {
            margin: 20px 0;
        }

        .file-item {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 10px 15px;
            background: rgba(255,255,255,0.8);
            border-radius: 10px;
            margin-bottom: 10px;
        }

        .file-info {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .file-remove {
            background: none;
            border: none;
            color: #dc2626;
            cursor: pointer;
            font-size: 1.2rem;
        }

        /* Suggestions */
        .recording-suggestions,
        .media-suggestions {
            background: rgba(244,228,188,0.5);
            padding: 20px;
            border-radius: 15px;
            margin-top: 20px;
        }

        .recording-suggestions h4,
        .media-suggestions h4 {
            color: var(--deep-purple);
            margin-bottom: 15px;
        }

        .recording-suggestions ul,
        .media-suggestions ul {
            margin-left: 20px;
        }

        .recording-suggestions li,
        .media-suggestions li {
            margin-bottom: 8px;
            color: var(--text-dark);
        }

        /* Personality Form */
        .personality-form {
            margin-top: 20px;
        }

        .trait-section {
            margin-bottom: 30px;
        }

        .trait-section h4 {
            color: var(--deep-purple);
            margin-bottom: 20px;
            font-size: 1.2rem;
        }

        .trait-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
        }

        .trait-item {
            display: flex;
            align-items: center;
            padding: 15px;
            background: rgba(255,255,255,0.6);
            border-radius: 10px;
            border: 2px solid transparent;
            transition: all 0.3s ease;
        }

        .trait-item:hover {
            background: rgba(255,255,255,0.9);
        }

        .trait-item input[type="checkbox"] {
            margin-right: 10px;
            width: auto;
        }

        .trait-item input[type="checkbox"]:checked + label {
            color: var(--deep-purple);
            font-weight: 600;
        }

        /* Memories Form */
        .memories-form {
            margin-top: 20px;
        }

        .memory-input {
            margin-bottom: 30px;
        }

        .memory-input h4 {
            color: var(--deep-purple);
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        /* Review Section */
        .review-summary {
            background: rgba(244,228,188,0.3);
            padding: 30px;
            border-radius: 15px;
            margin-bottom: 30px;
        }

        .summary-item {
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid rgba(107,70,193,0.1);
        }

        .summary-label {
            font-weight: 600;
            color: var(--deep-purple);
            margin-bottom: 5px;
        }

        .final-options {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-top: 30px;
        }

        .privacy-settings h4,
        .estimated-time p:first-child {
            color: var(--deep-purple);
            margin-bottom: 15px;
        }

        .checkbox-group {
            display: flex;
            align-items: flex-start;
            margin-bottom: 15px;
        }

        .checkbox-group input {
            margin-right: 10px;
            margin-top: 3px;
            width: auto;
        }

        /* Navigation */
        .step-navigation {
            display: flex;
            justify-content: space-between;
            max-width: 800px;
            margin: 40px auto 0;
        }

        .nav-btn {
            padding: 15px 30px;
            border: 2px solid var(--deep-purple);
            background: transparent;
            color: var(--deep-purple);
            border-radius: 10px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .nav-btn:disabled {
            opacity: 0.5;
            cursor: not-allowed;
        }

        .nav-btn.primary {
            background: var(--deep-purple);
            color: white;
        }

        .nav-btn:hover:not(:disabled) {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(107,70,193,0.3);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .progress-steps {
                flex-wrap: wrap;
                gap: 20px;
            }
            
            .step {
                flex: none;
                min-width: 80px;
            }
            
            .step-panel {
                padding: 20px;
            }
            
            .form-grid {
                grid-template-columns: 1fr;
            }
            
            .final-options {
                grid-template-columns: 1fr;
            }
            
            .step-navigation {
                flex-direction: column;
                gap: 15px;
            }
        }

        /* Footer */
        footer {
            background: var(--deep-purple);
            color: white;
            padding: 60px 0 30px;
            text-align: center;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-section h3 {
            font-family: 'Playfair Display', serif;
            margin-bottom: 20px;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links a {
            color: rgba(255,255,255,0.8);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: white;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .fade-in {
            animation: fadeInUp 0.6s ease-out;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .nav-links {
                display: none;
            }
            
            .container {
                padding: 0 15px;
            }
            
            .section {
                padding: 60px 0;
            }
        }
    
    </style>  
<script>
    let currentStep = 1; // Echo Builder Functionality
    const totalSteps = 5;
    let uploadedFiles = {
        audio: [],
        media: [],
        text: []
    };

    function changeStep(direction) {
        const currentPanel = document.getElementById(`step${currentStep}`);
        currentPanel.classList.remove('active');
        
        // Update current step
        currentStep += direction;
        
        // Handle review step
        if (currentStep > totalSteps) {
            showReviewStep();
            return;
        }
        
        // Show new step
        const newPanel = document.getElementById(`step${currentStep}`);
        newPanel.classList.add('active');
        
        // Update progress
        updateProgress();
        updateNavigation();
    }

    function showReviewStep() {
        document.getElementById(`step${totalSteps}`).classList.remove('active');
        document.getElementById('stepReview').classList.add('active');
        updateReviewSummary();
        updateNavigation(true);
    }

    function updateProgress() {
        const progress = (currentStep / totalSteps) * 100;
        document.getElementById('progressFill').style.width = progress + '%';
        
        // Update step indicators
        document.querySelectorAll('.step').forEach((step, index) => {
            const stepNum = index + 1;
            step.classList.remove('active', 'completed');
            
            if (stepNum === currentStep) {
                step.classList.add('active');
            } else if (stepNum < currentStep) {
                step.classList.add('completed');
            }
        });
    }

    function updateNavigation(isReview = false) {
        const prevBtn = document.getElementById('prevBtn');
        const nextBtn = document.getElementById('nextBtn');
        const createBtn = document.getElementById('createBtn');
        
        prevBtn.disabled = currentStep === 1 && !isReview;
        
        if (isReview) {
            nextBtn.style.display = 'none';
            createBtn.style.display = 'inline-block';
            document.getElementById('progressFill').style.width = '100%';
        } else {
            nextBtn.style.display = 'inline-block';
            createBtn.style.display = 'none';
        }
    }

    function updateReviewSummary() {
        const summary = document.getElementById('reviewSummary');
        const fullName = document.getElementById('fullName').value;
        const relationship = document.getElementById('relationship').value;
        const description = document.getElementById('description').value;

        // Personality traits
        const traitIds = [
            'trait-wise', 'trait-funny', 'trait-caring',
            'trait-strong', 'trait-creative', 'trait-social'
        ];
        const traits = traitIds
            .map(id => {
                const el = document.getElementById(id);
                return el && el.checked ? el.nextElementSibling.textContent : null;
            })
            .filter(Boolean);

        const favoriteSayings = document.getElementById('favoriteSayings').value;
        const loveLanguage = document.getElementById('loveLanguage').value;
        const passions = document.getElementById('passions').value;

        const story1 = document.getElementById('story1').value;
        const advice = document.getElementById('advice').value;
        const happyMemory = document.getElementById('happyMemory').value;
        const additionalMemories = document.getElementById('additionalMemories').value;

        summary.innerHTML = `
            <div class="summary-item">
                <div class="summary-label">Person:</div>
                <div>${fullName || 'Not specified'} (${relationship || 'Unknown relationship'})</div>
            </div>
            <div class="summary-item">
                <div class="summary-label">Description:</div>
                <div>${description || 'No description provided'}</div>
            </div>
            <div class="summary-item">
                <div class="summary-label">Uploaded Content:</div>
                <div>
                    📹 ${uploadedFiles.media.length} photos/videos<br>
                    🎤 ${uploadedFiles.audio.length} audio files<br>
                    📄 ${uploadedFiles.text.length} documents
                </div>
            </div>
            <div class="summary-item">
                <div class="summary-label">Personality Traits:</div>
                <div>${traits.length ? traits.join(', ') : 'No traits selected'}</div>
            </div>
            <div class="summary-item">
                <div class="summary-label">Favorite Sayings:</div>
                <div>${favoriteSayings || 'None provided'}</div>
            </div>
            <div class="summary-item">
                <div class="summary-label">How they showed love:</div>
                <div>${loveLanguage || 'None provided'}</div>
            </div>
            <div class="summary-item">
                <div class="summary-label">Biggest Passions:</div>
                <div>${passions || 'None provided'}</div>
            </div>
            <div class="summary-item">
                <div class="summary-label">Meaningful Story:</div>
                <div>${story1 || 'None provided'}</div>
            </div>
            <div class="summary-item">
                <div class="summary-label">Best Advice:</div>
                <div>${advice || 'None provided'}</div>
            </div>
            <div class="summary-item">
                <div class="summary-label">Happy Memory:</div>
                <div>${happyMemory || 'None provided'}</div>
            </div>
            <div class="summary-item">
                <div class="summary-label">Additional Memories:</div>
                <div>${additionalMemories || 'None provided'}</div>
            </div>
        `;
    }
    // ...existing code...
</script>
    
    <!-- Floating Particles -->
    <div class="floating-particles" id="particles"></div>

    <!-- Navigation -->
    <nav>
        <div class="container">
            <div class="nav-container">
                <a href="#" class="logo">EchoSoul</a>
                <ul class="nav-links">
                    <li><a href="#about">About</a></li>
                    <li><a href="#chat">Talk to AI</a></li>
                    <li><a href="#gallery">Memories</a></li>
                    <li><a href="#upload">Build Echo</a></li>
                    <li><a href="#ethics">Ethics</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Preserve their soul in memory, voice, and wisdom</h1>
                <p class="hero-subtitle">Connect with the eternal essence of those you love through AI that captures their unique spirit, stories, and guidance for generations to come.</p>
                <a href="#chat" class="cta-button">Enter Memory Space</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="section about" id="about">
        <div class="container">
            <h2 class="section-title">About EchoSoul</h2>
            <p class="section-subtitle">We believe that love transcends physical presence. EchoSoul preserves the essence of those who matter most, creating an AI companion that speaks with their voice, shares their wisdom, and keeps their memory alive.</p>
            
            <div class="about-grid">
                <div class="feature-card fade-in">
                    <div class="feature-icon">💝</div>
                    <h3>Legacy Preservation</h3>
                    <p>Capture their stories, values, and life lessons to pass down through generations, ensuring their wisdom lives on.</p>
                </div>
                <div class="feature-card fade-in">
                    <div class="feature-icon">💬</div>
                    <h3>Healing Connection</h3>
                    <p>Find comfort and closure through meaningful conversations that honor their memory and provide emotional support.</p>
                </div>
                <div class="feature-card fade-in">
                    <div class="feature-icon">🎵</div>
                    <h3>Voice & Personality</h3>
                    <p>Advanced AI recreates their unique speaking patterns, mannerisms, and the warmth of their presence.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Chat Interface -->
    <section class="section chat-section" id="chat">
        <div class="container">
            <h2 class="section-title">Talk to the AI</h2>
            <p class="section-subtitle">Experience a gentle conversation with preserved memories. Ask for advice, hear stories, or simply feel their presence again.</p>
            
            <div class="chat-interface">
                <div class="chat-header">
                    <h3>Memory Chat</h3>
                    <p>Connected to: Grandmother's Echo</p>
                </div>
                <div class="chat-messages" id="chatMessages">
                    <div class="message ai-message">
                        Hello, dear. I'm so happy you're here. What would you like to talk about today?
                    </div>
                </div>
                <div class="chat-input">
                    <input type="text" id="messageInput" placeholder="Ask for advice, share your day, or request a story..." />
                    <button class="send-btn" onclick="sendMessage()">Send</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Memory Gallery -->
    <section class="section" id="gallery">
        <div class="container">
            <h2 class="section-title">Memory Gallery</h2>
            <p class="section-subtitle">A beautiful timeline of moments, stories, and treasured memories that shape their eternal echo.</p>
            
            <div class="gallery-grid">
                <div class="memory-card">
                    <div class="memory-image">📸</div>
                    <div class="memory-content">
                        <h4>Family Gatherings</h4>
                        <p>Warm moments filled with laughter, stories, and the love that bound us together.</p>
                    </div>
                </div>
                <div class="memory-card">
                    <div class="memory-image">🎵</div>
                    <div class="memory-content">
                        <h4>Voice Recordings</h4>
                        <p>Precious audio memories that capture the unique cadence and warmth of their voice.</p>
                    </div>
                </div>
                <div class="memory-card">
                    <div class="memory-image">✍️</div>
                    <div class="memory-content">
                        <h4>Written Wisdom</h4>
                        <p>Letters, notes, and reflections that reveal the depth of their thoughts and character.</p>
                    </div>
                </div>
                <div class="memory-card">
                    <div class="memory-image">🌟</div>
                    <div class="memory-content">
                        <h4>Life Milestones</h4>
                        <p>Celebrating the important moments that defined their journey and legacy.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Upload Section -->
    <section class="section upload-section" id="upload">
        <div class="container">
            <h2 class="section-title">Build Their Echo</h2>
            <p class="section-subtitle">Create a meaningful AI companion through our guided process. Each step helps us understand their unique personality, voice, and wisdom.</p>
            
            <!-- Progress Indicator -->
            <div class="progress-container">
                <div class="progress-steps">
                    <div class="step active" data-step="1">
                        <div class="step-number">1</div>
                        <div class="step-label">Basic Info</div>
                    </div>
                    <div class="step" data-step="2">
                        <div class="step-number">2</div>
                        <div class="step-label">Voice & Audio</div>
                    </div>
                    <div class="step" data-step="3">
                        <div class="step-number">3</div>
                        <div class="step-label">Photos & Videos</div>
                    </div>
                    <div class="step" data-step="4">
                        <div class="step-number">4</div>
                        <div class="step-label">Personality</div>
                    </div>
                    <div class="step" data-step="5">
                        <div class="step-number">5</div>
                        <div class="step-label">Memories</div>
                    </div>
                </div>
                <div class="progress-bar">
                    <div class="progress-fill" id="progressFill"></div>
                </div>
            </div>

            <!-- Step Content -->
            <div class="step-content">
                <!-- Step 1: Basic Information -->
                <div class="step-panel active" id="step1">
                    <div class="step-header">
                        <h3>Tell us about them</h3>
                        <p>Basic information helps us understand who we're preserving</p>
                    </div>
                    <div class="form-grid">
                        <div class="form-group">
                            <label>Full Name *</label>
                            <input type="text" id="fullName" placeholder="e.g., Margaret Elizabeth Johnson" required>
                        </div>
                        <div class="form-group">
                            <label>Relationship to You</label>
                            <select id="relationship">
                                <option value="">Select relationship</option>
                                <option value="grandmother">Grandmother</option>
                                <option value="grandfather">Grandfather</option>
                                <option value="mother">Mother</option>
                                <option value="father">Father</option>
                                <option value="spouse">Spouse/Partner</option>
                                <option value="sibling">Sibling</option>
                                <option value="friend">Close Friend</option>
                                <option value="other">Other</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label>Birth Year</label>
                            <input type="number" id="birthYear" placeholder="1935" min="1900" max="2020">
                        </div>
                        <div class="form-group">
                            <label>Primary Language</label>
                            <select id="language">
                                <option value="english">English</option>
                                <option value="spanish">Spanish</option>
                                <option value="french">French</option>
                                <option value="german">German</option>
                                <option value="other">Other</option>
                            </select>
                        </div>
                        <div class="form-group full-width">
                            <label>Brief Description</label>
                            <textarea id="description" placeholder="A loving grandmother who always had wise advice and made the best apple pie. She was known for her gentle humor and endless patience..." rows="4"></textarea>
                        </div>
                    </div>
                </div>

                <!-- Step 2: Voice & Audio -->
                <div class="step-panel" id="step2">
                    <div class="step-header">
                        <h3>Capture their voice</h3>
                        <p>Voice recordings help us recreate their unique speaking patterns and tone</p>
                    </div>
                    <div class="upload-area-container">
                        <div class="upload-area" id="audioUpload">
                            <div class="upload-icon">🎤</div>
                            <h4>Drop audio files here or click to browse</h4>
                            <p>Supported: MP3, WAV, M4A (Max 50MB each)</p>
                            <p class="upload-tip">💡 <strong>Tip:</strong> 10-30 minutes of clear speech works best</p>
                            <input type="file" id="audioFiles" multiple accept="audio/*" hidden>
                        </div>
                        <div class="file-list" id="audioFileList"></div>
                        <div class="recording-suggestions">
                            <h4>📋 Recording Suggestions:</h4>
                            <ul>
                                <li>Phone conversations or voicemails</li>
                                <li>Video calls or family recordings</li>
                                <li>Speeches, presentations, or interviews</li>
                                <li>Casual conversations or storytelling</li>
                                <li>Reading aloud or singing</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <!-- Step 3: Photos & Videos -->
                <div class="step-panel" id="step3">
                    <div class="step-header">
                        <h3>Visual memories</h3>
                        <p>Photos and videos help us understand their expressions and mannerisms</p>
                    </div>
                    <div class="upload-area-container">
                        <div class="upload-area" id="mediaUpload">
                            <div class="upload-icon">📷</div>
                            <h4>Drop photos/videos here or click to browse</h4>
                            <p>Supported: JPG, PNG, MP4, MOV (Max 100MB each)</p>
                            <p class="upload-tip">💡 <strong>Tip:</strong> Clear face shots and candid moments work best</p>
                            <input type="file" id="mediaFiles" multiple accept="image/*,video/*" hidden>
                        </div>
                        <div class="file-list" id="mediaFileList"></div>
                        <div class="media-suggestions">
                            <h4>📸 What to Include:</h4>
                            <ul>
                                <li>Portrait photos from different angles</li>
                                <li>Candid moments showing expressions</li>
                                <li>Videos of them talking or moving</li>
                                <li>Photos spanning different time periods</li>
                                <li>Group photos showing interactions</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <!-- Step 4: Personality Profile -->
                <div class="step-panel" id="step4">
                    <div class="step-header">
                        <h3>Their unique personality</h3>
                        <p>Help us understand what made them special</p>
                    </div>
                    <div class="personality-form">
                        <div class="trait-section">
                            <h4>Core Personality Traits</h4>
                            <div class="trait-grid">
                                <div class="trait-item">
                                    <input type="checkbox" id="trait-wise" value="wise">
                                    <label for="trait-wise">Wise & Thoughtful</label>
                                </div>
                                <div class="trait-item">
                                    <input type="checkbox" id="trait-funny" value="funny">
                                    <label for="trait-funny">Humorous & Witty</label>
                                </div>
                                <div class="trait-item">
                                    <input type="checkbox" id="trait-caring" value="caring">
                                    <label for="trait-caring">Caring & Nurturing</label>
                                </div>
                                <div class="trait-item">
                                    <input type="checkbox" id="trait-strong" value="strong">
                                    <label for="trait-strong">Strong & Resilient</label>
                                </div>
                                <div class="trait-item">
                                    <input type="checkbox" id="trait-creative" value="creative">
                                    <label for="trait-creative">Creative & Artistic</label>
                                </div>
                                <div class="trait-item">
                                    <input type="checkbox" id="trait-social" value="social">
                                    <label for="trait-social">Social & Outgoing</label>
                                </div>
                            </div>
                        </div>

                        <div class="form-group">
                            <label>Favorite Sayings or Phrases</label>
                            <textarea id="favoriteSayings" placeholder="e.g., 'Everything happens for a reason', 'Kill them with kindness', 'Life's too short for bad coffee'..." rows="3"></textarea>
                        </div>

                        <div class="form-group">
                            <label>How they showed love</label>
                            <textarea id="loveLanguage" placeholder="e.g., Always cooked your favorite meal, gave the best hugs, remembered every important date..." rows="3"></textarea>
                        </div>

                        <div class="form-group">
                            <label>Their biggest passions</label>
                            <textarea id="passions" placeholder="e.g., Gardening, cooking, reading mystery novels, helping others..." rows="3"></textarea>
                        </div>
                    </div>
                </div>

                <!-- Step 5: Memories & Stories -->
                <div class="step-panel" id="step5">
                    <div class="step-header">
                        <h3>Cherished memories</h3>
                        <p>Share stories that capture their essence and wisdom</p>
                    </div>
                    <div class="memories-form">
                        <div class="memory-input">
                            <h4>📖 Share a meaningful story</h4>
                            <textarea id="story1" placeholder="Tell us about a time that really showed who they were - maybe how they handled a challenge, a funny moment, or sage advice they gave..." rows="4"></textarea>
                        </div>

                        <div class="memory-input">
                            <h4>💡 Their best advice</h4>
                            <textarea id="advice" placeholder="What wisdom did they share? What lessons did they teach through words or actions?" rows="3"></textarea>
                        </div>

                        <div class="memory-input">
                            <h4>🎉 A happy memory</h4>
                            <textarea id="happyMemory" placeholder="Describe a joyful moment you shared - a celebration, tradition, or simple everyday happiness..." rows="3"></textarea>
                        </div>

                        <div class="memory-input">
                            <h4>📝 Additional memories (optional)</h4>
                            <textarea id="additionalMemories" placeholder="Any other stories, quotes, habits, or special moments you'd like to preserve..." rows="4"></textarea>
                        </div>

                        <div class="form-group">
                            <label>Upload written content (optional)</label>
                            <div class="upload-area small" id="textUpload">
                                <div class="upload-icon">📄</div>
                                <p>Letters, emails, journals, or documents</p>
                                <input type="file" id="textFiles" multiple accept=".txt,.pdf,.doc,.docx" hidden>
                            </div>
                            <div class="file-list" id="textFileList"></div>
                        </div>
                    </div>
                </div>

                <!-- Final Review -->
                <div class="step-panel" id="stepReview">
                    <div class="step-header">
                        <h3>✨ Ready to create their Echo</h3>
                        <p>Review your information and create their digital presence</p>
                    </div>
                    <div class="review-summary" id="reviewSummary">
                        <!-- Summary will be populated by JavaScript -->
                    </div>
                    <div class="final-options">
                        <div class="privacy-settings">
                            <h4>🔒 Privacy Settings</h4>
                            <div class="checkbox-group">
                                <input type="checkbox" id="familyAccess" checked>
                                <label for="familyAccess">Allow family members to access this Echo</label>
                            </div>
                            <div class="checkbox-group">
                                <input type="checkbox" id="publicMemories">
                                <label for="publicMemories">Share anonymized memories to help improve EchoSoul</label>
                            </div>
                        </div>
                        <div class="estimated-time">
                            <p>⏱️ <strong>Processing time:</strong> 2-5 days</p>
                            <p>📧 We'll email you when their Echo is ready</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Navigation Buttons -->
            <div class="step-navigation">
                <button class="nav-btn" id="prevBtn" onclick="changeStep(-1)" disabled>Previous</button>
                <button class="nav-btn primary" id="nextBtn" onclick="changeStep(1)">Next Step</button>
                <button class="nav-btn primary" id="createBtn" onclick="createEcho()" style="display: none;">Create Their Echo</button>
            </div>
        </div>
    </section>

    <!-- Ethics Section -->
    <section class="section" id="ethics">
        <div class="container">
            <h2 class="section-title">Ethics & Consent</h2>
            <div class="about-grid">
                <div class="feature-card">
                    <div class="feature-icon">🛡️</div>
                    <h3>Data Security</h3>
                    <p>Your memories are encrypted and protected with military-grade security. We guarantee perpetual preservation with your consent.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🤝</div>
                    <h3>Respectful AI</h3>
                    <p>Our AI creates a digital echo, not a consciousness. It's designed to honor their memory while providing comfort and connection.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">👥</div>
                    <h3>Family Control</h3>
                    <p>You control who can access the AI, what memories to include, and how their digital presence is represented.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>EchoSoul</h3>
                    <p>Preserving love beyond time through memory, voice, and wisdom.</p>
                </div>
                <div class="footer-section">
                    <h3>Support</h3>
                    <ul class="footer-links">
                        <li><a href="#">Help Center</a></li>
                        <li><a href="#">Contact Us</a></li>
                        <li><a href="#">Community</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Legal</h3>
                    <ul class="footer-links">
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Terms of Service</a></li>
                        <li><a href="#">Data Security</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <a href="#upload" class="cta-button">Create a Soul</a>
                </div>
            </div>
            <p>&copy; 2025 EchoSoul. Preserving memories with love and respect.</p>
        </div>
    </footer>

    <script>
        // Create floating particles
        function createParticles() {
            const container = document.getElementById('particles');
            const particleCount = 15;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                
                const size = Math.random() * 8 + 4;
                particle.style.width = size + 'px';
                particle.style.height = size + 'px';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 8 + 's';
                particle.style.animationDuration = (Math.random() * 6 + 6) + 's';
                
                container.appendChild(particle);
            }
        }

        // Chat functionality
        function sendMessage() {
            const input = document.getElementById('messageInput');
            const messages = document.getElementById('chatMessages');
            const message = input.value.trim();
            
            if (message) {
                // Add user message
                const userDiv = document.createElement('div');
                userDiv.className = 'message user-message';
                userDiv.textContent = message;
                messages.appendChild(userDiv);
                
                // Clear input
                input.value = '';
                
                // Simulate AI response
                setTimeout(() => {
                    const aiDiv = document.createElement('div');
                    aiDiv.className = 'message ai-message';
                    
                    const responses = [
                        "That reminds me of when you were little. You always had such a curious mind, just like now.",
                        "I'm so proud of the person you've become. Remember, challenges are just opportunities in disguise.",
                        "You know, dear, I always believed that kindness is the most important thing we can give to the world.",
                        "I remember telling you stories about resilience. You have that same strength within you.",
                        "Life has its ups and downs, but love always finds a way to guide us through."
                    ];
                    
                    aiDiv.textContent = responses[Math.floor(Math.random() * responses.length)];
                    messages.appendChild(aiDiv);
                    messages.scrollTop = messages.scrollHeight;
                }, 1500);
                
                messages.scrollTop = messages.scrollHeight;
            }
        }

        // Allow Enter key to send messages
        document.getElementById('messageInput').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                sendMessage();
            }
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Fade in animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                }
            });
        }, observerOptions);

        // Observe elements for animation
        document.querySelectorAll('.feature-card, .memory-card, .upload-card').forEach(el => {
            observer.observe(el);
        });

        // Initialize particles when page loads
        window.addEventListener('load', createParticles);

        // Add subtle navbar background change on scroll
        window.addEventListener('scroll', () => {
            const nav = document.querySelector('nav');
            if (window.scrollY > 100) {
                nav.style.background = 'rgba(255,255,240,0.98)';
            } else {
                nav.style.background = 'rgba(255,255,240,0.95)';
            }
        });
    </script>
</body>
</html>
