<template>
    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="#">
                <img src="../assets/logo.png" alt="Apex Consulting">
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#services">Services</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="/about">About</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="/results">Results</a>
                    </li>
                    <li class="nav-item">
                        <a class="btn btn-primary" href="/contact">Get Started</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero hero-img" id="home">
        <div class="">
            <div class="hero-content">
                <h1>
                    Transform Strategy Into
                    <span class="highlight">Measurable Results</span>
                </h1>
                <p>Partner with industry-leading consultants who drive sustainable growth through data-driven insights and
                    proven methodologies.</p>
                <div class="hero-buttons">
                    <button class="btn btn-primary">Start Your Transformation →</button>
                    <button class="btn btn-outline">Our Approach</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <div class="section-header">
                <h2>Our Expertise</h2>
                <p>Comprehensive solutions tailored to your unique challenges and opportunities</p>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <h3>Management Consulting</h3>
                    <p>Develop winning strategies to attract, retain, and develop talent. Optimize business processes and
                        improve efficiency
                    </p>
                </div>
                <div class="service-card">
                    <h3>ICT Consulting</h3>
                    <p>Align IT with business objectives. Build and implement custom software solutions and robust
                        IT infrastructure.
                    </p>
                </div>
                <div class="service-card">
                    <h3>Training</h3>
                    <p>Create customized training solutions for teams. Equip project teams with the skills to plan,
                        execute, and deliver projects successfully using industry best practices</p>
                </div>
                <div class="service-card">
                    <h3>Performance Optimization</h3>
                    <p>Maximize operational efficiency and profitability through data-driven process improvement.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Why Choose Us Section -->
    <section class="why-us">
        <div class="container">
            <div class="why-us-content">
                <div class="why-us-text">
                    <h2>
                        Why Leading Organizations
                        <span class="highlight">Choose Us</span>
                    </h2>
                    <p>We combine deep industry knowledge with innovative thinking to deliver transformative results that
                        stand the test of time.</p>
                    <ul class="benefits">
                        <li>Proven track record across successful engagements</li>
                        <li>Industry expertise spanning SME's to high-growth startups</li>
                        <li>Proprietary/open-source frameworks backed by extensive research</li>
                        <li>Dedicated teams committed to your long-term success</li>
                        <li>Measurable ROI with clear, actionable deliverables</li>
                        <li>Global presence with local market insights</li>
                    </ul>
                </div>
                <div class="stats-box" id="results">
                    <div class="stat">
                        <div class="stat-number">98%</div>
                        <div class="stat-label">Client Satisfaction Rate</div>
                    </div>
                    <div class="stat">
                        <div class="stat-number">Millions</div>
                        <div class="stat-label">in Value Created for Clients</div>
                    </div>
                    <div class="stat">
                        <div class="stat-number">5+</div>
                        <div class="stat-label">Countries Served</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Why Working With Us Section -->
    <section class="services">
        <div class="container">
            <div class="section-header">
                <h2>
                    Working with Us is Simple
                </h2>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">📩</div>
                    <h3>Schedule a Consultation</h3>
                    <p>Develop winning strategies that drive sustainable competitive advantage and accelerate market
                        leadership.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">🗓</div>
                    <h3>Develop a Custom Plan</h3>
                    <p>Build high-performing teams and cultures that consistently deliver exceptional business outcomes.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">✔</div>
                    <h3>Achieve your Desired Success</h3>
                    <p>Maximize operational efficiency and profitability through data-driven process improvement.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Why Choose Us Section -->
    <section class="why-us">
        <div class="container">
            <div class="why-us-content">
                <div class="">
                    <img src="../assets/team.jpg" class="img-fluid w-100" alt="Responsive image" />
                </div>
                <div class="why-us-text">
                    <h2>
                        What Makes Us Different,
                        <span class="highlight">Our Offering</span>
                    </h2>
                    <p>We follow a collaborative and client-centric approach, working closely with
                        our clients to understand their specific needs and challenges. Our
                        methodology involves:</p>
                    <ul class="benefits">
                        <li>Thoroughly analyzing the client's business and industry</li>
                        <li>Developing customized solutions tailored to the client's needs</li>
                        <li>Executing the plan effectively and efficiently</li>
                        <li>Tracking progress and making adjustments as needed</li>
                        <li>Measuring the impact of our solutions and ensuring client
                            satisfaction</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Clients Section with Bootstrap Carousel -->
    <section class="clients" id="clients">
        <div class="container">
            <div class="section-header">
                <h2>Featured Clients</h2>
                <p>Partnering with organizations that shape the future</p>
            </div>

            <div id="clientsCarousel" class="carousel slide" data-bs-ride="carousel">
                <!-- Indicators -->
                <div class="carousel-indicators">
                    <button type="button" data-bs-target="#clientsCarousel" data-bs-slide-to="0" class="active"
                        aria-current="true" aria-label="Slide 1"></button>
                    <button type="button" data-bs-target="#clientsCarousel" data-bs-slide-to="1"
                        aria-label="Slide 2"></button>
                    <button type="button" data-bs-target="#clientsCarousel" data-bs-slide-to="2"
                        aria-label="Slide 3"></button>
                    <button type="button" data-bs-target="#clientsCarousel" data-bs-slide-to="3"
                        aria-label="Slide 4"></button>
                    <button type="button" data-bs-target="#clientsCarousel" data-bs-slide-to="4"
                        aria-label="Slide 5"></button>
                </div>

                <!-- Carousel Items -->
                <div class="carousel-inner">
                    <div class="carousel-item active">
                        <div class="client-logo-wrapper">
                            <img src="../assets/client1.png" class="d-block" alt="Client 1">
                        </div>
                    </div>
                    <div class="carousel-item">
                        <div class="client-logo-wrapper">
                            <img src="../assets/client2.png" class="d-block" alt="Client 2">
                        </div>
                    </div>
                    <div class="carousel-item">
                        <div class="client-logo-wrapper">
                            <img src="../assets/client3.png" class="d-block" alt="Client 3">
                        </div>
                    </div>
                    <div class="carousel-item">
                        <div class="client-logo-wrapper">
                            <img src="../assets/client4.png" class="d-block" alt="Client 4">
                        </div>
                    </div>
                    <div class="carousel-item">
                        <div class="client-logo-wrapper">
                            <img src="../assets/client5.png" class="d-block" alt="Client 5">
                        </div>
                    </div>
                </div>

                <!-- Controls -->
                <button class="carousel-control-prev" type="button" data-bs-target="#clientsCarousel" data-bs-slide="prev">
                    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Previous</span>
                </button>
                <button class="carousel-control-next" type="button" data-bs-target="#clientsCarousel" data-bs-slide="next">
                    <span class="carousel-control-next-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Next</span>
                </button>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta" id="contact">
        <div class="container">
            <h2>Ready to Transform Your Business?</h2>
            <p>Let's discuss how our proven methodologies can drive measurable results for your organization. Schedule a
                complimentary consultation today.</p>
            <div class="cta-buttons">
                <button class="btn btn-primary">Schedule Consultation →</button>
                <button class="btn btn-outline">✉ Contact Us</button>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <!-- Address Row -->
            <div class="row footer-row">
                <div class="col-12">
                    <h5 class="footer-heading">Our Office</h5>
                    <p><i class="bi bi-geo-alt-fill me-2"></i>Plot 13A Wada Nas Street, Guzape</p>
                    <p><i class="bi bi-geo-alt-fill me-2"></i>Federal Capital Territory, Nigeria.</p>
                    <p><i class="bi bi-envelope-fill me-2"></i>provenperformanceltd@gmail.com</p>
                </div>
            </div>

            <!-- Quick Links Row -->
            <div class="row footer-row">
                <div class="col-12">
                    <h5 class="footer-heading">Quick Links</h5>
                    <div class="row">
                        <div class="col-md-3 col-6">
                            <a href="#services">Services</a>
                        </div>
                        <div class="col-md-3 col-6">
                            <a href="/about">About Us</a>
                        </div>
                        <div class="col-md-3 col-6">
                            <a href="/results">Results</a>
                        </div>
                        <div class="col-md-3 col-6">
                            <a href="/contact">Contact</a>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Social Media Row -->
            <div class="row footer-row">
                <div class="col-12">
                    <h5 class="footer-heading">Follow Us</h5>
                    <div class="social-icons">
                        <a href="#" aria-label="Facebook"><i class="bi bi-facebook"></i></a>
                        <a href="#" aria-label="Twitter"><i class="bi bi-twitter"></i></a>
                        <a href="#" aria-label="LinkedIn"><i class="bi bi-linkedin"></i></a>
                        <a href="#" aria-label="Instagram"><i class="bi bi-instagram"></i></a>
                        <a href="#" aria-label="YouTube"><i class="bi bi-youtube"></i></a>
                    </div>
                </div>
            </div>

            <!-- Copyright Row -->
            <div class="row">
                <div class="col-12">
                    <hr class="footer-divider">
                    <p class="copyright-text">© 2025 Proven Performance Ltd. All rights reserved.</p>
                    <p class="copyright">Transforming businesses worldwide</p>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'HomeView',
    data() {
        return {
            mobileMenuOpen: false,
        }
    },
    methods: {
        toggleMobileMenu() {
            this.mobileMenuOpen = !this.mobileMenuOpen;
        },
    }
}
</script>

<style scoped>
/* Navigation */
.navbar {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    background: rgba(255, 255, 255, 0.95) !important;
    backdrop-filter: blur(10px);
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    z-index: 1000;
    padding: 0;
}

.navbar .container-fluid {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 24px;
    height: 80px;
}

.navbar-brand {
    display: flex;
    align-items: center;
}

.navbar-brand img {
    height: 60px;
    /* Adjust this value based on your logo size */
    width: auto;
    object-fit: contain;
}

.navbar-nav {
    gap: 32px;
    align-items: center;
}

.navbar-nav .nav-link {
    color: var(--gray-dark) !important;
    font-weight: 500;
    transition: color 0.3s;
    padding: 0.5rem 0;
}

.navbar-nav .nav-link:hover {
    color: var(--gold) !important;
}

.navbar-nav .btn-primary {
    padding: 0.5rem 1.5rem;
    font-weight: 500;
}

/* Mobile styles */
@media (max-width: 991.98px) {
    .navbar-nav {
        gap: 1rem;
        padding: 1rem 0;
    }

    .navbar-nav .nav-item {
        text-align: center;
    }

    .navbar .container-fluid {
        height: auto;
    }
}

.btn {
    padding: 12px 32px;
    border: none;
    border-radius: 8px;
    font-weight: 600;
    font-size: 16px;
    cursor: pointer;
    transition: all 0.3s;
    text-decoration: none;
    display: inline-block;
}

.btn-primary {
    background: var(--gold);
    color: var(--navy);
}

.btn-primary:hover {
    background: var(--gold-dark);
    transform: translateY(-2px);
    box-shadow: 0 10px 30px rgba(212, 175, 55, 0.3);
}

.btn-outline {
    background: transparent;
    border: 2px solid var(--white);
    color: var(--white);
}

.btn-outline:hover {
    background: var(--white);
    color: var(--navy);
}

.mobile-menu {
    display: none;
    font-size: 24px;
    cursor: pointer;
    color: var(--navy);
}

/* Hero Section */
.hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy-light) 100%);
    position: relative;
    overflow: hidden;
    padding-top: 80px;
}

.hero-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 24px;
    color: var(--white);
    animation: fadeInUp 0.8s ease-out;
}

.hero h1 {
    font-size: 72px;
    line-height: 1.1;
    margin-bottom: 24px;
}

.hero .highlight {
    color: var(--gold);
    display: block;
}

.hero p {
    font-size: 24px;
    margin-bottom: 40px;
    max-width: 700px;
    opacity: 0.9;
}

.hero-buttons {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
}

/* Services Section */
.services {
    padding: 100px 24px;
    background: var(--gray-light);
}

.container {
    max-width: 1200px;
    margin: 0 auto;
}

.section-header {
    text-align: center;
    margin-bottom: 64px;
}

.section-header h2 {
    font-size: 48px;
    margin-bottom: 16px;
    color: var(--navy);
}

.section-header p {
    font-size: 20px;
    color: var(--gray);
}

.services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 32px;
}

.service-card {
    background: var(--white);
    padding: 40px;
    border-radius: 12px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
    transition: all 0.3s;
}

.service-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 12px 40px rgba(0, 0, 0, 0.15);
}

.service-icon {
    width: 64px;
    height: 64px;
    background: rgba(212, 175, 55, 0.1);
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 24px;
    font-size: 32px;
}

.service-card h3 {
    font-size: 24px;
    margin-bottom: 16px;
    color: var(--navy);
}

.service-card p {
    color: var(--gray);
    line-height: 1.7;
}

/* Why Choose Us Section */
.why-us {
    padding: 100px 24px;
}

.why-us-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 64px;
    align-items: center;
}

.why-us h2 {
    font-size: 48px;
    margin-bottom: 24px;
    color: var(--navy);
}

.why-us .highlight {
    color: var(--gold);
    display: block;
}

.why-us-text p {
    font-size: 18px;
    color: var(--gray);
    margin-bottom: 32px;
}

.benefits {
    list-style: none;
}

.benefits li {
    display: flex;
    gap: 12px;
    margin-bottom: 16px;
    color: var(--gray-dark);
}

.benefits li::before {
    content: "✓";
    color: var(--gold);
    font-weight: bold;
    font-size: 20px;
    flex-shrink: 0;
}

.stats-box {
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy-light) 100%);
    padding: 64px;
    border-radius: 16px;
    color: var(--white);
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.15);
}

.hero-img {
    background-image: linear-gradient(to right, rgba(26, 35, 50, 0.95), rgba(26, 35, 50, 0.7)), url('../assets/hero.jpg');
    background-size: cover;
    background-position: center;
}

.stat {
    margin-bottom: 40px;
}

.stat:last-child {
    margin-bottom: 0;
}

.stat-number {
    font-size: 56px;
    font-weight: 700;
    margin-bottom: 8px;
}

.stat-label {
    font-size: 18px;
    opacity: 0.9;
}

/* CTA Section */
.cta {
    padding: 100px 24px;
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy-light) 100%);
    text-align: center;
    color: var(--white);
}

.cta h2 {
    font-size: 48px;
    margin-bottom: 24px;
}

.cta p {
    font-size: 20px;
    margin-bottom: 40px;
    opacity: 0.9;
    max-width: 800px;
    margin-left: auto;
    margin-right: auto;
}

.cta-buttons {
    display: flex;
    gap: 16px;
    justify-content: center;
    flex-wrap: wrap;
}

/* Footer */
footer {
    background: var(--navy);
    color: var(--white);
    padding: 60px 24px 30px;
}

footer .container {
    max-width: 1200px;
}

.footer-row {
    margin-bottom: 40px;
    text-align: center;
}

.footer-heading {
    font-size: 20px;
    font-weight: 600;
    margin-bottom: 20px;
    color: var(--gold);
}

footer p {
    margin-bottom: 8px;
    opacity: 0.9;
}

/* Quick Links */
.footer-row a {
    color: var(--white);
    text-decoration: none;
    opacity: 0.9;
    transition: all 0.3s;
    display: inline-block;
    margin-bottom: 10px;
}

.footer-row a:hover {
    color: var(--gold);
    opacity: 1;
}

/* Social Media Icons */
.social-icons {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
}

.social-icons a {
    width: 45px;
    height: 45px;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 20px;
    transition: all 0.3s;
}

.social-icons a:hover {
    background: var(--gold);
    color: var(--navy);
    transform: translateY(-3px);
}

/* Copyright Section */
.footer-divider {
    border-color: rgba(255, 255, 255, 0.2);
    margin: 30px 0 20px;
}

.copyright-text {
    margin-bottom: 8px;
    font-weight: 500;
    text-align: center;
}

footer .copyright {
    opacity: 0.7;
    font-size: 14px;
    margin-bottom: 0;
    text-align: center;
}

/* Responsive */
@media (max-width: 768px) {
    .footer-row {
        margin-bottom: 30px;
    }

    .footer-heading {
        font-size: 18px;
    }

    .social-icons a {
        width: 40px;
        height: 40px;
        font-size: 18px;
    }
}

/* Responsive */
@media (max-width: 768px) {
    .footer-row {
        margin-bottom: 30px;
    }

    .footer-heading {
        font-size: 18px;
    }

    .social-icons a {
        width: 40px;
        height: 40px;
        font-size: 18px;
    }
}

/* Clients Section */
.clients {
    padding: 100px 24px;
    background: var(--gray-light);
}

.clients .container {
    max-width: 1200px;
    margin: 0 auto;
}

.clients .section-header {
    text-align: center;
    margin-bottom: 64px;
}

.clients .section-header h2 {
    font-size: 48px;
    margin-bottom: 16px;
    color: var(--navy);
}

.clients .section-header p {
    font-size: 20px;
    color: var(--gray);
}

/* Carousel Styling */
#clientsCarousel {
    max-width: 800px;
    margin: 0 auto;
}

.client-logo-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 60px 40px;
    min-height: 300px;
}

.client-logo-wrapper img {
    max-width: 100%;
    max-height: 200px;
    width: auto;
    height: auto;
    object-fit: contain;
    filter: grayscale(100%);
    opacity: 0.7;
    transition: all 0.3s ease;
}

.carousel-item.active .client-logo-wrapper img {
    filter: grayscale(0%);
    opacity: 1;
}

/* Carousel Controls */
.carousel-control-prev,
.carousel-control-next {
    width: 50px;
    height: 50px;
    background-color: var(--navy);
    border-radius: 50%;
    top: 50%;
    transform: translateY(-50%);
    opacity: 0.8;
}

.carousel-control-prev {
    left: -80px;
}

.carousel-control-next {
    right: -80px;
}

.carousel-control-prev:hover,
.carousel-control-next:hover {
    opacity: 1;
    background-color: var(--gold);
}

.carousel-control-prev-icon,
.carousel-control-next-icon {
    width: 20px;
    height: 20px;
}

/* Carousel Indicators */
.carousel-indicators {
    margin-bottom: -40px;
}

.carousel-indicators button {
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background-color: var(--gray);
    opacity: 0.5;
    border: none;
}

.carousel-indicators button.active {
    background-color: var(--gold);
    opacity: 1;
}

/* Responsive */
@media (max-width: 768px) {
    .clients .section-header h2 {
        font-size: 36px;
    }

    .client-logo-wrapper {
        padding: 40px 20px;
        min-height: 250px;
    }

    .client-logo-wrapper img {
        max-height: 150px;
    }

    .carousel-control-prev,
    .carousel-control-next {
        width: 40px;
        height: 40px;
    }

    .carousel-control-prev {
        left: 10px;
    }

    .carousel-control-next {
        right: 10px;
    }
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

/* Responsive */
@media (max-width: 768px) {
    .nav-links {
        display: none;
    }

    .mobile-menu {
        display: block;
    }

    .hero h1 {
        font-size: 40px;
    }

    .hero p {
        font-size: 18px;
    }

    .section-header h2 {
        font-size: 36px;
    }

    .why-us-content {
        grid-template-columns: 1fr;
    }

    .hero-buttons,
    .cta-buttons {
        flex-direction: column;
    }

    .btn {
        width: 100%;
        text-align: center;
    }
}
</style>