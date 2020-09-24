<template>
  <button
    class="button"
    :class="btnStyle"
    v-bind="$attrs"
    v-on="$listeners"><slot /></button>
</template>

<script>
export default {
  name: 'AppButton',
  props: {
    btnStyle: {
      type: String,
      default: ''
    }
  }
}
</script>


<style scoped>
.button {
  font: inherit;
  background-color: #FF761E;
  color: white;
  cursor: pointer;
  width: 50%;
  height: 50px;
  border: none;
  margin-left: 0;
  font-size: 18px;
  border-radius: 8px;
  margin: 10px 0;
}
@media (min-width: 768px) { 
.button {
  width: 20%;
  margin-right: 15%;
}
}
</style>
