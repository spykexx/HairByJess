<template>
  <div>
    <transition-group name="slide" tag="div" class="imgslider" :class="getDirection">
      <div v-for="i in [currentIndex]" :key="i">
        <img class="sliderimg" :src="currentImg" />
      </div>
    </transition-group>
    <a class="prev" @click="prev, setDirection('prev')" href="#" >&#10094; Previous</a>
    <a class="next" @click="next, setDirection('next')" href="#">&#10095; Next</a>
  </div>
</template>
<script>
export default {
  name: "Slider",
  data() {
    return {
      images: [
        "https://cdn.pixabay.com/photo/2015/12/12/15/24/amsterdam-1089646_1280.jpg",
        "https://cdn.pixabay.com/photo/2016/02/17/23/03/usa-1206240_1280.jpg",
        "https://cdn.pixabay.com/photo/2015/05/15/14/27/eiffel-tower-768501_1280.jpg",
        "https://cdn.pixabay.com/photo/2016/12/04/19/30/berlin-cathedral-1882397_1280.jpg"
      ],
      timer: null,
      currentIndex: 0,
      direction: '',
    };
  },

  mounted: function() {
    this.startSlide();
  },

  methods: {
    startSlide: function() {
    //   this.timer = setInterval(this.next, 4000);
    },

    next: function() {
      this.currentIndex += 1;
    },
    prev: function() {
      this.currentIndex -= 1;
    },
    setDirection: function(dir){
        this.direction = dir;
    },
    getDirection: function(){
        return direction;
    },
  },

  computed: {
    currentImg: function() {
      return this.images[Math.abs(this.currentIndex) % this.images.length];
      
    },
    
    
  }
};
</script>