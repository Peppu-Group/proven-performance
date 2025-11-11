<template>
<!-- Navigation -->
<nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="/">
                <img src="../assets/logo.png" alt="Apex Consulting">
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="/about">About</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="/services">Services</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="/contact">Contact</a>
                    </li>
                    <li class="nav-item">
                        <a class="btn btn-primary" href="/contact">Get Started</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
  name: 'NavBar',
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

</style>