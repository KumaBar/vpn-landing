<template>
  <div class="footer">
    <div class="footer-row">
      <div class="footer-block">
        <img src="../assets/LogoH.png" />
        <p>
          LaslesVPN is a private virtual network that <br />
          has unique features and has high security.
        </p>
        <div class='footer-social'>
            <img src="../assets/Facebook.png">
            <img src="../assets/Twitter.png">
            <img src="../assets/Instagram.png">
        </div>
        <div class='footer-copy'>©2020LaslesVPN</div>
      </div>
      <div class='footer-column'>
          <div class='footer-title'>Product</div>
          <div class='footer-item'>Download</div>
          <div class='footer-item'>Pricing</div>
          <div class='footer-item'>Locations</div>
          <div class='footer-item'>Server</div>
      </div>
       <div class='footer-column'>
          <div class='footer-title'>Engage</div>
          <div class='footer-item'>LaslesVPN</div>
          <div class='footer-item'>FAQ</div>
          <div class='footer-item'>Tutorials</div>
          <div class='footer-item'>About Us</div>
      </div>
       <div class='footer-column'>
          <div class='footer-title'>Earn Money</div>
          <div class='footer-item'>Affiliate</div>
          <div class='footer-item'>Become Partner</div>
      </div>
    </div>
  </div>
</template>

<style>
.footer{
    padding-top:150px;
    padding-bottom:30px;
}
.footer-row{
    display:flex;
    justify-content: space-between;
}
.footer-block img{
    display:inline-block;
    margin-bottom:20px;
}
.footer-block p{
    margin-bottom:30px;
    line-height:30px;
}
.footer-block-social{
    margin-bottom:30px;
}
.footer-title{
    margin-bottom:20px;
    font-weight:500;
    color:black;
}
.footer-item{
    margin-bottom:10px;
}
.footer-title,
.footer-item{
    line-height:30px;
}
@media(max-width:800px){
    .footer-column{
        display:none;
    }
    .footer-row{
        justify-content: center;
    }
    .footer-copy{
text-align:center;
    }
    .footer-social img{
        display:block;
    }
    .footer-social{
        display:flex;
        justify-content: center;
    }
}
</style>