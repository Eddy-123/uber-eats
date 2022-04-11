<template>
  <div class="homeLand">
    <RestaurantRow/>
  </div>
</template>

<script>
import BDD from '../db'
import { onMounted } from 'vue'

import RestaurantRow from '../components/RestaurantRow.vue'

export default {
    name: 'HomeLand',
    components: {
      RestaurantRow
    },
    setup() {
      
      class Restaurant {
        constructor (name, note, image, drive_time) {
          this.name = name
          this.note = note
          this.image = image
          this.drive_time = drive_time
        }
      }

      let dataRestaurant = []
  
      const makeDataRestaurant = () => {
        let three_restaurants = []
        for (const restaurant of BDD) {
          const new_restaurant = new Restaurant(restaurant.name, restaurant.note, restaurant.image, restaurant.drive_time)
          three_restaurants.push(new_restaurant)
          if (three_restaurants.length == 3) {
            dataRestaurant.push(three_restaurants)
            three_restaurants = []
          }
        }
      }
      onMounted(makeDataRestaurant)
    }
}
</script>

<style>

</style>