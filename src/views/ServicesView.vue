<template>
    <!-- ========== Site Navigation ========== -->
    <!-- Reusable navbar component fixed to the top of the viewport -->
    <NavBar />

    <!-- ========== Hero Section ========== -->
    <!-- Page banner with a dark gradient background.
         id="home" enables anchor linking to this section.
         hero-img applies the background image overlay defined in the styles.
         Text is center-aligned here, unlike the left-aligned heroes on other pages -->
    <section class="hero hero-img" id="home">
        <div class="">
            <div class="hero-content">
                <!-- Plain heading with no highlight span; centered via .hero-content text-align -->
                <h1>Our Services</h1>
                <!-- Subtitle describing the breadth of services offered -->
                <p>Comprehensive consulting solutions designed to transform your business and drive
                    sustainable competitive advantage</p>
            </div>
        </div>
    </section>

    <!-- ========== Services Detail Section ========== -->
    <!-- Three service blocks stacked vertically. Each block is a two-column grid
         with content on one side and an impact stats panel on the other.
         Even-numbered blocks flip their column order using direction:rtl -->
    <section class="services-detail">
        <div class="container">

            <!-- ── Service Block 1: Management Consulting ── -->
            <!-- Odd block: content left, stats panel right -->
            <div class="service-detail">

                <!-- Left column: heading, description, feature list, and CTA link -->
                <div class="service-content">
                    <h2>Management Consulting</h2>
                    <!-- Intro paragraph; note this copy references digital transformation
                         which may be better suited to an ICT Consulting block -->
                    <p>Accelerate your digital journey with comprehensive transformation programs that modernize operations,
                        and enhance customer experiences.</p>

                    <!-- Feature list; → arrow bullets injected via CSS ::before pseudo-element -->
                    <ul class="service-features">
                        <li>Defining clear and actionable strategies for growth and market leadership</li>
                        <li>Implementing systems to track and improve performance</li>
                        <li>Optimizing business processes and improving efficiency</li>
                        <li>Planning, executing, and controlling projects to achieve specific objectives</li>
                        <li>Guiding organizations through successful transformations</li>
                        <li>Developing strategies to attract, retain, and develop talent</li>
                    </ul>

                    <!-- CTA routes to the contact page for enquiries about this service -->
                    <a href="/contact" class="btn btn-primary">Learn More →</a>
                </div>

                <!-- Right column: impact statistics displayed in a light gray card -->
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

            <!-- ── Service Block 2: Training ── -->
            <!-- Even block: direction:rtl flips column order so the stats panel
                 appears on the left and content on the right for visual variety.
                 direction:ltr is restored on child elements to keep text readable -->
            <div class="service-detail">

                <div class="service-content">
                    <h2>Training</h2>
                    <p>Build high-performing organizations through strategic workforce planning, leadership development, and
                        culture transformation initiatives that drive sustainable business results.</p>

                    <ul class="service-features">
                        <!-- Leadership development program -->
                        <li>Cultivate effective leaders at all levels with programs focusing on strategic thinking,
                            communication, team building, and change management</li>
                        <!-- Project management training (PRINCE2, Agile) -->
                        <li>Equip your project teams with the skills to plan, execute, and deliver projects successfully
                            using industry best practices like PRINCE2 and Agile methodologies. Offerings range from
                            foundational project management to advanced program management</li>
                        <!-- Change management training -->
                        <li>Prepare your organization for successful transformations by training your team on change
                            management principles and techniques, minimizing disruption and maximizing adoption</li>
                        <!-- Process optimization training (Lean, Six Sigma) -->
                        <li>Improve efficiency and productivity through training in process optimization, Lean principles,
                            Six Sigma methodologies, and performance management</li>
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

            <!-- ── Service Block 3: Strategy & Growth ── -->
            <!-- Odd block: content left, stats panel right (same layout as block 1) -->
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

    <!-- ========== Footer ========== -->
    <!-- Reusable footer component with address, links, social icons, and copyright -->
    <FooterView />
</template>

<script>
// Importing reusable layout components
import NavBar from '../components/NavBar.vue'
import FooterView from '../components/FooterView.vue'

export default {
    name: 'ServicesView', // Identifies this page component in Vue DevTools
    components: { NavBar, FooterView }, // Registers both components for use in this template
}
</script>

<style scoped>
/* =============================================
   HERO SECTION
   Slightly shorter than other page heroes
   (60vh vs 70vh) since this is a content-heavy
   page and the detail section should appear
   sooner. padding-top offsets the fixed navbar.
   ============================================= */
.hero {
    min-height: 60vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy-light) 100%); /* Fallback if image fails */
    position: relative;
    overflow: hidden;
    padding-top: 80px; /* Clears the fixed navbar */
}

/* Hero content is center-aligned on this page, unlike left-aligned heroes elsewhere */
.hero-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 24px;
    color: var(--white);
    animation: fadeInUp 0.8s ease-out; /* Assumes fadeInUp keyframes are defined globally */
    text-align: center;
}

.hero h1 {
    font-size: 60px; /* Slightly smaller than the 72px used on other pages */
    line-height: 1.1;
    margin-bottom: 24px;
}

/* Defined but not used in this template's hero heading; kept for consistency */
.hero .highlight {
    color: var(--gold);
    display: block;
}

/* Subtitle constrained to a comfortable reading width and centered via the parent */
.hero p {
    font-size: 20px;
    margin-bottom: 40px;
    max-width: 700px;
    opacity: 0.9;
}

/* Hero button row defined but not used on this page; kept for structural consistency */
.hero-buttons {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
}


/* =============================================
   SERVICES DETAIL SECTION
   Outer section wrapper with generous vertical
   padding to give each service block room.
   ============================================= */
.services-detail {
    padding: 100px 24px;
}

/* Shared container utility; constrains and centers content site-wide */
.container {
    max-width: 1200px;
    margin: 0 auto;
}

/* Individual service block: two-column grid with text on one side and stats on the other.
   Large bottom margin creates clear visual separation between blocks */
.service-detail {
    margin-bottom: 120px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 64px;
    align-items: center;
}

/* Removes the bottom margin from the last service block to avoid excess whitespace
   before the footer */
.service-detail:last-child {
    margin-bottom: 0;
}

/* Alternating layout trick: applying direction:rtl on even blocks visually flips the
   column order (stats panel moves left, content moves right) without changing the HTML.
   This creates a zigzag reading pattern down the page */
.service-detail:nth-child(even) {
    direction: rtl;
}

/* Restores normal left-to-right text direction for all children of flipped blocks,
   so headings, paragraphs, and lists still read correctly */
.service-detail:nth-child(even) > * {
    direction: ltr;
}

/* Service block heading */
.service-content h2 {
    font-size: 42px;
    margin-bottom: 24px;
    color: var(--navy);
}

/* Intro paragraph with comfortable line height for longer copy */
.service-content p {
    font-size: 18px;
    color: var(--gray);
    margin-bottom: 32px;
    line-height: 1.8;
}

/* Feature list: default bullets replaced with a gold → arrow via ::before */
.service-features {
    list-style: none;
    margin-bottom: 32px;
}

.service-features li {
    display: flex;
    align-items: start; /* Aligns arrow to the top of multi-line list items */
    gap: 12px;
    margin-bottom: 16px;
    font-size: 16px;
    color: var(--gray-dark);
}

/* Gold arrow injected before each feature item; flex-shrink:0 keeps it from compressing */
.service-features li::before {
    content: "→";
    color: var(--gold);
    font-weight: bold;
    font-size: 20px;
    flex-shrink: 0;
}

/* Stats panel: light gray card with rounded corners sitting alongside the text content.
   min-height ensures it has visual weight even when stat count varies */
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

/* "Impact Delivered" label above the stat numbers */
.service-image h3 {
    font-size: 24px;
    color: var(--navy);
    margin-bottom: 24px;
}

/* Individual stat entry: large number above a descriptive label */
.service-stat {
    margin-bottom: 24px;
}

/* Large gold number for strong visual impact */
.service-stat-number {
    font-size: 48px;
    font-weight: 700;
    color: var(--gold);
    margin-bottom: 8px;
}

/* Smaller gray descriptor beneath each stat number */
.service-stat-label {
    font-size: 16px;
    color: var(--gray);
}


/* =============================================
   RESPONSIVE BREAKPOINT — TABLET & BELOW
   At 768px and below, two-column service blocks
   collapse to a single column and the rtl column
   flip is disabled so content always reads
   top-to-bottom naturally on mobile.
   ============================================= */
@media (max-width: 768px) {

    /* Collapses the two-column grid to a single column */
    .service-detail {
        grid-template-columns: 1fr;
        gap: 40px;
        margin-bottom: 80px; /* Reduced spacing between stacked blocks on mobile */
    }

    /* Disables the direction:rtl flip on even blocks so layout stays consistent */
    .service-detail:nth-child(even) {
        direction: ltr;
    }

    /* Scales down service headings to fit narrow screens */
    .service-content h2 {
        font-size: 32px;
    }

    /* CTA button expands to full width on mobile for easier tapping */
    .btn {
        width: 100%;
    }
}
</style>