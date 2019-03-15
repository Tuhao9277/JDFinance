<template lang="html">
    <div>
      <Heador/>
      <Navbar/>
      <Slider/>
      <Novice/>
      <Borrow/>
      <Money/>
      <Bounty/>
      <Insurance/>
      <Footor/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Footor from "../public/footer.vue"
import Navbar from "../public/navbar.vue"
import Slider from "./hslider.vue"
import Novice from "./novice.vue"
import Borrow from "./borrow.vue"
import Money from "./money.vue"
import Bounty from "./bounty.vue"
import Insurance from "./insurance.vue"
export default {
  components: {
    Heador,
    Footor,
    Navbar,
    Slider,
    Novice,
    Borrow,
    Money,
    Bounty,
    Insurance
  }
}
</script>
