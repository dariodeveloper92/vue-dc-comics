<template>
  <div class="fumetti-card">
        <div class="boxImg">
          <img :src="prod.thumb" :alt="prod.series">
        </div>
        <div class="coverTitle">
            <div class="boxTitle">
                <h1 class="title"> {{ prod.series }} </h1>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'FumettiCard',
  props: ['prod']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .fumetti-card {
        width: calc(100% / 6);
        display: flex;
        justify-content: space-around;
        align-items: center;
        float: left;
        padding: 20px;
         
        .boxImg {
            display: flex;
            justify-content: flex-start;
                
            img {
                object-fit: cover;
                vertical-align: middle;
            }
        }
        .coverTitle {
            width: calc(100% / 6);
            display: flex;
            justify-content: center;
            align-items: flex-end;
            float: left;
            padding: 20px;
                    
            .boxTitle {
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: center;
            margin: 10px 5px;    
            }
        }
    }
</style>