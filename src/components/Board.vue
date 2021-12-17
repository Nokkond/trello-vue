<template>
      <div class="board" v-for="item in itemsNew" :key="item.id">
        {{item.title}}
      </div>
      {{itemsNew}}
</template>

<script>

export default {
    props: ['data', 'id'],
    methods: {
        itemsNew(){
            return data.find((thing) => thing.id === id);
        }
    }
}
</script>

<style>
.board {
  min-width: 200px;
  min-height: 100px;
  border-color: white;
  border: 1px solid;
  border-radius: 10%;
  padding: 10px;
  margin: 10px;
  display: flex;
  flex-direction: row;
  align-content: center;
  justify-content: center;
  align-items: center;
}
</style>