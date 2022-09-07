<template>
  <div>
    <the-header></the-header>
    <button @click="show('active-goals')">Show Active</button>
    <button @click="show('manage-goals')">Show Manage</button>
    <!-- <badge-list></badge-list>
    <user-info
      :full-name="activeUser.name"
      :info-text="activeUser.description"
      :role="activeUser.role"
    ></user-info> -->
    <!-- <active-goals></active-goals>
    <manage-goals></manage-goals> -->
    <component :is='selectedComponent'></component>
  </div>
  
  <!-- <course-goals>
    <template #default="slotProps">
      <h2>{{slotProps.item}}</h2>
    </template>
  </course-goals> -->

</template>

<script>
  import TheHeader from './components/TheHeader.vue';
  // import BadgeList from './components/BadgeList.vue';
  // import UserInfo from './components/UserInfo.vue';
  // import CourseGoals from './components/CourseGoals.vue'; 
  import ActiveGoals from './components/ActiveGoals.vue'; 
  import ManageGoals from './components/ManageGoals.vue'; 
  
  export default {
  components:{
    'the-header':TheHeader,
    // BadgeList,
    // UserInfo,
    // CourseGoals,
    ActiveGoals,
    ManageGoals,

    
  },
  data() {
    return {
      selectedComponent:"active-goals",
      activeUser: {
        name: 'Maximilian Schwarzmüller',
        description: 'Site owner and admin',
        role: 'admin',
      },
    };
  },
  methods:{
    show(cmp){
    this.selectedComponent=cmp;
    // alert(cmp)
  }
  }
 
};
</script>

<style>
html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>