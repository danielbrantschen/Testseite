/* ===================================
   GLOBAL STYLES
   =================================== */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

:root {
    --primary-color: #667eea;
    --secondary-color: #764ba2;
    --accent-color: #f093fb;
    --dark-color: #2d3748;
    --light-color: #f7fafc;
    --text-color: #333;
    --border-color: #e2e8f0;
    --success-color: #48bb78;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: var(--text-color);
    background-color: #fff;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

/* ===================================
   NAVIGATION BAR
   =================================== */
.navbar {
    background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
    padding: 1rem 0;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.navbar .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.nav-brand h2 {
    color: white;
    font-size: 1.8rem;
}

.nav-menu {
    display: flex;
    list-style: none;
    gap: 2rem;
}

.nav-menu a {
    color: white;
    text-decoration: none;
    transition: all 0.3s ease;
    font-weight: 500;
    position: relative;
}

.nav-menu a::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 0;
    height: 2px;
    background-color: var(--accent-color);
    transition: width 0.3s ease;
}

.nav-menu a:hover::after,
.nav-menu a.active::after {
    width: 100%;
}

/* ===================================
   HERO SECTION
   =================================== */
.hero {
    background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
    color: white;
    padding: 100px 20px;
    text-align: center;
    min-height: 500px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    overflow: hidden;
}

.hero::before {
    content: '';
    position: absolute;
    top: 0;
    right: 0;
    width: 400px;
    height: 400px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 50%;
    animation: float 6s ease-in-out infinite;
}

.hero-content {
    position: relative;
    z-index: 2;
}

.hero h1 {
    font-size: 3.5rem;
    margin-bottom: 1rem;
    animation: slideDown 0.8s ease;
}

.hero p {
    font-size: 1.3rem;
    margin-bottom: 2rem;
    opacity: 0.95;
    animation: slideUp 0.8s ease;
}

@keyframes float {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(20px); }
}

@keyframes slideDown {
    from {
        opacity: 0;
        transform: translateY(-30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes slideUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* ===================================
   BUTTONS
   =================================== */
.btn {
    display: inline-block;
    padding: 12px 30px;
    border: none;
    border-radius: 5px;
    text-decoration: none;
    cursor: pointer;
    font-size: 1rem;
    font-weight: 600;
    transition: all 0.3s ease;
}

.btn-primary {
    background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
    color: white;
}

.btn-primary:hover {
    transform: translateY(-2px);
    box-shadow: 0 10px 20px rgba(102, 126, 234, 0.4);
}

/* ===================================
   PAGE HEADER
   =================================== */
.page-header {
    background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
    color: white;
    padding: 60px 20px;
    text-align: center;
}

.page-header h1 {
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
}

.page-header p {
    font-size: 1.1rem;
    opacity: 0.95;
}

/* ===================================
   FEATURES SECTION
   =================================== */
.features {
    padding: 60px 20px;
    background-color: var(--light-color);
}

.features h2 {
    text-align: center;
    font-size: 2rem;
    margin-bottom: 3rem;
    color: var(--dark-color);
}

.features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
}

.feature-card {
    background: white;
    padding: 2rem;
    border-radius: 10px;
    text-align: center;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
}

.feature-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 30px rgba(102, 126, 234, 0.2);
}

.feature-icon {
    font-size: 3rem;
    margin-bottom: 1rem;
}

.feature-card h3 {
    font-size: 1.3rem;
    margin-bottom: 0.5rem;
    color: var(--primary-color);
}

.feature-card p {
    color: #666;
}

/* ===================================
   ABOUT SECTION
   =================================== */
.about-section {
    padding: 60px 20px;
}

.about-content {
    max-width: 800px;
    margin: 0 auto 3rem;
}

.about-content h2,
.team-section h2,
.values-section h2 {
    font-size: 2rem;
    margin-bottom: 2rem;
    color: var(--dark-color);
}

.about-content p {
    font-size: 1.1rem;
    line-height: 1.8;
    color: #666;
}

/* Team Section */
.team-section {
    margin: 3rem 0;
}

.team-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 2rem;
}

.team-member {
    background: var(--light-color);
    padding: 2rem;
    border-radius: 10px;
    text-align: center;
    transition: all 0.3s ease;
}

.team-member:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.member-avatar {
    font-size: 4rem;
    margin-bottom: 1rem;
}

.team-member h3 {
    font-size: 1.3rem;
    margin-bottom: 0.5rem;
    color: var(--dark-color);
}

.team-member .role {
    color: var(--primary-color);
    font-weight: 600;
    margin-bottom: 1rem;
}

.team-member .bio {
    color: #666;
}

/* Values Section */
.values-section {
    margin-top: 3rem;
}

.values-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
}

.value-card {
    background: white;
    padding: 2rem;
    border-left: 4px solid var(--primary-color);
    border-radius: 5px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
}

.value-card h3 {
    color: var(--primary-color);
    margin-bottom: 0.5rem;
}

.value-card p {
    color: #666;
}

/* ===================================
   SERVICES SECTION
   =================================== */
.services-section {
    padding: 60px 20px;
    background-color: var(--light-color);
}

.services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    margin-bottom: 3rem;
}

.service-card {
    background: white;
    padding: 2rem;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
    border-top: 3px solid var(--primary-color);
}

.service-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 30px rgba(102, 126, 234, 0.2);
}

.service-icon {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    display: block;
}

.service-card h3 {
    font-size: 1.3rem;
    margin-bottom: 1rem;
    color: var(--dark-color);
}

.service-card p {
    color: #666;
    margin-bottom: 1.5rem;
}

.service-list {
    list-style: none;
}

.service-list li {
    color: #666;
    margin-bottom: 0.5rem;
}

.cta-section {
    text-align: center;
    background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
    color: white;
    padding: 3rem;
    border-radius: 10px;
    margin-top: 3rem;
}

.cta-section h2 {
    color: white;
    margin-bottom: 1rem;
}

/* ===================================
   PORTFOLIO SECTION
   =================================== */
.portfolio-section {
    padding: 60px 20px;
}

.filter-buttons {
    text-align: center;
    margin-bottom: 3rem;
    display: flex;
    justify-content: center;
    gap: 1rem;
    flex-wrap: wrap;
}

.filter-btn {
    padding: 10px 20px;
    border: 2px solid var(--primary-color);
    background: transparent;
    color: var(--primary-color);
    border-radius: 5px;
    cursor: pointer;
    font-weight: 600;
    transition: all 0.3s ease;
}

.filter-btn:hover,
.filter-btn.active {
    background: var(--primary-color);
    color: white;
}

.portfolio-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
    gap: 2rem;
}

.portfolio-item {
    background: white;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    transition: all 0.3s ease;
}

.portfolio-item:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 30px rgba(102, 126, 234, 0.2);
}

.portfolio-image {
    background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
    color: white;
    height: 200px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 3rem;
}

.portfolio-info {
    padding: 1.5rem;
}

.portfolio-info h3 {
    font-size: 1.2rem;
    margin-bottom: 0.5rem;
    color: var(--dark-color);
}

.portfolio-info p {
    color: #666;
    margin-bottom: 1rem;
}

.tags {
    display: flex;
    gap: 0.5rem;
    flex-wrap: wrap;
}

.tags span {
    background: var(--light-color);
    color: var(--primary-color);
    padding: 0.3rem 0.8rem;
    border-radius: 20px;
    font-size: 0.85rem;
    font-weight: 500;
}

/* Stats Section */
.stats-section {
    background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
    color: white;
    padding: 60px 20px;
    text-align: center;
}

.stats-section h2 {
    font-size: 2rem;
    margin-bottom: 3rem;
    color: white;
}

.stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 2rem;
}

.stat-card {
    background: rgba(255, 255, 255, 0.1);
    padding: 2rem;
    border-radius: 10px;
    backdrop-filter: blur(10px);
}

.stat-card h3 {
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
}

/* ===================================
   CONTACT SECTION
   =================================== */
.contact-section {
    padding: 60px 20px;
    background-color: var(--light-color);
}

.contact-wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
    max-width: 1000px;
    margin: 0 auto;
}

.contact-form-wrapper h2,
.contact-info-wrapper h2 {
    font-size: 1.8rem;
    margin-bottom: 2rem;
    color: var(--dark-color);
}

.form-group {
    margin-bottom: 1.5rem;
}

.form-group label {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: 600;
    color: var(--dark-color);
}

.form-group input,
.form-group textarea {
    width: 100%;
    padding: 10px;
    border: 1px solid var(--border-color);
    border-radius: 5px;
    font-family: inherit;
    font-size: 1rem;
    transition: all 0.3s ease;
}

.form-group input:focus,
.form-group textarea:focus {
    outline: none;
    border-color: var(--primary-color);
    box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
}

.contact-info-card {
    display: flex;
    gap: 1rem;
    margin-bottom: 2rem;
    background: white;
    padding: 1.5rem;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
}

.info-icon {
    font-size: 2rem;
    min-width: 40px;
}

.info-content h3 {
    font-size: 1.1rem;
    margin-bottom: 0.5rem;
    color: var(--dark-color);
}

.info-content p {
    color: #666;
}

.info-content a {
    color: var(--primary-color);
    text-decoration: none;
    font-weight: 500;
}

.info-content a:hover {
    text-decoration: underline;
}

.social-icons {
    display: flex;
    gap: 1rem;
}

.social-icon {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
    color: white;
    border-radius: 50%;
    text-decoration: none;
    transition: all 0.3s ease;
    font-weight: bold;
}

.social-icon:hover {
    transform: scale(1.1) rotateZ(10deg);
}

.map-section {
    padding: 60px 20px;
}

.map-section h2 {
    text-align: center;
    font-size: 2rem;
    margin-bottom: 2rem;
}

.map-placeholder {
    background: var(--light-color);
    border: 2px dashed var(--border-color);
    border-radius: 10px;
    height: 400px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #999;
}

/* ===================================
   FOOTER
   =================================== */
.footer {
    background: var(--dark-color);
    color: white;
    padding: 2rem;
    text-align: center;
}

.footer p {
    margin-bottom: 1rem;
}

.social-links {
    display: flex;
    justify-content: center;
    gap: 1rem;
}

.social-links a {
    color: white;
    text-decoration: none;
    transition: all 0.3s ease;
    font-weight: bold;
}

.social-links a:hover {
    color: var(--accent-color);
    transform: scale(1.2);
}

/* ===================================
   RESPONSIVE DESIGN
   =================================== */
@media (max-width: 768px) {
    .nav-menu {
        gap: 1rem;
        font-size: 0.9rem;
    }

    .hero h1 {
        font-size: 2rem;
    }

    .hero p {
        font-size: 1rem;
    }

    .features-grid,
    .team-grid,
    .values-grid,
    .services-grid,
    .stats-grid {
        grid-template-columns: 1fr;
    }

    .contact-wrapper {
        grid-template-columns: 1fr;
    }

    .page-header h1 {
        font-size: 1.8rem;
    }

    .filter-buttons {
        flex-direction: column;
    }

    .filter-btn {
        width: 100%;
    }

    .portfolio-grid {
        grid-template-columns: 1fr;
    }
}

@media (max-width: 480px) {
    .navbar .container {
        flex-direction: column;
        gap: 1rem;
    }

    .nav-menu {
        flex-wrap: wrap;
        justify-content: center;
        gap: 0.5rem;
    }

    .hero h1 {
        font-size: 1.5rem;
    }

    .hero {
        min-height: 300px;
        padding: 50px 20px;
    }

    .page-header {
        padding: 40px 20px;
    }

    .page-header h1 {
        font-size: 1.5rem;
    }
}
