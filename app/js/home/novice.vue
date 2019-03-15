<template lang="html">
  <Panel title="新手特权" :class="$style.panel">
    <section :class="$style.content">
      <!-- 下左 -->
      <div :class="$style.item">
        <h4>下载APP<span :class="$style.red">送888元红包</span></h4>
        <p :class="$style.gray">新手专享</p>
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t27850/30/1789047580/4856/13f8bcb9/5bee6bcbN996fb433.png?width=90&height=90" alt="">
      </div>
      <!-- 下右 -->
      <div :class="$style.item">
        <ul>
          <li>
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t28189/232/289098066/5076/dfe2d74f/5bee6bb4N4ec4cede.png?width=90&height=90" alt="">
            <h4 :class="$style.red">领128元现金红包</h4>
            <p :class="$style.gray">立即开通</p>
          </li>
          <li>
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135" alt="">
            <h4>打白条<span :class="$style.red">抢免息</span></h4>
            <p :class="$style.gray">立即开通抢豪礼</p>
          </li>

        </ul>
      </div>
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
  components:{
    Panel,
  }
}
</script>

<style lang="scss" module>
  @import "../../css/element.scss";
  .panel{
    @include panel;
    >h4{
      border-bottom: 1px solid #ddd;
    }
    .content{
      @include list(row);
      .item{
        width: 50%;
        box-sizing: border-box;
        &:first-child{
          padding: 32px 20px;
          text-align: center;
          border-right: 1px solid #ddd;
          img{
            width: 132px;
            height: 132px;
            margin: 20px auto 0;
          }
        }
        h4{
          font-size: 26px;
          line-height: 40px;
        }
        .red{
          color: #f00;
        }
        .gray{
          color: #999;
          font-size: 24px;
        }
        p{
          margin-top: 6px;
          font-size: 24px;
        }
        ul{
          width: 100%;
          li{
            height: 144px;
            width: 100%;
            padding: 32px 28px;
            box-sizing: border-box;
            &:first-child{
              border-bottom: 1px solid #ddd;
            }
            h4{
              white-space: nowrap;
              text-overflow: ellipsis;
              overflow: hidden;
              text-align: left;
            }
            img{
              width: 80px;
              height: 80px;
              float: right;
            }
          }
        }
      }
    }
  }

</style>
