<template>
  <div>
    <div class="home_nav">
      <div class="nav_wrap">
        <div class="logo_wrap">
          <img class="logo" src="./images/logo.png" alt="logo">
        </div>
        <div>
          <router-link :class="{native:this.$route.path === '/Home'}" to='Home' class="title">首页</router-link>
        </div>
        <div>
          <router-link :class="this.$route.path === '/Retail' ? 'native': ''" to='Retail' class="title">新零售S2B2C
          </router-link>
        </div>
        <div class="">
          <router-link :class="this.$route.path === '/Social' ? 'native': ''" to='Social' class="title">社交电商
          </router-link>
        </div>
        <div class="">
          <router-link :class="this.$route.path === '/Husbandry' ? 'native': ''" to='Husbandry' class="title">智慧农牧业
          </router-link>
        </div>
        <div class="">
          <router-link :class="this.$route.path === '/Applet' ? 'native': ''" to='Applet' class="title">小程序开发
          </router-link>
        </div>
        <div class="">
          <router-link :class="this.$route.path === '/Case' ? 'native': ''" to='Case' class="title">案例</router-link>
        </div>
        <div class="">
          <router-link :class="this.$route.path === '/Scheme' ? 'native': ''" to='Scheme' class="title">解决方案
          </router-link>
        </div>
        <div class="">
          <router-link :class="this.$route.path === '/About' ? 'native': ''" to='About' class="title">关于我们</router-link>
        </div>
      </div>
    </div>
    <keep-alive>
      <router-view></router-view>
    </keep-alive>
    <Footer/>
  </div>
</template>

<script>
  import Footer from './Footer/Footer'

  export default {
    data() {
      return {}
    },
    components: {
      Footer
    },
    methods: {}
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
  .home_nav {
    height: 200px
    position: relative
    left: 0
    top: 0
    right: 0
    margin-bottom -200px
    z-index: 99

    .nav_wrap {
      display: flex
      padding: 0 300px

      & div {
        flex: 1
        height: 100px
        line-height: 100px
        margin-top: 41px
        cursor: pointer

        a {
          color: #ffffff
        }

        .native {
          border-bottom 2px solid red
          padding-bottom 20px
          color: red
        }

        .title:hover {
          color: red
          border-bottom 2px solid red
          padding-bottom 20px
        }
      }

      .logo_wrap {
        margin-top: 61px
        width: 140px
        height: auto

        .logo {
          width: 140px
          height: auto
        }
      }
    }
  }
</style>
