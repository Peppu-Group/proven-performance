<template>
    <!-- ========== Site Navigation ========== -->
    <!-- Fixed top navbar using Bootstrap's responsive navbar component.
         Collapses into a hamburger menu on screens smaller than 'lg' (992px) -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">

            <!-- Brand / Logo -->
            <!-- Clicking the logo navigates back to the homepage -->
            <a class="navbar-brand" href="/">
                <img src="../assets/logo.png" alt="Apex Consulting">
                <!-- alt text serves as a text fallback and improves screen reader accessibility -->
            </a>

            <!-- Hamburger Toggle Button -->
            <!-- Visible only on mobile/tablet; toggles the collapsed nav menu.
                 data-bs-target links this button to the collapsible nav panel below -->
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>

            <!-- Collapsible Navigation Links -->
            <!-- Collapses on small screens; expands when the hamburger button is toggled.
                 ID must match data-bs-target on the toggle button above -->
            <div class="collapse navbar-collapse" id="navbarNav">

                <!-- Nav link list; ms-auto pushes it to the right on larger screens -->
                <ul class="navbar-nav ms-auto">

                    <!-- Home link -->
                    <li class="nav-item">
                        <a class="nav-link" href="/">Home</a>
                    </li>

                    <!-- About page link -->
                    <li class="nav-item">
                        <a class="nav-link" href="/about">About</a>
                    </li>

                    <!-- Services page link -->
                    <li class="nav-item">
                        <a class="nav-link" href="/services">Services</a>
                    </li>

                    <!-- Contact CTA -->
                    <!-- Styled as a primary button rather than a plain link
                         to visually distinguish it as the key action item -->
                    <li class="nav-item">
                        <a class="btn btn-primary" href="/contact">Contact</a>
                    </li>

                </ul>
            </div>

        </div>
    </nav>
</template>

<script>
export default {
    name: 'NavBar', // Component name used in Vue DevTools and when registered in parent components
}
</script>

<style scoped>
/* =============================================
   NAVBAR
   Fixed to the top of the viewport so it
   remains visible while the user scrolls.
   Scoped styles only apply to this component.
   ============================================= */
.navbar {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    background: rgba(255, 255, 255, 0.95) !important;
    /* !important overrides Bootstrap's bg-light utility */
    backdrop-filter: blur(10px);
    /* Frosted glass effect; blurs content scrolling behind the navbar */
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    /* Subtle drop shadow to separate navbar from page content */
    z-index: 1000;
    /* Ensures the navbar sits above all other page content */
    padding: 0;
    /* Removes Bootstrap's default navbar padding; height is controlled on the container */
}

/* Inner container: constrains content width and sets a fixed navbar height */
.navbar .container-fluid {
    max-width: 1200px;
    margin: 0 auto;
    /* Centers the container within the full-width navbar */
    padding: 0 24px;
    height: 80px;
}

/* Vertically centers the logo within the navbar height */
.navbar-brand {
    display: flex;
    align-items: center;
}

/* Logo image sizing; width is auto to preserve aspect ratio */
.navbar-brand img {
    height: 60px;
    /* Adjust this value based on your logo's dimensions */
    width: auto;
    object-fit: contain;
    /* Prevents the logo from stretching or cropping */
}

/* Spacing and alignment for the nav link list on desktop */
.navbar-nav {
    gap: 32px;
    /* Consistent spacing between nav items */
    align-items: center;
    /* Vertically centers links and the CTA button */
}

/* Default nav link styling; color overrides Bootstrap's default */
.navbar-nav .nav-link {
    color: var(--gray-dark) !important;
    /* !important needed to override Bootstrap's navbar-light link color */
    font-weight: 500;
    transition: color 0.3s;
    /* Smooth color change on hover */
    padding: 0.5rem 0;
}

/* Hover state: highlights the active link using the brand gold color */
.navbar-nav .nav-link:hover {
    color: var(--gold) !important;
}

/* CTA button padding; keeps it visually balanced within the nav height */
.navbar-nav .btn-primary {
    padding: 0.5rem 1.5rem;
    font-weight: 500;
}


/* =============================================
   MOBILE STYLES
   Applies to screens narrower than Bootstrap's
   'lg' breakpoint (991.98px and below).
   The hamburger menu is visible at this range.
   ============================================= */
@media (max-width: 991.98px) {

    /* Reduces the gap between stacked nav items in the collapsed menu */
    .navbar-nav {
        gap: 1rem;
        padding: 1rem 0;
        /* Adds breathing room above and below the link list */
    }

    /* Centers each nav item when stacked vertically on mobile */
    .navbar-nav .nav-item {
        text-align: center;
    }

    /* Removes the fixed height so the container can expand to fit the open menu */
    .navbar .container-fluid {
        height: auto;
    }
}
</style>