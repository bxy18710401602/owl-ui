<template>
  <owl-page>
    <div class="button-wrap">
      <owl-button @click="handle">Default Button</owl-button>

      <owl-button type="disabled">Disabled Button</owl-button>

      <owl-button type="light">Light Button</owl-button>

      <owl-button :inline="true">Inline Button</owl-button>

      <owl-button :outline="true">Outline Button</owl-button>

      <owl-button-group>
        <owl-button type="light"
                    :outline="true"
                    :inline="true">Inline Button</owl-button>
        <owl-button type="light"
                    :inline="true">Light Button</owl-button>
      </owl-button-group>

      <owl-button :btnStyle="btnStyle">Custom Button</owl-button>
    </div>
  </owl-page>
</template>

<script>
export default {
  data () {
    return {
      btnStyle: {
        border: '1px solid #090A0D',
        background: '#584628',
        color: '#F1D024'
      }
    }
  },
  methods: {
    handle (event) {
      console.log('event', event)
    }
  }
}
</script>

<style lang="less" scoped>
.button-wrap {
  text-align: center;
  padding: 0 30px;
}
button {
  margin: 20px 0;
}
</style>