<template>
  <div class="container">
    <nuxt-link to="/vuedraggable">back</nuxt-link>
    <Draggable v-model="list1" class="dragArea">
      <div v-for="element in list1" :key="element.id" class="list-group-item">
        {{ element.name }}
      </div>
    </Draggable>
  </div>
</template>

<script>
import Draggable from 'vuedraggable';
export default {
  components: {
    Draggable,
  },
  data() {
    return {
      list1: [
        { name: 'dog 1', id: 1 },
        { name: 'dog 2', id: 2 },
        { name: 'dog 3', id: 3 },
        { name: 'dog 4', id: 4 },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.dragArea {
  display: flex;
  width: 400px;
  flex-direction: column;
}
.list-group-item {
  border: solid 1px gray;
}
</style>
