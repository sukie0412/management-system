<template>
  <section class="container">
    <el-container>
      <el-header>
        <button-top></button-top>
      </el-header>
      <el-container>
        <el-aside>
          <aside-List></aside-List>
        </el-aside>
          <el-main>
            <breadcrumb></breadcrumb>
            <nuxt/>
          </el-main>
        </el-container>
    </el-container>
  </section>
</template>

<script>
import buttonTop from '~/components/buttonTop'
import asideList from '~/components/asideList'
import breadcrumb from '~/components/breadcrumb'

export default {
  // layout: 'one',
  components: {
    buttonTop,
    asideList,
    breadcrumb
  },
  data () {
    return {
    }
  },
  methods: {
  }
}
</script>

<style>
</style>
