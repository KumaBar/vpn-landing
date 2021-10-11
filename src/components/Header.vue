<template>
  <div class="header">
    <div class="header-row">
      <img src="../assets/LogoH.png" class="logo" />
      <div class="navigation">
        <div class="navigation-i" v-for="link in links" :key="link.id">
          {{ link.name }}
        </div>
      </div>
      <div class="account">
        <button classs="account-in">Sign in</button>
        <button classs="account-up">Sign up</button>
      </div>
      <div :class="{ burger: true, change: isOpen }" @click="toggle(); open();">
        <div class="bar1"></div>
        <div class="bar2"></div>
        <div class="bar3"></div>
      </div>
     
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      isOpen: false,
      links: [
        { id: 1, name: "About" },
        { id: 2, name: "Features" },
        { id: 3, name: "Pricing" },
        { id: 4, name: "Testimonials" },
        { id: 5, name: "Help" },
      ],
    };
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
      console.log(this.isOpen,'header');
    },
    open(){
        this.$emit('isOpenPopup',this.isOpen)
    }
  },
  components: {
  
  },
};
</script>

<style>
.header {
  position: fixed;
  width: 100%;
  background: white;
  top: 0;
left:0;
padding-top: 20px;
  padding-bottom: 10px;
  box-shadow: 0px 8px 12px -6px rgba(34, 60, 80, 0.2);
  z-index:3;
}
.header-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  
    padding: 0 20px;
  margin: 0 auto;
  max-width: 1140px;
}
.logo {
  display: block;
  width: 130px;
}
.navigation {
  display: flex;
}
.navigation-i {
  margin-right: 40px;
  cursor: pointer;
  transition: 0.2s;
}
.navigation-i:last-child {
  margin-right: 0;
}
.account button {
  background: none;
  color: black;
  font-weight: 500;
  padding: 13px 45px;
  border-radius: 50px;
  border: 1px solid transparent;
  transition: 0.2s;
}
.account button:hover {
  border-color: #f53855;
  color: #f53855;
}
.account button:first-child {
  margin-right: -40px;
}
.burger {
  display: none;
  position: relative;
  z-index:3;
  cursor:pointer;
}
.burger div {
  width: 36px;
  height: 5px;
  background-color: black;
  margin: 6px 0;
}
.bar1,
.bar2,
.bar3 {
  width: 35px;
  height: 5px;
  background-color: #333;
  margin: 6px 0;
  transition: 0.4s;
}

/* Поворот первой полосы */
.change .bar1 {
  -webkit-transform: rotate(-45deg) translate(-9px, 6px);
  transform: rotate(-45deg) translate(-9px, 6px);
}

/* Исчезание второй полосы */
.change .bar2 {
  opacity: 0;
}

/* Поворот последней полосы */
.change .bar3 {
  -webkit-transform: rotate(45deg) translate(-8px, -8px);
  transform: rotate(45deg) translate(-8px, -8px);
}
@media (max-width: 950px) {
  .navigation,
  .account {
    display: none;
  }
  .burger {
    display: block;
  }
}

</style>