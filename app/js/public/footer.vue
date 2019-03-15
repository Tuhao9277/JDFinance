<template lang="html">
  <Panel title="公司信息" :class="$style.panel">
    <ul :class="$style.content">
      <li>
        <div>
          <img src="//img12.360buyimg.com/jrpmobile/jfs/t7618/313/3082994165/3330/e1692006/59b90247Nac3c9ebe.png?width=56&height=56" alt="">
          <p>客户端</p>
        </div>
        <div>
          <img src="//img12.360buyimg.com/jrpmobile/jfs/t7618/313/3082994165/3330/e1692006/59b90247Nac3c9ebe.png?width=56&height=56" alt="">
          <p>触屏版</p>
        </div>
        <div>
          <img src="//img12.360buyimg.com/jrpmobile/jfs/t7618/313/3082994165/3330/e1692006/59b90247Nac3c9ebe.png?width=56&height=56" alt="">
          <p>电脑版</p>
        </div>
      </li>
      <li>Copyright © 2004-2019 京东JD.com 版权所有</li>
      <li>投资有风险，购买需谨慎</li>
      <li>京东金融平台服务协议</li>
      <li>京东金融隐私政策</li>

    </ul>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue";
export default {
  components: {
    Panel
  }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
    margin-bottom: 100px;
    & > h4 {
        display: none;
    }
    .content {
        @include flex;
        background: #f5f5f5;
        li {
            width: 100%;
            text-align: center;
            color: #999;
            font-size: 20px;
            &:nth-child(1) {
                @include flex(row);
                height: 186px;

                box-sizing: border-box;
                > div {
                    width: 33.33333%;
                    text-align: center;
                    box-sizing: border-box;
                    padding-top: 20px;
                    img {
                        width: 90px;
                        height: 90px;
                    }
                    p {
                        font-size: 26px;
                        text-align: center;
                        display: block;
                        color: #999;
                        margin-top: 20px;
                        white-space: nowrap;
                        text-overflow: ellipsis;
                        overflow: hidden;
                    }
                }
            }
            &:nth-child(n+2) {
                padding: 24px 0;
                height: 38px;
                line-height: 38px;
                border-top: 1px solid #ddd;
            }
        }

    }
}
</style>
