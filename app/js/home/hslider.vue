<template lang="html">
  <article class="">
    <Slider :items="items" :cname="$style.slider"/>
    <section :class="$style.list">
      <div :class="$style.item" v-for="item in enters" :key="item.img">
      <router-link :to="{ name: item.href }">
        <img :src="item.img" :alt= "item.title">
          <h4>{{item.title}}</h4>
        </img>
      </router-link>
      </div>
    </section>
  </article>
</template>

<script>
import Slider from "../core/slider.vue"
export default {
  components: {
    Slider,
  },
  data() {
    return {
      items: [{
          href: "Home",
          src: "//img12.360buyimg.com/jrpmobile/jfs/t1/15728/17/9256/37518/5c7cbafcEcec56aa3/d478a4f664671e07.jpg?width=750&height=320"
        },
        {
          href: "Home",
          src: "//img12.360buyimg.com/jrpmobile/jfs/t1/11521/24/9922/39391/5c7cbb4eE0d439ba7/bcfdaa5cb9f1df78.jpg?width=750&height=320"
        },
      ],
      enters: [{
          href: "Home",
          img: "//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
          title: "优惠券"
        }, {
          href: "Home",
          img: "//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
          title: "领福利"
        },
        {
          href: "Home",
          img: "//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132",
          title: "抢钢镚"
        },
        {
          href: "Home",
          img: "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
          title: "白条提额"
        },
        {
          href: "Home",
          img: "//img12.360buyimg.com/jrpmobile/jfs/t1/520/34/950/3686/5b9239e3Eaaf5465c/8d8c35badacfc114.png?width=90&height=90",
          title: "工资理财"
        }, {
          href: "Home",
          img: "//img12.360buyimg.com/jrpmobile/jfs/t1/1216/39/659/4516/5b923b1cE5943d1c6/dabaf8b842f57eb9.png?width=90&height=90",
          title: "众筹"
        },
        {
          href: "Home",
          img: "//img12.360buyimg.com/jrpmobile/jfs/t1/3924/28/657/3552/5b9240dbE60256c31/78b52d5ab675f800.png?width=90&height=90",
          title: "租房"
        },
        {
          href: "Home",
          img: "//img12.360buyimg.com/jrpmobile/jfs/t27088/243/2089650291/12365/2469f395/5bf677f9N795eec5e.png?width=120&height=120",
          title: "车主服务"
        },
      ],
    }
  },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.slider {
    margin-top: 100px;
    img {
        width: 100%;
    }
}
.list {
    @include list(row);
    background: #fff;
    padding-top: 40px;
    padding-bottom: 20px;
    justify-content: space-around; //两端对齐
    a {
        text-decoration: none;
    }
    .item {
        margin: 10px;
        text-align: center;
        img {
            margin: 10px 30px;
            display: inline-block;
            width: 80px;
            height: 80px;
        }
        h4 {
            font-size: 26px;
            margin-top: 12px;
            color: #666;
        }
    }
}
</style>
