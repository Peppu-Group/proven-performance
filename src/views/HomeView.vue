<template>
    <!-- ========== Site Navigation ========== -->
    <!-- Reusable navbar component fixed to the top of the viewport -->
    <NavBar />

    <!-- ========== Hero Section ========== -->
    <!-- Full-viewport-height banner with a background image overlay.
         id="home" allows anchor links to scroll here directly.
         hero-img applies the background image with a dark gradient overlay -->
    <section class="hero hero-img" id="home">
        <div class="">
            <div class="hero-content">
                <!-- Two-line heading: plain text on line one, gold highlight on line two -->
                <h1>
                    Transform Strategy Into
                    <span class="highlight">Measurable Results</span>
                </h1>
                <!-- Supporting value proposition subtitle -->
                <p>Partner with industry-leading consultants who drive sustainable growth through data-driven insights
                    and
                    proven methodologies.</p>
                <!-- Two CTA buttons: primary action navigates to contact, secondary to about -->
                <div class="hero-buttons">
                    <button @click="goContact()" class="btn btn-primary">Start Your Transformation →</button>
                    <button @click="goAbout()" class="btn btn-outline">Our Approach</button>
                </div>
            </div>
        </div>
    </section>

    <!-- ========== Services Section ========== -->
    <!-- Four service cards in a responsive auto-fit grid.
         id="services" allows direct anchor navigation from other pages -->
    <section class="services" id="services">
        <div class="container">
            <div class="section-header">
                <h2>Our Expertise</h2>
                <p>Comprehensive solutions tailored to your unique challenges and opportunities</p>
            </div>

            <!-- Auto-fit grid: cards expand to fill space, minimum 250px wide each -->
            <div class="services-grid">

                <!-- Service Card 1: Management Consulting -->
                <div class="service-card">
                    <h3>Management Consulting</h3>
                    <p>Develop winning strategies to attract, retain, and develop talent. Optimize business processes
                        and
                        improve efficiency</p>
                </div>

                <!-- Service Card 2: ICT Consulting -->
                <div class="service-card">
                    <h3>ICT Consulting</h3>
                    <p>Align IT with business objectives. Build and implement custom software solutions and robust
                        IT infrastructure.</p>
                </div>

                <!-- Service Card 3: Training -->
                <div class="service-card">
                    <h3>Training</h3>
                    <p>Create customized training solutions for teams. Equip project teams with the skills to plan,
                        execute, and deliver projects successfully using industry best practices</p>
                </div>

                <!-- Service Card 4: Performance Optimization -->
                <div class="service-card">
                    <h3>Performance Optimization</h3>
                    <p>Maximize operational efficiency and profitability through data-driven process improvement.</p>
                </div>

            </div>
        </div>
    </section>

    <!-- ========== Why Choose Us Section ========== -->
    <!-- Two-column layout: benefit list on the left, image on the right.
         id="results" on the image column allows anchor linking to this area -->
    <section class="why-us">
        <div class="container">
            <div class="why-us-content">

                <!-- Left: Heading, intro text, and bulleted benefit list -->
                <div class="why-us-text">
                    <h2>
                        Why Leading Organizations
                        <span class="highlight">Choose Us</span>
                    </h2>
                    <p>We combine deep industry knowledge with innovative thinking to deliver transformative results
                        that
                        stand the test of time.</p>
                    <!-- ✓ checkmark bullets are injected via CSS ::before pseudo-element -->
                    <ul class="benefits">
                        <li>Proven track record across successful engagements</li>
                        <li>Global (exposure) presence with local market insights</li>
                        <li>Proprietary/open-source frameworks backed by extensive research</li>
                        <li>Dedicated teams committed to your long-term success</li>
                        <li>Measurable ROI with clear, actionable deliverables</li>
                        <!-- NOTE: This bullet duplicates "Global presence with local market insights" above -->
                        <li>Global presence with local market insights</li>
                    </ul>
                </div>

                <!-- Right: Supporting image inside the styled stats-box container -->
                <!-- stats-box retains its navy gradient background style even though it
                     now holds an image instead of stat numbers; consider renaming the class -->
                <div class="stats-box" id="results">
                    <img src="../assets/why-us.jpg" class="img-fluid w-100" alt="Responsive image" />
                </div>

            </div>
        </div>
    </section>

    <!-- ========== Working With Us Section ========== -->
    <!-- Single clickable card that acts as a CTA to the contact page.
         Reuses the .services class for consistent background and padding -->
    <section class="services">
        <div class="container">
            <div class="section-header">
                <h2>Working with Us is Simple</h2>
            </div>

            <div class="services-grid">
                <!-- Clickable card: .clickme sets cursor:pointer; @click routes to /contact -->
                <div class="service-card clickme" @click="goContact()">
                    <div class="service-icon">📩</div>
                    <h3>Schedule a Consultation</h3>
                    <p>Develop winning strategies that drive sustainable competitive advantage and accelerate market
                        leadership.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ========== Our Offering Section ========== -->
    <!-- Two-column layout mirroring the Why Choose Us section but with
         the image on the left and text on the right for visual variety -->
    <section class="why-us">
        <div class="container">
            <div class="why-us-content">

                <!-- Left: Supporting team image -->
                <div class="">
                    <img src="../assets/team.jpg" class="img-fluid w-100" alt="Responsive image" />
                </div>

                <!-- Right: Methodology heading and step-by-step benefit list -->
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
                        <li>Measuring the impact of our solutions and ensuring client satisfaction</li>
                    </ul>
                </div>

            </div>
        </div>
    </section>

    <!-- ========== Clients Carousel (Commented Out) ========== -->
    <!-- This Bootstrap carousel section is intentionally disabled because
         client assets are not yet available. Uncomment and populate
         src attributes with real client logos when ready.
         The surrounding CSS for .clients and #clientsCarousel is kept
         in the styles so it's ready to use without rework. -->
    <!--
    <section class="clients" id="clients">
        ...
    </section>
    -->

    <!-- ========== Footer ========== -->
    <!-- Reusable footer component with address, links, social icons, and copyright -->
    <FooterView />
</template>

<script>
// Importing reusable layout components
import NavBar from '../components/NavBar.vue'
import FooterView from '../components/FooterView.vue'

export default {
    name: 'HomeView', // Identifies this page in Vue DevTools
    components: { NavBar, FooterView }, // Registers both components for use in this template

    data() {
        return {
            // Tracks mobile menu open/close state.
            // NOTE: mobileMenuOpen is defined here but not currently wired to any
            // toggle logic in this template — the NavBar component handles its own menu.
            mobileMenuOpen: false,
        }
    },

    methods: {
        /**
         * goAbout()
         * Navigates the user to the About page via Vue Router.
         * Triggered by the "Our Approach" outline button in the hero section.
         */
        goAbout() {
            this.$router.push({ path: `/about` })
        },

        /**
         * goContact()
         * Navigates the user to the Contact page via Vue Router.
         * Triggered by the hero CTA button and the "Schedule a Consultation" card.
         */
        goContact() {
            this.$router.push({ path: `/contact` })
        }
    }
}
</script>

<style scoped>
/* =============================================
   SHARED BUTTON STYLES
   Base .btn class shared by both .btn-primary
   (defined globally) and .btn-outline (defined here).
   ============================================= */
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

/* Outline variant: white border and text on the dark hero background;
   fills solid white and flips to navy on hover */
.btn-outline {
    border: 2px solid var(--white);
    color: var(--white);
}

.btn-outline:hover {
    background: var(--white);
    color: var(--navy);
}

/* Legacy mobile menu toggle; nav is now handled by the NavBar component */
.mobile-menu {
    display: none;
    font-size: 24px;
    cursor: pointer;
    color: var(--navy);
}


/* =============================================
   HERO SECTION
   Full-viewport-height banner. padding-top
   offsets the fixed navbar. Background image
   applied via .hero-img class below.
   ============================================= */
.hero {
    min-height: 100vh;
    /* Full screen height; taller than inner page heroes (70vh) */
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy-light) 100%);
    /* Fallback if image fails */
    position: relative;
    overflow: hidden;
    padding-top: 80px;
    /* Clears the fixed navbar */
}

/* Constrains and centers hero content; fadeInUp defined in @keyframes below */
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

/* display:block forces the gold span onto its own line below the first line of text */
.hero .highlight {
    color: var(--gold);
    display: block;
}

/* Subtitle text constrained to a comfortable reading width */
.hero p {
    font-size: 24px;
    margin-bottom: 40px;
    max-width: 700px;
    opacity: 0.9;
}

/* Flex row for CTA buttons; wraps to column on mobile via the media query below */
.hero-buttons {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
}

/* Background image with a two-stop dark overlay ensuring text legibility.
   Left side nearly opaque, right side slightly lighter for depth */
.hero-img {
    background-image: linear-gradient(to right, rgba(26, 35, 50, 0.95), rgba(26, 35, 50, 0.7)), url('../assets/hero.jpg');
    background-size: cover;
    background-position: center;
}


/* =============================================
   SERVICES SECTION
   Reused for both the "Our Expertise" and
   "Working With Us" sections for consistent
   padding and gray background.
   ============================================= */
.services {
    padding: 100px 24px;
    background: var(--gray-light);
}

/* Shared container utility across all sections */
.container {
    max-width: 1200px;
    margin: 0 auto;
}

/* Centered section title and subtitle block */
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

/* Responsive auto-fit grid: cards fill available space, minimum 250px each.
   Automatically reflows from 4 columns down to 1 as the viewport narrows */
.services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 32px;
}

/* Applied to the "Schedule a Consultation" card to indicate it's clickable */
.clickme {
    cursor: pointer;
}

/* White card with rounded corners and a lift-on-hover effect */
.service-card {
    background: var(--white);
    padding: 40px;
    border-radius: 12px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
    transition: all 0.3s;
}

/* Hover: card lifts and shadow deepens to create a raised appearance */
.service-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 12px 40px rgba(0, 0, 0, 0.15);
}

/* Gold-tinted square icon container above the card title */
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


/* =============================================
   WHY CHOOSE US / OUR OFFERING SECTIONS
   Reused for both two-column sections.
   align-items:center keeps columns vertically
   centered regardless of height difference.
   ============================================= */
.why-us {
    padding: 100px 24px;
}

/* Two equal columns side by side; collapses to one column on mobile */
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

/* display:block pushes the gold highlight onto its own line */
.why-us .highlight {
    color: var(--gold);
    display: block;
}

.why-us-text p {
    font-size: 18px;
    color: var(--gray);
    margin-bottom: 32px;
}

/* Custom bulleted list; default list-style replaced with a gold ✓ via ::before */
.benefits {
    list-style: none;
}

.benefits li {
    display: flex;
    gap: 12px;
    margin-bottom: 16px;
    color: var(--gray-dark);
}

/* Gold checkmark injected before each list item via CSS pseudo-element */
.benefits li::before {
    content: "✓";
    color: var(--gold);
    font-weight: bold;
    font-size: 20px;
    flex-shrink: 0;
    /* Prevents the checkmark from compressing on narrow widths */
}

/* Stats box: originally designed to hold stat numbers, now repurposed as an image container.
   Consider renaming this class to something like .image-box for clarity */
.stats-box {
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy-light) 100%);
    padding: 64px;
    border-radius: 16px;
    color: var(--white);
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.15);
}

/* Stat number and label styles kept for potential future use if stats are reintroduced */
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


/* =============================================
   CLIENTS SECTION & CAROUSEL STYLES
   Kept intact even though the section is
   commented out in the template, so no rework
   is needed when client logos become available.
   ============================================= */
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

/* Constrains carousel width and centers it within the section */
#clientsCarousel {
    max-width: 800px;
    margin: 0 auto;
}

/* Centers logo images vertically and horizontally within each carousel slide */
.client-logo-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 60px 40px;
    min-height: 300px;
}

/* Logos are desaturated and dimmed when not active; maintains visual consistency */
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

/* Active slide logo: full color and full opacity */
.carousel-item.active .client-logo-wrapper img {
    filter: grayscale(0%);
    opacity: 1;
}

/* Circular prev/next control buttons positioned outside the carousel track */
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
    /* Sits to the left of the carousel track */
}

.carousel-control-next {
    right: -80px;
    /* Sits to the right of the carousel track */
}

/* Hover: controls fill gold for brand consistency */
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

/* Dot indicators pushed below the carousel; gold dot marks the active slide */
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


/* =============================================
   ENTRANCE ANIMATION
   Used by .hero-content to slide and fade in
   on page load. Referenced globally so other
   components (about, contact heroes) can also
   use it without redefining it.
   ============================================= */
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
        /* Starts 30px below its final position */
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}


/* =============================================
   RESPONSIVE BREAKPOINTS
   ============================================= */

/* Tablet and below (768px): collapse two-column layouts, scale down typography,
   stack hero CTA buttons, and hide legacy nav classes */
@media (max-width: 768px) {

    /* These footer classes are scoped to FooterView; these rules may have no
       effect here and could be moved or removed to avoid confusion */
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

    /* Legacy class from a non-Vue version; not present in this template */
    .nav-links {
        display: none;
    }

    /* Legacy class; mobile menu is now handled inside NavBar component */
    .mobile-menu {
        display: block;
    }

    /* Scales down hero heading and subtitle on smaller screens */
    .hero h1 {
        font-size: 40px;
    }

    .hero p {
        font-size: 18px;
    }

    .section-header h2 {
        font-size: 36px;
    }

    /* Why Us and Our Offering two-column grids collapse to single column */
    .why-us-content {
        grid-template-columns: 1fr;
    }

    /* Hero and footer CTA buttons stack vertically and expand to full width */
    .hero-buttons,
    .cta-buttons {
        flex-direction: column;
    }

    .btn {
        width: 100%;
        text-align: center;
    }

    /* Carousel adjustments for mobile: reduce logo size and move controls inside the track */
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

    /* Moves controls inside the carousel frame on mobile since -80px would clip off-screen */
    .carousel-control-prev {
        left: 10px;
    }

    .carousel-control-next {
        right: 10px;
    }
}
</style>