<template>
  <main>
      <div id="container-main-top">
          <img src="@/assets/jumbotron.jpg" alt="">
      </div>
      <div id="container-main-central">
          <div class="buttonTop">
              <button class="buttonBlue"> CURRENT SERIES</button>
          </div>
          <!-- CARICATO TRAMITE CARTELLA DATA -->
            <div class="boxFumetti">
                <FumettiCard 
                v-for="(comic, index) in comics" 
                :key="index"
                :prod="comic"
                /> <!--prod/saluto = nome attributo -->
                <div class="buttonBottom">
                    <button class="buttonBlue"> LOAD MORE </button>
                </div>
            </div>
      </div>
      <div id="container-main-bottom">
          <div class="container-icons">
              <ul>
                  <li>
                        <a href="#">
                            <img src="@/assets/buy-comics-digital-comics.png" alt="logo dc">
                            <p>DIGITAL COMICS</p>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <img src="@/assets/buy-comics-merchandise.png" alt="logo merchandise">
                            <p>DC MERCHANDISE</p>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <img src="@/assets/buy-comics-subscriptions.png" alt="">
                            <p>SUBSCRIPTON</p>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <img src="@/assets/buy-comics-shop-locator.png" alt="">
                            <p>COMIC SHOP LOCATOR</p>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <img src="@/assets/buy-dc-power-visa.svg" alt="">
                            <p>DC POWER VISA</p>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </main>
</template>

<script>
import FumettiCard from '@/components/FumettiCard.vue'
import Fumetti from '@/data/Fumetti.js'
export default {
  name: 'Main',
  components: {
      FumettiCard
  },
  data() {
        return {
            comics: Fumetti,
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    main {
        width: 100%;
        height: 100%;

        #container-main-top {
            width: 100%;
            height: 70vh;  
            position: relative;

            img {
            width: 100%;
            height: 162%;
            position: absolute;
            object-fit: cover;
            }
        }

        #container-main-central {
            width: 100%;
            height: 100%;
            background-color: #232323;
            position: relative;
            color: white;
            display: flex;
            justify-content: center;
            padding: 50px;

            .buttonTop {
                position: relative;
                bottom: 75px;
                left: 150px;
            }

            .boxFumetti {
                width: 100%;
                
                h1 {
                    color: white;
                    padding: 0px;
                }
            }
                .buttonBottom {
                width: 100%;
                display: flex;
                justify-content: center; 
                padding: 5px;
                }

                .buttonBlue {
                    width: 160px;
                    height: 40px;
                    color: white;
                    background-color: #0282F9;
                    text-align: center;
                    border: 2px #0282F9;
                    font-size: 15px;
                }
        }
        #container-main-bottom {
            width: 100%;
            height: 100%;
            background-color: #0282F9;
            display: flex;
            justify-content: center;
            position: relative;
            
            .container-icons {
                width: 100%;
                height: 20vh;
                display: flex;
                justify-content: center;
                align-items: center;
            }

            img {
                width: 70px;
                height: 80px;
                object-fit: contain;
            }

            img, ul {
                list-style: none;
                display: flex;
                float: left;
                padding: 10px 10px;

                li a {
                    display: inline-block;
                    padding: 1rem;
                    text-decoration: none;
                    font-weight: 600;
                    transition: color 0.3s;
                    color: white;
                    display: flex;
                    align-items: center;
                }
            }
        }
        
    }
</style>