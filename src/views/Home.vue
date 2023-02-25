<template>
  <div class="home">
    <h1>Videos</h1>

    <div class="video-container">
      <div v-for="video in videos" :key="video">
        <div class="video-box">
          <img :src="video.thumbnail"/>
          <div>
            <h3>{{video.name}}</h3>
            <div v-html="video.description"></div>
          </div>
        </div>

      </div>
    </div>

  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {

  },
  data() {
    return {
      img: require("@/assets/dog.jpeg"),
      videos: [
        {
          name: "1",
          description: "<p>thjfuydghdjdhdgdhyyhfhjfhf</p>",
          thumbnail: require("@/assets/dog.jpeg")
        },
        {
          name: "2",
          description: "",
          thumbnail: require("@/assets/roadView.mp4")
        },
        {
          name: "3",
          description: "",
          thumbnail: require("@/assets/noStress.mp4")
        },
        {
          name: "4",
          description: "",
          thumbnail: require("@/assets/roadView.mp4")
        },
        {
          name: "5",
          description: "",
          thumbnail: require("@/assets/dog.jpeg")
        },
        {
          name: "6",
          description: ""
        },
        {
          name: "7",
          description: ""
        },
        {
          name: "8",
          description: ""
        },
        // {
        //   name: "",
        //   description: ""
        // }
      ]

    }
  }
}
</script>

<style scoped>
.video-box {
  border: 1px solid black;
  border-radius: 10px;
  margin: 10px;
  padding: 10px;

  text-align: left;

  display: flex;
  justify-content: flex-start;

}

img {
  max-height: 150px;
  padding: 10px;
}

</style>
