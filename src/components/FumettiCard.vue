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
        float: left;
        padding: 10px;
    }
</style>