<template>
    <div class="task">
        <div class="task__header">
            <div class="task__title">
                {{ taskList.title }}
            </div>
            <div class="task__options">
                <font-awesome-icon icon="fa-solid fa-ellipsis-vertical" />
            </div>
        </div>
        <div class="task__body">
            <input type="text">
            <div class="task__body__row" v-for="task in taskList.tasks" :key="task.id">
                <div class="task__body__row__left">
                 <div class="task__icon"></div>
                </div>
               <!-- <font-awesome-icon class="task__icon__cicle" icon="fa-solid fa-circle-notch" /> -->
               <!-- <font-awesome-icon class="task__icon__check" icon="fa-solid fa-check" /> -->
                <div class="task__body__row__title">
                    {{  task.title }}
                </div>
                <div class="task__body__row__right">

                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TaskComponent',
    props: {
        taskList: {
            type: Object,
            required: true
        }
    },
    data() {
        return {
            
        }
    }
}
</script>

<style scoped>
.task {
}
.task__header {
    display: flex;
    justify-content: space-between;
    /* margin-bottom: 30px; */
    padding: 15px;
}
.task__body {
}
.task__title {
    color: #999999;
    font-size: 17px;
    font-weight: 500;
}
.task__body__row {
    display: flex;
    align-items: center;
    padding-left: 15px;
    padding-right: 15px;
    padding-bottom: 5px;
    padding-top: 5px;
}
.task__body__row:hover {
        box-shadow: rgb(169 174 183 / 50%) 0px 1px 2px 1px;
}
.task__icon__cicle {
    margin-right: 10px;
}
.task__icon__cicle:hover {
    display: none;
}
.task__icon__check {
    display: none;
    margin-right: 10px;
}
 .task__icon__check .task__icon__cicle:hover {
    display: flex;
}
.task__icon {
    background-color:#fff;
    border:2px solid #ccc;    
    height:15px;
    border-radius:50%;
    -moz-border-radius:50%;
    -webkit-border-radius:50%;
    width:15px;
}
.task__icon:hover {
    display: inline-block;
    border: none;
    border-radius:0px;
    -moz-border-radius:0px;
    -webkit-border-radius:0px;
      transform: rotate(45deg);
      height: 12px;
      width: 6px;
      margin-left: 25%; 
      border-bottom: 2px solid #4285F4;
      border-right: 2px solid #4285F4;
      cursor: pointer;
}
.task__body__row__title {
    margin-left: 10px;
}
.task__body__row__left {
    min-width: 20px;
}
.task__body__row__right {
    min-width: 20px;
}
</style>>
