<template>
  <div>
    <h3>slot으로 템플릿 조각 전달하기</h3>
    <small>props 외에도 부모에서 자식으로 컨텐츠 전달이 가능</small>
    <p><slot>대체: slot에 컨텐츠를 못 받았어요! 😮</slot></p>
  </div>
</template>

<style scoped>
p {
  width: full;
  text-align: center;
  border: 1px solid gray;
  padding-top: 2rem;
  padding-bottom: 2rem;
}
</style>
