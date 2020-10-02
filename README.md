# tasking
1. 创建数据
2. 插入的页面的功能，需要保存起来（watcher）
3. 把数据定义为响应式的（defineReactive）
    1. 把每一个属性都通过defineProperty定义
4. 发布事件

    2. 设置一个active全局变量，事件执行之前将watcher存入active
    3. 每个属性中都需要设置一个收集器dep
    4. 获取数据时通过判断active收集active中存放的watcher事件
    5. 如果触发数据更新set，就将对应属性中dep中的watchers依次触发
    6. 首次执行完成事件后，将active清除，方便下一次收集事件

# to be continued