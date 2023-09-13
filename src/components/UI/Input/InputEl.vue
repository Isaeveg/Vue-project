<template>
    <label class="forms">
        <span class="forms__title">{{ title }}</span>
        <div class="forms__input-wrapper">
            <input :type="inputType" :name="name" :value="value" @input="handleInputChange" :placeholder="placeholder"
                class="forms__input" :autocomplete="autocomplete" />
            <div class="forms__input-svg">
                <span v-if="type != 'password'" @click="handleClearClick">
                    <CrossIcon />
                </span>
                <span v-if="type == 'password'" @click="handleTogglePassword">
                    <template v-if="showPassword">
                        <HideIcon />
                    </template>
                    <template v-else>
                        <HideDef />
                    </template>
                </span>
            </div>
        </div>
    </label>
</template>
  
<script>
import {ref, computed}  from 'vue';
import  CrossIcon  from "./../../icons/CrossIcon";
import HideIcon  from "./../../icons/HideIcon.vue";
import HideDef  from "./../../icons/HideDef.vue";

export default {
    props: {
        title: String,
        type: String,
        name: String,
        placeholder: String
    },
    components: {
        CrossIcon,
        HideIcon,
        HideDef
    },
    setup(props) {
        const value = ref("");
        const showPassword = ref(false);

        const handleInputChange = (e) => {
            value.value = e.target.value;
        };

        const handleClearClick = () => {
            console.log("delete email");
            value.value = "";
        };

        const handleTogglePassword = () => {
            showPassword.value = !showPassword.value;
        };

        const inputType = computed(() => showPassword.value ? "text" : props.type);

        return {
            value,
            showPassword,
            handleInputChange,
            handleClearClick,
            handleTogglePassword,
            inputType,
            autocomplete: "off"
        };
    }
};
</script>
  
<style scoped lang="scss">
.forms {
    &:not(:last-child) {
        margin-bottom: 20px;
    }

    display: block;

    &__title {
        color: #344054;
        font-family: Inter;
        font-size: 14px;
        font-weight: 500;
        line-height: 20px;
    }

    &__input-wrapper {
        position: relative;
    }

    &__input-svg {
        position: absolute;
        right: 14px;
        top: 50%;
        transform: translateY(-50%);
        cursor: pointer;

        span {
            display: flex;
        }
    }

    &__input {
        margin-top: 8px;
        height: 44px;
        width: 100%;
        display: block;
        border-radius: 8px;
        border: 1px solid #d0d5dd;
        padding: 10px 40px 10px 14px;
        background: transparent;
    }
}
</style>