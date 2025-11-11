<template>
    <!-- Navigation -->
    <NavBar />
    <!-- Hero Section -->
    <section class="hero hero-img" id="home">
        <div class="">
            <div class="hero-content">
                <h1>
                    <span class="highlight">About Us</span>
                </h1>
                <p>About Us - The Company</p>
            </div>
        </div>
    </section>
    <!--Core Values-->
    <section class="services">
        <div class="container">
            <div class="section-header">
                <h2>Company Profile</h2>
                <p>
                    Proven Performance Ltd is a management and ICT consulting firm dedicated
                    to empowering organizations to achieve sustainable growth and operational
                    excellence. We provide tailored solutions that address our clients' unique
                    challenges and opportunities, leveraging our deep industry expertise and
                    innovative thinking to deliver measurable results. We believe in building
                    long-term partnerships with our clients, acting as trusted advisors and
                    strategic problem-solvers.
                </p>
            </div>
        </div>
    </section>
    <!-- Mission, Vision & Values Section -->
    <section class="mvv-section">
        <div class="container">
            <div class="mvv-intro">
                <h2>Our Foundation</h2>
                <p>Built on decades of excellence, guided by timeless principles</p>
            </div>

            <div class="mvv-grid">
                <div class="mvv-card mission-card">
                    <div class="mvv-icon">🎯</div>
                    <h3>Mission</h3>
                    <p>To empower businesses with strategic insights and cutting-edge technology
                        solutions that drive transformative growth and create lasting value.</p>
                </div>

                <div class="mvv-card vision-card">
                    <div class="mvv-icon">✨</div>
                    <h3>Vision</h3>
                    <p>To be the preferred partner for organizations seeking innovative and
                        impactful management and ICT consulting services.</p>
                </div>
            </div>

            <div class="values-section">
                <h3>Core Values</h3>
                <div class="values-grid">
                    <div class="value-item">
                        <div class="value-number">01</div>
                        <h4>Client Focus</h4>
                        <p>We prioritize our clients' needs and strive to exceed their
                            expectations.</p>
                    </div>
                    <div class="value-item">
                        <div class="value-number">02</div>
                        <h4>Integrity</h4>
                        <p>We adhere to the highest ethical standards in all our1
                            interactions.</p>
                    </div>
                    <div class="value-item">
                        <div class="value-number">03</div>
                        <h4>Innovation</h4>
                        <p>We embrace creativity and continuously seek new and better
                            ways to serve our clients.</p>
                    </div>
                    <div class="value-item">
                        <div class="value-number">04</div>
                        <h4>Excellence</h4>
                        <p>We are committed to delivering exceptional quality in our
                            services.</p>
                    </div>
                    <div class="value-item">
                        <div class="value-number">05</div>
                        <h4>Collaboration</h4>
                        <p>We foster a collaborative environment, both internally and with
                            our clients.</p>
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
    name: 'AboutView',
    components: { NavBar, FooterView },
}
</script>

<style>
/* Hero Section */
.hero {
    min-height: 70vh;
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

.hero-img {
    background-image: linear-gradient(to right, rgba(26, 35, 50, 0.95), rgba(26, 35, 50, 0.7)), url('../assets/about.jpg');
    background-size: cover;
    background-position: center;
}

/**Core Values */
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

/* Mission, Vision & Values Section */
.mvv-section {
    padding: 100px 24px;
    background: linear-gradient(180deg, var(--white) 0%, var(--gray-light) 100%);
}

.mvv-intro {
    text-align: center;
    margin-bottom: 80px;
}

.mvv-intro h2 {
    font-size: 48px;
    color: var(--navy);
    margin-bottom: 16px;
}

.mvv-intro p {
    font-size: 20px;
    color: var(--gray);
}

.mvv-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 32px;
    margin-bottom: 100px;
}

.mvv-card {
    background: var(--white);
    padding: 48px;
    border-radius: 20px;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.08);
    transition: transform 0.3s, box-shadow 0.3s;
}

.mvv-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 20px 60px rgba(0, 0, 0, 0.12);
}

.mvv-icon {
    font-size: 48px;
    margin-bottom: 24px;
}

.mvv-card h3 {
    font-size: 32px;
    color: var(--navy);
    margin-bottom: 20px;
}

.mvv-card p {
    font-size: 18px;
    line-height: 1.8;
    color: var(--gray);
}

.mission-card {
    border-top: 4px solid var(--gold);
}

.vision-card {
    border-top: 4px solid var(--navy);
}

.values-section {
    text-align: center;
}

.values-section>h3 {
    font-size: 42px;
    color: var(--navy);
    margin-bottom: 64px;
}

.values-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 40px;
}

.value-item {
    text-align: left;
    padding: 32px;
    background: var(--white);
    border-radius: 16px;
    transition: all 0.3s;
    border: 2px solid transparent;
}

.value-item:hover {
    border-color: var(--gold);
    transform: translateY(-4px);
    box-shadow: 0 10px 30px rgba(212, 175, 55, 0.2);
}

.value-number {
    font-size: 14px;
    font-weight: 700;
    color: var(--gold);
    margin-bottom: 16px;
    letter-spacing: 2px;
}

.value-item h4 {
    font-size: 24px;
    color: var(--navy);
    margin-bottom: 12px;
}

.value-item p {
    font-size: 15px;
    line-height: 1.7;
    color: var(--gray);
}

@media (max-width: 480px) {
    .mvv-grid {
    grid-template-columns: 1fr;
}

.values-grid {
    grid-template-columns: 1fr;
}
}
</style>