<template>
  <div class="review">
    <div class="review-title">Trusted by Thousands of<br />Happy Customer</div>
    <div class="review-text">
      These are the stories of our customers who have joined us with great
      <br />
      pleasure when using this crazy feature.
    </div>
    <carousel
      class="review-slider"
      :per-page="1"
      :mouse-drag="false"
      :autoplay="true"
      :loop="true"
      :mouseDrag="false"
      :touchDrag="false"
      :perPage="maxSlide"
      :navigationEnabled="true"
    >
      <slide>
        <div class="review-slide">
          <div class="review-row">
            <img src="../assets/veizh.png" />
            <div class="review-slide-title">
              <span>Viezh Robert</span><br />
              Warsaw, Poland
            </div>
            <div class="review-rating">4,5<img src="../assets/star.png" /></div>
          </div>
          <div class="review-slide-text">
            “Wow... I am very happy to use this VPN, it turned out to be more
            than my expectations and so far there have been no problems.
            LaslesVPN always the best”.
          </div>
        </div>
      </slide>
      <slide>
        <div class="review-slide">
          <div class="review-row">
            <img src="../assets/yessica.png" />
            <div class="review-slide-title">
              <span>Yessica Christy</span><br />
              Shanxi, China
            </div>
            <div class="review-rating">4,5<img src="../assets/star.png" /></div>
          </div>
          <div class="review-slide-text">
            “I like it because I like to travel far and still can connect with
            high speed.”.
          </div>
        </div>
      </slide>
      <slide>
        <div class="review-slide">
          <div class="review-row">
            <img src="../assets/kim.png" />
            <div class="review-slide-title">
              <span>Kim Young Jou</span><br />
              Seoul, South Korea
            </div>
            <div class="review-rating">4,5<img src="../assets/star.png" /></div>
          </div>
          <div class="review-slide-text">
            “This is very unusual for my business that currently requires a
            virtual private network that has high security.”.
          </div>
        </div>
      </slide>
      <slide>
        <div class="review-slide">
          <div class="review-row">
            <img src="../assets/veizh.png" />
            <div class="review-slide-title">
              <span>Viezh Robert</span><br />
              Warsaw, Poland
            </div>
            <div class="review-rating">4,5<img src="../assets/star.png" /></div>
          </div>
          <div class="review-slide-text">
            “Wow... I am very happy to use this VPN, it turned out to be more
            than my expectations and so far there have been no problems.
            LaslesVPN always the best”.
          </div>
        </div>
      </slide>
      <slide>
        <div class="review-slide">
          <div class="review-row">
            <img src="../assets/yessica.png" />
            <div class="review-slide-title">
              <span>Yessica Christy</span><br />
              Shanxi, China
            </div>
            <div class="review-rating">4,5<img src="../assets/star.png" /></div>
          </div>
          <div class="review-slide-text">
            “I like it because I like to travel far and still can connect with
            high speed.”.
          </div>
        </div>
      </slide>
      <slide>
        <div class="review-slide">
          <div class="review-row">
            <img src="../assets/kim.png" />
            <div class="review-slide-title">
              <span>Kim Young Jou</span><br />
              Seoul, South Korea
            </div>
            <div class="review-rating">4,5<img src="../assets/star.png" /></div>
          </div>
          <div class="review-slide-text">
            “This is very unusual for my business that currently requires a
            virtual private network that has high security.”.
          </div>
        </div>
      </slide>
    </carousel>
    <div class="review-block">
      <div class="review-block-left">
        <span>Subscribe Now for <br />Get Special Features!</span>
       <p> Let's subscribe with us and find the fun.</p>
      </div>
      <div class="review-block-right">
        <button>Subscribe Now</button>
      </div>
    </div>
  </div>
</template>

<script>
import { Carousel, Slide } from "vue-carousel";
export default {
  name: "SectionReview",
  data() {
    return {
      window: {
        width: 0,
        height: 0,
      },
    };
  },
  created() {
    window.addEventListener("resize", this.handleResize);
    this.handleResize();
  },
  destroyed() {
    window.removeEventListener("resize", this.handleResize);
  },
  methods: {
    handleResize() {
      this.window.width = window.innerWidth;
      this.window.height = window.innerHeight;
    },
  },
  computed: {
    maxSlide() {
      console.log(this.window.width);
      if (this.window.width >= 900) {
        return 3;
      }
      if (this.window.width >= 680) {
        return 2;
      }
      return 1;
    },
  },
  components: {
    Carousel,
    Slide,
  },
};
</script>

<style>
.review-title {
margin-top: 50px;
  margin-bottom: 20px;
  text-align: center;
  line-height: 50px;
  font-size: 35px;
  font-weight: 500;
  color: black;
}
.review-text {
  margin-bottom: 140px;
  text-align: center;
  line-height: 30px;
}
.review-slide {
  padding: 30px;
  border-radius: 10px;
  border: 1px solid #f53838;
  background: white;
  display: flex;
  flex-direction: column;
  transition: 0.2s;
  margin: 0 10px;
  height: 100%;
  z-index: 1;
}
.review-slide-title span {
  font-weight: 500;
  font-size: 18px;
  color: black;
}
.review-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 8px;
}
.review-row > img {
  margin: 0 10px;
}
.VueCarousel-pagination {
  text-align: left !important;
}
.VueCarousel-dot-container {
  margin-top: 0 !important;
   
}
.VueCarousel-dot {
  background: #dde0e4 !important;
  padding: 1px !important;
  margin: 10px !important;
  transition: 0.2s;
  
}
.VueCarousel-dot--active {
  background: #f53838 !important;
  padding-right: 20px !important;
  border-radius: 10px !important;
}
.VueCarousel-navigation {
  position: absolute !important;
  bottom: 10px !important;
  right: 75px !important;
  width: 50px !important;
}
.VueCarousel-navigation button {
  border: 2px solid #f53838 !important;
  border-radius: 10px;
  color: #f53838 !important;
  padding: 5px 15px !important;
  transition: 0.2s;
}
.VueCarousel-navigation button:hover {
  color: white !important;
  background: #f53838 !important;
}
.review-block{
    position:relative;
    background:white;
    box-shadow: 0px 5px 26px 5px rgba(34, 60, 80, 0.2);
    bottom:-90px;
    display:flex;
    justify-content: space-between;
    padding:50px 70px;
}
.review-block-left span{
    display:inline-block;
    font-size:35px;
    font-weight:500;
    color:black;
    line-height:45px;
    margin-bottom:20px;
}
.review-block-right {
    display:flex;
    align-items:center;
}
.review-block-right button{
    padding:17.5px 66px;
    color:white;
    font-weight: 500;
    background: #F53838; 
    border-radius: 10px;
box-shadow: 0px 11px 15px -1px rgba(34, 60, 80, 0.2);
}
@media (max-width: 1100px) {
.review-block{
   flex-direction: column;
    padding:15px;
    text-align:center;
    justify-content: space-between;
}
.review-block-left {
    margin-bottom:20px;
}
.review-block-right{
    margin:0 auto;
}
}
@media (max-width: 580px) {
  .VueCarousel-navigation {
    bottom: -20px !important;
  }
  .review-block-left span{
      font-size:24px;
  }
  .review-slide{
      padding:5px;
  }
  .review-block{
      padding:7.5px;
  }

}
@media(max-width:400px){
   .review-slide-title,
    .review-slide-title span,
   .review-slide-text{
       font-size:14px;
   } 
}
</style>