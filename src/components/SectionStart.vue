<template>
  <section class="start">
    <div class="start-row">
      <div class="start-i">
        <div class="start-i-title">
          Want anything to be easy with <span>LaslesVPN.</span>
        </div>
        <div class="start-i-text">
          Provide a network for all your needs with ease and fun using LaslesVPN
          discover interesting features from us.
        </div>
        <button class="start-i-btn">Get Started</button>
      </div>
      <img src="../assets/start-img.png" class="start-i-img" />
    </div>
    <div class="start-stats">
      <div class="start-stats-i">
        <img src="../assets/user.svg" />
        <div>
          <span>90+</span>
          Users
        </div>
      </div>
      <div class="start-stats-i">
        <img src="../assets/location.svg" />
        <div>
          <span>90+</span>
          Users
        </div>
      </div>
      <div class="start-stats-i">
        <img src="../assets/Server.svg" />
        <div>
          <span>90+</span>
          Users
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.start{
    margin-top:100px;
    margin-bottom:100px;
}
.start-row {
  display: flex;
  justify-content: space-between;
}
.start-i {
  flex-basis: 50%;
}
.start-i-title {
  font-weight: 500;
  color: #0b132a;
  font-size: 50px;
  line-height: 70px;
  margin-bottom: 20px;
}
.start-i-title span {
  font-weight: bold;
  color: #0b132a;
  font-size: 50px;
}
.start-i-text {
  line-height: 30px;
  margin-bottom: 50px;
}
.start-i-btn {
  padding: 17.5px 77px;
  background: #f53838;
  color: white;
  font-weight: bold;
  border-radius: 10px;
  box-shadow: -1px 25px 35px -10px rgba(96, 22, 22, 0.35);
}
.start-i-img {
  display: block;
  max-width: 500px;
  width: 100%;
  margin-left: 20px;
}
.start-stats {
  display: flex;
  justify-content: space-around;
    box-shadow: 0px 41px 47px -3px rgba(34, 60, 80, 0.2);
  padding: 40px;
  margin-top:40px;
}
.start-stats-i {
    width:100%;
    margin:0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
    padding:20px;
  border-right: 1px solid rgba(34, 60, 80, 0.2);
}
.start-stats-i:last-child{
      border-right:none;
}
.start-stats-i img {
  display: block;
  margin-right: 30px;
}
.start-stats-i div {
  display: flex;
  flex-direction: column;
}
.start-stats-i div span {
  margin-bottom: 10px;
}
@media (max-width: 1100px) {
  .start-row {
    display: block;
  }
  .start-i-title {
    text-align: center;
    margin-bottom: 10px;
  }
  .start-i-text {
    text-align: center;
    margin-bottom: 20px;
  }
  .start-i-btn {
    display: block;
    margin: 0 auto;
    margin-bottom: 30px;
  }
  .start-i-img {
    display: none;
  }
}
@media(max-width:640px){
    .start-stats{
        flex-wrap:wrap;
        flex-direction:column;
        max-width:350px;
        margin:0 auto;
    }
    .start-stats-i{
        border-right:none;
        
        border-bottom: 1px solid rgba(34, 60, 80, 0.2);
    }
    .start-stats-i:last-child{
        border-bottom:none;
    }
}
@media(max-width:580px){
    .start-i-title
    ,.start-i-title span{
        font-size:30px;
        line-height: 40px;
    }
}
</style>