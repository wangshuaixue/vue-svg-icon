<template>
    <div class="hello">
        <div
            class="icon icon-more"
            v-for="(name, index) in iconList"
            :key="index">
            <svg-icon
                :icon-class="name"
                :class-name="`svg-icon-${name}`"
            ></svg-icon>
            <p>{{`icon-${name}`}}</p>
        </div>
    </div>
</template>

<script>
import SvgIcon from '../components/svg-icon/index';
export default {
    name: 'HelloWorld',
    data() {
        return {
            iconList: ['step-not-finish']
        }
    },
    components: {
        SvgIcon,
    },
}
</script>

<style media="screen">
.svg-icon-more {
    height: 40px;
    width: 40px;
}
</style>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.icon-wrap {
    padding: 10px 30px;
    display: flex;
}
.icon {
    flex: 1;
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    padding: 10px;
}

.svg-icon-more {
    color: #2c3e50;
}
</style>
