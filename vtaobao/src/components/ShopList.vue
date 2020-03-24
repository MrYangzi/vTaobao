<template>
  <div class="shop-list">
      <ul>
        <li v-for="(item,index) in shops" :key="index">
            <div class="shop-wrap">
                <div class="shop-img">
                    <img :src="item.imgSrc" />
                </div>
                <p class="shop-name">{{item.title}}</p>
                <p class="shop-desc"><span class="price"><em>￥</em>{{item.price}}</span><span class="pay-num">{{item.pay_num}}人付款</span></p>
            </div>
        </li>
      </ul>
  </div>  
</template>

<script>
import shop1 from '@/assets/images/shop_1.jpg'
import shop2 from '@/assets/images/shop_2.jpg'
import shop3 from '@/assets/images/shop_3.jpg'
import shop4 from '@/assets/images/shop_4.jpg'


export default {
  name: 'ShopList',
  data () {
    return {
       shops:[{
         url:'/shopDetail/1',
         title:'男士2019工装外套秋季胖子夹克大码宽松百搭',
         price:'128',
         old_price:'688.99',
         pay_num:'840',
         imgSrc:shop1
       },{
         url:'/shopDetail/2',
         title:'飞天茅台酒国产白酒43度500ml酱香型白酒',
         price:'838',
         old_price:'998',
         pay_num:'4370',
         imgSrc:shop2
       },{
         url:'/shopDetail/3',
         title:'外套男春秋季2019新款韩版潮流工装',
         price:'118',
         old_price:'338',
         pay_num:'24617',
         imgSrc:shop3
       },{
         url:'/shopDetail/4',
         title:'5.0蓝牙耳机运动跑步无线双耳入耳塞头戴',
         price:'79',
         old_price:'199',
         pay_num:'23651',
         imgSrc:shop4
       }]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
  @import '../assets/styles/common';
  .shop-list{
      width:100%;
      ul{
          width:100%;
          margin:0;
          padding:0;
          li{
              width:50%;
              list-style: none;
              overflow:hidden;
              float:left;
              margin:5px 0 15px;
          }
      }
  }
  .shop-wrap{
      padding:2px;
      p{
          font-size:14px;
          padding:0;
          margin:0;
          text-align: left;
      }
      p.shop-name{
          color:#333;
      }
      p.shop-desc{
          color:#999999;
          span.price{
              font-size:18px;
              color:#de2727;
          }
          span.pay-num{
              float:right;
          }
          em{
              font-style:normal;
          }
      }
  }
  .shop-img{
      width:100%;
      height:172px;
      overflow:hidden
  }
  .shop-img img{
      width:100%;
      height:100%;
  }
</style>
