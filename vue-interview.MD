#### watch
深度监听引用类型无法拿到oldval，因为指针相同，此时已指向新的val  
```
watch: {
  info: {
    handler(oldVal, val) {
      console.log("watch info", oldVal, val)
    },
    deep: true, // 深度监听
  }
}
```

#### v-if v-show区别
dom结构显示隐藏，v-show是display：none;v-if是销毁dom；（在重复多次的显示隐藏是尽量使用v-show）