<template>
  <div>
    <div class="home-page">
      <mdb-container>
        <mdb-row class="justify-content-center mt-5">
          <h1>EAT FIT, KEEP FIT</h1>
        </mdb-row>

        <mdb-row>
          <mdb-col class="mt-5"> </mdb-col>
        </mdb-row>

        <mdb-row class="justify-content-center">
          <mdb-col>
            <h2>What We Offer <mdb-icon icon="check-double" /></h2>
            <p class="info">
              Trying to lose weight, keep fit, or eat healthy?<br />We provide
              you with the right features to reach your goals.
            </p>
          </mdb-col>
        </mdb-row>
        <mdb-row class="justify-content-center">
          <mdb-col lg="3">
            <mdb-icon
              icon="dumbbell"
              size="4x"
              class="teal-text mt-2 mr-4 ml-4 mb-2"
            />
            <mdb-row>
              <mdb-col>
                <p>Fitness plans crafted by professional fitness coaches</p>
              </mdb-col>
            </mdb-row>
          </mdb-col>
          <mdb-col lg="3">
            <mdb-icon
              icon="apple-alt"
              size="4x"
              class="teal-text mt-2 mr-4 ml-4 mb-2"
            />
            <mdb-row>
              <mdb-col>
                <p>Nutrition plans crafted by nutritionists</p>
              </mdb-col>
            </mdb-row>
          </mdb-col>
          <mdb-col lg="3">
            <mdb-icon
              icon="book"
              size="4x"
              class="teal-text mt-2 mr-4 ml-4 mb-2"
            />
            <mdb-row>
              <mdb-col>
                <p>
                  Healthy food recipes generated and customized to your tastes
                  and preferences
                </p>
              </mdb-col>
            </mdb-row>
          </mdb-col>
        </mdb-row>

        <mdb-row>
          <mdb-col class="mt-5"> </mdb-col>
        </mdb-row>

        <mdb-row>
          <mdb-col>
            <h2>User Stories</h2>
            <p>What our users say after using homefit+diet!</p>

            <mdb-row class="justify-content-center">
              <mdb-carousel
                :items="3"
                indicators
                indicatorsColor="secondary-color"
                slide
              >
                <template #[i+1] v-for="(item, i) in stories">
                  <mdb-card :key="i" class="w-50 text-center mx-auto p-2">
                    <mdb-row>
                      <mdb-card-image
                        :src="item.img"
                        class="img w-75 text-center mx-auto mt-2"
                      ></mdb-card-image>
                    </mdb-row>
                    <br />
                    <mdb-row>
                      <mdb-card-body color="warning">
                        <mdb-card-title class="black-text">{{
                          item.title
                        }}</mdb-card-title>
                        <mdb-card-text class="black-text"
                          ><mdb-icon icon="quote-left" size="3x" />
                          {{ item.text }}</mdb-card-text
                        >
                        <br />
                      </mdb-card-body>
                    </mdb-row>
                  </mdb-card>
                </template>
              </mdb-carousel>
            </mdb-row>
          </mdb-col>
        </mdb-row>

        <mdb-row>
          <mdb-col class="mt-5"> </mdb-col>
        </mdb-row>

        <mdb-row>
          <mdb-col>
            <h2>Food Gallery</h2>
            <p>Our users' very own healthy creations!</p>

            <mdb-row class="justify-content-center">
              <mdb-carousel
                :interval="8000"
                slide
                :items="foodGallery"
                controlls
                indicators
              ></mdb-carousel>
            </mdb-row>
          </mdb-col>
        </mdb-row>

        <mdb-row>
          <mdb-col class="mt-5"> </mdb-col>
        </mdb-row>
      </mdb-container>
    </div>
  </div>
</template>

<script>
import firebase from "../firebase";
export default {
  name: "HomePage",
  components: {},
  data() {
    return {
      stories: [
        {
          title: "HF+D Helped me to stay fit!",
          img: "/images/User1.jpg",
          text:
            "Homefit+diet provided me with fitness and nutrition plans to stay healthy during the circuit breaker period!",
        },
        {
          title: "Trusted fitness & nutrition website",
          img: "/images/User2.jpg",
          text:
            "Homefit+diet provided me with fitness and nutrition plans to stay healthy during the circuit breaker period!",
        },
        {
          title: "Trusted fitness & nutrition website",
          img: "/images/User3.jpg",
          text:
            "Homefit+diet provided me with fitness and nutrition plans to stay healthy during the circuit breaker period!",
        },
      ],
      foodGallery: [
        {
          img: true,
          src:
            "https://mdbootstrap.com/img/Photos/Horizontal/Food/4-col/img%20(53).jpg",
          mask: "black-slight",
        },
        {
          img: true,
          src:
            "https://mdbootstrap.com/img/Photos/Horizontal/Food/4-col/img%20(45).jpg",
          mask: "black-slight",
        },
        {
          img: true,
          src:
            "https://mdbootstrap.com/img/Photos/Horizontal/Food/4-col/img%20(51).jpg",
          mask: "black-slight",
        },
        {
          img: true,
          src: "/images/food4.jpg",
          mask: "black-slight",
        },
        {
          img: true,
          src: "/images/food5.jpg",
          mask: "black-slight",
        },
        {
          img: true,
          src: "/images/food6.jpg",
          mask: "black-slight",
        },
      ],
    };
  },
};
</script>

<style scoped>
h2 {
  font-size: 30pt;
  font-family: Impact;
  margin-top: 50pt;
}

h1 {
  font-size: 100pt;
  font-family: Impact;
}
</style>
