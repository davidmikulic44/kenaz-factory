<script setup>
    import './styles/header.scss'
</script>

<template>
    <header class="header-container">
        <div class="logo-section">
            <img src="@/assets/Vector Smart Objecta 1.svg" alt="">
            <h1 id="header-title">Kenaz</h1>
        </div>


        <div class="navigation-section">
            <nav id="mainNavigation">
                <h3 class="main-nav-item">Media</h3>
                <h3 class="main-nav-item">Marketing</h3>
                <h3 class="main-nav-item">Contact</h3>
            </nav>
            <img src="@/assets/search 1.svg" alt="Search" id="searchIcon">
        </div>
    </header>
</template>