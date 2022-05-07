<template>
  <div class="board">
    <div class="board__list"  v-for="item in taskList" :key="item.id">
      <task-component :task-list="item" />
    </div>
  </div>
</template>

<script>
import TaskComponent from './TaskComponent.vue'

export default {
  name: 'BoardComponent',
  components: {
    TaskComponent
  },
  props: {
    
  },
  data() {
    return {
      taskList: [
        {
          id: 1,
          title: 'TaskList 1',
          tasks: [
            {
              id: 101,
              title: 'Task 1',
            },
            {
              id: 102,
              title: 'Task 2',
            },
            {
              id: 103,
              title: 'Task 3',
            },
          ]
        },
        {
          id: 2,
          title: 'TaskList 2',
          tasks: [
            {
              id: 201,
              title: 'Task 4',
            },
            {
              id: 202,
              title: 'Task 5',
            },
          ]
        },
        {
          id: 3,
          title: 'TaskList 3',
        }]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.board {
  display: flex;
  justify-content: flex-start;
  margin-top: 30px;
  margin-left: 20px;
}

.board__list {
  width: 300px;
  max-width: 800px;
  height: 100%;
  border-radius: 5px;
  margin-right: 20px;
  background: rgb(255, 255, 255);
  box-shadow: rgb(169 174 183 / 50%) 0px 1px 2px 0px;
  border-radius: 8px;
  margin: 10px;
  overflow: hidden;
  cursor: default !important;
}
</style>
