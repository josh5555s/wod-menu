<template>
    <div id="select-menu">
      <router-link :to="`${location}/flower`"><h2>Flower</h2></router-link>
      <router-link :to="`${location}/preroll`"><h2>Preroll</h2></router-link>
      <router-link :to="`${location}/cartridge`"><h2>Cartridge</h2></router-link>
      <router-link :to="`${location}/concentrate`"><h2>Concentrate</h2></router-link>
      <router-link :to="`${location}/edible`"><h2>Edible</h2></router-link>
      <router-link :to="`${location}/tincture`"><h2>Tincture</h2></router-link>
      <router-link :to="`${location}/topical`"><h2>Topical</h2></router-link>
    </div>
</template>

<script>

export default {
  emits: ['product-titles'],
  data() {
    return {
      location: ''
    }
  },
  methods: {
    getLocation() {
      this.location = this.$route.path
    },
    productTitles() {
      this.$emit('product-titles')
    },
  },
  created() {
    this.getLocation(),
    this.productTitles()
  }
}
</script>

<style>
/* unvisited link */
a:link {
  color: #c1d448;
}
a:link {
  text-decoration: none;
}

/* visited link */
a:visited {
  color: #c1d448;
}

/* mouse over link */
a:hover,
button:hover {
  color: white;
  border-block-color: white;
  cursor: pointer;
}

/* selected link */
a:active {
  color: white;
}

#select-menu {
  margin: auto;
  text-align: center;
}

button {
  background: black;
  color: #c1d448;
  border-block-color: #c1d448;
  border-radius: 5px;
}

.active {
  color: white;
  border-block-color: white;
}

</style>