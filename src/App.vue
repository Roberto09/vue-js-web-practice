<template>
  <v-app>

      <NavBar />
  <v-card>
    <v-layout>
      <v-main>

      <CustomTitle title="My Pets App"/>
      <div class="text-h5">
        Some of the pets we like a lot are:
      </div>
      <CustomImg :picture="img_url" :picture_name="img_name"/>
      <CustomButton :on_click_func="changeImg" text="Next image!"/>
      <div class="text-h5" style="margin-top:50px">
        Things you must know about us:
      </div>
      <TextList :items="text_list"/>
      <div class="text-h5" style="margin-top:50px">
        How much do you like the following pets? Modve the sliders!
      </div>
      <LoveSlider what_to_love="perritos"/>
      <LoveSlider what_to_love="gatitos"/>
      <LoveSlider what_to_love="pescaditos"/>
      <div style="margin-top:50px; margin-bottom:50px">
        <div v-if="show_want_to_get" class="text-h5" style="margin-top:50px">
          Want to get a pet?
        </div>
        <CustomButton :on_click_func="toggleWantToGet" text="Toggle this!"/>
      </div>

      </v-main>

    </v-layout>
  </v-card>
  </v-app>

</template>

<script>
import NavBar from "./components/NavBar.vue"
import CustomTitle from "./components/CustomTitle.vue"
import CustomImg from "./components/CustomImg.vue"
import CustomButton from "./components/CustomButton.vue"
import TextList from "./components/TextList.vue"
import LoveSlider from "./components/LoveSlider.vue"
export default {
  name: 'App',
  components: {
    NavBar,
    CustomTitle,
    CustomImg,
    CustomButton,
    TextList,
    LoveSlider, 
  },
  data() {
    return {
      img_url : "https://www.elliotcolburn.co.uk/sites/www.elliotcolburn.co.uk/files/2020-09/Puppy.jpg",
      img_name : "Dog",
      img_to_show : 0,
      text_list : ["- We love pets!", "- We encourage adopting pets!", "- Our favorite pets are dogs, cats and fish!"],
      show_want_to_get : true,
    }
  },
  methods:{
    async changeImg(){
      console.log("changing image");
      this.img_to_show = (this.img_to_show + 1) % 3;
      let imgs = ["https://www.elliotcolburn.co.uk/sites/www.elliotcolburn.co.uk/files/2020-09/Puppy.jpg",
      "https://cdn.theatlantic.com/thumbor/vDZCdxF7pRXmZIc5vpB4pFrWHKs=/559x0:2259x1700/1080x1080/media/img/mt/2017/06/shutterstock_319985324/original.jpg",
      "https://images.unsplash.com/photo-1535591273668-578e31182c4f?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjM2NTI5fQ"];
      let img_names = ["Dog", "Cat", "Fish"];
      this.img_url = imgs[this.img_to_show];
      this.img_name = img_names[this.img_to_show]
    },
    async toggleWantToGet(){
      this.show_want_to_get = !this.show_want_to_get;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
