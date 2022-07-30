<template>
    <div class="main">
        <div class="bar">
            <button class="list-icon" @click="isGrid = false">LIST</button>
            <button class="grid-icon active" @click="isGrid = true">GRID</button>
        </div>
        <ul :class="{
            grid: isGrid,
            list: !isGrid
        }">
            <li>
                <a href="https://tutorialzine.com/2016/03/what-you-need-to-know-about-css-variables/" target="_blank">
                    <img src="https://tutorialzine.com/media/2016/03/css-variables.jpg">
                    <span class="title">What You Need To Know About CSS Variables</span>
                </a>
            </li>
            <li>
                <a href="https://tutorialzine.com/2016/02/freebie-4-great-looking-pricing-tables/" target="_blank">
                    <img src="https://tutorialzine.com/media/2016/02/great-looking-pricing-tables.jpg">
                    <span class="title">What You Need To Know About CSS Variables</span>
                </a>
            </li>
            <li>
                <a href="https://tutorialzine.com/2016/02/20-interesting-javascript-and-css-libraries-for-february-2016/" target="_blank"><img src="https://tutorialzine.com/media/2016/02/interesting-resources-february.jpg">
                <span class="title">What You Need To Know About CSS Variables</span>
            </a>
        </li>
            <li>
                <a href="https://tutorialzine.com/2016/02/quick-tip-easiest-way-to-make-responsive-headers/" target="_blank">
                    <img src="https://tutorialzine.com/media/2016/02/quick-tip-responsive-headers.png">
                    <span class="title">What You Need To Know About CSS Variables</span>
                </a>
            </li>
            <li>
                <a href="https://tutorialzine.com/2016/01/learn-sql-in-20-minutes/" target="_blank">
                    <img src="https://tutorialzine.com/media/2016/01/learn-sql-20-minutes.png">
                    <span class="title">What You Need To Know About CSS Variables</span>
                </a>
            </li>
            <li>
                <a href="https://tutorialzine.com/2015/12/creating-your-first-desktop-app-with-html-js-and-electron/" target="_blank">
                    <img src="https://tutorialzine.com/media/2015/12/creating-your-first-desktop-app-with-electron.png">
                    <span class="title">What You Need To Know About CSS Variables</span>
                </a>
            </li>
        </ul>
    </div>
</template>
<script setup>
import { ref } from 'vue';
const isGrid = ref(true);
</script>
<style>
    .main {
        width: 960px;
        border: 1px solid #000;
        margin-top: 100px;
    }
    .bar {
        display: flex;
        align-items: center;
        justify-content: flex-end;
        background: #5c9bb7;
        padding: 10px 10px;
        margin-bottom: 20px;
    }
    ul {
        display: flex;
        flex-wrap: wrap;
        list-style: none;
        padding: 0;
    }
    ul.grid li {
        flex: 0 0 50%;
        max-width: 50%;
    }
    ul.grid .title {
        display: none;
    }
    ul.list {
        flex-direction: column;
    }
    ul.list li {
        flex: 0 0 100%;
        max-width: 100%;
    }
    ul.list li a {
        display: flex;
        justify-content: flex-start;
        align-items: flex-start;
    }

    ul.list li img {
        width: 100px;
        margin-right: 10px;
    }

    li img {
        width: 100%;
        height: 100%;
    }
</style>