<template>
  <NavBar/>
  <router-view/>
  <FooterVue/>
  <ScrollUp/>
</template>
<script>
import 'boxicons'
import NavBar from './components/NavBar.vue'
import FooterVue from './components/Footer.vue'
import ScrollUp from './components/ScrollUp.vue'
export default {
  name: 'App',
  components:{
    NavBar,
    FooterVue,
    ScrollUp
  }
}
</script>
<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap");
  :root{
    --header-height: 3rem;
    /*========== Colors ==========*/
    --hue: 202;
    --sat: 45%;
    --first-color: hsl(var(--hue), var(--sat), 60%);
    --first-color-light: hsl(var(--hue), var(--sat), 85%);
    --first-color-lighten: hsl(var(--hue), var(--sat), 80%);
    --first-color-alt: hsl(var(--hue), var(--sat), 53%);
    --title-color: hsl(var(--hue), 4%, 15%);
    --text-color: hsl(var(--hue), 4%, 35%);
    --text-color-light: hsl(var(--hue), 4%, 65%);
    --body-color: hsl(var(--hue), 0%, 100%);
    --container-color: #FFF;
    --scroll-bar-color: hsl(var(--hue), 4%, 85%);
    --scroll-thumb-color: hsl(var(--hue), 4%, 75%);
    /*========== Font and typography ==========*/
    --body-font: 'Poppins', sans-serif;
    --biggest-font-size: 2rem;
    --h2-font-size: 1.25rem;
    --h3-font-size: 1.125rem;
    --normal-font-size: .938rem;
    --small-font-size: .813rem;
    --smaller-font-size: .75rem;
    /*========== Font weight ==========*/
    --font-semi-bold: 600;
    --font-bold: 700;
    /*========== Margenes ==========*/
    --mb-0-5: .5rem;
    --mb-0-75: .75rem;
    --mb-1: 1rem;
    --mb-1-5: 1.5rem;
    --mb-2: 2rem;
    /*========== z index ==========*/
    --z-tooltip: 10;
    --z-fixed: 100;

    @media screen and (min-width: 968px){
      --biggest-font-size: 3rem;
      --h2-font-size: 1.75rem;
      --h3-font-size: 1.25rem;
      --normal-font-size: 1rem;
      --small-font-size: .875rem;
      --smaller-font-size: .813rem;
    }
  }
  *, ::before, ::after {
    box-sizing: border-box;
    padding: 0;
    margin: 0;
  }
  html {
    scroll-behavior: smooth;
  }

  body {
    margin: var(--header-height) 0 0 0;
    font-family: var(--body-font);
    font-size: var(--normal-font-size);
    background-color: var(--body-color);
    color: var(--text-color);
    transition: .5s;

    @media screen and (min-width: 767px){
      margin: 0;
    }
  }
  
  h1, h2, h3 {
    font-weight: var(--font-semi-bold);
    color: var(--title-color);
    line-height: 1.5;
  }
  
  ul {
    list-style: none;
  }
  
  a {
    text-decoration: none;
  }
  
  img {
    max-width: 100%;
    height: auto;
  }

  .section {
    padding: 4.5rem 0 1rem;
    @media screen and (max-width: 360px){
      padding: 3.5rem 0 1rem;
    }
    @media screen and (min-width: 767px){
      padding: 6rem 0 2rem;
    }
  }

  .section-title, .section-title-center {
    font-size: var(--h2-font-size);
    color: var(--title-color);
    text-align: center;
    margin-bottom: var(--mb-1);
  }
  .section-title-center{
    @media screen and (min-width: 576px){
      text-align: initial;
    }
  }
  
  .svg-color {
    fill: var(--first-color);
  }
  
  .svg-blob {
    fill: var(--first-color-light);
  }
  
  .svg-img {
    width: 300px;
    justify-self: center;
    @media screen and (max-width: 360px){
      width: 100%;
    }
    @media screen and (min-width: 576px){
      width: 100%;
    }
    @media screen and (min-width: 968px){
      width: 470px;
    }
  }
  
  /*=============== LAYOUT ===============*/
  .container {
    max-width: 968px;
    margin-left: var(--mb-1-5);
    margin-right: var(--mb-1-5);
    @media screen and (min-width: 1024px){
      margin-left: auto;
      margin-right: auto;
    }
  }
  
  .grid {
    display: grid;
    gap: 1.5rem;
  }

  .button {
    display: inline-block;
    background-color: var(--first-color);
    color: #1A1A1A;
    padding: .75rem 1.5rem;
    border-radius: 3rem;
    font-weight: var(--font-semi-bold);
    transition: .3s;

    &:hover{
      background-color: var(--first-color-alt);
    }
  }
  
  .button-header {
    display: none;
    @media screen and (min-width: 968px){
      display: block;
    }
  }
  
  .button-link {
    background: none;
    padding: 0;
    color: var(--title-color);

    &:hover{
      background-color: transparent;
    }
  }

  .button-flex {
    display: inline-flex;
    align-items: center;
    column-gap: .25rem;
    padding: .75rem 1rem;
  }
  
  .button-icon {
    font-size: 1.5rem;
  }
  
  .scrollup {
    position: fixed;
    background: var(--first-color);
    right: 1rem;
    bottom: 3rem;
    display: inline-flex;
    padding: .3rem;
    border-radius: .25rem;
    z-index: var(--z-tooltip);
    opacity: .8;
    transition: .4s;

    &:hover{
      background-color: var(--first-color);
      opacity: 1;
    }
  }
  .scrollup-icon {
      font-size: 1.25rem;
      color: var(--title-color);
    }
  .show-scroll {
    bottom: 3rem;
  }
  ::-webkit-scrollbar {
    width: .6rem;
    border-radius: .5rem;
    background-color: var(--scroll-bar-color);
  }
  ::-webkit-scrollbar-thumb {
    background-color: var(--scroll-thumb-color);
    border-radius: .5rem;
    &:hover{
      background-color: var(--text-color-light);
    }
  }
  
</style>
