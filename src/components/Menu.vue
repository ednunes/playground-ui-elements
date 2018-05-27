<template>
  <div>
    <nav class="Menu-navbar">
      <a href="#" class="Menu-logo">Logo</a>
      <ul class="Menu-links">
        <li class="Menu-item-list"><a href="#">About</a></li>
        <li class="Menu-item-list"><a href="#">Work</a></li>
        <li class="Menu-item-list"><a href="#">Blog</a></li>
        <li class="Menu-item-list"><a href="#">Contact</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Menu',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}

</script>

<style scoped>
.Menu-navbar {
  padding: 1% 5%;
}

.Menu-logo {
  float: left;
  color: #000;
  text-decoration: none;
}

.Menu-links {
  /* Dont show any customization in li */
  list-style: none;
  /* Horizontal position */
  display: flex;
  display: -webkit-flex;
  margin: 0;
  float: right;
}

.Menu-item-list{
  margin: 0 30px;
}

/* Links */
.Menu-item-list > a {
  color: #000;
  font-size: 1em;
  position: relative;
  text-decoration: none;
}

.Menu-item-list > a:hover {
  color: #000;
}

.Menu-item-list > a:before {
  left: 0;
  bottom: -0.35vw;
  content: "";
  width: 100%;
  height: 3px;
  border-bottom: 3px solid tomato;
  position: absolute;
  visibility: hidden;
  transform: scaleX(0);
  -webkit-transform: scaleX(0);
  -webkit-transition: all 0.3s ease-in-out 0s;
  transition: all 0.3s ease-in-out 0s;
}

.Menu-item-list > a:hover:before {
  visibility: visible;
  -webkit-transform: scaleX(1);
  transform: scaleX(1);
}
</style>
