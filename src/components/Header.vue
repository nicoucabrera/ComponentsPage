<script>
export default {
    name: 'HeaderComponent',
};
</script>

<template>
    <header class="header">
        <div class="logo">
            <a href="https://github.com/nicoucabrera" target="_blank" rel="noopener noreferrer">
                <img src="https://img.icons8.com/ios-filled/50/000000/github.png" alt="Logo" />
            </a>
        </div>
        { Nicolas Cabrera }
        <div class="nav-button">
            <input type="checkbox" id="menu">
            <label for="menu" class="nav-button-label">
                <div class="div-nav one"></div>
                <div class="div-nav two"></div>
                <div class="div-nav three"></div>
            </label>
            <div class="blur-background">
                <nav class="nav-menu">
                    <ul>
                        <li class="home"><a  href="#">Home</a></li>
                        <li class="about"><a href="#">About</a></li>
                        <li class="projects"><a href="#">Projects</a></li>
                        <li class="contact"><a href="#">Contact</a></li>
                    </ul>
                </nav>
            </div>
            
        </div>
    </header>
</template>



<!-- <button class="nav-button">
    <div class="div-nav"></div>
    <div class="div-nav"></div>
    <div class="div-nav"></div>
</button> -->