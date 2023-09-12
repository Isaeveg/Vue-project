<template>
  <label class="checkbox">
    <input type="checkbox" class="checkbox__input" />
    <span class="checkbox__span">Remember me </span>
  </label>
</template>

<style scoped lang="scss">
.checkbox {
  display: flex;
  align-items: center;
  gap: 8px;
}
.checkbox__input {
  width: 16px;
  height: 16px;
  border-radius: 4px;
  border: 1px solid #d0d5dd;
}
.checkbox__input:hover {
  border: 5px solid #000;
  border-radius: 0;
}
.checkbox__span {
  color: #344054;
  font-family: Inter;
  font-size: 14px;
  font-weight: 500;
  line-height: 20px;
  user-select: none;
}
.label__a {
  color: #5429ff;
  font-family: Inter;
  font-size: 14px;
  font-weight: 500;
  line-height: 20px;
}
</style>
