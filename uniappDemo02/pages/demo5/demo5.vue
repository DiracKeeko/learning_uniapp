<template>
  <view class="">
    <demo-child ref="child"></demo-child>
    <view>---------</view>
    <button @click="handleClick">父组件调用子组件方法</button>
		<navigator url="/pages/demo6/demo6?name=Mikey">点击跳转demo6</navigator>
  </view>
</template>

<script setup>
import { onMounted, ref } from "vue";
const child = ref(null);

console.log("child->", child.value);

onMounted(() => {
  console.log("child->", child.value);
});

function handleClick() {
  child.value.updateCount();
}

</script>

<style lang="scss" scoped></style>
