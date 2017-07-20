<template>

</template>
<script>
// import stores from '@/stores'

export default {
  name: 'Home',
  // created () {
  //   this.refreshInfo()
  // },
  data () {
    return {
      profileMenu: false,
      actionMenu: false,
      notificationMenu: false,
      sidemenutoggle: false,
      menus: [ {
        name: 'Home',
        icon: 'fa fa-home',
        location: '/dashboard'
      } ],
      loggedInUser: null
    }
  },
  methods: {
    refreshInfo: function () {
      // stores.user.refreshInfo(true)
      //   .then((userInfo) => {
      //     this.loggedInUser = userInfo
        // })
    },
    toggleSidebar: function () {
      this.sidemenutoggle = !this.sidemenutoggle
    },
    toggleNotif: function () {
      this.collapseAllHeaderDropDowns()
      this.notificationMenu = true
    },
    toggleAction: function () {
      this.collapseAllHeaderDropDowns()
      this.actionMenu = true
    },
    toggleProfile: function () {
      this.collapseAllHeaderDropDowns()
      this.profileMenu = true
    },
    collapseAllHeaderDropDowns: function () {
      this.profileMenu = false
      this.actionMenu = false
      this.notificationMenu = false
    },
    logout: function () {
      console.warn('Logging out')
      // window.localStorage.clear()
      // this.$router.push({name: 'Login'})
    }
  }
}
</script>
