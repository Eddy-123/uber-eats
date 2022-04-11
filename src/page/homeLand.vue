<template>
  <div class="homeLand">
    <RestaurantRow/>
  </div>
</template>

<script>
//import BDD from '../db'

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

      var resto = new Restaurant('Delicious', 10, 'img', '30 mm')
      console.log(resto)
    }
}
</script>

<style>

</style>