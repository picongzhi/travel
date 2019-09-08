<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data() {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl:
            '//imgs.qunarzz.com/vs_ceph_vs_tts/32014fe7-4918-4bdc-b361-ce6ffb9bc5bb.jpg_r_480x320x90_bf60e27b.jpg',
          title: '北京-广州 3天自由行',
          desc:
            '中秋国庆大促 畅玩长隆欢乐世界+赏马戏团表演+维也纳酒店+接送机 广州3天游'
        },
        {
          id: '0002',
          imgUrl:
            '//imgs.qunarzz.com/vs_ceph_vs_tts/d2fd1bcb-1ce3-427e-a61c-7c0c41c2196a.jpg_r_390x260x90_733fb20e.jpg',
          title: '北京-乌鲁瓦图情人崖 6天跟团游',
          desc:
            '国庆🔥相约巴厘岛，共度浪漫时光💞巴厘6日游 打卡网红景点网红大秋千+鸟巢'
        },
        {
          id: '0003',
          imgUrl:
            '//imgs.qunarzz.com/vs_ceph_vs_tts/fb5fbf5c-4f85-482b-91d6-4ce17a42618d.jpg_r_390x260x90_aae85edf.jpg',
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
.item
  display: flex
  height: 1.9rem
  overflow: hidden
  .item-img
    width: 1.7rem
    height: 1.7rem
    padding: .1rem
  .item-info
    flex: 1
    padding: .1rem
    min-width: 0
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
    .item-button
      line-height: .44rem
      margin-top: .16rem
      background: #ff9300
      padding: 0 .2rem
      border-radius: .06rem
      color: #fff
</style>
