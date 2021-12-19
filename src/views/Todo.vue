<template>
  <div class="home">
    
    

    <list-tasks 
      v-if="$store.state.tasks.length"
    />
    
  <no-tasks v-else />
  <button-done-sorting 
    v-if="$store.state.sorting"/>
  </div>
</template>

<script>

import ListTasks from '@/components/Todo/ListTasks'
import NoTasks from '@/components/Todo/NoTasks'
import ButtonDoneSorting from '@/components/Todo/ButtonDoneSorting'
export default {
  name: 'Home',
   components: {
      ListTasks, NoTasks, ButtonDoneSorting
      
    }
  
}
</script>

<style lang="sass">
  .no-tasks
    position: absolute
    left: 50%
    top: 50%
    transform: translate(-50%, -50%)
    opacity: 0.5
</style>