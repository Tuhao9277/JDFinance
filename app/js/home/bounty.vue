<template lang="html">
  <Panel title="赏金任务" :class="$style.panel">
    <section :class="$style.content">
    <div class="arrow">查看更多任务></div>
      <Slider :options="options" :items="items" cname="bounty-slider" />
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel";
import Slider from "../core/slider";
export default {
  components: {
    Panel,
    Slider,
  },
  data() {
    return {
      items: [{
          href: "Home",
          src: "//img12.360buyimg.com/jrpmobile/jfs/t26893/316/1416172900/5740/58f20b1e/5bc82e3aN7aa90a89.png?width=210&height=260",
        },
        {
          href: "Home",
          src: "//img12.360buyimg.com/jrpmobile/jfs/t26767/72/1365822552/8516/2e071d95/5bc82e6eN0be93809.png?width=210&height=260",
        },
        {
          href: "Home",
          src: "//img12.360buyimg.com/jrpmobile/jfs/t27040/190/1395454031/8316/d3d74de2/5bc82eb2N34a7625d.png?width=210&height=260",
        },
        {
          href: "Home",
          src: "//img12.360buyimg.com/jrpmobile/jfs/t26182/297/1417522782/7864/19181a3b/5bc82ec0N0824153d.png?width=210&height=260",
        }
      ],
      options: {
        slidesPerView: 3,
        spaceBetween: 30,

      },
    }
  }
}
</script>

<style lang="scss" >
.bounty-slider {
    .swiper-container {
        box-sizing: border-box;
        padding: 0 24px;
        .swiper-slide {
            a {
                display: inline-block;
                width: 100%;
                img {
                    width: 100%;
                    display: block;
                    height: 100%;
                    border: 1px solid #fafafa;
                }
            }
        }
    }
}
</style>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
    .content {
        position: relative;
        padding-bottom: 40px;
        & > div {
            position: absolute;
            font-size: 24px;
            color: #999;
            right: 30px;
            top: -66px;
        }
    }
}
</style>
