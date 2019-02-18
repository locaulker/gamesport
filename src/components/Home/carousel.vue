<template>
  <div>
    <carousel
      :per-page="1"
      :mouse-drag="true"
      :paginationEnabled="false"
    >
      <slide v-for="(slide, index) in slides" :key="index">
        <div 
          class="slider_bck"
          :style="{'background': `url(${slide.bgImg})`}"
        >
          <!-- Display Title -->
          <div class="gradient">
            <div class="container">
              <div class="content">

                <app-button
                  type="link"
                  linkTo="#"
                  :addClass="['hello', 'there']"
                  :action="trigger"
                >
                  See Review
                </app-button>
                <div class="item">
                  {{ slide.title }}
                </div>

              </div>
            </div>
          </div>
          <!-- End Display Title -->

        </div>
      </slide>
    </carousel>
  </div>
</template>

<script>
  import { Carousel, Slide } from 'vue-carousel'
  import SlideOne from '../../assets/images/featured/1.jpg'
  import SlideTwo from '../../assets/images/featured/2.jpg'
  import SlideThree from '../../assets/images/featured/3.jpg'
  import SlideFour from '../../assets/images/featured/4.jpg'

  export default {
    data() {
      return {
        slides: [
          {
            title: 'Red Dead Redemption 2',
            bgImg: SlideOne
          },
          {
            title: 'Watchdogs 2',
            bgImg: SlideTwo
          },
          {
            title: 'Rise of the tomb rider',
            bgImg: SlideThree
          },
          {
            title: 'Spider-Man',
            bgImg: SlideFour
          }
        ]
      }
    },
    components: {
      Carousel,
      Slide
    }
  }
</script>