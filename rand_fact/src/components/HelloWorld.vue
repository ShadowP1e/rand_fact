<template>
<div class="container">
 <p>{{value.fact}}</p>
</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: ['value']
}
</script>

<style>
  .container{
        width: 400px;
        margin: auto;
        border: 1px solid rgb(27, 70, 38);
        border-radius: 5px;
        padding: 20px;
        background: #12ac4d;
        color: #fff;
    }
</style>
