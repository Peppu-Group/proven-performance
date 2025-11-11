<template>
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
                    <p><i class="bi bi-geo-alt-fill me-2"></i>Plot 13A Wada Nas Street, Guzape. Federal Capital Territory, Nigeria</p>
                    <p><i class="bi bi-envelope-fill me-2"></i>provenperformanceltd@gmail.com</p>
                </div>
            </div>

            <!-- Quick Links Row -->
            <div class="row footer-row">
                <div class="col-12">
                    <h5 class="footer-heading">Quick Links</h5>
                    <div class="row">
                        <div class="col-md-3 col-6">
                            <a href="/about">About Us</a>
                        </div>
                        <div class="col-md-3 col-6">
                            <a href="/services">Services</a>
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
    name: 'FooterView',
}
</script>
<style>
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
</style>