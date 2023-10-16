<script>
export default {
  data() {
    return {
        
    }
  }
}
</script>

<template>
    <div class="container">
        <div class="box">
            <div class="item paper">
                <div class="icon">
                    <img src="../assets/icon-paper.svg" alt="Paper icon">
                </div>
            </div>
            <div class="item scissors">
                <div class="icon">
                    <img src="../assets/icon-scissors.svg" alt="Paper icon">
                </div>
            </div>
            <div class="item rock">
                <div class="icon">
                    <img src="../assets/icon-rock.svg" alt="Paper icon">
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import '../main.scss';

.container {
    display: flex;
    justify-content: center;
    padding-top: 100px;

    .box {
        position: relative;
        width: 450px;
        height: 450px;
        background-image: url('../assets/bg-triangle.svg');
        background-size: 80%;
        background-position: center;
        background-repeat: no-repeat;
    }

    .item {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 200px;
        height: 200px;
        border-radius: 50%;
        cursor: pointer;

        
        &.paper {
            position: absolute;
            top: 0;
            left: 0;
            transform: translate(-12%, -15%);
            background: linear-gradient(to top, $gradient-accent-100);
            box-shadow: 0 8px #2946BD;
        }

        &.scissors {
            position: absolute;
            top: 0;
            right: 0;
            transform: translate(12%, -15%);
            background: linear-gradient(to top, $gradient-accent-200);
            box-shadow: 0 8px #C46B17;
        }

        &.rock {
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translate(-50%, -15%);
            background: linear-gradient(to top, $gradient-accent-300);
            box-shadow: 0 8px #991636;
        }
    }

    .icon {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 150px;
        height: 150px;
        border-radius: 50%;
        background: #DEDEE0;
        box-shadow: inset 0 7px #B9BCCF;

        img {
            width: 70px;
        }
    }
}

</style>
