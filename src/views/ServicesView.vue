<template>
    <!-- Navigation -->
    <NavBar />
    <!-- Hero Section -->
    <section class="hero hero-img" id="home">
        <div class="">
            <div class="hero-content">
                <h1>
                    Our Services
                </h1>
                <p>Comprehensive consulting solutions designed to transform your business and drive
                    sustainable competitive advantage</p>
            </div>
        </div>
    </section>

    <!-- Services Detail -->
    <section class="services-detail">
        <div class="container">
            <!-- Management Consulting -->
            <div class="service-detail">
                <div class="service-content">
                    <h2>Management Consulting</h2>
                    <p>Accelerate your digital journey with comprehensive transformation programs that modernize operations,
                        and enhance customer experiences.</p>

                    <ul class="service-features">
                        <li>Defining clear and actionable strategies for growth
                            and market leadership</li>
                        <li>Implementing systems to track and improve
                            performance</li>
                        <li>Optimizing business processes and improving
                            efficiency</li>
                        <li>Planning, executing, and controlling projects to achieve
                            specific objectives</li>
                        <li>Guiding organizations through successful
                            transformations</li>
                        <li>Developing strategies to attract, retain, and
                            develop talent</li>
                    </ul>

                    <a href="/contact" class="btn btn-primary">Learn More →</a>
                </div>

                <div class="service-image">
                    <h3>Impact Delivered</h3>
                    <div class="service-stat">
                        <div class="service-stat-number">20%</div>
                        <div class="service-stat-label">Average Cost Reduction</div>
                    </div>
                    <div class="service-stat">
                        <div class="service-stat-number">2.8x</div>
                        <div class="service-stat-label">Faster Time-to-Market</div>
                    </div>
                    <div class="service-stat">
                        <div class="service-stat-number">98%</div>
                        <div class="service-stat-label">Project Success Rate</div>
                    </div>
                </div>
            </div>

            <!-- Organizational Excellence -->
            <div class="service-detail">
                <div class="service-content">
                    <h2>Training</h2>
                    <p>Build high-performing organizations through strategic workforce planning, leadership development, and
                        culture transformation initiatives that drive sustainable business results.</p>

                    <ul class="service-features">
                        <li>Cultivate effective leaders at all levels with
                            programs focusing on strategic thinking, communication, team building, and
                            change management</li>
                        <li>Equip your project teams with the skills to plan,
                            execute, and deliver projects successfully using industry best practices like
                            PRINCE2 and Agile methodologies. Offerings range from foundational
                            project management to advanced program management</li>
                        <li>Prepare your organization for successful
                            transformations by training your team on change management principles
                            and techniques, minimizing disruption and maximizing adoption</li>
                        <li>Improve efficiency and productivity through training
                            in process optimization, Lean principles, Six Sigma methodologies, and
                            performance management</li>
                    </ul>

                    <a href="/contact" class="btn btn-primary">Learn More →</a>
                </div>

                <div class="service-image">
                    <h3>Impact Delivered</h3>
                    <div class="service-stat">
                        <div class="service-stat-number">68%</div>
                        <div class="service-stat-label">Improvement in Employee Engagement</div>
                    </div>
                    <div class="service-stat">
                        <div class="service-stat-number">35%</div>
                        <div class="service-stat-label">Reduction in Turnover</div>
                    </div>
                    <div class="service-stat">
                        <div class="service-stat-number">2.5x</div>
                        <div class="service-stat-label">Leadership Effectiveness Increase</div>
                    </div>
                </div>
            </div>

            <!-- Strategy & Growth -->
            <div class="service-detail">
                <div class="service-content">
                    <h2>Strategy & Growth</h2>
                    <p>Navigate complex market dynamics and unlock new growth opportunities with our strategic consulting
                        expertise. We partner with leadership teams to craft winning strategies that create lasting
                        competitive advantages.</p>

                    <ul class="service-features">
                        <li>Corporate strategy development and execution</li>
                        <li>Market entry and expansion strategies</li>
                        <li>M&A strategy and due diligence</li>
                        <li>Business model innovation</li>
                        <li>Portfolio optimization and rationalization</li>
                        <li>Growth acceleration programs</li>
                    </ul>

                    <a href="/contact" class="btn btn-primary">Learn More →</a>
                </div>

                <div class="service-image">
                    <h3>Impact Delivered</h3>
                    <div class="service-stat">
                        <div class="service-stat-number">3.2x</div>
                        <div class="service-stat-label">Average Revenue Growth</div>
                    </div>
                    <div class="service-stat">
                        <div class="service-stat-number">87%</div>
                        <div class="service-stat-label">Strategy Success Rate</div>
                    </div>
                    <div class="service-stat">
                        <div class="service-stat-number">6-12mo</div>
                        <div class="service-stat-label">Typical Engagement Duration</div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!--Footer-->
    <FooterView />
</template>

<script>
import NavBar from '../components/NavBar.vue'
import FooterView from '../components/FooterView.vue'

export default {
    name: 'ServicesView',
    components: { NavBar, FooterView },
}
</script>

<style scoped>
/* Hero Section */
.hero {
    min-height: 60vh;
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
    text-align: center;
}

.hero h1 {
    font-size: 60px;
    line-height: 1.1;
    margin-bottom: 24px;
}

.hero .highlight {
    color: var(--gold);
    display: block;
}

.hero p {
    font-size: 20px;
    margin-bottom: 40px;
    max-width: 700px;
    opacity: 0.9;
}

.hero-buttons {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
}

/* Services Detail Section */
.services-detail {
    padding: 100px 24px;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
}

.service-detail {
    margin-bottom: 120px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 64px;
    align-items: center;
}

.service-detail:last-child {
    margin-bottom: 0;
}

.service-detail:nth-child(even) {
    direction: rtl;
}

.service-detail:nth-child(even)>* {
    direction: ltr;
}

.service-content h2 {
    font-size: 42px;
    margin-bottom: 24px;
    color: var(--navy);
}

.service-content p {
    font-size: 18px;
    color: var(--gray);
    margin-bottom: 32px;
    line-height: 1.8;
}

.service-features {
    list-style: none;
    margin-bottom: 32px;
}

.service-features li {
    display: flex;
    align-items: start;
    gap: 12px;
    margin-bottom: 16px;
    font-size: 16px;
    color: var(--gray-dark);
}

.service-features li::before {
    content: "→";
    color: var(--gold);
    font-weight: bold;
    font-size: 20px;
    flex-shrink: 0;
}

.service-image {
    background: var(--gray-light);
    border-radius: 16px;
    padding: 64px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    min-height: 400px;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.08);
}

.service-image h3 {
    font-size: 24px;
    color: var(--navy);
    margin-bottom: 24px;
}

.service-stat {
    margin-bottom: 24px;
}

.service-stat-number {
    font-size: 48px;
    font-weight: 700;
    color: var(--gold);
    margin-bottom: 8px;
}

.service-stat-label {
    font-size: 16px;
    color: var(--gray);
}

/* Responsive */
@media (max-width: 768px) {



    .service-detail {
        grid-template-columns: 1fr;
        gap: 40px;
        margin-bottom: 80px;
    }

    .service-detail:nth-child(even) {
        direction: ltr;
    }

    .service-content h2 {
        font-size: 32px;
    }

    .btn {
        width: 100%;
    }
}
</style>