<div class='content-container'>
	<slot />
</div>

<style lang='sass'>
  @import '../../vars'
  *
    box-sizing: border-box

  .content-container
    width: 100%
    margin: 0 auto
    position: relative
    @media screen and (max-width: $mobile)
      max-width: 90%
    @media screen and (min-width: $desktop)
      max-width: 100%
    @media screen and (min-width: $large)
      max-width: 1536px
</style>
