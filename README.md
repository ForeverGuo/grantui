### vue3 + pinia + vk-uview-ui

### 项目架构

```js
.
├── .hbuilderx                // HBuilderX 启动配置
│   └── launch.json
├── App.vue                   // 启动页
├── README.md
├── common                    // 公用文件
│   ├── css                   // 公共样式
│   │   └── base.scss
│   └── utils                 // 公共方法
│       ├── index.js
│       └── version.js
├── components                // 自动注册组件（注意：目录和文件名称需一致）
│      └── upload
│       └── upload.vue
├── main.js                   // 配置入口
├── manifest.json
├── package-lock.json
├── package.json              // 包配置文件
├── pages                     // 主包
│   └── index
│       └── index.vue
├── pages.json                // 路由配置
├── server                    // 服务请求
│   ├── api
│   │   └── user.js
│   └── index.js
├── static                    // 静态文件
│   └── logo.png
├── uni_modules                  // gt-ui 组件库
│   └── gt-ui
├── uni.scss                  // gt-ui 配置
└── yarn.lock

```

### 引导
 
 1. npm install or yarn

 2. open the HbuilderX 工具

 3. 选择运行到小程序模拟器



