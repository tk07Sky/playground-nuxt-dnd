<template>
  <div>
    <NestedDraggable :items="list1" />
    <NestedDraggable :items="list2" />
  </div>
</template>

<script>
import NestedDraggable from '~/components/vuedraggable/NestedDraggable';
export default {
  components: {
    NestedDraggable,
  },
  data() {
    return {
      list1: [
        {
          name: 'item1 task 1',
          tasks: [
            {
              name: 'item1 task 2',
              tasks: [],
            },
          ],
        },
        {
          name: 'item1 task 3',
          tasks: [
            {
              name: 'item1 task 4',
              tasks: [],
            },
          ],
        },
        {
          name: 'item1 task 5',
          tasks: [],
        },
      ],
      list2: [
        {
          name: 'item2 task 1',
          tasks: [
            {
              name: 'item2 task 2',
              tasks: [],
            },
          ],
        },
        {
          name: 'item2 task 3',
          tasks: [
            {
              name: 'item2 task 4',
              tasks: [],
            },
          ],
        },
        {
          name: 'item2 task 5',
          tasks: [],
        },
      ],
    };
  },
};
</script>
