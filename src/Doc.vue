<style lang=less>
</style>

<template>
  <div>
    <doc :name="name"
      :desc="desc"
      :parm_desc="parm_desc"
      :parms="parms"
      :code="code"
      :call_back="call_back"
      >
      <bz type="warning">出错了</bz>
    </doc>
  </div>
</template>

<script>
  import 'bz-semantic-ui-card'
  import 'bz-semantic-ui-grid'
  import Bz from './Bz'
  import Doc from 'bz-doc'
  export default {
    components: {
      Bz,
      Doc
    },
    route: {
      deactivate: function (transition) {
      }
    },
    data: function () {
      return {
        datas: [1],
        name: 'bz-weui-toast',
        desc: '用来弹出we-ui的信息提示',
        parms: [
          {parm: 'type', desc: 'info success loading warning'}
        ],
        parm_desc: `info 和 warning 依赖引入 semantic 的 icon css`,
        code: `<bz type="warning">出错了</bz>`
      }
    },
    methods: {
    }
  }
</script>
