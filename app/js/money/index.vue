<template lang="html">
    <div>
      <Heador/>
      <Adb/>
      <Navbar/>
      <Slider/>
      <Footor/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Adb from "./adb.vue"
import Footor from "../public/footer.vue"
import Navbar from "../public/navbar.vue"
import Slider from "./mslider.vue"

export default {
  components: {
    Heador,
    Adb,
    Footor,
    Navbar,
    Slider,

  }
}
</script>
