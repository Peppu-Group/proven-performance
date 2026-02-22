<template>
    <!-- ========== Site Navigation ========== -->
    <!-- Reusable navbar component fixed to the top of the viewport -->
    <NavBar />

    <!-- ========== Hero Section ========== -->
    <!-- Page banner with a dark gradient background and an id of "home" for anchor linking.
         hero-img applies the background image overlay defined in the styles -->
    <section class="hero hero-img" id="home">
        <div class="">
            <div class="hero-content">
                <h1>
                    <!-- Gold-highlighted page title; display:block forces it onto its own line -->
                    <span class="highlight">Get In Touch</span>
                </h1>
                <!-- Supporting subtitle encouraging visitors to make contact -->
                <p>Ready to transform your business? Let's discuss how we can help you achieve your strategic goals.</p>
            </div>
        </div>
    </section>

    <!-- ========== Contact Section ========== -->
    <!-- Two-column grid layout: contact info panel on the left, contact form on the right.
         Collapses to a single column on tablet and mobile screens -->
    <section class="contact-section">

        <!-- ── Left Column: Contact Information Panel ── -->
        <!-- Dark navy card displaying all contact details and social media links -->
        <div class="contact-info">
            <h2>Let's Connect</h2>
            <p>We're here to answer your questions and discuss how we can support your business objectives.</p>

            <!-- Individual contact detail items (email, address, hours, phone) -->
            <div class="contact-details">

                <!-- Email contact item -->
                <div class="contact-item">
                    <div class="contact-icon">📧</div>
                    <div class="contact-item-content">
                        <h3>Email</h3>
                        <!-- mailto: link opens the user's default email client -->
                        <p><a href="mailto:info@provenperformanceltd.com">info@provenperformanceltd.com</a></p>
                    </div>
                </div>

                <!-- Physical office address -->
                <div class="contact-item">
                    <div class="contact-icon"> ⟟ </div>
                    <div class="contact-item-content">
                        <h3>Office</h3>
                        <p>Plot 13A Wada Nas Street, Guzape. Federal Capital Territory, Nigeria</p>
                    </div>
                </div>

                <!-- Business operating hours -->
                <div class="contact-item">
                    <div class="contact-icon">⏰</div>
                    <div class="contact-item-content">
                        <h3>Business Hours</h3>
                        <!-- <br> used to stack the two time ranges without extra markup -->
                        <p>Monday - Friday: 9:00 AM - 6:00 PM<br>Saturday - Sunday: Closed</p>
                    </div>
                </div>

                <!-- Phone contact item -->
                <div class="contact-item">
                    <div class="contact-icon">📞</div>
                    <div class="contact-item-content">
                        <h3>Call</h3>
                        <p>+234 901 911 1152</p>
                    </div>
                </div>

            </div>

            <!-- Social Media Links -->
            <!-- href values should be updated with actual profile URLs before going live.
                 aria-label attributes ensure screen readers identify each platform correctly
                 since the visible text is just a single character/symbol -->
            <div class="social-links">
                <a href="#" class="social-link" aria-label="LinkedIn">in</a>
                <a href="#" class="social-link" aria-label="Twitter">𝕏</a>
                <a href="#" class="social-link" aria-label="Facebook">f</a>
            </div>
        </div>

        <!-- ── Right Column: Contact Form ── -->
        <!-- White card containing the enquiry form.
             NOTE: @click on the <form> element should be @submit to correctly
             capture the native form submission event -->
        <div class="contact-form-container">
            <h2>Send us a Message</h2>
            <p>Fill out the form below and we'll get back to you within 24 hours.</p>

            <!-- @click should ideally be @submit for proper form event handling.
                 handleSubmit calls event.preventDefault() to stop a full page reload -->
            <form id="contactForm" @click="handleSubmit(event)">

                <!-- Name row: first and last name side by side -->
                <div class="form-row">
                    <div class="form-group">
                        <label for="firstName">First Name *</label>
                        <!-- required attribute triggers native browser validation -->
                        <input type="text" id="firstName" name="firstName" required>
                    </div>
                    <div class="form-group">
                        <label for="lastName">Last Name *</label>
                        <input type="text" id="lastName" name="lastName" required>
                    </div>
                </div>

                <!-- Contact details row: email and optional phone number -->
                <div class="form-row">
                    <div class="form-group">
                        <label for="email">Email *</label>
                        <!-- type="email" triggers native email format validation -->
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <!-- Phone is optional; no required attribute -->
                        <label for="phone">Phone</label>
                        <input type="tel" id="phone" name="phone">
                    </div>
                </div>

                <!-- Optional company name field -->
                <div class="form-group">
                    <label for="company">Company</label>
                    <input type="text" id="company" name="company">
                </div>

                <!-- Service interest dropdown -->
                <!-- Helps route or prioritize the enquiry before any server-side processing -->
                <div class="form-group">
                    <label for="service">Service Interest</label>
                    <select id="service" name="service">
                        <option value="">Select a service...</option>
                        <option value="strategic">Strategic Planning</option>
                        <option value="operations">Operations Excellence</option>
                        <option value="change">Change Management</option>
                        <option value="project">Project Management</option>
                        <option value="digital">Digital Transformation</option>
                        <option value="training">Training</option>
                        <option value="other">Other</option>
                    </select>
                </div>

                <!-- Message textarea; required and vertically resizable via CSS -->
                <div class="form-group">
                    <label for="message">Message *</label>
                    <textarea id="message" name="message" required></textarea>
                </div>

                <!-- Full-width submit button styled in brand gold -->
                <button type="submit" class="submit-button">Send Message</button>

            </form>
        </div>

    </section>

    <!-- ========== Inline Footer ========== -->
    <!-- Simplified footer used here instead of the full FooterView component;
         consider replacing with <FooterView /> for consistency across pages -->
    <footer>
        <p>&copy; 2025 Proven Performance Ltd. All rights reserved.</p>
    </footer>

</template>

<script>
// Importing the reusable navbar component
import NavBar from '../components/NavBar.vue'

export default {
    name: 'ContactView', // Identifies this page component in Vue DevTools
    components: { NavBar }, // Registers NavBar for use in this template

    methods: {
        /**
         * handleSubmit(event)
         * Intercepts the form submission to prevent a full page reload,
         * collects all form field values, logs them, alerts the user,
         * and resets the form.
         *
         * NOTE: This is currently wired to @click on the <form> element instead
         * of @submit — this should be corrected to @submit="handleSubmit($event)"
         * for reliable cross-browser behaviour and proper keyboard submission support.
         *
         * TODO: Replace console.log and alert with a real API call (e.g. fetch/axios)
         * to send form data to a backend or email service.
         */
        handleSubmit(event) {
            event.preventDefault(); // Stops the browser from reloading the page on submit

            // Collects all named form fields into a key-value object
            const formData = new FormData(event.target);
            const data = Object.fromEntries(formData);

            // Placeholder: replace with actual API call to send the data server-side
            console.log('Form submitted:', data);

            // Temporary user feedback; replace with an inline success message for better UX
            alert('Thank you for your message! We will get back to you within 24 hours.');

            // Clears all form fields after successful submission
            event.target.reset();
        }
    }
}
</script>

<style scoped>
/* =============================================
   HERO SECTION
   Reuses the same hero pattern as other pages:
   full-height banner with gradient background,
   offset by the fixed navbar height.
   ============================================= */
.hero {
    min-height: 70vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy-light) 100%); /* Fallback if bg image fails */
    position: relative;
    overflow: hidden;
    padding-top: 80px; /* Prevents content from sitting behind the fixed navbar */
}

/* Constrains and centers hero text; fadeInUp assumes global keyframe animation */
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

/* display:block makes the highlighted title occupy its own line */
.hero .highlight {
    color: var(--gold);
    display: block;
}

/* Subtitle text; constrained width for comfortable line length */
.hero p {
    font-size: 24px;
    margin-bottom: 40px;
    max-width: 700px;
    opacity: 0.9;
}

/* Flex container for CTA buttons — defined but not used on this page */
.hero-buttons {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
}


/* =============================================
   CONTACT SECTION
   Two-column grid layout: info panel left,
   form right. Collapses to one column below
   the 1024px breakpoint.
   ============================================= */
.contact-section {
    max-width: 1400px;
    margin: 0 auto;
    padding: 100px 5%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: start; /* Aligns both columns to the top rather than stretching to equal height */
}


/* =============================================
   CONTACT INFO PANEL
   Dark navy card on the left column containing
   contact details and social media links.
   height:fit-content prevents it from stretching
   to match the taller form column.
   ============================================= */
.contact-info {
    background: linear-gradient(135deg, var(--navy) 0%, #2d3e50 100%);
    padding: 60px;
    border-radius: 20px;
    color: var(--white);
    height: fit-content;
}

/* Gold heading color to stand out against the dark background */
.contact-info h2 {
    font-family: 'Playfair Display', serif;
    font-size: 36px;
    color: var(--gold);
    margin-bottom: 20px;
}

.contact-info p {
    font-size: 18px;
    margin-bottom: 40px;
    opacity: 0.9;
}

/* Vertical stack of contact items with consistent spacing */
.contact-details {
    display: flex;
    flex-direction: column;
    gap: 30px;
}

/* Each contact item: icon on the left, text content on the right */
.contact-item {
    display: flex;
    align-items: flex-start; /* Aligns icon to the top of multi-line content */
    gap: 20px;
}

/* Gold square icon container; flex-shrink:0 prevents it from compressing */
.contact-icon {
    background: var(--gold);
    color: var(--navy);
    width: 50px;
    height: 50px;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 24px;
    flex-shrink: 0;
}

/* Gold label for each contact item type (Email, Office, etc.) */
.contact-item-content h3 {
    font-size: 20px;
    color: var(--gold);
    margin-bottom: 8px;
}

/* Resets default paragraph margin so text sits flush under the label */
.contact-item-content p {
    margin: 0;
    opacity: 0.9;
}

/* Email link inherits white color; transitions to gold on hover */
.contact-item-content a {
    color: var(--white);
    text-decoration: none;
    transition: color 0.3s;
}

.contact-item-content a:hover {
    color: var(--gold);
}

/* Row of social platform icon buttons below the contact details */
.social-links {
    display: flex;
    gap: 15px;
    margin-top: 40px;
}

/* Individual social button: translucent gold background at rest */
.social-link {
    background: rgba(212, 175, 55, 0.2);
    color: var(--gold);
    width: 45px;
    height: 45px;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    font-size: 20px;
    transition: all 0.3s;
}

/* Hover state: fills solid gold, flips to navy text, and lifts the button */
.social-link:hover {
    background: var(--gold);
    color: var(--navy);
    transform: translateY(-3px);
}


/* =============================================
   CONTACT FORM CONTAINER
   White card on the right column housing
   the enquiry form fields and submit button.
   ============================================= */
.contact-form-container {
    background: var(--white);
    padding: 60px;
    border-radius: 20px;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1); /* Soft shadow lifts the card off the page */
}

.contact-form-container h2 {
    font-family: 'Playfair Display', serif;
    font-size: 36px;
    color: var(--navy);
    margin-bottom: 20px;
}

/* Direct child selector avoids accidentally targeting paragraph tags inside form fields */
.contact-form-container > p {
    color: var(--text-gray);
    margin-bottom: 40px;
    font-size: 16px;
}

/* Spacing below each label/input pair */
.form-group {
    margin-bottom: 25px;
}

/* Side-by-side two-column layout for paired fields (name, email/phone) */
.form-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 25px;
}

/* Block display ensures the label appears above its input */
label {
    display: block;
    margin-bottom: 8px;
    font-weight: 500;
    color: var(--navy);
}

/* Shared styles for all interactive form inputs */
input,
textarea,
select {
    width: 100%;
    padding: 15px;
    border: 2px solid #e0e0e0; /* Light gray default border */
    border-radius: 10px;
    font-family: 'Inter', sans-serif;
    font-size: 16px;
    transition: border-color 0.3s;
}

/* Focus state: replaces default browser outline with a gold brand-colored border */
input:focus,
textarea:focus,
select:focus {
    outline: none;
    border-color: var(--gold);
}

/* Textarea can be resized vertically only; min-height ensures adequate initial space */
textarea {
    resize: vertical;
    min-height: 150px;
}

/* Full-width gold CTA button at the bottom of the form */
.submit-button {
    background: var(--gold);
    color: var(--navy);
    border: none;
    padding: 18px 50px;
    border-radius: 10px;
    font-size: 18px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s;
    width: 100%;
    font-family: 'Inter', sans-serif;
}

/* Hover state: button lifts and a warm gold-tinted shadow appears below it */
.submit-button:hover {
    transform: translateY(-2px);
    box-shadow: 0 10px 30px rgba(212, 175, 55, 0.3);
}


/* =============================================
   INLINE FOOTER
   Minimal footer used on this page only.
   Consider replacing with <FooterView /> for
   consistency with the rest of the site.
   ============================================= */
footer {
    background: var(--navy);
    color: var(--white);
    text-align: center;
    padding: 3rem 5%;
}

footer p {
    opacity: 0.8;
}


/* =============================================
   RESPONSIVE BREAKPOINTS
   ============================================= */

/* Tablet (1024px and below): collapse two-column layout to single column */
@media (max-width: 1024px) {
    .contact-section {
        grid-template-columns: 1fr;
        gap: 50px;
    }
}

/* Large mobile (768px and below): reduce padding, stack form rows, hide legacy nav classes */
@media (max-width: 768px) {

    /* These classes are not present in this Vue component; likely leftover from a
       non-Vue version of this page and can be safely removed */
    .nav-links {
        display: none;
    }

    .mobile-menu-btn {
        display: block;
    }

    /* .page-header is not used in this template; also likely legacy and can be removed */
    .page-header {
        padding: 120px 24px 60px;
    }

    .page-header h1 {
        font-size: 36px;
    }

    .page-header p {
        font-size: 18px;
    }

    /* Reduces section padding on smaller screens */
    .contact-section {
        padding: 60px 24px;
        gap: 40px;
    }

    /* Reduces card padding so content isn't too tight on narrow screens */
    .contact-info,
    .contact-form-container {
        padding: 40px 30px;
    }

    .contact-info h2,
    .contact-form-container h2 {
        font-size: 28px;
    }

    /* Stacks paired form fields (name, email/phone) vertically on mobile */
    .form-row {
        grid-template-columns: 1fr;
        gap: 20px;
    }
}

/* Small mobile (480px and below): tighten padding and scale down typography further */
@media (max-width: 480px) {
    .page-header h1 {
        font-size: 28px;
    }

    .page-header p {
        font-size: 16px;
    }

    .contact-info,
    .contact-form-container {
        padding: 30px 20px;
    }

    .contact-info h2,
    .contact-form-container h2 {
        font-size: 24px;
    }

    /* Shrinks icon container on very small screens to preserve layout */
    .contact-icon {
        width: 40px;
        height: 40px;
        font-size: 20px;
    }

    .contact-item-content h3 {
        font-size: 18px;
    }

    /* Reduces input padding on small screens to save vertical space */
    input,
    textarea,
    select {
        padding: 12px;
    }

    .submit-button {
        padding: 15px 40px;
        font-size: 16px;
    }
}
</style>