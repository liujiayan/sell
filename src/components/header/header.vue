<template>
  <div class="header">
      <div class="content-wrapper">
          <div class="avatar">
              <img :src="seller.avatar" width="64" height="64">
          </div>
          <div class="content">
              <div class="title">
                  <span class="brand"></span>
                  <span class="name">{{seller.name}}</span>
              </div>
              <div class="description">
                  {{seller.description}}/{{seller.deliveryTime}}分钟送达
              </div>
              <div v-if="seller.supports" class="support">
                  <span class="icon"></span>
                  <span class="text">{{seller.supports[0].description}}</span>
              </div>
          </div>
      </div>
      <div class="bulletin-wrapper">

      </div>
  </div>
</template>

<script>
export default  {
    props:{
        seller:{
            type:Object
        }
    }
}
</script>

<style lang="scss" rel="stylesheet/scss">
    @import "../../common/sass/mixin";
    .header{
        color:#fff;
        background:#000;
        .content-wrapper{
            padding: 24px 12px 18px 24px;
            font-size: 0;
            .avatar{
                display: inline-block;
                vertical-align: top;
                img{
                    border-radius: 2px;
                }
            }
            .content{
                display: inline-block;
                margin-left: 14px;
                .title{
                    margin:2px 0 8px 0;
                    .brand{
                        display: inline-block;
                        vertical-align: top;
                        width: 30px;
                        height: 18px;
                        @include bg-image("brand");
                        background-size: 30px 18px;
                        background-repeat: no-repeat;
                    }
                    .name{
                        margin-left: 6px;
                        font-size: 16px;
                        line-height: 18px;
                        font-weight: bold;
                    }
                }
                .description{
                    margin-bottom:10px;
                    line-height: 12px;
                    font-size: 12px;
                }
            }
        }
    }

</style>
