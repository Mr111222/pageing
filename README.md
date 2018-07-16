<template lang="pug">
.main
  CbPaging(:allPage="allPage" :currentPage="currentPage" :currentChange="toPage")
  br
  CbPaging(:allPage="allPage" size="smail" :currentPage="currentPage" :currentChange="toPage")
  br
  CbPaging(:allPage="allPage" size="mini" :currentPage="currentPage" :currentChange="toPage")
  br
  CbPaging(:allPage="allPage" :currentPage="currentPage" :background="true" :currentChange="toPage")
  br
  CbPaging(:total="total" :pageSize="pageSize" :currentPage="currentPage" :currentChange="toPage" :sizeChange="sizeChange")
</template>
<script>
export default {
  data () {
    return {
      allPage: 12,
      total: 184,
      currentPage: 5,
      pageSize: 10
    }
  },
  methods: {
    toPage (pageNo) {
      console.log('page', pageNo)
      this.currentPage = pageNo
    },
    sizeChange (size) {
      console.log('size', size)
      this.size = size
    }
  }
}
</script>