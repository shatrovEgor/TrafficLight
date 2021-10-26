<template>
    <div class="stopwatch"><p>{{currentTime -1}}</p>
    </div>
</template>

<script>
export default {
  name: 'stopwatch',
  props: ['currentTime'],
  mounted () {
    setInterval(() => {
      this.currentTime--
    }, 1000)
  }
}
</script>

<style>
  .stopwatch {
    width: 90px;
    height: 45px;
    background: rgb(211, 173, 3);
    border: 2px solid #000;
    border-radius: 3px;
    margin-left: auto;
    margin-right: auto;
    overflow: hidden;
    text-align: center;
    vertical-align: middle
  }
  .stopwatch p {
    font-size: 28px;
    margin: 7px;
  }
</style>
