<template lang="html">
  <Panel title="轮播图" :class="$style.panel">
    <section :class="$style.content">
      <Slider :items="items" :cname="$style.slider" />
      <div :class="$style.sign">
          <div :class="$style.member">会员等级</div>
          <div :class="$style.main">立即登录，马上赚钱</div>
          <div :class="$style.login">签到</div>

      </div>
    </section>
    <section :class="$style.list">
      <div :class="$style.item" v-for="item in enters" :key="item.img">
      <router-link :to="{ name: item.href }">
        <img :src="item.img" :alt= "item.title">
          <h4>{{item.title}}</h4>
        </img>
      </router-link>
      </div>
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
import Slider from "../core/slider.vue"
export default {
  components: {
    Panel,
    Slider,
  },
  data() {
    return {
      items: [{
          href: "Home",
          src: "//img12.360buyimg.com/jrpmobile/jfs/t1/24150/11/2262/34198/5c1b0bd5E34fa892f/054c0bf91c3bcb76.jpg?width=750&height=400"
        },
        {
          href: "Home",
          src: "//img12.360buyimg.com/jrpmobile/jfs/t1/20317/19/9235/129533/5c7cb47aEedbdd8ee/1c8891785c20bf48.jpg?width=750&height=400"
        },
        {
          href: "Home",
          src: "//img12.360buyimg.com/jrpmobile/jfs/t1/10417/12/14059/132199/5c85b9beE945f7162/8b5f01aed40f1725.jpg?width=750&height=400"
        },
        {
          href: "Home",
          src: "//img12.360buyimg.com/jrpmobile/jfs/t1/10269/23/13597/54795/5c820caaE075c87c5/49bd5c51d63b1034.jpg?width=750&height=400"
        },
      ],
      enters: [{
          href: "Home",
          img: "//img12.360buyimg.com/jrpmobile/jfs/t28189/232/289098066/5076/dfe2d74f/5bee6bb4N4ec4cede.png?width=90&height=90",
          title: "领红包"
        }, {
          href: "Home",
          img: "//img12.360buyimg.com/jrpmobile/jfs/t27334/12/1829630702/5159/f8133cd6/5bee6bbdN8606cfbb.png?width=90&height=90",
          title: "领福利"
        },
        {
          href: "Home",
          img: "//img12.360buyimg.com/jrpmobile/jfs/t27796/46/1836066448/4169/de69ccb0/5bee6bc3N92ca0e60.png?width=90&height=90",
          title: "领券"
        },
        {
          href: "Home",
          img: "//img12.360buyimg.com/jrpmobile/jfs/t27850/30/1789047580/4856/13f8bcb9/5bee6bcbN996fb433.png?width=90&height=90",
          title: "领京豆"
        },
        {
          href: "Home",
          img: "//img12.360buyimg.com/jrpmobile/jfs/t29131/288/288291507/3943/bed46aef/5bee6bd5Nfc5d5360.png?width=90&height=905",
          title: "全部"
        },

      ],
    }
  }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
    > h4 {
        display: none;
    }
    .content {
        height: 440px;
        .slider {
            margin-top: 100px;
            img {
                width: 100%;
            }
        }
        .sign {
            @include flex(row);
            margin: 0 16px;
            background: #fff;
            box-shadow: 0 0 10px 0.5px rgba(101,118,155,.15);
            border-radius: 4px;
            height: 120px;
            line-height: 120px;
            position: relative;
            z-index: 3;
            .member {

                color: #fff;
                height: 66px;
                line-height: 66px;
                font-size: 25px;
                margin-top: 20px;
                margin-left: 20px;
                border-radius: 2px;
                background: url("data:image/png;base64,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") 50% no-repeat;
                background-size: cover;
                box-shadow: 0 3px 4px 0 hsla(41,44%,63%,.51);
            }
            .main {
                font-family: PingFangSC-Semibold;
                font-size: 28px;
                color: #c6a76f;
                letter-spacing: 0;
                line-height: 130px;
                text-align: left;
                padding-left: 20px;
                box-sizing: border-box;
            }
            .login {
                position: absolute;
                right: 30px;
                width: 140px;
                height: 66px;
                line-height: 66px;
                color: #fff;
                text-align: center;
                font-size: 24px;
                margin-top: 20px;
                background: orange;
                border-radius: 30px;
                background: url("data:image/png;base64,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") 50% no-repeat;
                background-size: cover;
                box-shadow: 0 8px 12px 0 hsla(40,41%,61%,.41);
            }
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

            text-align: center;
            img {
                margin: 10px 20px;
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
}
</style>
