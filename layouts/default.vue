<template>
  <div>
    <header class="header">
      <div class="header__content">
        <div class="_container">
          <div class="header__content-inner">
            <div class="logo">
              <img width='166' height='36' src="@/assets/img/svg/logo.svg" alt="Logo">
            </div>
            <div class="fast-access">
              <btn class='fast-access__item header-btn header-btn_login' darkBtn :name="`Login`"/>
              <btn class='fast-access__item header-btn header-btn_register' gradientBtn :name="`Register`"/>
            </div>
          </div>
        </div>
      </div>
      <div class="header__nav">
        <div class="_container">
          <div class="header__nav-inner">
            <nuxt-link to="#"  class="nav-item">
              Acapellas
            </nuxt-link>
            <nuxt-link to="#"  class="nav-item">
              Loop & Samples
            </nuxt-link>
            <nuxt-link to="#"  class="nav-item">
              Presets
            </nuxt-link>
            <nuxt-link to="#"  class="nav-item">
              Projects
            </nuxt-link>
            <nuxt-link to="#"  class="nav-item">
              MIDI
            </nuxt-link>
            <nuxt-link to="#"  class="nav-item">
              VST plugins
            </nuxt-link>
            <nuxt-link to="#"  class="nav-item">
              FAQ
            </nuxt-link>
            <nuxt-link to="#"  class="nav-item">
              Community
            </nuxt-link>
            <nuxt-link to="#"  class="nav-item">
              Support/Donate
            </nuxt-link>
          </div>
        </div>
      </div>
    </header>
    <Nuxt/>
    <footer class="footer">
      <div class="footer__nav">
        <div class="_container">
          <div class="footer__nav-inner">
            <div class="logo">
              <img width='166' height='36' src="@/assets/img/svg/logo.svg" alt="Logo">
            </div>
            <div class="nav-items">
              <nuxt-link to="#" class="item">Privacy Policy</nuxt-link>
              <nuxt-link to="#" class="item">Terms And Conditions</nuxt-link>
              <nuxt-link to="#" class="item">Our Contacts</nuxt-link>
            </div>
          </div>
        </div>
      </div>
      <div class="footer__copy">
        <div class="_container">
          <div class="footer__copy-inner">
            <div class="text copyright">Copyright (C) Soundidea 2020</div>
            <div class="text made-by">Created by MaxBush</div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  components:{
    btn:() => import("@/components/controls/btn.vue")
  }
}
</script>

<style lang="scss">
  .header{
    &__content{
      background: #16162C;
      height: 65px;
      &-inner{
        justify-content: space-between;
        height: 100%;
        width: 100%;
        display: flex;
        align-items: center;
      }
      .fast-access{
        display: flex;
        &__item{
          &:not(:last-child){
            margin-right: 19px;
          }
          &:first-child{
            margin-right: 30px;
          }
        }
        .header-btn{
          height: 29px;
          border-radius: 50px;
          padding: 0 21px;
        }

      }
    }
    &__nav{
      height: 35px;
      &-inner{
        height: 100%;
        width: 100%;
        display: flex;
        align-items: center;
      }
      background: #444674;
      .nav-item{
        text-decoration: none;
        cursor: pointer;
        color: white;
        font-size: 10px;
        &:not(:last-child){

          margin-right: 16px;
        }
      }
    }
  }

  .footer{
    &__nav{
      background: #16162C;
      &-inner{
        height: 65px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        .nav-items{
          display: flex;
          .item{
            text-decoration: none;
            font-size: 10px;
            line-height: 12px;
            color: #59596E;
            &:not(:last-child){
              margin-right: 23px;
            }
          }
        }
      }
    }
    &__copy{
      background: #444674;
      &-inner{
        height: 35px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        .text{
          color: #9C9DB5;
          font-size: 10px;
          line-height: 12px;
        }
      }
    }
  }
</style>
