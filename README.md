# blog_summary_of_khaos
the summary of writing khaos ( a website)

### khaos:
前端: tauri ( vite + react )  
后端: go ( gin )

---

### 前端
1. react 第三方组件库
2. `echarts-for-react` 不要用 yarn 下，有错(麻了别用这玩意一堆错），用 `react-chartjs-2`，这个好用。
3. `typescript` 在添加比较老的 `javascript` 包时可能会报缺失 `type` 的错，一般可通过 `yarn add @type/xxx` 解决
4. 字符串拼接可通过 ``` `${stringA}${stringB}` ``` 来解决
5. `antd` 表格的 `fliter`，需要使 `fliter` 的字段唯一。
6. `antd` 表格的 `fliter` 中的字段数据是 `ColumnFilterItem[]` 格式，就是一个树的数据结构（woc头一回见用这种复杂结构的东西）

### 后端
1. 使用 `vscode` 开发 `golang` 时要打开文件目录，不然依赖报错
2. `mysql` 查到空数据时返回空而不时报错（话说我为什么会觉得它要报错）
3. 关于`database/GetUsersList`  
最初直接返回返回了53个结构体数组，后来考虑返回指针但怕垂悬引用，最后在调用的时候传入指针用于返回    
由于返回的是一整个数组，所以定义了 `len` 来截取长度，截取方式是 `切片` ，由于取得是地址不浪费性能  
4. `mysql`中的表名不要叫 `order`，关键字重复 (我说sql怎么突然这么毒)
5. 数据库连接池可以指定由一个 `init` 函数实现，每个连接创建一个连接池会导致报错（连接过多）
6. `golang` 的单元测试项目启动地址不是项目根目录，读取配置文件的时候导致错误
