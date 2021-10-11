<template>
  <section class="features">
    <div class="features-row">
      <img class="features-i-img" src="../assets/Illustration 2.png" />
      <div class="features-i-block">
        <div class="features-i-title">We Provide Many <br/> Features You Can Use</div>
        <div class="features-i-text">
          You can explore the features that we provide with fun and have their
          own functions each feature.
        </div>
        <ul class="features-list">
          <li>
            <img src="../assets/checkbox.png" />Powerfull online protection.
          </li>
          <li><img src="../assets/checkbox.png" />Internet without borders.</li>
          <li><img src="../assets/checkbox.png" />Supercharged VPN.</li>
          <li><img src="../assets/checkbox.png" />No specific time limits.</li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style>
.features{
    background: white;
}
.features-row {
  display: flex;
  justify-content: space-between;
}
.features-i-img {
  max-width: 400px;
  width: 100%;
  margin: 0 auto;
}
.features-i-img,
.features-i-block{
    flex-basis:50%;
}
.features-i-block{
    margin-left:20px;
}
.features-i-title {
  font-size: 35px;
  font-weight: 500;
  color: black;
  margin-bottom: 20px;
  line-height: 50px;
}
.features-i-text {
  line-height: 30px;
  margin-bottom: 20px;
}
.features-list li {
  margin-bottom: 15px;
  display: flex;
  align-items: center;
}
.features-i-block img {
  display: block;
  padding-right: 10px;
}
@media(max-width:980px){
    .features-i-img{
        display: none;
    }
    .features-i-block{
        flex-basis:100%;
        text-align:center;
    }
    .features-list{
        display: flex;
        flex-wrap: wrap;
          justify-content: center;
        max-width:600px;
        margin:0 auto;
    }
    .features-list li{
        flex-basis:50%;
        padding:10px;
    }
}
@media(max-width:600px){
    .features-list{
        max-width:260px;
        justify-content: center;
    }
    .features-list li{
        flex-basis:100%;
        padding:0px;
      
    }
    .features-i-title{
        font-size:30px;
    }
}
</style>