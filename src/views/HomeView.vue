<template>
  <div class="home">
    <div class="gradient-background"></div>
    <div class="gradient-background-overlay"></div>
    <div class="home-container">
     <div class="section-01">
      <div class="section-01-container">
        <div class="img-container">
          <img :src="images.furniture" alt="" id="furniture" >
        </div>
        <div class="menu">
          <a href="">Objects </a>
          <a href="">Our Gallery </a>
          <a href="">About </a>
          <a href="">Contacts </a>
        </div>      
        <div class="icon">
          <div class="icon-container">
            <i class="fa-solid fa-cubes"></i>
            <p>Design <br /> Award</p>
            <p class="arrow"><i class="fa-solid fa-arrow-right"></i></p>
          </div>
        </div>  
      </div>
     </div>
     <div class="section-02">
      <div class="section-02-container">
        <div class="logo">
          <i class="fa-solid fa-xmarks-lines"></i>
        </div>
        <div class="search">  
          <div class="search-container">
            <i class="fa-solid fa-magnifying-glass"></i>
            <input type="text" placeholder="Search.." name="search">
          </div>        
        </div>
        <div class="gallery">
          <div class="gallery-container">
            <i class="fa-solid fa-table-cells-large"></i>
            <p>Our <br /> gallery</p>
          </div>
        </div>
        <div class="title">
          <div class="Title"><p>Furniture & </p></div>
          <div class="Title"><p>interior design</p></div>
          <div class="text">
            <p>Founded in 2017 by Terence Ngan, the studio is accustomed to creating remarkable environments.</p>            
          </div>
        </div>
        <div class="year">
          <h1>2017</h1>
          <p>Since</p>
        </div>
        <div class="dispImage">
          <div class="disp-image-container">            
            <scroll-parallax speed=0.1>
              <div class="image-one">
                <img :src="images.wood" alt="wood" id="wood" />
              </div>
              <div class="image-two">
                <img :src="images.portrait" alt="portrait" id="portrait" />
              </div>
            </scroll-parallax>
          </div>
        </div>
        <div class="title2">
          <div class="Title"><p>Objects</p></div>
          <div class="text">
            <p>We are motivated by pushing the possibilities of form and exploring differnent techniques to challenge what exists.</p>            
          </div>
          <button>
            <div class="ps">
              <p>Explore</p> <p>Explore</p> <p>Explore</p>
            </div>
          </button>
        </div>
      </div>
     </div>
      <div class="section-03"  @mouseenter="expand()">
        <div class="background-02">
          <img :src="images.background" alt="" id="background-02" />
          <div class="overlay" @click="close()"></div>
        </div>
        <div class="section-03-container">
          <div class="carousel">
            <div class="carousel-tag">
              <h2>our <br />gallery</h2>
              <p>
                Designers can use photo rooms as repiration for their next project. 
                This will allow them to create a superior interior
              </p>
            </div>
            <div class="carousel-cont " v-for="(item) in items" :key="item.id" :id="item.id" @click="getId(item.id)">
              <div class="carousel-items">
                <img :src="item.img" alt="" >
                <div class="details">
                  <p class="name">{{item.name}}</p>
                  <p class="price">${{item.price}}</p>
                </div>
              </div>
            </div>
              <div class="expand-carousel-item">
              </div>
          </div>
        </div>
      </div>
      <div class="section-04">
        <div class="section-04-cont">
          <div class='column-01'>
            <h1>JUO</h1>
            <h3>Studio</h3> 
          </div>
          <div class='column-02'>
            <div class="title" >
              <h1>About</h1>
            </div>
            <div class="text" >
              <p>An expandned design studio with a main stage and loft offer customers a space to show their furniture design ideas, and
                access a design team who work closely with them to develop their unique vision fo their space.
              </p>
          </div>            
            <button>
              <div class="ps">
                <p>Explore</p> <p>Explore</p> <p>Explore</p>
              </div>
            </button>       
            <div class="dispImage">
              <div class="disp-image-container">
                <div class="image-one">
                  <img :src="images.wood" alt="wood" id="wood" />
                </div>
                <div class="image-two">
                  <img :src="images.portrait" alt="portrait" id="portrait" />
                </div>
              </div>
            </div>
          </div>
          <div class="column-03">   
            <div class="img-container">
              <img :src="images.furniture" alt="" id="furniture" >
            </div>  
          </div>
        </div>
      </div>
      <div class="section-05">
        <div class="section-05-container">
          <div class="row-01">
            <div class="title">
              <div class="title-cont">
                <p>Let's have  a chat!</p>
                <p>Let's have  a chat!</p>
              </div>
            </div>
          </div>
          <div class="row-02">
            <div class="column-01">
              <div class="logo">
                <p>Juo</p>
              </div>
              <p>The addition of larger design sutdios, offering customers private space</p>
            </div>
            <div class="columns 02">
              <div class="logo">
                <p>Sitemap</p>
              </div>
              <div class="list">
                <p>Objects</p>
                <p>About</p>
                <p>Our gallery</p>
                <p>Contacts</p>
              </div>
            </div>
            <div class="columns 03">
              <div class="logo">
                <p>Contact</p>
              </div>
              <div class="list">
                <p>www.halo-lab.com</p>
                <p>UK: +38 0665438912</p>
                <p>mail@halo-lab.com</p>
                <p>Ukraine, Odessa, 65058</p> 
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="footer">
        <div class="left">
          <p id="logo">Juo</p>
          <div class="text">
            <p>2021 Halo Lab</p>
            <p>	&copy; All right reserved</p>
          </div>
        </div>
        <div class="right">
          <a href=""><i class="fa-brands fa-facebook-f"></i></a>
          <a href=""><i class="fa-brands fa-facebook-f"></i></a>
          <a href=""><i class="fa-brands fa-facebook-f"></i></a>
          <a href=""><i class="fa-brands fa-facebook-f"></i></a>
          <a href=""><i class="fa-brands fa-facebook-f"></i></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ScrollParallax from 'vue3-parallax/src/components/ScrollParallax.vue';

export default {
  name: 'HomeView',
  components: {
    ScrollParallax
  },
  data () {
    return  {
      images: {
        wood: 'https://images.unsplash.com/photo-1586023492125-27b2c045efd7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2158&q=80',
        furniture: 'https://images.unsplash.com/photo-1567016520496-0cb37d8467a7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=880&q=80',
        portrait: 'https://images.unsplash.com/photo-1531384441138-2736e62e0919?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1974&q=80',
        background: 'https://images.unsplash.com/photo-1638962502979-05d81dcaa096?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1577&q=80',

      },
      items: [
        {
          id: 1,
          img: 'https://images.unsplash.com/photo-1543512214-4f76e81f8bfc?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80',
          name: 'Shaken Lamp',
          price: 1900,
          weight: '8kg',
          material: '95% polystar, Solid Wood',
          color: 'Bruh Green',
          catridge: 'E14',
          about: 'We are motivated by pushing the possibilities of form and exploring different techniques to challenge what exists of form exploring different techniques to challenge.'
        },
        {
          id: 2,
          img: 'https://images.unsplash.com/photo-1543512214-4f76e81f8bfc?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80',
          name: 'Shaken Lamp',
          price: 2900,
          weight: '8kg',
          material: '95% polystar, Solid Wood',
          color: 'Bruh Green',
          catridge: 'E14',
          about: 'We are motivated by pushing the possibilities of form and exploring different techniques to challenge what exists of form exploring different techniques to challenge.'
        },
        {
          id: 3,
          img: 'https://images.unsplash.com/photo-1543512214-4f76e81f8bfc?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80',
          name: 'Shaken Lamp',
          price: 3900,
          weight: '8kg',
          material: '95% polystar, Solid Wood',
          color: 'Bruh Green',
          catridge: 'E14',
          about: 'We are motivated by pushing the possibilities of form and exploring different techniques to challenge what exists of form exploring different techniques to challenge.'
        },
        {
          id: 4,
          img: 'https://images.unsplash.com/photo-1543512214-4f76e81f8bfc?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80',
          name: 'Shaken Lamp',
          price: 900,
          weight: '8kg',
          material: '95% polystar, Solid Wood',
          color: 'Bruh Green',
          catridge: 'E14',
          about: 'We are motivated by pushing the possibilities of form and exploring different techniques to challenge what exists of form exploring different techniques to challenge.'
        },
        {
          id: 5,
          img: 'https://images.unsplash.com/photo-1543512214-4f76e81f8bfc?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80',
          name: 'Shaken Lamp',
          price: 900,
          weight: '8kg',
          material: '95% polystar, Solid Wood',
          color: 'Bruh Green',
          catridge: 'E14',
          about: 'We are motivated by pushing the possibilities of form and exploring different techniques to challenge what exists of form exploring different techniques to challenge.'
        },
        {
          id: 6,
          img: 'https://images.unsplash.com/photo-1543512214-4f76e81f8bfc?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80',
          name: 'Shaken Lamp',
          price: 900,
          weight: '8kg',
          material: '95% polystar, Solid Wood',
          color: 'Bruh Green',
          catridge: 'E14',
          about: 'We are motivated by pushing the possibilities of form and exploring different techniques to challenge what exists of form exploring different techniques to challenge.'
        },
        {
          id: 7,
          img: 'https://images.unsplash.com/photo-1543512214-4f76e81f8bfc?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687&q=80',
          name: 'Shaken Lamp',
          price: 900,
          weight: '8kg',
          material: '95% polystar, Solid Wood',
          color: 'Bruh Green',
          catridge: 'E14',
          about: 'We are motivated by pushing the possibilities of form and exploring different techniques to challenge what exists of form exploring different techniques to challenge.'
        } 
      ],
      activeId : null,
      indexHistory: [],
    }
  },
  created () {
  },
  methods: {
    //Algorithim that manipulates an item in a list
    getId(id) {
      this.activeId = id
      this.indexHistory.push(id)
      document.querySelector('.overlay').style.zIndex = 3
      for(var i = 0; i <= this.items.length; i++) {
        if(i == id) {
          document.getElementById(`${i}`).classList.add('active')
          //document.getElementById(`${i}`).style.transform = `translateX(-${i * 50}%)`
        } else if (this.indexHistory.includes(i)) {
          document.getElementById(`${i}`).classList.remove('active')
          console.log(i)
        }
      }
    },
    expand () {

    },
    close ()  {
      document.querySelector('.overlay').style.zIndex = 2
          document.getElementById(`${this.activeId}`).classList.remove('active')
      document.querySelector('.carousel-cont').style.transform = `none`
    }
  }
}
</script>

<style lang="scss" scoped>
  @mixin scrollbars($size, $foreground-color, $background-color: mix($foreground-color, white,  50%)) {
  // For Google Chrome
  &::-webkit-scrollbar {
    width:  $size;
    height: $size;
  }

  &::-webkit-scrollbar-thumb {
    background: $foreground-color;
  }

  &::-webkit-scrollbar-track {
    background: $background-color;
  }

  // For Internet Explorer
  & {
    scrollbar-face-color: $foreground-color;
    scrollbar-track-color: $background-color;
  }
}
@keyframes gradient-animation {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}
@keyframes curtain {
  0% {
    transform: scaleY(0);
    transform-origin: 50% 0%;    
  }
  100% {
    transform: scaleY(1);
    transform-origin: 50% 0%;  
  }
}
@keyframes curtain2 {
  0% {
    transform: scaleY(0);
    transform-origin: 50% 0%;    
  }
  100% {
    transform: scaleY(1);
    transform-origin: 50% 0%;  
  }
}
@keyframes right-left {
  0% {
    transform: translateX(200%);
  }
  100% {
    transform: translateX(0%);
  }
}
@keyframes left-right {
  0% {
    transform: translateX(-200%);
  }
  100% {
    transform: translateX(0%);
  }
}
@keyframes lefty-right {
  0% {
    transform: scaleX(0);
    transform-origin: 0% 50%;
  }
  100% {
    transform: scaleX(1);
    transform-origin: 0% 50%;
  }
}
@keyframes button-caruos {
  0% {
    transform: translateX(0%);
  }
  50% {
    transform: translateX(-140%);
  }
  100% {
    transform: translateX(-280%);
  }
}
@keyframes down-up {
  0% {
    transform: translateY(200%);
  }
  100% {
    transform: translateY(0%);
  }
}
@keyframes appear {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

        button {
          padding: 3% 5%;
          width: 25%;
          overflow: hidden;
          outline: none;
          border: none;
          cursor: pointer;
          .ps {
            display: flex;
            transform: translateX(0%);
            p {
              font-size: 18px;
              margin: 0 35% 0 10%;
              font-weight: bold;
            }
          }
        }
        button:hover {
          .ps {            
            animation: button-caruos 2s alternate infinite ease;
          }
        }
.home {
  width: 100%;
  height: 100%;
  position: relative;
}
  .gradient-background {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(232deg,#000000,#000000,#ff292d, #ff292d,#42e9ff,#42e9ff);
    background-size: 300% 300%;
    animation: gradient-animation 20s ease infinite;
    z-index: 0;
  }
  .gradient-background-overlay {
    position: fixed;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    background: rgba(0, 0, 0, 0.5);
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
  }
.home-container {
  width: 90%;
  margin: 2% auto;
  position: relative;
  z-index: 1;
  .section-01 {
    position: absolute;
    margin-top: -6%;
    width: 40vw;
    height: 50vh;
    right: 0;
    z-index: 2;
    .section-01-container {
      position: relative;
      width: 100%;
      height: 100%;
    }
    .img-container {
      width: 100%;
      height: 100%;
      position: absolute; 
      top: -20%;
      img {
        width: 100%;
        animation: curtain 450ms;
        position: relative;
        z-index: 0;
        box-shadow: rgba(0, 0, 0, 0.3) 50px 50px 35px 10px, rgba(0, 0, 0, 0.05) 0px 4px 6px -2px;
      }
    }
    .menu {
      position: absolute;
      display: flex;
      right: 5%;
      top: 15%;
      flex-direction: column;
      justify-content: right;
      overflow: hidden;
      a {
        text-decoration: none;
        color: #fff;
        font-weight: bolder;
        text-align: right;
        text-transform: uppercase;
        margin: 5% 0%;
      }
      a::before {
        content: '';
        position: absolute;
        width: 0%;
        border-bottom: 3px solid #fff;
        height: auto;
        margin-top: 10%;
        margin: 5%;
        margin-left: -10%;
        transform: scale(1);
        transform-origin: 0% 0%;
        transition: all 450ms;
      }
      a:hover::before {
        width: 110%;
        border-bottom: 3px solid #fff;
        transform: scale(1);
        transform-origin: 0% 0%;
        transition: all 450ms;
      }      
      a:nth-child(1){
        animation: right-left 450ms ease-out;        
      }
      a:nth-child(2){
        animation: right-left 800ms ease-out;        
      }
      a:nth-child(3){
        animation: right-left 1200ms ease-out;        
      }
      a:nth-child(4){
        animation: right-left 1400ms ease-out;        
      }
    }
    .icon {
      position: absolute;
      width: 7vw;
      height: 12vh;
      bottom: -5%;
      right: 12%;
      .icon-container {
        position: relative;
        text-align: left;
        height: 100%;
        width: 100%;
        padding: 15%;
        padding-right: 0%;
        background-color: rgb(255, 47, 47);
        animation: curtain2 450ms;
        transition: height 450ms;
        cursor: pointer;
        i {
          font-size: 40px;
          transform: scaleY(-1);
          animation: appear 2s ;
          margin-bottom: 25%;
        }
        p {
          font-size: 20px;
          text-transform: uppercase;
          animation: appear 2s ;
          margin: 0;
        }
        .arrow {
          width: 50%;
          margin: auto;
          margin-top: 15%;
          transform: rotate(-45deg);
          display: none;
          opacity: 0;
          transition: all 450ms;
        }
      }
      .icon-container:hover {
        height: 170%;
        transition: height 450ms ;
        .arrow {
          display: block;
          opacity: 1;
          transition: all 450ms;
        }
      }
    }
  }
  
  .section-02 {
    position: relative;
    width: 100%;
    height: 100vh;
    display: block;
    margin-bottom: 10%;
    .section-02-container {
      position: relative;
      display: grid;
      width: 100%;
      height: 100%;
      grid-template-columns: .8fr 1.5fr 1.5fr;
      grid-template-rows: 1fr 1.5fr 2fr 2fr;
      grid-template-areas: 
      "logo   search  empty"
      "gallery  title  title"
      "gallery  title  title"
      "sidebar img   title2";
      text-align: left;
      .logo {
        grid-area: logo;
        overflow: hidden;
        cursor: pointer;
        i {
          font-size: 50px;
          animation: lefty-right 450ms;
        }
      }
      .search {
        grid-area: search;
        width: 60%;
        cursor: pointer;
        animation: appear 1s;
        .search-container {
          padding-bottom: 5%;
          border-bottom: 2px solid #fff;
        }
        input {
          background-color: transparent;
          border: none;
          font-size: 20px;
          padding-left: 5%;
          color: #fff;
        }
        input:focus {
          border: none;
          outline: none;
        }
        i { 
          font-size: 20px;
          margin: 0;     
        }
      }
      .gallery {
        grid-area: gallery; 
        cursor: pointer;
        .gallery-container {
          overflow: hidden;
        }
        i {
          font-size: 45px;
          animation: left-right 450ms;
        }
        p { 
          text-transform: uppercase;
          font-size: 18px;
          animation: left-right 450ms;
        }
      }
      .title {
        grid-area: title; 
        .Title {
          font-size: 95px;
          height: auto;
          overflow: hidden;
          position: relative;
          z-index: 2;
          p {
            margin: 0;
            animation: down-up 450ms;
          }
        } 
        .text {
          width: 35%;
          font-size: 18px;          
          overflow: hidden;
          p {
            animation: left-right 450ms;
          }
        }
      }
      .year {        
        grid-area: sidebar;
        h1 {
          margin: 0;
        }
        p {
          margin: 0;
          margin-top: 2%;
          text-transform: uppercase;
          font-size: 18px;
        }
      }
      .dispImage {
        grid-area: img;
        position: relative;
        .disp-image-container {
          .image-one {
            position: absolute;
            width: 100%;
            left: 0;
            img {
              width: 85%;
              animation: curtain 450ms ;
            }
          }
          .image-two {
            position: absolute;
            width: 50%;
            right: -5%;
            img {
              margin-top: 40%;
              width: 80%;
            }
          }
        }
      }
      .title2 {
        grid-area: title2;
        margin-left: 10%;
        .Title {
          font-size: 95px;
          height: auto;
          overflow: hidden;
          position: relative;
          z-index: 2;
          p {
            margin: 0;
            animation: down-up 450ms;
          }
        } 
        .text {
          margin: 5% 0;
          width: 80%;
          font-size: 18px;          
          overflow: hidden;
          p {
            animation: down-up 450ms;
          }
        }
        button {
          padding: 3% 5%;
          width: 25%;
          overflow: hidden;
          outline: none;
          border: none;
          cursor: pointer;
          .ps {
            display: flex;
            transform: translateX(0%);
            p {
              font-size: 18px;
              margin: 0 35% 0 10%;
              font-weight: bold;
            }
          }
        }
        button:hover {
          .ps {            
            animation: button-caruos 2s alternate infinite ease;
          }
        }
      }
    }
  }

  .section-03 {
    position: relative;
    width: 100vw;
    height: 100vh;
    margin-top: 25%;
    z-index: 1;
    .background-02 {
      width: 100vw;
      height: 100%;
      position: absolute;
      left: -6%;
      img {
        width: 100vw;
        height: 100%;
      }
      .overlay {
        width: 100vw;
        position: absolute;
        height: 100%;
        top: 0;
        background: rgba(0, 0, 0, 0.3);
        backdrop-filter: blur(3px);
      }
    }
    .section-03-container {
      z-index: 2;
      width: 100%;
      overflow-x: hidden;
      height: 100%;
      @include scrollbars(.5em, rgb(17, 111, 205));
      .carousel {
        position: relative;
        z-index: 2;
        display: flex;
        width: 250%;
        overflow-x: scroll;
        .carousel-tag {          
          position: relative ;
          z-index: 2;
          background-color: rgb(255, 47, 47);
          width: 5.2%;
          height: 100%;
          margin-right: 1%;
          text-align: left;
          padding: .3%;
          h2 {
            text-transform: uppercase;
          }
          p {
            font-size: 20px;
          }
        }
        .carousel-cont {
          position: relative;
          z-index: 2;
          width: 6%;
          margin: 2% 3%;
          transition: all 450ms;
          cursor: pointer;      
          .carousel-items {
            width: 100%;
            background-color: #fff;
            color: #000;
            padding: 5%;
            img {
              width: 100%;
            }
            .details {
              display: flex;
              justify-content: left;
              position: relative;
              text-align: left;
              .name{ 
                margin-left: 0%;
              }
              .price{ 
                position: absolute;
                right: 0%;
                color: red;
              }
            }
          }  
        }
        .carousel-cont.active {
          position: absolute;
          margin-top: 7%;
          left: 0;
          z-index: 5;
          transition: all 450ms;
          .carousel-items {
            background-color: rgb(0, 126, 194);
          }
        }
        .carousel-cont:nth-child(odd) {
          margin-top: 4%;
        }
      }
    }
  }
  .section-04 {
    position: relative;
    width: 100%;
    height: 70vh;
    .section-04-cont {
      position: absolute;
      width: 100vw;
      margin-left: -10%;
      padding: 5% 10%;
      padding-right: 0;
      height: 100%;
      background-color: #fff;
      display: flex;
      color: #000;
      .column-01 {
        width: 20%;
        display: flex;
        flex-direction: column;
        text-align: left;
        overflow: hidden;
        h1, h3 {
          margin: 0;
          color: #000;
          text-transform: uppercase;
          animation: left-right 450ms;
        }
        h1{
          font-size: 50px
        }
        h3 {
          font-size: 20px;
          font-weight: lighter;
          color: grey;
        }
      }
      .column-02 {
        display: flex;
        flex-direction: column;
        width: 30%;
        text-align: left;
        .text,.title {
          overflow: hidden;
        }
        h1 {
          font-size: 70px;
          font-weight: bolder;
          margin: 0;
          margin-bottom: 10%;
          animation: down-up 450ms;
        }
        p {
          font-size: 20px;
          color: grey;
          animation: down-up 450ms;
        }
        button {
          margin: 10% 0;
          width: 35%;
          background-color: #000;
          .ps {
            p {
              color: white;
            }
          }
        }
      .dispImage {
        position: relative;
        .disp-image-container {
          .image-one {
            position: absolute;
            width: 100%;
            left: 0;
            img {
              width: 85%;
              animation: curtain 450ms ;
            }
          }
          .image-two {
            position: absolute;
            width: 50%;
            right: -5%;
            img {
              margin-top: -10%;
              width: 80%;
              animation: curtain 450ms ;
            }
          }
        }
      }
      }
      .column-03 {
        position: relative;
        .img-container {
          margin-left: 45%;
          overflow: hidden;
          img {
            width: 54vw;
            margin-top: -30%;
            transform: scaleX(-1);
          }
        }
      }
    }
  }
  .section-05 {
    margin-top: 25%;
    .section-05-container {      
      display: flex;
      flex-direction: column;
      text-align: left;
      .row-01 {
        width: 100%;
        border-bottom: 1px solid #fff;
        .title {
          height: 120px;
          overflow: hidden;
          .title-cont {
            margin-top : 0px;
            transition: all 450ms ease;
          }
          p {
            font-size: 80px;
            margin: 2% 0;
            cursor: pointer;
          }
        } 
        .title:hover {
          .title-cont {
            margin-top : -120px;
            transition: all 450ms ease;
          }
        }
      }
      .row-02 {
        margin-top:5%;
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        .column-01 {
          display: flex;
          flex-direction: column;
          .logo {
            p {
              width: fit-content;
              background-color: #fff;
              color: #000;
              text-transform: uppercase;
              padding: 2% 5%;
              font-size: 30px;
              font-weight: bolder;
              cursor: pointer;
            }
          }
          p {
            width: 45%;
            font-size: 18px; 
          }
        }
        .columns {
          .logo {
            p {
              font-size: 30px;
              padding: 2% 0%;    
              cursor: pointer;       
            }
          }
          p{ 
            font-size: 18px;
            cursor: pointer;
          }
          .list {
            display: grid;
            grid-template-columns: 1fr 1fr;
            p {
              cursor: pointer;
            }
          }
        }
      }
    }
  }
  .footer {
    display: flex;
    width: 100%;
    margin-top: 5%;
    .left {
      display: flex;
      align-items: center;
      width: 50%;
      #logo {
        background-color: #000;
        color: #fff;
        text-transform: uppercase;
        height: auto; 
        border-radius: 50%;
        width: 10%;
        padding: 4% 0%;
      }
      .text {
        margin-left: 2%;
        width: 100%;
        text-align: left;
        p {
          margin: 5px 0;
          font-weight: lighter;
        }
      }
    }
    .right {
      display: flex;
      align-items: center;
      margin-left: 20%;
      a {
          padding: 12px 14px;
          color: #fff;
          border: 1px solid #fff;
          margin: 10px;
      }
      a:nth-child(even) {
        rotate: 180deg;
      }
    }
  }
}
</style>
