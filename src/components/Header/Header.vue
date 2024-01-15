<script setup>
    import './styles/_header.scss'
</script>

<template>
    <div class="container">
        <header class="header-container">
        <div class="logo-section">
            <div class="logo-container">
                <img id="logo" src="@/assets/Vector Smart Objecta 1.svg" alt="">
            </div>
            <h1 id="headerTitle">Kenaz</h1>
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
    </div>
</template>