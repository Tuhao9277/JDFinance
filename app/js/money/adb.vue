<template lang="html">
  <Panel :class="$style.panel">
    <section :class="$style.content">
      <img src="//img12.360buyimg.com/jrpmobile/jfs/t1/10419/26/10047/15305/5c540db7E72492e34/fa1c644b16d67f8a.png?width=750&height=120" alt="">
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
  components: {
    Panel,
  }

}
</script>
<style lang="scss" module>
@import "../../css/element";
.panel {
    @include panel;
    position: fixed;
    margin-top: 0;
    width: 100%;
    background: none;
    text-align: center;
    z-index: 999;
    > h4 {
        display: none;
    }
    img {

        width: 100%;
    }
}
</style>
