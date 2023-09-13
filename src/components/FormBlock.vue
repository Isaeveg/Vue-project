<template>
  <form class="form">
    <div class="form__title">NFT Access</div>
    <div class="form__desc">
      Please fill your detail to access your account.
    </div>

    <InputEl
      title="Email"
      type="email"
      name="Email"
      placeholder="bebra.holt@example.com"
    />

    <InputEl
      title="Password"
      type="password"
      name="password"
      placeholder="••••••••"
    />

    <div class="row">
      <CheckboxEl label="Remember me" />

      <a href="/" class="label__a"> Forgot Password? </a>
    </div>

    <div class="form__btn">
      <button class="btn _primary">Sign in</button>
      <button class="btn _secondary">
        <GoogleIcon />
        Sign in with Google
      </button>
    </div>
    <div class="ending">
      Don’t have an account?
      <a class="ending__a" href="/"> Sign up </a>
    </div>
  </form>
</template>

<script>
import GoogleIcon from "./icons/GoogleIcon";
import InputEl from "./UI/Input/InputEl";
import CheckboxEl from "./UI/Checkbox/CheckboxEl";

export default {
  components: {
    InputEl,
    CheckboxEl,
    GoogleIcon,
  },
};
</script>

<style lang="scss">
.form {
  padding-left: 140px;
  margin-top: 149px;
  align-items: center;
}
.form__title {
  color: #344054;
  font-family: Inter;
  font-size: 40px;
  font-weight: 700;
  letter-spacing: 0.4px;
  text-transform: capitalize;
  margin-bottom: 8px;
}

.email {
  &:not(:last-child) {
    margin-bottom: 20px;
  }
}

.form__desc {
  color: #667085;
  font-family: Inter;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
  margin-bottom: 56px;
}
.email__title {
  color: #344054;
  font-family: Inter;
  font-size: 14px;
  font-weight: 500;
  line-height: 20px;
  margin-bottom: 8px;
}
.email__input {
  color: #667085;
  font-family: Inter;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
  display: flex;
  padding: 10px 40px 10px 14px;
  justify-content: center;
  align-items: center;
  border-radius: 8px;
  border: 1px solid #d0d5dd;
  width: 360px;
  margin-bottom: 20px;
}
.pas__title {
  color: #344054;
  font-family: Inter;
  font-size: 14px;
  font-weight: 500;
  line-height: 20px;
  margin-bottom: 8px;
}
.pas__input {
  color: #667085;
  font-family: Inter;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
  display: flex;
  padding: 10px 14px;
  justify-content: center;
  align-items: center;
  border-radius: 8px;
  border: 1px solid var(--Accent-1, #d0d5dd);
  width: 360px;
  margin-bottom: 22px;
}

.row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 34px;
}
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

.form__btn {
  display: grid;
  gap: 20px;
}
._primary {
  display: inline-flex;
  padding: 12px 154px;
  justify-content: center;
  align-items: center;
  border-radius: 8px;
  background: #5429ff;
  color: #fff;
  font-family: Inter;
  font-size: 16px;
  font-weight: 500;
  line-height: 20px;
  border: transparent;
  cursor: pointer;
  border: 1px solid #5429ff;
  transition: 0.3s ease-in-out;

  &:hover {
    background-color: transparent;
    border: 1px solid #5429ff;
    color: #5429ff;
  }
}
._secondary {
  border-radius: 8px;
  border: 1px solid #d0d5dd;
  display: inline-flex;
  padding: 10px 90px;
  justify-content: center;
  align-items: center;
  gap: 8px;
  color: #344054;
  font-family: Inter;
  font-size: 16px;
  font-weight: 500;
  line-height: 20px;
  background-color: transparent;
  cursor: pointer;
  margin-bottom: 20px;
  transition: 0.3s ease-in-out;

  &:hover {
    box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.25),
      inset 0 -3px 0 rgba(0, 0, 0, 0.2);
  }
}
.ending {
  display: flex;
  color: #344054;
  text-align: center;
  font-family: Inter;
  font-size: 14px;
  font-weight: 400;
  line-height: 24px;
  gap: 5px;
  flex-shrink: 0;
  justify-content: center;
}
.ending__a {
  color: #5429ff;
  font-family: Inter;
  font-size: 14px;
  font-weight: 500;
  line-height: 20px;
}

.email__input-wrapper {
  position: relative;
}

.email__input-svg {
  position: absolute;
  right: 14px;
  top: 50%;
  transform: translateY(-50%);
  cursor: pointer;
}

.pas__span {
  display: flex;
}
</style>
