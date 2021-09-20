<template>
  <main>
      <div id="container-main-top">
          <h1> --> Content goes here -- </h1>
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
export default {
  name: 'Main',
    
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    main {
        width: 100%;
        height: 100%;

        #container-main-top {
            width: 100%;
            height: 100%;
            background-color: black;
            display: flex;
            

            h1 {
                color: white;
                padding: 50px;
            }
        }
        #container-main-bottom {
            width: 100%;
            height: 100%;
            background-color: #0282F9;
            display: flex;
            justify-content: center;
            
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