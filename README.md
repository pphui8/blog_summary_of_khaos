# blog_summary_of_khaos
the summary of writing khaos ( a website)

### khaos:
前端: tauri ( vite + react )  
后端: go ( gin )

---

### 前端
1. react 第三方组件库
2. `echarts-for-react` 不要用 yarn 下，有错

### 后端
1. 使用 `vscode` 开发 `golang` 时要打开文件目录，不然依赖报错
2. `mysql` 查到空数据时返回空而不时报错（话说我为什么会觉得它要报错）
3. `database/GetUsersList` 最初直接返回返回了53个结构体数组，后来考虑返回指针但怕垂悬引用，最后在调用的时候传入指针用于返回
