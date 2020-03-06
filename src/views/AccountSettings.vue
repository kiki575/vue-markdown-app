<template>
  <div class="app-page account-page">
    <div class="page-form-container account-settings-form-container">
      <h1 class="page-form-title">
        用户设置
      </h1>
      <base-tabs
        v-model="currentTab"
        :options="options"
      />
      <profile-settings-form v-if="currentTab === 'profile'"/>
      <password-settings-form v-else-if="currentTab === 'password'"/>
    </div>
  </div>
</template>

<script>
import ProfileSettingsForm from '@/components/ProfileSettingsForm'
import PasswordSettingsForm from '@/components/PasswordSettingsForm'

export default {
  components: {
    ProfileSettingsForm,
    PasswordSettingsForm
  },

  data () {
    return {
      currentTab: 'profile',
      options: [
        { key: 'profile', title: '基本信息' },
        { key: 'password', title: '修改密码' }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.account-settings-form-container
  max-width: 500px
  margin: 0 auto
  background: #FFF

.base-tabs
  width: 100%
  padding: 15px 0 0
</style>
