<template>
    <div>
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
                    <td align="center"><button>-</button>{{ item.num }}<button>+</button></td>
                    <td align="center">{{ item.price }}</td>
                    <td align="center">
                        <button>
                            删除
                        </button>
                    </td>
                </tr>
            </tbody>
            <tfoot>
                <td></td>
                <td></td>
                <td></td>
                <td align="center">总价:500</td>
            </tfoot>
        </table>
    </div>

</template>

<script setup lang="ts">
import { ar } from 'element-plus/es/locale';
import { shallowRef, triggerRef, customRef, reactive, toRef, computed, ref } from 'vue';
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

// const obj = {
//     foo: 1,
//     bar: 1
// }
// const state = toRef(obj, 'bar')

// const change = () => {
//     state.value++

//     console.log("--->原始对象",obj)
//     console.log("--->引用对象",state)
// }


// let firstname = ref('')
// let lastname = ref('')

// const name = computed({
//     get() {
//         return firstname.value + lastname.value
//     },
//     set() {
//         firstname.value + lastname.value
//     }
// })

type Shop = {
    name: string,
    num: number,
    price: number
}
const data = reactive<Shop[]>([
    {
        name: "小兵的裤子",
        num: 1,
        price: 120
    },
    {
        name: "小兵的鞋子",
        num: 1,
        price: 200
    },
    {
        name: "小兵的帽子",
        num: 1,
        price: 240
    }
])

</script>

<style>
</style>
