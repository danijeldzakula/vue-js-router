<template>
  <div class="red">{{ count }}</div>
  <div>
    <button @click="this.decrement('dec')">Decrement</button>
    <button @click="this.increment('inc')">Increment</button>
  </div>

  <ul>
    <li v-for="item in items" :key="item._id">
      {{ item.name }}
    </li>
  </ul>

  <AccordionToggle count />
</template>

<script>
import AccordionToggle from './AccordionToggle.vue'


export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: {
    AccordionToggle
  },

  data() {
    return {
      count: 0,
      items: [
        { _id: 'fddhsfjksdf', name: 'Jedan'},
        { _id: 'dfdsfsdfdfd', name: 'Dva'},
        { _id: 'fjksdfdkfjk', name: 'Tri'},
        { _id: 'sdjfdjfjdjs', name: 'Cetiri'},
        { _id: 'sdfefeuifej', name: 'Pet'},
        { _id: 'sdfjdfdjfjd', name: 'Sest'},
        { _id: 'dsffdfjdjfd', name: 'Sedam'},
        { _id: 'sdfjsdfsdff', name: 'Osam'},
        { _id: 'sdjfdjfdfff', name: 'Devet'},
        { _id: 'sdfjigjrgir', name: 'Deset'}
      ]
    }
  },  

  methods: {
    increment(el) {
      console.log(el)

      if (this.count >= 10) {
        this.count = 10
      } else { 
        this.count++
      }
    },
    decrement(el) {
      console.log(el)

      if (this.count <= 0) {
        this.count = 0
      } else { 
        this.count--
      }
    }
  }  
}
</script>

<style scoped>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
</style>
