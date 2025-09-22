<script>
    let isMenuOpen = false;

    function toggleMenu() {
        isMenuOpen = !isMenuOpen;
    }
</script>


<nav>
    <div class="logo">Logo</div>
    <div class="menu">
        <a href="#section1">Section 1</a>
        <a href="#section2">Section 2</a>
        <a href="#section3">Section 3</a>
    </div>
    <div class="hamburger" on:click={toggleMenu}>
        <div></div>
        <div></div>
        <div></div>
    </div>
    {#if isMenuOpen}
        <div class="mobile-menu">
            <a href="#section1" on:click={() => (isMenuOpen = false)}>Section 1</a>
            <a href="#section2" on:click={() => (isMenuOpen = false)}>Section 2</a>
            <a href="#section3" on:click={() => (isMenuOpen = false)}>Section 3</a>
        </div>
    {/if}
</nav>


<style>
    nav {
        position: sticky;
        top: 0;
        background-color: #333;
        color: white;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0.5rem 1rem;
        z-index: 1000;
    }

    .logo {
        font-size: 1.5rem;
        font-weight: bold;
    }

    .menu {
        display: flex;
        gap: 1rem;
    }

    .menu a {
        color: white;
        text-decoration: none;
        font-size: 1rem;
    }

    .menu a:hover {
        text-decoration: underline;
    }

    .hamburger {
        display: none;
        flex-direction: column;
        cursor: pointer;
    }

    .hamburger div {
        width: 25px;
        height: 3px;
        background-color: white;
        margin: 3px 0;
    }

    .mobile-menu {
        display: none;
        flex-direction: column;
        background-color: #333;
        position: absolute;
        top: 100%;
        right: 0;
        width: 200px;
        padding: 1rem;
    }

    .mobile-menu a {
        color: white;
        text-decoration: none;
        margin-bottom: 0.5rem;
    }

    .mobile-menu a:hover {
        text-decoration: underline;
    }

    @media (max-width: 768px) {
        .menu {
            display: none;
        }

        .hamburger {
            display: flex;
        }

        .mobile-menu {
            display: flex;
        }
    }
</style>