<template>
  <footer>
      <div id="container-footer-top">
          <div>
                <ul>
                    <li>
                        <a href="#">
                            <h2> DC COMICS </h2>
                            <h5> Characters </h5>
                            <h5> Comics </h5>
                            <h5> Movies </h5>
                            <h5> TV </h5>
                            <h5> Games </h5>
                            <h5> Videos </h5>
                            <h5> News </h5>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <h2> SHOP </h2>
                            <h5> Shop DC </h5>
                            <h5> Shop DC Collectibles </h5>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <h2> DC </h2>
                            <h5> Terms of Use </h5>
                            <h5> Privacy policy (New) </h5>
                            <h5> Ad Cholces </h5>
                            <h5> Advertising </h5>
                            <h5> Jobs </h5>
                            <h5> Subscriptions </h5>
                            <h5> Talent Workshops </h5>
                            <h5> CPSC Certificates </h5>
                            <h5> Ratings </h5>
                            <h5> Shop Help </h5>
                            <h5> Contact Us </h5>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <h2> SITES </h2>
                            <h5> DC </h5>
                            <h5> MAD Magazine </h5>
                            <h5> DC Kids </h5>
                            <h5> DC Universe </h5>
                            <h5> DC Power Visa </h5>
                        </a>
                    </li>
                </ul>
            </div>
        </div>
      <div id="container-footer-bottom">
          <div class="container-icons">
                <div class="button">
                    <button> SIGN-UP NOW! </button>
                </div>
                <ul>
                    <li>
                        <a href="#">
                            <h1> FOLLOW US </h1>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <img src="@/assets/footer-facebook.png" alt="logo facebook">
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <img src="@/assets/footer-twitter.png" alt="logo twitter">
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <img src="@/assets/footer-youtube.png" alt="logo youtube">
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <img src="@/assets/footer-pinterest.png" alt="logo pinterest">
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <img src="@/assets/footer-periscope.png" alt="logo periscope">
                        </a>
                    </li>
                </ul>
          </div>
       </div>
</footer>
</template>

<script>
export default {
  name: 'Footer',
    
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    footer {
        width: 100%;
        height: 100%;
        
        #container-footer-top {
            width: 100%;
            height: 80%;
            background-color: red;
            display: flex;
            
            ul {
                list-style: none;
                display: flex;
                float: left;
                ;

                li a {
                    display: inline-block;
                    padding: 1rem;
                    text-decoration: none;
                    font-weight: 600;
                    transition: color 0.3s;
                    color: #FFFFFF;
                }
            }
        }
        #container-footer-bottom {
            width: 100%;
            height: 20%;
            background-color: #303030;
            display: flex;
            
            .container-icons {
                width: 100%;
                height: 100%;
                display: flex;
                justify-content: space-between;
            }

            button {
                width: 200px;
                height: 50px;
                color: #FFFFFF;
                background-color: #303030;
                border: 2px solid #0282F9;
            }

            h1 {
                color: #0282F9;
            }

            .button, ul {
                padding: 20px 50px;
                text-align: center;
                display: flex;
                align-items: center;
            }

            ul {
                list-style: none;
                display: flex;
                float: left;
                
                li a {
                    display: inline-block;
                    padding: 1rem;
                    text-decoration: none;
                    font-weight: 600;
                    transition: color 0.3s;
                    color: #EC1F26;
                    
                }
            }
        }
    }
</style>