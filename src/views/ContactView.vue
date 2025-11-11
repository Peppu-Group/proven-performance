<template>
    <!-- Navigation -->
    <NavBar />
    <!-- Hero Section -->
    <section class="hero hero-img" id="home">
        <div class="">
            <div class="hero-content">
                <h1>
                    <span class="highlight">Get In Touch</span>
                </h1>
                <p>Ready to transform your business? Let's discuss how we can help you achieve your strategic goals.</p>
            </div>
        </div>
    </section>
   <!-- Contact Section -->
   <section class="contact-section">
        <!-- Contact Info -->
        <div class="contact-info">
            <h2>Let's Connect</h2>
            <p>We're here to answer your questions and discuss how we can support your business objectives.</p>
            
            <div class="contact-details">
                <div class="contact-item">
                    <div class="contact-icon">📧</div>
                    <div class="contact-item-content">
                        <h3>Email</h3>
                        <p><a href="mailto:provenperformanceltd@gmail.com">provenperformanceltd@gmail.com</a></p>
                    </div>
                </div>

                <div class="contact-item">
                    <div class="contact-icon"> ⟟ </div>
                    <div class="contact-item-content">
                        <h3>Office</h3>
                        <p>Plot 13A Wada Nas Street, Guzape. Federal Capital Territory, Nigeria</p>
                    </div>
                </div>

                <div class="contact-item">
                    <div class="contact-icon">⏰</div>
                    <div class="contact-item-content">
                        <h3>Business Hours</h3>
                        <p>Monday - Friday: 9:00 AM - 6:00 PM<br>Saturday - Sunday: Closed</p>
                    </div>
                </div>
            </div>

            <div class="social-links">
                <a href="#" class="social-link" aria-label="LinkedIn">in</a>
                <a href="#" class="social-link" aria-label="Twitter">𝕏</a>
                <a href="#" class="social-link" aria-label="Facebook">f</a>
            </div>
        </div>

        <!-- Contact Form -->
        <div class="contact-form-container">
            <h2>Send us a Message</h2>
            <p>Fill out the form below and we'll get back to you within 24 hours.</p>
            
            <form id="contactForm" @click="handleSubmit(event)">
                <div class="form-row">
                    <div class="form-group">
                        <label for="firstName">First Name *</label>
                        <input type="text" id="firstName" name="firstName" required>
                    </div>
                    <div class="form-group">
                        <label for="lastName">Last Name *</label>
                        <input type="text" id="lastName" name="lastName" required>
                    </div>
                </div>

                <div class="form-row">
                    <div class="form-group">
                        <label for="email">Email *</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="phone">Phone</label>
                        <input type="tel" id="phone" name="phone">
                    </div>
                </div>

                <div class="form-group">
                    <label for="company">Company</label>
                    <input type="text" id="company" name="company">
                </div>

                <div class="form-group">
                    <label for="service">Service Interest</label>
                    <select id="service" name="service">
                        <option value="">Select a service...</option>
                        <option value="strategic">Strategic Planning</option>
                        <option value="operations">Operations Excellence</option>
                        <option value="change">Change Management</option>
                        <option value="project">Project Management</option>
                        <option value="digital">Digital Transformation</option>
                        <option value="other">Other</option>
                    </select>
                </div>

                <div class="form-group">
                    <label for="message">Message *</label>
                    <textarea id="message" name="message" required></textarea>
                </div>

                <button type="submit" class="submit-button">Send Message</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Apex Consulting Partners. All rights reserved.</p>
    </footer>

</template>

<script>
import NavBar from '../components/NavBar.vue'

export default {
    name: 'ContactView',
    components: { NavBar },

    methods: {
        handleSubmit(event) {
            event.preventDefault();
            
            // Get form data
            const formData = new FormData(event.target);
            const data = Object.fromEntries(formData);
            
            // Here you would typically send the data to a server
            console.log('Form submitted:', data);
            
            // Show success message
            alert('Thank you for your message! We will get back to you within 24 hours.');
            
            // Reset form
            event.target.reset();
        }
    }
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

/* Contact Section */
        .contact-section {
            max-width: 1400px;
            margin: 0 auto;
            padding: 100px 5%;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 80px;
            align-items: start;
        }

        /* Contact Info */
        .contact-info {
            background: linear-gradient(135deg, var(--navy) 0%, #2d3e50 100%);
            padding: 60px;
            border-radius: 20px;
            color: var(--white);
            height: fit-content;
        }

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

        .contact-details {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 20px;
        }

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

        .contact-item-content h3 {
            font-size: 20px;
            color: var(--gold);
            margin-bottom: 8px;
        }

        .contact-item-content p {
            margin: 0;
            opacity: 0.9;
        }

        .contact-item-content a {
            color: var(--white);
            text-decoration: none;
            transition: color 0.3s;
        }

        .contact-item-content a:hover {
            color: var(--gold);
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 40px;
        }

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

        .social-link:hover {
            background: var(--gold);
            color: var(--navy);
            transform: translateY(-3px);
        }

        /* Contact Form */
        .contact-form-container {
            background: var(--white);
            padding: 60px;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.1);
        }

        .contact-form-container h2 {
            font-family: 'Playfair Display', serif;
            font-size: 36px;
            color: var(--navy);
            margin-bottom: 20px;
        }

        .contact-form-container > p {
            color: var(--text-gray);
            margin-bottom: 40px;
            font-size: 16px;
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 25px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: var(--navy);
        }

        input,
        textarea,
        select {
            width: 100%;
            padding: 15px;
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            font-family: 'Inter', sans-serif;
            font-size: 16px;
            transition: border-color 0.3s;
        }

        input:focus,
        textarea:focus,
        select:focus {
            outline: none;
            border-color: var(--gold);
        }

        textarea {
            resize: vertical;
            min-height: 150px;
        }

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

        .submit-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.3);
        }

        /* Footer */
        footer {
            background: var(--navy);
            color: var(--white);
            text-align: center;
            padding: 3rem 5%;
        }

        footer p {
            opacity: 0.8;
        }

        /* Responsive */
        @media (max-width: 1024px) {
            .contact-section {
                grid-template-columns: 1fr;
                gap: 50px;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }

            .mobile-menu-btn {
                display: block;
            }

            .page-header {
                padding: 120px 24px 60px;
            }

            .page-header h1 {
                font-size: 36px;
            }

            .page-header p {
                font-size: 18px;
            }

            .contact-section {
                padding: 60px 24px;
                gap: 40px;
            }

            .contact-info,
            .contact-form-container {
                padding: 40px 30px;
            }

            .contact-info h2,
            .contact-form-container h2 {
                font-size: 28px;
            }

            .form-row {
                grid-template-columns: 1fr;
                gap: 20px;
            }
        }

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

            .contact-icon {
                width: 40px;
                height: 40px;
                font-size: 20px;
            }

            .contact-item-content h3 {
                font-size: 18px;
            }

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