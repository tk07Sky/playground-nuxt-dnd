<template>
  <Draggable :list="items" :group="{ name: 'g1' }" class="dragArea" tag="ul">
    <li v-for="el in items" :key="el.name">
      <p>{{ el.name }}</p>
      <NestedDraggable :items="el.tasks" />
    </li>
  </Draggable>
</template>

<script>
import Draggable from 'vuedraggable';
export default {
  name: 'NestedDraggable',
  components: {
    Draggable,
  },
  props: {
    items: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style lang="scss" scoped>
.dragArea {
  min-height: 50px;
  outline: 1px dashed;
  li {
    cursor: pointer;
  }
}
</style>
