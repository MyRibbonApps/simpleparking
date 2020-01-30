<template>
    <div>
          <div class="container">
      <header>
      <img src="~/assets/images/logo.svg" alt="Simple family organizer" class="logo" @click="goHome">

      <nav>
              <a class="hide-desktop" @click="menuOpen = true">
                  <img src="~/assets/images/ham.svg" alt="toggle-menu" class="menu" id="menu">
              </a>
              <ul class="show-desktop" :class="{open : menuOpen}" id="nav">
                  <li @click="menuOpen = false"><img src="~/assets/images/exit.svg" class="exit-btn hide-desktop"></li>
                  <li @click="goHome"><a class="nav-link-hover">Hem</a></li>
                  <li @click="goContact"><a class="nav-link-hover">Kontakt</a></li>
              </ul>

           
      </nav>
      </header>

  </div>
    </div>
</template>


<script>
export default {
    data() {
          return {
      menuOpen: false,
      readyToClose: false,
    }
  },

   methods: {

       goHome() {
        this.$router.push('/');
       },
       goContact() {
        this.$router.push('/contact');
       },
    openNav() {
      this.menuOpen = true
     setTimeout(() => {
          this.readyToClose = true
        }, 100);
    },
    }
}
</script>


<style lang="scss" scoped>

* {
  margin: 0;
  padding: 0;
}


.hamburger-menu{
   height: 100vh;
  /* background: #36393F;*/
  background: black;
  /* border-left: rgb(112, 112, 112) 1px solid;*/
   width: 100%;
   position: fixed;
   right: 0;
   transform: translateY(100%);
   transition: transform .3s linear;
   z-index: 99;
   overflow-y: scroll;
   &.open{
      transform: translateY(0);
   }
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
cursor: pointer;
width: 100px;
margin-top: -7px;
margin-right: 48px;
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


nav ul {
    position: fixed;
    width: 60%;
    top: 0;
    right: 0;
    text-align: left;
    background: #424242;
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
    background: #424242;
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
    nav ul {
        width: 40%;
    }

}
@media only screen and (min-width: 1024px)  {
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
        color: rgb(255, 255, 255);
        background-color: inherit;
        text-align: right;
        padding: 1em 2em;
    }

    nav ul li a:hover {
        background-color: inherit;
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

.nav-link-hover {
    cursor: pointer;
}


</style>