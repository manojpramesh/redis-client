<template>
  <div>
    <div>
      <b-navbar toggleable="lg" :type="theme?'dark':'light'" :variant="theme?'dark':'light'">
        <b-navbar-brand href="#">Redis Lion</b-navbar-brand>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item-dropdown right>
            <!-- Using 'button-content' slot -->
            <template v-slot:button-content>
              <em>Settings</em>
            </template>
            
              <b-dropdown-item href="#">Sign Out</b-dropdown-item>
              Dark Theme:<b-form-checkbox v-model="theme" name="check-button" switch>
              </b-form-checkbox>
     
            
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-navbar>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      theme: false
    }
  }
}
</script>
