<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" />
        </div>
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data() {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl:
            '//imgs.qunarzz.com/p/p29/201302/28/3d20251a1b60350a93835fbb.jpg_256x160_e8f468b0.jpg',
          title: '北京-广州 3天自由行',
          desc:
            '中秋国庆大促 畅玩长隆欢乐世界+赏马戏团表演+维也纳酒店+接送机 广州3天游'
        },
        {
          id: '0002',
          imgUrl:
            '//imgs.qunarzz.com/p/p29/201302/28/3d20251a1b60350a93835fbb.jpg_256x160_e8f468b0.jpg',
          title: '北京-乌鲁瓦图情人崖 6天跟团游',
          desc:
            '国庆🔥相约巴厘岛，共度浪漫时光💞巴厘6日游 打卡网红景点网红大秋千+鸟巢'
        },
        {
          id: '0003',
          imgUrl:
            '//imgs.qunarzz.com/p/p29/201302/28/3d20251a1b60350a93835fbb.jpg_256x160_e8f468b0.jpg',
          title: '北京-海南 6天跟团游',
          desc:
            '中秋国庆付100抵300🔥住1线海景房玩双岛|蜈支洲+分界洲+天涯三亚6日'
        }
      ]
    }
  }
}
</script>

<style lang='stylus' scoped>
@import '~styles/mixins.styl';

.title
  margin-top: .2rem
  line-height: .8rem
  background: #eee
  text-indent: .2rem
.item-img-wrapper
  overflow: hidden
  height: 0
  padding-bottom: 33.9%
  .item-img
    width: 100%
.item-info
  padding: .1rem
  .item-title
    line-height: .54rem
    font-size: .32rem
    ellipsis()
  .item-desc
    line-height: .4rem
    color: #ccc
    ellipsis()
</style>
