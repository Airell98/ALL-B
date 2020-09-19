<template>
  <div class="wrapper">
      <div class="instruction">
          <div class="instruction-text">
              <h2>Click the images below for <span style="border-bottom: 1px solid white"> further details.</span></h2>
          </div>
      </div>
    <div class="part-1" >
      <div class="part-1-image">
        <div class="part-1-header">
          <h3>
            Fullstack Developer Class
          </h3>
        </div>
        <div class="fullstack-image">
          <img
            src="https://images.unsplash.com/photo-1531482615713-2afd69097998?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80"
            alt="image1"
            class="image1"
          />
        </div>
      </div>
    </div>

    <div class="part-2" >
      <div class="part-2-image">
        <div class="part-2-header">
          <h3>
            Beginner Web Developer Class
          </h3>
        </div>
        <div class="beginner-image">
          <img
            src="https://images.unsplash.com/photo-1555066931-bf19f8fd1085?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=751&q=80"
            alt="image2"
            class="image2"
          />
        </div>
      </div>
    </div>

    <div class="part-3" >
      <div class="part-3-image">
        <div class="part-3-header">
          <h3>
            Website Development Service
          </h3>
        </div>
        <div class="service-image">
          <img
            src="https://images.unsplash.com/photo-1519389950473-47ba0277781c?ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80"
            alt="image3"
            class="image3"
          />
        </div>
      </div>
    </div>
    <!-- <div class="arrow" @click="slideOut" style="cursor:pointer;">
      <img src="Next Arrow.svg" alt="Next Arrow" />
    </div> -->
  </div>
</template>

<script>
import { gsap } from "gsap/dist/gsap";
import { ScrollTrigger } from "gsap/dist/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);
export default {
  name: "HomeMiddle",
  data() {
    return {
      kondisi: 1,
    };
  },
    mounted() {
     let part1 = gsap.timeline({
        scrollTrigger: {
          trigger: ".part-1",
        },
      });
      let part2 = gsap.timeline({
        scrollTrigger: {
          trigger: ".part-2",
        },
      });

      let part3 = gsap.timeline({
        scrollTrigger: {
          trigger: ".part-3",
        },
      });
        part1.from(".part-1-image", { x: -100, opacity: 0, duration: 1.5 });
         part2.from(".part-2-image", { x: 100, opacity: 0, duration: 1.5 });
          part3.from(".part-3-image", { y: 200, opacity: 0, duration: 1 }, "-=1");
    },
  methods: {
    slideOut() {
      let part1 = gsap.timeline({
        scrollTrigger: {
          trigger: ".part-1",
        },
      });
      let part2 = gsap.timeline({
        scrollTrigger: {
          trigger: ".part-2",
        },
      });

      let part3 = gsap.timeline({
        scrollTrigger: {
          trigger: ".part-3",
        },
      });
      let kondisi = this.kondisi;
      switch (kondisi) {
        case 1:
          part1.to(".part-1-image", { x: 100, opacity: 0, duration: 1.5 });
          part2.from(".part-2-image", { x: -100, opacity: 0, duration: 1 });
          setTimeout(()=> {
            this.kondisi++;
          }, 3000);

          break;
        case 2:
          // code block
          break;
        default:
        // code block
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.wrapper {
    .instruction{
         margin-top : 80px;
         margin-bottom : 120px;
        .instruction-text{
            h2{
                color: white;
            }
        }
    }
  .part-1 {
      margin-bottom : 100px;
    .part-1-header {
        margin-bottom: 30px;
      h3 {
        font-family: "Tienne", serif;
        color: whitesmoke;
        letter-spacing: 3px;
        font-size: 35px;
      }
    }
    .part-1-image {
      .fullstack-image {
        .image1 {
          width: 50%;
          height: 400px;
        }
      }
    }
  }

  .part-2 {
      margin-bottom : 100px;
    .part-2-header {
         margin-bottom: 30px;
      h3 {
        font-family: "Tienne", serif;
        color: whitesmoke;
        letter-spacing: 3px;
        font-size: 35px;
      }
    }
    .part-2-image {
      .beginner-image {
        .image2 {
          width: 50%;
          height: 400px;
        }
      }
    }
  }

  .part-3 {
      margin-bottom : 100px;
    .part-3-header {
         margin-bottom: 30px;
      h3 {
        font-family: "Tienne", serif;
        color: whitesmoke;
        letter-spacing: 3px;
        font-size: 35px;
      }
    }
    .part-3-image {
      .service-image {
        .image3 {
          width: 50%;
          height: 400px;
        }
      }
    }
  }
}
</style>
