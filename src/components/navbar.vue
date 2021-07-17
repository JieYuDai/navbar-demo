<template>
  <div class="nav-comps">
    <nav class="clearfix">
      <span href="#" id="pull">Menu</span>
      <ul class="clearfix" ref="navbar">
        <li><img src="../assets/logo.png" style="margin-top: 4px;"></li>
        <li><span :class="active === '/home' ? 'active' : ''">首页</span></li>
        <li><span :class="active === '/product' ? 'active' : ''">产品介绍</span></li>
        <li><span :class="active === '/case' ? 'active' : ''">案例分享</span></li>
        <li><span :class="active === '/news' ? 'active' : ''">新闻动态</span></li>
        <li><span :class="active === '/about' ? 'active' : ''">关于XX</span></li>
        <li><span :class="active === '/contact' ? 'active' : ''">联系我们</span></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  data () {
    return {
      active: '/home'
    }
  }
}
</script>

<style lang="less" scoped>
.nav-comps {
  nav {
    height: 60px;
    position: fixed;
    width: 100%;
    background: #FFF;
    font-size: 15px;
    font-family: 'PT Sans', Arial, sans-serif;
    font-weight: bold;
    border-bottom: 1px solid #eeeeee;
    ul {
      display: table;
      height: 60px;
      margin: 0 auto;
      li {
        display: inline;
        float: left;
        &:first-child {
          margin-right: 120px;
        }
        span {
          color: #333;
          display: inline-block;
          width: 100px;
          text-align: center;
          text-decoration: none;
          line-height: 60px;
          cursor: pointer;
          &:hover {
            color: #1896D3;
          }
        }
        .active {
          color: #1896D3;
        }
      }
    }
  }
}
</style>