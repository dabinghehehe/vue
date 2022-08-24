<template>
    <div>
        <div><button @click="change">改变</button></div>
        <div>{{state}}</div>
    </div>

</template>

<script setup lang="ts">
import { ar } from 'element-plus/es/locale';
import { shallowRef, triggerRef, customRef, reactive, toRef } from 'vue';
// let message = ref<string>("小兵")
// let message: Ref<string> = ref("小兵")
// let message = shallowRef({
//     name: "小兵"
// })

// const changeMsg = () => {
//     message.value.name = "大兵"
//     triggerRef(message)
// }

// function MyRef<T>(value: T) {
//     return customRef((trank, trigger) => {
//         return {
//             get() {
//                 trank()
//                 return value
//             },
//             set(newValue: T) {
//                 console.log("set")
//                 value = newValue
//                 trigger()
//             }
//         }
//     })
// }
// let message = MyRef<string>("xiaobing")
// const changeMsg = () => {
//     message.value = "dabing"
// }
// let message = reactive<number[]>([])
// let obj = reactive({
//     name: "xiaobing"
// })

// setTimeout(() => {
//     let arr = [1, 2, 3, 4];
//     // message = arr;
//     message.push(...arr)
//     console.log(message)
// },1000)

const obj = {
    foo: 1,
    bar: 1
}
const state = toRef(obj, 'bar')

const change = () => {
    state.value++

    console.log("--->原始对象",obj)
    console.log("--->引用对象",state)
}
</script>

<style>
</style>
