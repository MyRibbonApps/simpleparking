<template>
<div class="page">
<navBar/>

<main class="page">
  <section class="presentation hide-mobile-boxes show-desktop-boxes">
    <div class="introduction">
      <div class="intro-text">
        <h2>Ribbon Five</h2>
      </div>
    </div>
  </section>

</main>
<br>
<br>
<!-- <footerBar/> -->
</div>
</template>

<script>
import navBar from '@/components/nav';
// import footerBar from '@/components/footer';
export default {
  data() {
    return {
      menuOpen: false,
      readyToClose: false,
    }
  },

    components: {
      navBar,
      // footerBar
  },
  methods: {
    openNav() {
      this.menuOpen = true
     setTimeout(() => {
          this.readyToClose = true
        }, 100);
    },

    close() {
      console.log(this.$refs)
      // if(this.$refs.menu.outerHTML === '<div class="hamburger-menu open" data-v-2a183b29=""></div>') {
      //   console.log('djsjks')
      //    this.menuOpen = false
      // }
      if(this.readyToClose === true) {
        this.menuOpen = false
        this.readyToClose = false
      }
      console.log(this.$refs.menu.outerHTML)

    },

    closeMenu() {
         if(this.menuOpen === true) {
           console.log('start')
       setTimeout(function(){
          console.log('finish')
            }, 10);
                this.menuOpen = false
      }
    }

  },
}
</script>

<style lang="scss" scoped>

* {
  margin: 0;
  padding: 0;
}
button {
border: none;
border-radius: 2rem;
height: 4rem;
font-size: 2rem;
padding: 0 2rem;
}
body {
margin: 0;
font-family: 'Helvetica', sans-serif;
overflow-x: hidden;
}

.menu ul {
display: inline-flex;
margin: 50px;
}

.menu ul li {
list-style: none;
margin: 0 20px;
color: #b2b1b1;
cursor: pointer;
}
.logo {
width: 100px;
margin-top: -7px;
margin-right: 48px;
}

h1 {
margin-left: 40px;
flex-grow: 1;
color: rgb(255, 255, 255);
}

/*
.container {
padding-bottom: 60px;
padding-top: 20px;
display: flex;
background: #ffffff;
&.open {
  padding-top: 0px;
}
}
*/

.anotherWrapper {
display: flex;
max-width:50%;
margin: 0 auto;
/* margin-right: 20%; */
margin-right: 2%;
}
.read-more-button-1 {
text-decoration: none;
color: rgb(255, 255, 255) !important;
font-size: 14px;
font-weight: 500;
background-color: rgb(255, 255, 255);
height: 55px;
width: auto;
border-radius: 50px;
cursor: pointer;
border: none;
text-align: center;
width: 60%;
margin-top: 45px;
padding-top: 18px;
}


.start-container {
width: 80%;
height: 100vh;
left: 130px;
position: absolute;
color: rgb(0, 0, 0);
margin-top: 50px;
}

.start-box{
width: 50%;
float: left;
}

.start-box h3 {
font-size: 50px;
font-weight: 700;
margin-left: 35px;
letter-spacing: 0.1px;
line-height: 1.09;
}

.start-box p {
width: 650px;
font-size: 25px;
margin: 30px 0 30px 40px;
line-height: 25px;
color: #ffffff;
font-weight: 500;
font-stretch: normal;
line-height: 1.47;
}


.start-image {
display: flex;
max-width:40%;
margin: 0 auto;
/* margin-right: 20%; */
margin-left: 1%;
margin-top: -20px;
padding-bottom: 30px;
}

@media screen and (min-width: 1900px) {
.presentation {
display: flex;
width: 85%;
margin: auto;
min-height: 88vh;
margin-top: 95px;
}

.presentation2 {
display: flex;
width: 90%;
margin: auto;
margin-top: 10em;
padding-bottom: 250px;
}
.intro-text2 p {
font-size: 25px;
line-height: 25px;
color: #ffffff;
font-weight: 500;
font-stretch: normal;
line-height: 1.47;
}

.presentation3 {
display: flex;
width: 85%;
margin: auto;
margin-top: 195px;
}

.cover img {
height: 55vh;
flex: 1;
}
}

.menu-wrapper {
display: flex;
width: 93%;
margin: auto;
min-height: 88vh;
margin-top: 35px;
}


.introduction {
flex: 1;
}

.intro-text h2 {
font-size: 44px;
font-weight: 600;
margin-top: 35px;
color: rgb(0, 0, 0);
}

.intro-text2 h2 {
font-size: 44px;
font-weight: 600;
color: rgb(0, 0, 0);
}

.intro-text p {
font-size: 25px;
line-height: 25px;
color: #ffffff;
font-weight: 500;
font-stretch: normal;
line-height: 1.47;
}

.cover2 img {
height: 62vh;
flex: 1;
margin-top: 50px;
}

.cover3 img {
height: 30vh;
flex: 1;
margin-top: 20px;
}

.logo-image img {
  height: 28px;
  margin-top: 5px;
  cursor: pointer;
}

.cross img {
height: 35px;
margin-top: 5px;
cursor: pointer;
}

.menu-text h2 {
font-size: 44px;
font-weight: 600;
margin-top: 35px;
color: rgb(255, 255, 255);
cursor: pointer;
}


.menu-text h2:hover {
transition: all .2s ease-out;
color: rgb(201, 201, 201);
}

.menu-text p {
font-size: 25px;
line-height: 25px;
color: #ffffff;
font-weight: 500;
font-stretch: normal;
line-height: 1.47;
}















/* COOLA BOXAR MED NICE STUFF BITCH!! */


@media (max-width: 1900px) {
#container img {
margin-right: -5%;
margin-top: 20px;
width: 55%;
height: 55%;
object-fit:contain;
}
/*#container img {
margin-right: 10%;
margin-top: 20px;
width: 25%;
height: 25%;
object-fit:contain;
}
*/
#container {
  padding-top: 30px;
  padding-bottom: 30px;
  margin: auto;
  width: 90%;
  height: 80%;
  /* background: #0000f9; */
  /* background: #000037;*/
  background: #3a3a3a;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  max-width: 90%;
}

.points-box {
    margin-top: 50px;
}

.text-box-new {
    padding-top: 0px;
    margin-right: 20%;
    margin-left: 0%;
    width: 25%;
}

.read-more-button-1 {
text-decoration: none;
color: rgb(255, 255, 255) !important;
font-size: 14px;
font-weight: 500;
background-color: rgb(255, 255, 255);
height: 55px;
width: auto;
border-radius: 50px;
cursor: pointer;
border: none;
text-align: center;
width: 60%;
margin-top: 45px;
padding-top: 18px;
}
.text-box-new {
padding-top: 0px;
margin-right: 22%;
margin-left: 0%;
width: 25%;
}
.text-box-new p {
color: rgb(255, 255, 255);
font-size: 17px;
line-height: 1.7em;
font-weight: 400;
}
.text-box-new h2 {
color: rgb(255, 255, 255);
font-size: 4rem;
line-height: 1.1em;
font-weight: 600;
}
}

@media (min-width: 1900px) {
#container {
  padding-top: 40px;
  padding-bottom: 30px;
  margin: auto;
  width: 90%;
  height: 60%;
 /* background: #0000f9; */
 /* background: #000037;*/
  background: #f2f2f2f2;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  max-width: 90%;
}

#container img {
  margin-right: -5%;
  margin-top: 20px;
  width: 55%;
  height: 55%;
  object-fit:contain;
}
.text-box-new {
    padding-top: 0px;
    margin-right: 22%;
    margin-left: 0%;
    width: 25%;
}

.text-box-new p {
color: rgb(255, 255, 255);
font-size: 17px;
line-height: 1.7em;
font-weight: 400;
}
.text-box-new h2 {
color: rgb(255, 255, 255);
font-size: 4rem;
line-height: 1.1em;
font-weight: 600;
}

.read-more-button-1 {
text-decoration: none;
color: rgb(255, 255, 255) !important;
font-size: 18px;
font-weight: 500;
background-color: rgb(255, 255, 255);
height: 55px;
width: auto;
border-radius: 50px;
cursor: pointer;
border: none;
text-align: center;
width: 60%;
margin-top: 88px;
padding-top: 18px;
}
}


@media (max-width: 780px) {

        .hide-mobile-boxes {
            display: none;
        }
           .container {
        width: 85%;
        margin: 0 auto;
    }
}

@media (min-width: 780px) {
    .presentation-for-mobile {
        display: none;
    }
}
   .introduction-mobile {
       text-align: center;

    } .intro-text-mobile p {

        font-size: 1em;
        line-height: 25px;
        color: #ffffff;
        font-weight: 500;
        font-stretch: normal;
        line-height: 1.47;
        padding-bottom: 2em;
        width: 80%;
        margin: auto;
    } 

     .intro-text-mobile h2 {
        font-size: 1.7em;
        color: rgb(255, 255, 255);
       font-weight: 500;
    }
    .under-text-button-mobile {
        text-align: center;
        border-radius: 50px;
        padding: 10px;
        height: 40px;
        font-size: 1em;
        font-weight: 500;
        color: rgb(255, 255, 255);
        width: 40%;
        background: #0075E1;
        margin: auto;
        margin-top: 30px;

    } .cover-mobile1 img {
        height: 50vh;
    }

    .cover-mobile2 img {
        height: 50vh;
    }
    
    .cover-mobile1 {
        text-align: center;
    }

        .cover-mobile2 {
        text-align: center;
    }







/* NY CSS */

ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

.container {
    text-align: center;
    padding: .8em 0.2em;
}

.logo {
    width: 170px;
}

.hide-mobile {
    display: none;
}
header {
    display: flex;
    justify-content: space-between;
}

.menu {
    width: 25px;
    margin-top: 45%;
}

.server {
    width: 70%;
    margin: 2em auto 2em 25%;
}

h1, .subhead {
    position: relative;
    z-index: 3;
}

.subhead {
    font-size: 1.1em;
}

.blue-container {
    width: 100%;
    background: #0075E1;
    color: #fff;
    margin-top: 15%;
    padding: 6em 0 4em;
    border-top-left-radius: 40px;
    transform: skewY(-2deg);
}

.blue-container:before {
    content: "";
    width: 40px;
    height: 40px;
    background-color: #0075E1;
    position: absolute;
    top: -39px;
    right: 0;
    z-index: -2;
}

.blue-container:after {
    content: "";
    width: 80px;
    height: 80px;
    background-color: #fff;
    top: -80px;
    position: absolute;
    right: 0;
    border-radius: 50%;
    z-index: -1;
}

.blue-container ul {
    transform: skewY(2deg);
}

.container-blue {
    width: 80%;
    margin: auto;
    text-align: center;
    padding: 1em .3em;
}

.blue-container ul li {
    margin-bottom: 3em;
}

.blue-container ul li p {
    margin-top: 20px;
    font-size: 1em;
    padding: 0 .5em;
}

.blue-container img {
    width: 14%;
}

.blue-container ul li:nth-child(3) img {
    width: 8%;
}

.gray-container {
    background: #F6F6F6;
    padding: 4em 0 2em;
    margin-top: -3%;
}

.gray-container ul li:first-child {
    margin-bottom: 2em;
}

figure {
    margin: 0;
    padding: 0;
}

figcaption {
    font-weight: bold;
    color: #0075E1;
}

h2 {
    margin-top: 7%;
}


.footer-container {
    margin-top: 3em;
    width: 100%;
    background: #3D444A;
    color: #fff;
    padding: 3em 0;
    border-top-right-radius: 40px;
    transform: skewY(2deg);
}

.footer-container .container {
    transform: skewY(-2deg);
}

.footer-container:before {
    content: "";
    width: 40px;
    height: 40px;
    background-color: #3D444A;
    position: absolute;
    top: -39px;
    left: 0;
    z-index: -2;
}

.footer-container:after {
    content: "";
    width: 80px;
    height: 80px;
    background-color: #fff;
    position: absolute;
    z-index: -1;
    top: -80px;
    left: 0;
    border-radius: 50%;
}

ul.footer-links {
    margin: 0 auto;
}

ul.footer-links li {
    display: inline-block;
}

ul.footer-links li a {
    color: #9D9D9D;
    font-size: .8em;
}

nav ul {
    position: fixed;
    width: 60%;
    top: 0;
    right: 0;
    text-align: left;
    background: #31373b;
    height: 100%;
    z-index: 7;
    padding-top: 3em;
}

nav ul li a {
    color: white;
    text-decoration: none;
    display: block;
    width: 100%;
    padding: 1em 2em;
    background-color: rgb(49, 55, 59);
}

// nav ul li a:hover {
//     background-color: rgb(65, 73, 78);
// }

.exit-btn {
    margin-bottom: 1em;
    margin-top: -1.3em;
    text-align: right;
    padding: 0 1.4em;
    width: 65px;
}

.exit-btn img {
    width: 55px;
    height: 55px;
    cursor: pointer;
}

@media only screen and (min-width: 650px)  {

    .server {
        width: 50%;
    }

    h1 {
        font-size: 3em;
        margin: 0;
    }

    .subhead {
        font-size: 1.4em;
        margin-bottom: 12%;
    }

    .blue-container {
        margin: 0;
    }

    .blue-container img {
        width: 20%;
    }

    .blue-container ul li:nth-child(3) img {
        width: 11%;
        margin-top: -6px;
    }

    .blue-container ul {
        display: flex;
        margin-top: -1em;
        align-items: center;
    }

    .blue-container ul li {
        margin-bottom: 0;
    }

    .blue-container ul li p {
        padding: 0 .8em;
    }

    .gray-container ul {
        display: flex;
    }


    nav ul {
        width: 40%;
    }

}
.cta {
    background: #0075E1;
    width: 50%;
    display: block;
    color: #fff;
    border-radius: 50px;
    padding: .5em;
    text-decoration: none;
    font-size: 1.5em;
    margin: 3% auto 7%;
    position: relative;
    z-index: 4;
}
@media only screen and (min-width: 875px)  {

    .subhead {
        margin-bottom: 15%;
    }

    .blue-container ul {
        margin: 0 0 4% 0;
    }

    .gray-container ul {
        margin: 4% 0 0;
    }

}
@media only screen and (min-width: 1024px)  {
   .cta {
    background: #0075E1;
    width: 20%;
    display: block;
    color: #fff;
    border-radius: 50px;
    padding: .5em;
    text-decoration: none;
    font-size: 1.5em;
    margin: 3% auto 7%;
    position: relative;
    z-index: 4;
}

  .cta:hover {
    background: rgb(0, 111, 214);
    cursor: pointer;
}

    .container {
        width: 93%;
        margin: 0 auto;
    }

    .show-desktop {
        display: block;
        margin: 0 auto 13% auto;
    }

    .hide-desktop {
        display: none;
    }

    nav ul {
        position: inherit;
        width: auto;
        background: none;
        height: auto;
        display: flex;
        padding-top: 0;
    }

    nav ul li {
        float: left;
    }

    nav ul li a {
        color: black;
        background-color: inherit;
        text-align: right;
        padding: 1em 2em;
    }

    nav ul li a:hover {
        background-color: inherit;
    }

    .scroll {
        width: 30px;
        animation: move 1s infinite alternate;
    }

    @keyframes move {
        from {
            transform: translateY(0px);
        }
        to {
            transform: translateY(20px);
        }
    }

}

@media (max-width:1024px) {
    nav ul {

   transform: translateX(100%);
   transition: transform .3s linear;
   z-index: 99;
   overflow-x: hidden;
   &.open{
      transform: translateX(0);
   }
    }
}

@media only screen and (min-width: 1600px)  {

    .server {
        width: 40%;
        margin: 5em auto 4em 15%;
    }

    .container {
        width: 93%;
        margin: 0 auto;
    }

    .blue-container {
        padding: 7em 0 2em;
    }

    .blue-container ul li p, blockquote {
        font-size: 1.3em;
    }

    .gray-container {
        padding: 6em 0 4em;
    }

    h2 {
        margin-top: 4em;
    }

    .blue-container img {
        width: 15%;
    }

    .blue-container ul li:nth-child(3) img {
        width: 8%;
        margin-top: -4px;
    }

}

.nav-link-hover:hover {
    cursor: pointer;
    color:rgb(39, 39, 39);
}

.logo-footer {
    margin-left: 2em;
    padding-bottom: 1em;
}

.mobile-text-under-points {
    text-align: center;
    width: 70%;
    margin: auto;
    margin-top: 4em;
    color: rgb(255, 255, 255);
    font-size: 1rem;
    font-weight: 300;
}


.row {
  margin-top: 2em;
  margin-left: 15%;
  display: flex;
  flex-direction: row;
/*  width: 50%;*/
}



.downloads {
display: flex;
margin-top: -2em;
width: 100%;
  flex-direction: row;
}

.over-icons {
    display: flex;
margin-left: auto;
margin-right: auto;
}

.apple {
    padding-right: 5px;
padding-left: 5px;
}

.playstore-logo {
    width: 140px;
}

.row2{
margin-top: -3.5em;
margin-left: 15%;
display: flex;
flex-direction: row;
/*  width: 50%;*/
}
.column {
  display: flex;
  flex-direction: column;
  flex-basis: 10%;
  flex: 0;
}

.blue-column {
  height: 100px;
}

.green-column {
white-space: nowrap;
width: 100%;
margin-left: 15px;
font-size: 16px;
font-weight: 600;
color: rgb(255, 255, 255);
}

.tick {
height: 20px;
width: 20px;
}

.page {
  background: #464646;
}

</style>
