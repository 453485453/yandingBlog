<template lang="pug">
    div.content-friend
        myheader(:headerData="headerData")
        div.container-content
            v-container.v-container
                article#friend
                div.introduce
                    p 欢迎交换友链 ꉂ(ˊᗜˋ)
                    div.link-details
                        p 请发送邮件
                            span.code MjczOTA2OTA5M0BxcS5jb20=
                            span &nbsp;(base64)告诉我你的:
                        p 1、名字
                        p 2、一句话介绍
                        p 3、主页地址
                        p 4、头像地址（HTTPS*）
                    div.link-chestnut
                        p 栗子:
                        p ★ name: 凌寒初见
                        p ★ flag: 懒人一枚
                        P ★ webSite: https://yanding.com
                        P ★ avatar: url
                    div.link-explain
                        P ※ 欢迎大家互换友链,本站暂时只分两类、一类是'后宫'、一类是'冷宫'。
                            |'后宫'顾名思义就是我的后宫拉< (￣︶￣)>,
                            |'冷宫'顾名思义被我打入冷宫(如链接失效,保留一定时间,请及时联系我)
                            | 如果存在网站质量不佳,不会通知直接删除
                    div.link-title(v-if="allLink.harem.length? true:false")
                        P.title 后宫
                        p 看来今天朕的后宫也甚是安稳啊
                        friendItem(:friendData="allLink.harem")
                    div.link-title(v-if="allLink.coldPalace.length? true:false")
                        P.title 冷宫
                        P 大家不会怪我吧(￣o￣)
                        friendItem(:friendData="allLink.coldPalace")
</template>

<script>
import myheader from './../header/index'
import friendItem from './friendItem'

export default {
  name: 'friend',
  data: () => ({
    headerData: {
      background: require(`./../../assets/imgs/comic/689.png`),
      describe: '友人帐'
    },
    allLink: {
      harem: [
        { name: '素笺', webSite: 'http://sujian.yandingblog.cn', flag: '明天和意外，如果意外先来了，你的明天就不再是你的明天', avatar: 'http://img.cdn.yandingblog.cn/blog/favicon.ico' },
        { name: '素笺', webSite: 'http://sujian.yandingblog.cn', flag: '明天和意外，如果意外先来了，你的明天就不再是你的明天', avatar: 'http://img.cdn.yandingblog.cn/blog/favicon.ico' },
        { name: '素笺', webSite: 'http://sujian.yandingblog.cn', flag: '明天和意外，如果意外先来了，你的明天就不再是你的明天', avatar: 'http://img.cdn.yandingblog.cn/blog/favicon.ico' },
        { name: '素笺', webSite: 'http://sujian.yandingblog.cn', flag: '明天和意外，如果意外先来了，你的明天就不再是你的明天', avatar: 'http://img.cdn.yandingblog.cn/blog/favicon.ico' }
      ],
      coldPalace: [
        { name: '素笺', webSite: 'http://sujian.yandingblog.cn', flag: '明天和意外，如果意外先来了，你的明天就不再是你的明天', avatar: 'http://img.cdn.yandingblog.cn/blog/favicon.ico' },
        { name: '素笺', webSite: 'http://sujian.yandingblog.cn', flag: '明天和意外，如果意外先来了，你的明天就不再是你的明天', avatar: 'http://img.cdn.yandingblog.cn/blog/favicon.ico' },
        { name: '素笺', webSite: 'http://sujian.yandingblog.cn', flag: '明天和意外，如果意外先来了，你的明天就不再是你的明天', avatar: 'http://img.cdn.yandingblog.cn/blog/favicon.ico' },
        { name: '素笺', webSite: 'http://sujian.yandingblog.cn', flag: '明天和意外，如果意外先来了，你的明天就不再是你的明天', avatar: 'http://img.cdn.yandingblog.cn/blog/favicon.ico' }
      ]
    }
  }),
  components: {
    myheader,
    friendItem
  }
}
</script>

<style lang="stylus" scoped>
.link-details, .link-explain, .link-chestnut, .link-title, .link-title > p
  margin-top 24px

.title
  padding 0 10px
  font-size 18px
  color #6d6d6d
  border-left 3px solid #FE9600

.code
  background-color rgba(254,250,199,1)
  color #e67474
  text-shadow none
  border-radius 5px
</style>
