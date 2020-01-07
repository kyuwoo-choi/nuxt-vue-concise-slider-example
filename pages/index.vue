<template>
  <div class="carousel-wrapper">
    <client-only>
      <Slider :options="options">
        <SliderItem
          v-for="i in 5"
          :key="i"
          class="img-wrapper"
          style="width: 33.3%;"
        >
          <img :src="`https://picsum.photos/200/100?random=${i}`" />
        </SliderItem>
      </Slider>
    </client-only>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      options: {
        slidesToScroll: 3,
        loop: true
      }
    }
  }
}
</script>

<style>
.carousel-wrapper {
  padding: 40px;
  height: 180px;
}
.img-wrapper img {
  margin: auto;
  width: 200px;
  height: 100px;
  background-image: linear-gradient(gray 100%, transparent 0);
}
</style>
