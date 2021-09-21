<template>
  <main>
      <div id="container-main-top">
          <img src="@/assets/jumbotron.jpg" alt="">
      </div>
      <div id="container-main-central">
          <!-- CARICATO IMG DA data() -->
          <!-- <ul>
              <li v-for="(comic, index) in comics" :key="index">
                    <a>
                        <img src="" alt="">
                        {{ comic.thumb }}
                    </a>  
                    <a>
                       Ciao {{ comic.series }}
                    </a>
                </li>
            </ul> -->

            <!-- CARICATO TRAMITE CARTELLA DATA -->
            <div class="boxFumetti">
                <FumettiCard 
                v-for="(comic, index) in comics" 
                :key="index"
                :prod="comic"
                /> <!--prod/saluto = nome attributo -->
                <div class="containerButton">
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
            /*comics: [
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    price: "$19.99",
                    series: "Action Comics",
                    type: "comic book",
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    price: "$3.99",
                    series: "American Vampire 1976",
                    type: "comic book",
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    price: "$16.99",
                    series: "Aquaman",
                    type: "graphic novel",
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    price: "$2.99",
                    series: "Batgirl",
                    type: "comic book",
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    price: "$3.99",
                    series: "Batman",
                    type: "comic book",
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    price: "$2.99",
                    series: "Batman Beyond",
                    type: "comic book",
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    price: "$3.99",
                    series: "Batman/Superman",
                    type: "comic book",
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    price: "$4.99",
                    series: "Batman/Superman Annual",
                    type: "comic book",
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    price: "$5.99",
                    series: "Batman: The Joker War Zone",
                    type: "comic book",
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    price: "$6.99",
                    series: "Batman: Three Jokers",
                    type: "comic book",
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    price: "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    type: "comic book",
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                    price: "$16.99",
                    series: "Catwoman",
                    type: "graphic novel",
                },
            ]
        }*/
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
            height: 90vh;  
            position: relative;

            img {
            width: 100%;
            height: 100%;
            position: absolute;
            object-fit: cover;
            }
        }

        #container-main-central {
            width: 100%;
            height: 100%;
            background-color: black;
            position: relative;
            color: white;
            display: flex;
            justify-content: center;
            padding: 50px;

            .boxFumetti {
                width: 60%;
                

                h1 {
                    color: white;
                    padding: 50px;
                }
                .containerButton {
                display: flex;
                justify-content: center; 
                padding: 20px;
                }

                .buttonBlue {
                    width: 200px;
                    height: 50px;
                    color: white;
                    background-color: #0282F9;
                    text-align: center;
                    border: 2px #0282F9;
                    font-size: 20px;
                }
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
                width: 80%;
                height: 100%;
            }

            img {
                width: 80px;
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