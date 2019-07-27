<template>
    <div class="wrapper">
 <swiper :options="swiperOption">
    
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.url">
    </swiper-slide>


    
    <div class="swiper-pagination"  slot="pagination">   
    </div>
    
  </swiper>
  </div>
</template>

<script >
	export default{
		name: "HomeSwiper",
		data: function(){
			return {
				swiperOption:{
                    pagination: '.swiper-pagination',
                    loop: true
                },
                swiperList:[{
                    id: '0001',
                    url: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/f4168ba20e0f5218ed83e743efd802b2.jpg_750x200_53edd3a0.jpg'
                },{
                    id: '0002',
                    url: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/818f6cc784ae6669b74bbbb255414a53.jpg_750x200_66ca5873.jpg'
                }]
			}
		}
	}
</script>


<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
    background: #fff

.wrapper  /*防止网络慢的时候抖屏*/
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 31.25%
.swiper-img
    width: 100%

</style>