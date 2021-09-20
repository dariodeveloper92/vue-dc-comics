<template>
    <header>
        <div id="container-header">
            <a href="/">
                <img src="@/assets/dc-logo.png" alt="logo dc">
            </a>

            <nav>
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a :class="(link.current)" href="link.url">
                            {{ link.text }}
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
  name: 'Header',
    
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false,
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: false,
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false,
                },
                {
                    text: "TV",
                    url: "#",
                    current: false,
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false,
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false,
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false,
                },
                {
                    text: "COMFANSICS",
                    url: "#",
                    current: false,
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false,
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false,
                },
            ]
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    header {
        width: 100%;
        height: 10vh;

        #container-header {
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: space-around;

            img {
                width: 100%;
                height: 100%;
            }

            img, nav {
                float: left;
                display: flex;
            }

            ul {
                list-style: none;
                display: flex;

                li a {
                    display: inline-block;
                    padding: 1rem;
                    text-decoration: none;
                    font-weight: 600;
                    transition: color 0.3s;
                    float: left;

                    &:hover,
                    &:active {
                        color: blue;
                    }
                }
            }
            
        }   

    }

    
</style>