<script>
export default {
  data() {
    return {
        isRulesVisible: false
    }
  }
}
</script>

<template>

    <button class="rules-btn btn btn-inline" @click="isRulesVisible = true">Rules</button>
    
    <div class="overlay" v-show="isRulesVisible">
        <div class="box">
            <div class="box__header">
                <h3>Rules</h3>
                <button type="button" @click="isRulesVisible = false">
                    <img src="../assets/icon-close.svg" alt="Close">
                </button>
            </div>
            <img src="../assets/image-rules.svg" class="rules-img" alt="Game rules explanation">
        </div>
    </div>


</template>

<style lang="scss" scoped>
@import '../main.scss';

.rules-btn {
    position: fixed;
    bottom: 55px;
    right: 120px;

    @media only screen and (max-width: 550px) {
        right: 50%;
        transform: translateX(50%);
    }
}

.overlay {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    display: grid;
    place-items: center;
    background-color: rgba(0,0,0,0.6);
    z-index: 100;
}
.box {
    background: $color-neutral-100;
    border-radius: 10px;
    padding: 30px;

    @media only screen and (max-width: 550px) {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        border-radius: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        font-size: 2rem;
        font-weight: 700;
    }

    &__header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        color: $color-neutral-300;

        button {
            display: flex;

            @media only screen and (max-width: 550px) {
                position: fixed;
                bottom: 70px;
                left: 50%;
                transform: translateX(-50%);
            }
        }
    }

    .rules-img {
        margin-top: 30px;
    }
}

</style>
