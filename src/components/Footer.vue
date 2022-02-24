<template>
  <div class="footer-wrapper">
    <div class="copy-right-wrapper">
      <img class="logo" :src="logoUrl" :alt="$store.getters.imgAlt + 'footerLogo'" />
      <div class="copy-right">
        <span>轻云网盘 2022 版权所有</span>
        <span class="split">|</span>
        <span>
          <a class="link" style="color: white" target="_blank">xxxxxxxxxx号</a>&nbsp;
        </span>
        <p class="tip-website">
          为获得最佳浏览体验，建议使用IE11、FireFox50.5、Chrome51.0及以上版本的浏览器
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      logoUrl: require('@/assets/images/common/logo_footer.png'),
      joinList: [
        {
          class: 'qq',
          logo: 'icon-qq',
          // img: require('@/assets/images/footer/QQImg.png'),
          // title: 'QQ群'
        },
        {
          class: 'wechat',
          logo: 'icon-weixin-copy',
          // img: require('@/assets/images/footer/wechatImg.png'),
          // title: '微信公众号'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl';

.footer-wrapper {
  //margin-top: 20px;
  //display: flex;

  .copy-right-wrapper {

    width: 100%;
    color: $BorderLight;
    background: linear-gradient(to right, $Primary, #66b1ff);
    padding: 16px 0 16px 5vw;
    //margin:0 auto;
    font-size: 14px;
    color: $BorderLight;
    display: flex;
    align-items: center;

    .logo {
      width: 240px;
      display: block;
    }

    .split {
      margin: 0 8px;
    }

    .link {
      &:hover {
        text-decoration: underline;
      }
    }

    .tip-website {
      padding-top: 8px;
    }
  }

}
</style>
