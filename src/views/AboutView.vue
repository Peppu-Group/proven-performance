<template>
    <!-- ========== Site Navigation ========== -->
    <!-- Reusable navbar component fixed to the top of the viewport -->
    <NavBar />

    <!-- ========== Hero Section ========== -->
    <!-- Page banner with a background image overlay and centered heading.
         hero-img applies the background image defined separately in the styles -->
    <section class="hero hero-img">
        <div class="">
            <div class="hero-content">
                <h1>
                    <!-- Gold-colored highlight text; display:block makes it stack on its own line -->
                    <span class="highlight">About Us</span>
                </h1>
                <!-- Subtitle / breadcrumb-style descriptor for the page -->
                <p>About Us - Proven Performance Ltd</p>
            </div>
        </div>
    </section>

    <!-- ========== Company Profile Section ========== -->
    <!-- Reuses the .services class for consistent padding and background styling -->
    <section class="services">
        <div class="container">
            <div class="section-header">
                <h2>Company Profile</h2>
                <!-- High-level company overview paragraph -->
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

    <!-- ========== Mission, Vision & Values Section ========== -->
    <!-- Three-part section: intro heading, mission/vision cards, and a core values grid -->
    <section class="mvv-section">
        <div class="container">

            <!-- Section intro heading and tagline -->
            <div class="mvv-intro">
                <h2>Our Foundation</h2>
                <p>Built on decades of excellence, guided by timeless principles</p>
            </div>

            <!-- Mission & Vision Cards Grid -->
            <!-- Two-column grid on desktop; stacks to single column on mobile -->
            <div class="mvv-grid">

                <!-- Mission Card -->
                <!-- Gold top border distinguishes it visually from the vision card -->
                <div class="mvv-card mission-card">
                    <div class="mvv-icon">🎯</div>
                    <h3>Mission</h3>
                    <p>To empower businesses with strategic insights and cutting-edge technology
                        solutions that drive transformative growth and create lasting value.</p>
                </div>

                <!-- Vision Card -->
                <!-- Navy top border used as a visual counterpart to the mission card -->
                <div class="mvv-card vision-card">
                    <div class="mvv-icon">✨</div>
                    <h3>Vision</h3>
                    <p>To be the preferred partner for organizations seeking innovative and
                        impactful management and ICT consulting services.</p>
                </div>

            </div>

            <!-- Core Values Grid -->
            <!-- Displays five company values in a numbered card layout -->
            <div class="values-section">
                <h3>Core Values</h3>

                <!-- Three-column grid on desktop; collapses to one column on mobile -->
                <div class="values-grid">

                    <!-- Value 01: Client Focus -->
                    <div class="value-item">
                        <div class="value-number">01</div>
                        <h4>Client Focus</h4>
                        <p>We prioritize our clients' needs and strive to exceed their
                            expectations.</p>
                    </div>

                    <!-- Value 02: Integrity -->
                    <div class="value-item">
                        <div class="value-number">02</div>
                        <h4>Integrity</h4>
                        <!-- Note: "all our1" appears to be a typo — should likely read "all our" -->
                        <p>We adhere to the highest ethical standards in all our
                            interactions.</p>
                    </div>

                    <!-- Value 03: Innovation -->
                    <div class="value-item">
                        <div class="value-number">03</div>
                        <h4>Innovation</h4>
                        <p>We embrace creativity and continuously seek new and better
                            ways to serve our clients.</p>
                    </div>

                    <!-- Value 04: Excellence -->
                    <div class="value-item">
                        <div class="value-number">04</div>
                        <h4>Excellence</h4>
                        <p>We are committed to delivering exceptional quality in our
                            services.</p>
                    </div>

                    <!-- Value 05: Collaboration -->
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

    <!-- ========== Footer ========== -->
    <!-- Reusable footer component containing address, links, social icons, and copyright -->
    <FooterView />
</template>

<script>
// Importing reusable layout components
import NavBar from '../components/NavBar.vue'
import FooterView from '../components/FooterView.vue'

export default {
    name: 'AboutView', // Identifies this page component in Vue DevTools
    components: { NavBar, FooterView }, // Registers both components for use in this template
}
</script>

<style scoped>
/* =============================================
   HERO SECTION
   Full-viewport-height banner with a dark
   gradient overlay on top of a background image.
   padding-top offsets the fixed navbar height.
   ============================================= */
.hero {
    min-height: 70vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy-light) 100%);
    /* Fallback if image fails to load */
    position: relative;
    overflow: hidden;
    padding-top: 80px;
    /* Prevents content from sitting behind the fixed navbar */
}

/* Constrains and centers the hero text; entrance animation applied here */
.hero-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 24px;
    color: var(--white);
    animation: fadeInUp 0.8s ease-out;
    /* Assumes fadeInUp keyframes are defined globally */
}

/* Large display heading size for strong visual impact */
.hero h1 {
    font-size: 72px;
    line-height: 1.1;
    margin-bottom: 24px;
}

/* display:block forces the highlighted text to occupy its own line */
.hero .highlight {
    color: var(--gold);
    display: block;
}

/* Subtitle/descriptor text; constrained width for readability */
.hero p {
    font-size: 24px;
    margin-bottom: 40px;
    max-width: 700px;
    opacity: 0.9;
}

/* Flex container for hero CTA buttons — currently unused on this page but available */
.hero-buttons {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
}

/* Background image with a two-stop dark overlay to ensure text legibility.
   The left side is nearly opaque (0.95) and lightens slightly toward the right (0.7) */
.hero-img {
    background-image: linear-gradient(to right, rgba(26, 35, 50, 0.95), rgba(26, 35, 50, 0.7)), url('../assets/about.jpg');
    background-size: cover;
    background-position: center;
}


/* =============================================
   COMPANY PROFILE SECTION
   Reuses the .services class to maintain
   consistent spacing and background color
   across different content sections.
   ============================================= */
.services {
    padding: 100px 24px;
    background: var(--gray-light);
}

/* Shared container utility; centers and constrains content width site-wide */
.container {
    max-width: 1200px;
    margin: 0 auto;
}

/* Centered section heading block used across multiple sections */
.section-header {
    text-align: center;
    margin-bottom: 64px;
}


/* =============================================
   MISSION, VISION & VALUES SECTION
   Subtle top-to-bottom gradient background
   that transitions from white to light gray,
   separating it visually from adjacent sections.
   ============================================= */
.mvv-section {
    padding: 100px 24px;
    background: linear-gradient(180deg, var(--white) 0%, var(--gray-light) 100%);
}

/* Centered intro text above the mission/vision cards */
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

/* Two-column grid for mission and vision cards; collapses on mobile */
.mvv-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 32px;
    margin-bottom: 100px;
    /* Creates clear separation between cards and the values grid below */
}

/* Shared card styles: white surface with rounded corners and a lift-on-hover effect */
.mvv-card {
    background: var(--white);
    padding: 48px;
    border-radius: 20px;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.08);
    /* Soft ambient shadow at rest */
    transition: transform 0.3s, box-shadow 0.3s;
}

/* Hover state: card lifts and shadow deepens for depth */
.mvv-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 20px 60px rgba(0, 0, 0, 0.12);
}

/* Emoji icon sized up to act as a visual anchor for each card */
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

/* Gold top border visually ties the mission card to the brand's primary accent color */
.mission-card {
    border-top: 4px solid var(--gold);
}

/* Navy top border provides a complementary contrast to the mission card */
.vision-card {
    border-top: 4px solid var(--navy);
}


/* =============================================
   CORE VALUES GRID
   Five value cards arranged in a 3-column grid.
   Uses numbered labels and a gold border hover
   state for interactive feedback.
   ============================================= */
.values-section {
    text-align: center;
}

/* Section heading directly inside .values-section, not nested deeper */
.values-section>h3 {
    font-size: 42px;
    color: var(--navy);
    margin-bottom: 64px;
}

/* Three-column grid; collapses to one column on mobile via the media query below */
.values-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 40px;
}

/* Individual value card: left-aligned text on a white background */
.value-item {
    text-align: left;
    padding: 32px;
    background: var(--white);
    border-radius: 16px;
    transition: all 0.3s;
    border: 2px solid transparent;
    /* Transparent by default; animates to gold on hover */
}

/* Hover state: gold border appears, card lifts, and a warm gold-tinted shadow renders */
.value-item:hover {
    border-color: var(--gold);
    transform: translateY(-4px);
    box-shadow: 0 10px 30px rgba(212, 175, 55, 0.2);
}

/* Numbered label styled small and spaced for a refined, editorial look */
.value-number {
    font-size: 14px;
    font-weight: 700;
    color: var(--gold);
    margin-bottom: 16px;
    letter-spacing: 2px;
    /* Wide tracking gives the number a stylized label appearance */
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


/* =============================================
   RESPONSIVE BREAKPOINT — MOBILE
   At 480px and below, multi-column grids
   collapse to a single column for readability
   on small screens.
   ============================================= */
@media (max-width: 480px) {

    /* Mission/Vision cards stack vertically */
    .mvv-grid {
        grid-template-columns: 1fr;
    }

    /* Core value cards stack vertically */
    .values-grid {
        grid-template-columns: 1fr;
    }
}
</style>