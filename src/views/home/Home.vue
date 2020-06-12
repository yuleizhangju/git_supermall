<template>
  <div id="home">
    <nav-bar class="nav-home">

      <div slot="center">购物街</div>

    </nav-bar>

    <home-swiper :banners="banners" />


    <recommend :recommends="recommends" />

<!--    <Swiper>-->
<!--      <swiper-item v-for="item in banners">-->
<!--        <a :href="item.link">-->

<!--          <img :src="item.image">-->
<!--        </a>-->
<!--      </swiper-item>-->

<!--    </Swiper>-->


  </div>

</template>

<script>



  import NavBar from 'components/common/navbar/NavBar';

  import HomeSwiper from './childComps/HomeSwiper';

  import Recommend from './childComps/RecommendViw';


  import {getHomeMultidata} from 'network/home';



    export default {
        name: "Home",

        components:{

            NavBar,
            HomeSwiper,
            Recommend,

        },

        data() {

            return {

                banners:[],

                recommends:[]
            }

        },

        created() {

           // 1.请求多个数据
           getHomeMultidata().then(res => {

               console.log(res);

               this.banners = res.data.banner.list;

                this.recommends = res.data.recommend.list;
           })

        }
    }
</script>

<style scoped>

  .nav-home{

    box-shadow: 0 1px 1px rgba(100,100,100,.2);
    /*//变量赋值*/
    background-color:var(--color-tint);
    color: #ffffff;
  }

  .nav-home-left{

  }

</style>