<template>
  <div>
    <v-container>
      <v-row align="center" justify="center">
        <v-col cols="12" class="text-center">
          <h1>ยินดีต้อนรับสู่ ชมรม SMC</h1>
        </v-col>
      </v-row>
      <v-row align="center" justify="center">
        <v-col cols="12" class="text-center">
          <h3>ภาพกิจกรรมของชมรม SMC</h3>
        </v-col>
        <v-col cols="12" sm="6" md="100" class="centered-container">
          <v-carousel cycle min-height="50vh" hide-delimiter-background show-arrows-on-hover>
            <v-carousel-item v-for="(item, i) in items" :key="i">
              <v-img :src="item.src" class="image-frame"></v-img>
            </v-carousel-item>
          </v-carousel>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'HomeView',
  data () {
    return {
      items: [
        {
          src: require('@/assets/picture/photo1.jpg')
        },
        {
          src: require('@/assets/picture/photo2.jpg')
        },
        {
          src: require('@/assets/picture/photo3.jpg')
        },
        {
          src: require('@/assets/picture/photo4.jpg')
        },
        {
          src: require('@/assets/picture/ชมรม smc.jpg')
        }
      ]
    }
  }
}
</script>

<style scoped>
.centered-container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 50vh;
}

.centered-row {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}
.image-frame {
  border: 2px solid #000;
  padding: 0px;
  margin: 0px;
  box-shadow: 0px 0px 0px rgba(0, 0, 0, 0);
  border-radius: 4px;
  width: 2000px;
  height: 100%;
  object-fit: cover;
}
</style>
