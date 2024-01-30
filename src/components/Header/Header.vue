<script setup>
    import './styles/_header.scss'
</script>

<template>
    <div class="header-container-big primary">
        <header class="header-container">
            <div class="logo-section">
                <div class="logo-container">
                    <img id="logo" src="@/assets/Shape 2.svg" alt="">
                </div>
                <h1 id="headerTitle"><router-link to="/">Kenaz</router-link></h1>
            </div>
            <div class="navigation-section">
                <ul class="main-navigation">
                    <li class="main-nav-item"><a href="#" class="main-nav-link">Media</a></li>
                    <li class="main-nav-item"><a href="#" class="main-nav-link">Marketing</a></li>
                    <li class="main-nav-item"><a href="#" class="main-nav-link">Contact</a></li>
                </ul>
                <div class="logo-container">
                    <img src="@/assets/search 1.svg" alt="Search" id="searchIcon">
                </div>
            </div>
        </header>
    </div>
</template>