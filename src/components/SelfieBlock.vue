<template>
  <div class="selfie">
    <div v-for="(item, index) in self" :key="index + item.id" class="selfie__block">
      <span class="selfie__block__title">{{item.desc}}</span>
      <img :src="'/ya-prak-test/static/' + item.url" class="selfie__block__img" :alt="item.desc">
    </div>
  </div>
</template>

<script>
export default ({
  data: () => ({
    self: [{ desc: 'Фото со школы', url: 'high_school_avatar.jpg', id: '1' }, { desc: 'Актуальный аватар', url: 'today-avatar.jpg', id: '2' }],
  }),
});
</script>

<style lang="scss" scoped>
.selfie {
    margin: 40px auto;
    display: flex;
    flex-direction: row;
    justify-content: center;
  &__block {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
      &:first-child {
          margin-right: 40px;
      }
    &__title {
      font-size: 16px;
    }
    &__img {
      width: 200px;
      height: 150px;
      object-fit: cover;
    }
  }
}
</style>
