<template>
  <div clas="plan">
    <div class="plan-title">Choose Your Plan</div>
    <div class="plan-text">
      Let's choose the package that is best for you and explore it happily and
      cheerfully.
    </div>
    <div class="plan-list">
      <div class="plan-i">
        <img src="../assets/Free.png" />
        <div class="plan-i-title">Free plan</div>
        <div class="plan-i-list">
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />Unlimited Bandwitch
          </div>
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />Encrypted Connection
          </div>
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />No Traffic Logs
          </div>
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />Works on All Devices
          </div>
        </div>
        <div class="plan-i-price">
          <span>Free</span>
          <button>Select</button>
        </div>
      </div>
      <div class="plan-i">
        <img src="../assets/Standard.png" />
        <div class="plan-i-title">Standard plan</div>
        <div class="plan-i-list">
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />Unlimited Bandwitch
          </div>
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />Encrypted Connection
          </div>
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />No Traffic Logs
          </div>
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />Works on All Devices
          </div>
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />Connect Anyware
          </div>
        </div>
        <div class="plan-i-price">
          <span>$9 / mo</span>
          <button>Select</button>
        </div>
      </div>
      <div class="plan-i">
        <img src="../assets/Premium.png" />
        <div class="plan-i-title">Premium Plan</div>
        <div class="plan-i-list">
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />Unlimited Bandwitch
          </div>
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />Encrypted Connection
          </div>
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />No Traffic Logs
          </div>
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />Works on All Devices
          </div>
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />Connect Anyware
          </div>
          <div class="plan-i-list-i">
            <img src="../assets/check.png" />Get New Features
          </div>
        </div>
        <div class="plan-i-price">
          <span>$12 / mo</span>
          <button>Select</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionPlan",
};
</script>

<style>
.plan-title {
  margin-top: 80px;
  margin-bottom: 20px;
  text-align: center;
  font-size: 35px;
  font-weight: 500;
  color: black;
}
.plan-text {
  text-align: center;
  margin-bottom: 60px;
}
.plan-list {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}
.plan-i {
  background: white;
  padding: 60px;
  padding-bottom: 50px;
  border-radius: 10px;
  border: 2px solid #dddddd;
  display: flex;
  justify-content: space-between;
  flex-direction: column;
  margin:0 20px;
  margin-bottom:40px;
}
.plan-i > img {
  display: block;
  margin: 0 auto;
}
.plan-i-title {
  text-align: center;
  font-size: 18px;
  font-weight: 500;
  margin: 30px 0;
}
.plan-i-list-i img {
  display: inline-block;
  margin-right: 20px;
  margin-top: -7px;
}
.plan-i-list-i {
  font-size: 14px;
  margin-bottom: 10px;
}
.plan-i-price {
  justify-self: flex-end;
  margin-top: 100px;
  display: flex;
  flex-direction: column;
}
.plan-i-price span {
  font-size: 25px;
  font-weight: 500;
  margin-bottom: 20px;
  text-align: center;
}
.plan-i-price button {
  padding: 13px 60px;
  border-radius: 50px;
  color: #f53838;
  border: 2px solid #f53838;
  background: transparent;
  font-size: 16px;
  font-weight: bold;
  transition: 0.2s;
}
.plan-i-price button:hover {
  box-shadow: 0px 18px 17px -3px rgba(34, 60, 80, 0.2);
  background: #f53838;
  color: white;
}

@media (max-width: 1140px) {
  .plan-i {
    padding: 35px;
    padding-bottom: 10px;
  }
  .plan-i-price{
      margin-top:10px;
  }
}
@media(max-width:600px){
    .plan-title{
        font-size:30px;
    }
}
@media (max-width: 350px) {
  .plan-i {
    padding: 10px;
    padding-bottom: 10px;
  }
}
</style>