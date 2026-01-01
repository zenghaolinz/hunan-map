湖南
这是一个基于 Web 的交互式地图应用，旨在展示湖南省（特别是娄底地区）的现代景点分布与历史行政区划变迁。项目使用原生 JavaScript 和 Leaflet.js 构建，无需复杂的后端依赖。
🚀 功能特性
1. 双模式视图
🚀 现代景点 (Modern Tour)：展示高校、风景名胜、文化遗址等 POI 数据。
📜 历史疆域 (Historical Territory)：通过时间轴展示从秦汉时期到现代的行政区划演变（特别是梅山地区、湘南县到现代娄底市的变迁）。
2. 交互式地图
支持 全省概览 与 城市详情 两种视角切换。
集成高德地图（电子地图 & 卫星影像）作为底图。
支持点击地图区域进入下级行政区（如点击“湖南”进入各市州，点击“娄底”可查看县级区划）。
3. 数据检索与过滤
分类筛选：支持按“全部”、“高校”、“特定区县”筛选景点。
关键词搜索：支持实时检索景点名称或描述。
详情弹窗：点击景点图标可查看图片、简介及导航链接。
📂 项目结构
Plaintext
hunan-map/
├── index.html              # 应用入口文件 (UI 结构)
├── style.css               # 样式表 (布局、动画、响应式适配)
├── editor.html             # (可选) 辅助编辑工具
├── images/                 # 景点图片资源文件夹
├── city/                   # GeoJSON 地理数据文件夹
│   ├── hunan.json          # 湖南省级地图数据
│   └── *.geojson           # 各市州地图数据
├── js/
│   ├── app.js              # 核心逻辑 (地图初始化、交互、渲染)
│   ├── data.js             # 景点数据 (spots 数组) & 历史时期配置
│   ├── geo-data.js         # 地理数据配置索引
│   └── history.js          # 历史地图渲染模块
└── README.md               # 项目说明文档
🛠️ 技术栈
HTML5 / CSS3: 响应式布局，适配移动端与桌面端。
JavaScript (ES6+): 原生 JS 实现逻辑，无编译步骤。
Leaflet.js: 开源交互式地图库。
GeoJSON: 存储地理边界数据。
📦 安装与运行
由于项目使用 ES Modules 和 Fetch API 加载本地 JSON 资源，直接双击 index.html 可能会因浏览器的 CORS 策略（跨域限制）导致数据加载失败。
推荐运行方式：
确保已安装 Node.js。
在项目根目录下安装简易 HTTP 服务器（例如 http-server）：
Bash
npm install -g http-server
启动服务：
Bash
http-server .
在浏览器中访问：http://localhost:8080
或者使用 VS Code 的 Live Server 插件右键 index.html -> "Open with Live Server"。
🗺️ 数据来源
地图底图: 高德地图 (AutoNavi)
边界数据: 阿里云 DataV GeoAtlas
景点数据: 手动采集与整理 (js/data.js)
📝 待办事项
[ ] 优化移动端侧边栏的交互体验。
[ ] 丰富更多历史时期的行政区划演变细节。

License: MIT
