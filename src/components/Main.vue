<template>
  <main>
      <div id="container-main-top">
          <h1> --> Content goes here -- </h1>
      </div>
      <div id="container-main-bottom">
          
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
            height: 10vh;
            background-color: black;
            display: flex;

            h1 {
                color: white;
            }
        }
        #container-main-bottom {
            width: 100%;
            height: 10vh;
            background-color: blue;
            display: flex;
        }
        
    }
</style>