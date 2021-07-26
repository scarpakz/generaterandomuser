<template>
  <button>{{ text }}</button>
</template>

<script>
export default {
    props: {
        text: String
    }
}
</script>

<style scoped>
button{
    background-color: rgb(0, 0, 0);
    border: none;
    cursor: pointer;
    color: #fff;
    padding: 15px 30px;
    font-size: 18px;
}
</style>