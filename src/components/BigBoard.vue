<template>
    <div class="big_board">
      <div class="board" v-for='item in data' :key="item.id">
        {{item.name}}
        <button class="button" >
        X
        </button>
    </div>
    </div>
</template>

<script>

export default {
    props: ['data'],
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
.board:hover{
    box-shadow: inset 10px 10px 10px 10px rgba(255, 255, 255, 0.9);;
}


.big_board {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
}
</style>