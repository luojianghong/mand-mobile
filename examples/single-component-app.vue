<template>
  <div class="mand">
    <div class="md-example-wrapper">
      <demo></demo>
    </div>
  </div>
</template>

<script>
import './assets/responsive'

export default {
  name: 'app',
  components: {
    demo: () => import(`../components/${COMPONENT_NAME}/demo`),
  },
}

</script>

<style lang="stylus">
block()
  float left
  width 100%
.mand
  position relative
  min-height 100%
  max-width 750px
  font-size 28px
  font-size-adjust none
  -webkit-text-size-adjust 100%
  -webkit-overflow-scrolling touch
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  background color-primary-background
  .md-nav
    position relative
    display flex
    padding 32px 20px
    p
      position relative
      display inline-block
      line-height 1
      &.home
        top 10px
        .md-icon
          color color-text-base
      &.name
        margin-left h-gap-lg
        font-size font-heading-large
        font-weight font-weight-medium
        color color-text-base
      &.name-zh
        top 9px
        margin-left h-gap-sm
        font-size font-body-large
        font-weight font-weight-normal
        color color-text-minor
        
  .md-example-wrapper
    position relative
    z-index 3
    padding 20px
    clearfix()
    .md-example
      .md-example-section
        clearfix()
        margin-bottom 30px
        color color-text-base
        .md-example-title
          block()
          font-size font-body-normal
          font-weight font-weight-medium
          a
            margin-right 5px
            background color-primary
            color #fff
            padding 5px 10px
            border-radius radius-normal
            font-size font-minor-large
            font-weight 300
            line-height 28px
            text-decoration none
        .md-example-describe
          block()
          margin-top 15px
          font-size font-minor-large
          font-weight 300
          color color-text-minor
        .md-example-content
          block()
          position relative
          margin-top 20px
          box-sizing border-box
          font-size 28px
.md-dialog pre
  width 100%
  padding 20px 10px
  box-sizing border-box
  white-space pre-wrap
  word-wrap break-word
  font-size font-minor-normal
  background color-primary-background
  border-radius radius-normal
@media screen and (min-width: 749px)
  .mand
    margin-left -360px
    left 50%
</style>

