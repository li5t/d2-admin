<template>
  <d2-container>
    <template slot="header">Element 滚动条组件</template>
    <el-card shadow="never" class="demo-scrollbar-card d2-mb">
      <div class="demo-scrollbar-card-inner">
        <el-scrollbar>
          <div class="demo-scrollbar-group">
            <div v-for="n in 20" :key="n" class="demo-scrollbar-item">
              <el-button size="mini">n : {{n}}</el-button>
            </div>
          </div>
        </el-scrollbar>
      </div>
    </el-card>
    <d2-markdown :source="doc"/>
  </d2-container>
</template>

<script>
import doc from './md/doc.md'
export default {
  data () {
    return {
      doc
    }
  }
}
</script>


<style lang="scss" scoped>
@import '~@/assets/style/public.scss';
.demo-scrollbar-card {
  width: 300px;
  .demo-scrollbar-card-inner {
    margin: -20px;
  }
  .demo-scrollbar-group {
    height: 200px;
    .demo-scrollbar-item {
      padding: 10px;
      border-bottom: 1px solid $color-border-4;
      &:last-child {
        border-bottom: none;
      }
    }
  }
}
</style>
