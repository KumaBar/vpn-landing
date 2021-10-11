<template>
  <div :class="{ popup: true, open: isOpen }">
    <div class="popup-sign">
      <button classs="popup-sign-in">Sign in</button>
      <button classs="popup-sign-up">Sign up</button>
    </div>
    <div class="popup-row">
      <div class="popup-i" v-for="link in links" :key="link.id">
        {{ link.name }}
      </div>
    </div>
  </div>
</template>


<script>
export default {
  props: [
      'isOpen'
  ],
  name: "Popup",
  data() {
    return {
      links: [
        { id: 1, name: "About" },
        { id: 2, name: "Features" },
        { id: 3, name: "Pricing" },
        { id: 4, name: "Testimonials" },
        { id: 5, name: "Help" },
      ],
    };
  },

};
</script>

<style>
.popup {
  margin-top: 60px;
  position: fixed;
  top: 0;
  right: -500px;
  background: white;
  transition: 0.2s;
   z-index: 3;
}
.popup.open {
  right: 0;
}
.popup-i {
  text-align: center;
  padding: 20px;
}
.popup-sign button {
  background: none;
  color: black;
  font-weight: 500;
  padding: 13px 45px;
  border-radius: 50px;
  border: 1px solid transparent;
  transition: 0.2s;
}
.popup-sign button:hover {
  border-color: #f53855;
  color: #f53855;
}
.popup-sign button:first-child {
  margin-right: -40px;
}
</style>