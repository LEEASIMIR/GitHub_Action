<script>
import gsap from 'gsap';
import ScrollTrigger from "gsap/ScrollTrigger";
import menuItems from '@/assets/temp/data/menu.json'
gsap.registerPlugin(ScrollTrigger);

export default {
    data() {
        return {
            menuItems: menuItems,
            currentMenus: []
        }
    },
    mounted() {
        
    },
    methods: {
        getCurrentMenus(menus = [], name = '', result = []) {//name은 모든 메뉴 통틀어서 유일 해야함
            for(let menu of menus) {
                if(menu.name === name) {
                } else {
                }
            }
        }
    }
}
</script>

<template>
    <header class="header">
        <div class="logo">SITE LOGO</div>
        <nav class="navbar">
            <div class="container-fluid">
                <ul class="row">
                    <li class="col" v-for="menu1 in menuItems">
                        {{ menu1.name }}
                        <ul class="row">
                            <li class="col" v-for="menu2 in menu1.sub">
                                {{ menu2.name }}
                                <ul class="row">
                                    <li class="col" v-for="menu3 in menu2.sub">
                                        {{ menu3.name }}
                                    </li>
                                </ul>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
        </nav>
        <ul>
            <li></li>
        </ul>
    </header>

    <div class="page">
    </div>
</template>

<style>
@import '@/assets/scss/header.scss';
</style>