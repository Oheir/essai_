<template>
  <input v-model.number="k" placeholder="edit me" />
  <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
    <g>
      <circle cx="50" cy="20" r="10" />
    </g>
    <g fill="#D9D9D9">
      <circle cx="50" cy="20" r="9.7" />
    </g>
    <g
      v-for="i in range(k)"
      key="i"
      fill="#3500D3"
      :transform="`rotate(${angle_generator[i]} 50 20) translate(0 -20)`"
    >
      <circle cx="50" cy="50" r="2" />
      <text
        x="50"
        y="50"
        fill="white"
        font-size="20%"
        :transform="`rotate(0 50 50) translate(-1 5)`"
      >
        {{ id_generator[i] }}
      </text>
    </g>
  </svg>
</template>

<script>
export default {
  name: 'HelloWorld1',
  props: {
    msg: String
  },
  data() {
    return {
      i: '',
      k: 12,
    };
  },
  methods: {
    range(k) {
      let result = Array(k);
      for (let i = 0; i < k; i++) {
        result[i] = i;
      }
      return result;
    },
  },
  computed: {
    angle_generator() {
      let n = 1;
      let nbr_angle_base = 360 / this.k;
      let nbr_angle = 360 / this.k;
      let angles = [180];

      while (n < this.k) {
        angles.push(180 + nbr_angle);
        nbr_angle += nbr_angle_base;
        n++;
      }

      return angles;
    },
    id_generator() {
      let id = [0];
      let n = 1;

      while (n < this.k) {
        id.push(n);
        n++;
      }
      return id;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#a {
  transform-origin: 50% 50%;
}

</style>
