<script setup lang="ts">
import { onMounted, reactive } from 'vue'
const pageSrc = reactive({
    log: '页面创建了'
})
onMounted(() => {
    console.log(pageSrc.log);
})
</script>
<template>
    <div class="indexPage">
        <div>DANKEBIBI.cc</div>
    </div>
</template>
<style lang="scss">
body{
    margin: 0;
    padding: 0;
}
.indexPage{
    width: 100vw;
    height: 100vh;
    background-color:#2b2b2b;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    div{
        color: #3a3a3a;
        font-size: 8vw;
        position: relative;
        text-align: center;
        &::after{
            content: "DANKEBIBI.cc";
            color: transparent;
            position: absolute;
            left: 0;
            top: 0;
            background:linear-gradient(90deg,#23b9ff,#ffe11a,#f441a5,#0e24a3);
            background-clip: text;
            clip-path:circle(100px at 0% 50%);
            animation: light 5s infinite ease-in-out;
        }

    }
}
@keyframes light{
    0%{
        clip-path: circle(8vw at 0% 50%);
    }
    50%{
        clip-path: circle(20vw at 100%);
    }
    100%{
        clip-path: circle(8vw at 0% 50%);
    }
}
</style>