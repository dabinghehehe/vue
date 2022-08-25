<template>
    <!-- <div>
        <table border style="width:800px">
            <thead>
                <tr>
                    <th>名称</th>
                    <th>数量</th>
                    <th>单价</th>
                    <th>操作</th>
                </tr>
            </thead>
            <tbody>
                <tr :key="index" v-for="(item, index) in data">
                    <td align="center">{{ item.name }}</td>
                    <td align="center"><button @click="addAndSub(item, false)">-</button>{{ item.num }}<button
                            @click="addAndSub(item, true)">+</button></td>
                    <td align="center">{{ item.price * item.num }}</td>
                    <td align="center">
                        <button @click="del(index)">
                            删除
                        </button>
                    </td>
                </tr>
            </tbody>
            <tfoot>
                <td></td>
                <td></td>
                <td></td>
                <td align="center">总价:{{ $total }}</td>
            </tfoot>
        </table>
    </div> -->
    <div>
        <Hello></Hello>
    </div>



</template>

<script setup lang="ts">
// import { ar } from 'element-plus/es/locale';
import { shallowRef, triggerRef, customRef, reactive, toRef, computed, ref, watchEffect } from 'vue';
// // let message = ref<string>("小兵")
// // let message: Ref<string> = ref("小兵")
// // let message = shallowRef({
// //     name: "小兵"
// // })

// // const changeMsg = () => {
// //     message.value.name = "大兵"
// //     triggerRef(message)
// // }

// // function MyRef<T>(value: T) {
// //     return customRef((trank, trigger) => {
// //         return {
// //             get() {
// //                 trank()
// //                 return value
// //             },
// //             set(newValue: T) {
// //                 console.log("set")
// //                 value = newValue
// //                 trigger()
// //             }
// //         }
// //     })
// // }
// // let message = MyRef<string>("xiaobing")
// // const changeMsg = () => {
// //     message.value = "dabing"
// // }
// // let message = reactive<number[]>([])
// // let obj = reactive({
// //     name: "xiaobing"
// // })

// // setTimeout(() => {
// //     let arr = [1, 2, 3, 4];
// //     // message = arr;
// //     message.push(...arr)
// //     console.log(message)
// // },1000)

// // const obj = {
// //     foo: 1,
// //     bar: 1
// // }
// // const state = toRef(obj, 'bar')

// // const change = () => {
// //     state.value++

// //     console.log("--->原始对象",obj)
// //     console.log("--->引用对象",state)
// // }


// // let firstname = ref('')
// // let lastname = ref('')

// // const name = computed({
// //     get() {
// //         return firstname.value + lastname.value
// //     },
// //     set() {
// //         firstname.value + lastname.value
// //     }
// // })

// // type Shop = {
// //     name: string,
// //     num: number,
// //     price: number
// // }

// // let $total = ref(0)

// // const data = reactive<Shop[]>([
// //     {
// //         name: "小兵的裤子",
// //         num: 1,
// //         price: 120
// //     },
// //     {
// //         name: "小兵的鞋子",
// //         num: 1,
// //         price: 200
// //     },
// //     {
// //         name: "小兵的帽子",
// //         num: 1,
// //         price: 240
// //     }
// // ])

// // const addAndSub = (item: Shop, type: boolean): void => {
// //     if (item.num > 1 && !type) {
// //         item.num--
// //     }
// //     if (item.num < 99 && type) {
// //         item.num++
// //     }
// // }
// // const del = (index: number) => {
// //     data.splice(index, 2)
// // }

// // $total = computed<number>(() => {
// //     return data.reduce((prev, next) => {
// //         return prev + (next.num * next.price)
// //     }, 0)
// // })

// // ---------------------------------------------------------------------------------------------------------
// import { watch } from 'vue';

// let message = reactive({
//     nav: {
//         bar: {
//             name: "xiaobing"
//         }
//     }
// })


// watch(message, (newVal, oldVal) => {
//     console.log('new', newVal)
//     console.log('old', oldVal)
// })

// ---------------------------------------------------------------------------------------------------------
// ---------------------------------------------------------------------------------------------------------
// ---------------------------------------------------------------------------------------------------------

// import { WatchEffect } from 'vue';
// let message = ref<string>('飞机')

// let message2 = ref<string>('飞机杯')

// const stop = watchEffect((oninvalidate) => {
//     console.log('message======>', message.value)
//     console.log('message======>', message2.value)
//     oninvalidate(() => {
//         console.log('before')
//     })

// })
// const stopWatch = () => stop()

import Hello from './components/HelloWorld.vue';


</script>

<style>
</style>
