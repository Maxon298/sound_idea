<template>
  <div>
    <header class="header">
      <div class="header__content">
        <div class="_container">
          <div class="_row">
            <div class="logo">
              <img width='166' height='36' src="@/assets/img/svg/logo.svg" alt="Logo">
            </div>
            <div class="fast-access">

            </div>
          </div>
        </div>
      </div>
      <div class="header__nav">
        <div class="_container">
          <div class="_row">
            <div class="nav-item">
              Acapellas
            </div>
            <div class="nav-item">
              Loop & Samples
            </div>
            <div class="nav-item">
              Presets
            </div>
            <div class="nav-item">
              Projects
            </div>
            <div class="nav-item">
              MIDI
            </div>
            <div class="nav-item">
              VST plugins
            </div>
            <div class="nav-item">
              FAQ
            </div>
            <div class="nav-item">
              Community
            </div>
            <div class="nav-item">
              Support/Donate
            </div>
          </div>
        </div>
      </div>
    </header>
    <Nuxt class=''/>
    <footer class="footer"></footer>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss">
  .header{
    &__content{
      background: #16162C;
      height: 65px;
    }
    &__nav{
      height: 35px;
      ._row{
        align-items: center;
      }
      background: #444674;
      .nav-item{
        color: white;
        font-size: 10px;
        &:not(:last-child){
          
          margin-right: 16px;
        }
      }
    }
  }
</style>
