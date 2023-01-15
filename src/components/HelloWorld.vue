<template>
  <ul>
    <li>
      <a class="active dropdown"  href="#home">
          Arithmétique 
          <div class="dropdown-content">
          <p>Hello World!</p>
        </div>
      </a>
    </li>
    <li><a href="components/Exercices.vue" target="_self">Exercices</a></li>
    <li><a href="#contact">RSA</a></li>
    <li style="float:right"><a href="#about">Documentation</a></li>
  </ul>
  <div class="dropdown-content">
    <p>Hello World!</p>
  </div>
</template>

<script>

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body{
  margin:0;
  background: #282828
}

  ul {
  display: flex;
  justify-content: space-evenly;
  list-style-type: none;
  margin: 0;
  padding: 0;
  background-color: #1F2833;
  position: fixed;
  top: 0;
  width: 100%;
  }

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #C5C6C7;
  color: #3500D3;
}
.texte{
  color: white;
  text-align: center;
}
.dropdown {
  position: relative;
  display: inline-block;
}
.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(207, 0, 0, 0.2);
  padding: 12px 16px;
  z-index: 1;
}
.dropdown:hover .dropdown-content {
  display: block;
  }
</style>
