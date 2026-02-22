<template>
    <!-- ========== CTA (Call-to-Action) Section ========== -->
    <!-- Encourages visitors to take action by scheduling a consultation -->
    <section class="cta" id="contact">
        <div class="container">
            <!-- Section headline -->
            <h2>Ready to Transform Your Business?</h2>

            <!-- Supporting description text -->
            <p>Let's discuss how our proven methodologies can drive measurable results for your organization. Schedule a
                complimentary consultation today.</p>

            <!-- Button group; currently contains one primary CTA button -->
            <div class="cta-buttons">
                <!-- Triggers goContact() method to navigate to the contact/consultation page -->
                <button @click="goContact()" class="btn btn-primary">Schedule Consultation →</button>
            </div>
        </div>
    </section>

    <!-- ========== Footer ========== -->
    <!-- Site-wide footer containing office info, navigation links, social media, and copyright -->
    <footer>
        <div class="container">

            <!-- Office Address Row -->
            <!-- Displays physical location and contact email -->
            <div class="row footer-row">
                <div class="col-12">
                    <h5 class="footer-heading">Our Office</h5>
                    <!-- Physical office address -->
                    <p><i class="bi bi-geo-alt-fill me-2"></i>Plot 13A Wada Nas Street, Guzape. Federal Capital Territory, Nigeria</p>
                    <!-- Contact email address -->
                    <p><i class="bi bi-envelope-fill me-2"></i>info@provenperformanceltd.com</p>
                </div>
            </div>

            <!-- Quick Links Row -->
            <!-- Internal navigation links for easy access to key site pages -->
            <div class="row footer-row">
                <div class="col-12">
                    <h5 class="footer-heading">Quick Links</h5>
                    <!-- Links are split across 3 columns on medium screens, 2 on small -->
                    <div class="row">
                        <div class="col-md-4 col-6">
                            <a href="/about">About Us</a>
                        </div>
                        <div class="col-md-4 col-6">
                            <a href="/services">Services</a>
                        </div>
                        <div class="col-md-4 col-6">
                            <a href="/contact">Contact</a>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Social Media Row -->
            <!-- External social platform links; hrefs should be updated with actual profile URLs -->
            <div class="row footer-row">
                <div class="col-12">
                    <h5 class="footer-heading">Follow Us</h5>
                    <div class="social-icons">
                        <!-- aria-label attributes improve accessibility for screen readers -->
                        <a href="#" aria-label="Facebook"><i class="bi bi-facebook"></i></a>
                        <a href="#" aria-label="Twitter"><i class="bi bi-twitter"></i></a>
                        <a href="#" aria-label="LinkedIn"><i class="bi bi-linkedin"></i></a>
                        <a href="#" aria-label="Instagram"><i class="bi bi-instagram"></i></a>
                        <a href="#" aria-label="YouTube"><i class="bi bi-youtube"></i></a>
                    </div>
                </div>
            </div>

            <!-- Copyright Row -->
            <!-- Legal ownership notice and brand tagline -->
            <div class="row">
                <div class="col-12">
                    <!-- Divider line separating footer content from copyright notice -->
                    <hr class="footer-divider">
                    <!-- Copyright notice; update year annually or make it dynamic -->
                    <p class="copyright-text">© 2025 Proven Performance Ltd. All rights reserved.</p>
                    <!-- Brand tagline -->
                    <p class="copyright">Transforming businesses worldwide</p>
                </div>
            </div>

        </div>
    </footer>
</template>

<script>
export default {
    name: 'FooterView', // Registers the component under this name for Vue DevTools and parent references

    methods: {
        /**
         * goContact()
         * Programmatically navigates the user to the /contact page
         * using Vue Router's push method. Called when the CTA button is clicked.
         */
        goContact() {
            this.$router.push({ path: `/contact` })
        }
    }
}
</script>

<style>
/* =============================================
   CTA SECTION
   Full-width banner with gradient background
   designed to prompt user action
   ============================================= */
.cta {
    padding: 100px 24px; /* Generous vertical padding for visual impact */
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy-light) 100%); /* Diagonal gradient using brand colors */
    text-align: center;
    color: var(--white);
}

/* CTA headline */
.cta h2 {
    font-size: 48px;
    margin-bottom: 24px;
}

/* CTA supporting text; constrained width for readability */
.cta p {
    font-size: 20px;
    margin-bottom: 40px;
    opacity: 0.9; /* Slightly transparent to soften against the dark background */
    max-width: 800px;
    margin-left: auto;
    margin-right: auto; /* Centers the paragraph block */
}

/* Flex container for CTA buttons; wraps on smaller screens */
.cta-buttons {
    display: flex;
    gap: 16px;
    justify-content: center;
    flex-wrap: wrap; /* Allows buttons to stack on narrow viewports */
}


/* =============================================
   FOOTER
   Dark navy background with white text;
   structured in rows using Bootstrap grid
   ============================================= */
footer {
    background: var(--navy);
    color: var(--white);
    padding: 60px 24px 30px; /* More padding at the top than bottom */
}

/* Constrains footer content to consistent max-width */
footer .container {
    max-width: 1200px;
}

/* Shared row styling; adds spacing between footer sections and centers content */
.footer-row {
    margin-bottom: 40px;
    text-align: center;
}

/* Section heading inside footer rows; uses brand gold color for visual hierarchy */
.footer-heading {
    font-size: 20px;
    font-weight: 600;
    margin-bottom: 20px;
    color: var(--gold);
}

/* General paragraph spacing within the footer */
footer p {
    margin-bottom: 8px;
    opacity: 0.9;
}


/* =============================================
   QUICK LINKS
   Footer navigation links styled white
   with a gold hover state
   ============================================= */
.footer-row a {
    color: var(--white);
    text-decoration: none;
    opacity: 0.9;
    transition: all 0.3s; /* Smooth color/opacity transition on hover */
    display: inline-block;
    margin-bottom: 10px;
}

/* Hover state: highlights link in gold and restores full opacity */
.footer-row a:hover {
    color: var(--gold);
    opacity: 1;
}


/* =============================================
   SOCIAL MEDIA ICONS
   Circular icon buttons arranged in a flex row;
   styled with a subtle background that fills
   with gold on hover
   ============================================= */
.social-icons {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap; /* Wraps icons on very small screens */
}

/* Individual icon container: fixed size circular button */
.social-icons a {
    width: 45px;
    height: 45px;
    background: rgba(255, 255, 255, 0.1); /* Translucent white base */
    border-radius: 50%; /* Makes the container a circle */
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 20px;
    transition: all 0.3s;
}

/* Hover state: fills background with gold, flips icon to navy, and lifts the button */
.social-icons a:hover {
    background: var(--gold);
    color: var(--navy);
    transform: translateY(-3px); /* Subtle lift effect */
}


/* =============================================
   COPYRIGHT SECTION
   Sits below a divider at the bottom of the footer
   ============================================= */

/* Horizontal rule used as a visual separator; subtle opacity to blend with dark background */
.footer-divider {
    border-color: rgba(255, 255, 255, 0.2);
    margin: 30px 0 20px;
}

/* Primary copyright line; slightly bolder for emphasis */
.copyright-text {
    margin-bottom: 8px;
    font-weight: 500;
    text-align: center;
}

/* Brand tagline below copyright; reduced opacity and size for hierarchy */
footer .copyright {
    opacity: 0.7;
    font-size: 14px;
    margin-bottom: 0;
    text-align: center;
}
</style>