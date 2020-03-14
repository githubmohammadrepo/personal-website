<template>
  <div >
    <b-carousel
      id="carousel-fade"
      fade
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
      class="windows"
    >
      <!-- Text slides with image -->
      <b-carousel-slide
        caption="First slide"
        text="Nulla vitae elit libero, a pharetra augue mollis interdum."
        img-src="https://picsum.photos/1024/480/?image=52"
      ></b-carousel-slide>

      <!-- Slides with custom text -->
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=54">
        <h1>Hello world!</h1>
      </b-carousel-slide>

      <!-- Slides with image only -->
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=58"></b-carousel-slide>

      <!-- Slides with img slot -->
      <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
      <b-carousel-slide>
        <template v-slot:img>
          <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            src="https://picsum.photos/1024/480/?image=55"
            alt="image slot"
          >
        </template>
      </b-carousel-slide>

      <!-- Slide with blank fluid image to maintain slide aspect ratio -->
      <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eros felis, tincidunt
          a tincidunt eget, convallis vel est. Ut pellentesque ut lacus vel interdum.
        </p>
        <b-button variant="danger">Button</b-button>
      </b-carousel-slide>
    </b-carousel>

    <div class="leg-window d-flex">
        <div class="m-auto text-light">
            <span class="mx-2">&#9678;</span>&nbsp;&nbsp;
             <b-icon icon="circle" class="on" scale="1.4" variant="success"></b-icon>
            <span class="mx-2">&#8701;</span>&nbsp;&nbsp;
            <span class="mx-2">&#8702;</span>&nbsp;&nbsp;
        </div>
        <!-- <span class="m-auto text-light">&#9711;</span> -->
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        slide: 0,
        sliding: null
      }
    },
    methods: {
      onSlideStart() {
        this.sliding = true
      },
      onSlideEnd() {
        this.sliding = false
      }
    }
  }
</script>

<style lang="scss">
    .windows{
        box-shadow:
            2px 3px 2px rgb(41, 46, 46),
            2px 3px 2px red,
            2px 3px 2px blue,
            2px 3px 2px black,
            2px 3px 2px crimson,
    }
    .leg-window{
        width:100%;
        height: 50px;
        background-color: #000;
        margin:auto;

        box-shadow:
            2px 3px 2px rgb(41, 46, 46),
            2px 3px 2px red,
            2px 3px 2px blue,
            2px 3px 2px black,
            2px 3px 2px crimson,
    }

    // animation change color
    @keyframes example {
        from {background-color: rgb(0, 255, 213);}
        to {background-color: green;}
    }
    .on{
        background-color: white;
        animation-name: example;
        animation-duration: 4s;
        border:none;
        border-radius:50%;
        animation-iteration-count: infinite;
    }
     
    
</style>