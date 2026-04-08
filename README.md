# 全球银行卡代付及换汇系统

一个基于纯HTML/CSS/JavaScript实现的全功能高保真原型系统，支持代付全球银行卡和多币种换汇服务。。。

## 🌟 项目特色

- ✨ **深色玻璃态设计** - 采用现代化的Glassmorphism设计风格
- 💰 **多币种支持** - 支持USD、EUR、CNY三种货币
- 🔄 **完全可交互** - 包含完整的表单验证、数据流转和页面路由
- 💾 **本地数据存储** - 使用LocalStorage，刷新页面数据保持
- 📱 **响应式设计** - 优先保证1920x1080分辨率，兼容移动端
- 🎯 **无框架依赖** - 纯原生JavaScript实现，轻量高效

## 📦 核心功能

### 1. 账户总览
- 展示USD、EUR、CNY三个账户的余额信息
- 显示虚拟银行卡
- 展示最近交易记录
- 快捷操作入口

### 2. 代付功能
- 选择收款人进行代付
- 支持多币种代付
- 实时汇率显示
- 表单验证和错误提示
- 交易记录保存

### 3. 收款人管理
- 添加、编辑、删除收款人
- 支持批量删除
- 收款人信息完整录入（银行账号、SWIFT代码等）
- 搜索和筛选功能

### 4. 换汇功能
- USD、EUR、CNY之间的货币兑换
- 实时汇率计算
- 一键交换货币方向
- 即时到账

### 5. 交易记录
- 完整的交易历史记录
- 多维度筛选（类型、币种、日期、状态）
- 交易详情查看
- 数据导出（CSV格式）

## 🚀 快速开始

### 安装和运行

1. **克隆或下载项目**
   ```bash
   # 项目已经位于
   D:\product\Payment on behalf\
   ```

2. **启动本地服务器**

   由于浏览器的安全限制，需要使用本地服务器运行项目。

   **方式一：使用Python（推荐）**
   ```bash
   # 进入项目目录
   cd "D:\product\Payment on behalf"

   # Python 3.x
   python -m http.server 8000

   # Python 2.x
   python -m SimpleHTTPServer 8000
   ```

   **方式二：使用Node.js**
   ```bash
   # 安装http-server（首次需要）
   npm install -g http-server

   # 进入项目目录并启动
   cd "D:\product\Payment on behalf"
   http-server -p 8000
   ```

   **方式三：使用VS Code**
   - 安装"Live Server"扩展
   - 右键点击index.html
   - 选择"Open with Live Server"

3. **访问应用**

   在浏览器中打开：`http://localhost:8000`

### 系统要求

- **浏览器**：Chrome 90+、Edge 90+、Firefox 88+、Safari 14+
- **分辨率**：建议1920x1080或更高
- **浏览器特性**：需要支持`backdrop-filter`（玻璃态效果）

## 📁 项目结构

```
Payment on behalf/
├── index.html                    # 入口页面
├── pages/                        # 页面文件
│   ├── dashboard.html            # 账户总览页
│   ├── payment.html              # 代付页面
│   ├── exchange.html             # 换汇页面
│   ├── beneficiaries.html        # 收款人管理页
│   └── transactions.html         # 交易记录页
├── css/                          # 样式文件
│   ├── common.css                # 通用样式
│   ├── dashboard.css             # 账户总览样式
│   ├── payment.css               # 代付页面样式
│   ├── exchange.css              # 换汇页面样式
│   ├── beneficiaries.css         # 收款人管理样式
│   └── transactions.css          # 交易记录样式
├── js/                           # JavaScript文件
│   ├── app.js                    # 应用初始化
│   ├── router.js                 # 路由管理
│   ├── data.js                   # 数据管理
│   ├── utils.js                  # 工具函数
│   ├── components.js             # 通用组件
│   ├── dashboard.js              # 账户总览逻辑
│   ├── payment.js                # 代付页面逻辑
│   ├── exchange.js               # 换汇页面逻辑
│   ├── beneficiaries.js          # 收款人管理逻辑
│   └── transactions.js           # 交易记录逻辑
├── assets/                       # 资源文件
│   └── icons/                    # 图标文件
├── image/                        # 参考设计图
│   ├── 现有系统风格.png
│   ├── 代付页面参考图.png
│   └── 新增收款人参考页.png
└── README.md                     # 项目文档
```

## 💡 使用说明

### 初始数据

系统初次运行时会自动初始化以下数据：

- **账户余额**：
  - USD: $100,000.00
  - EUR: €50,000.00
  - CNY: ¥200,000.00

- **收款人**：2个示例收款人
- **交易记录**：2条示例交易
- **汇率**：固定汇率数据

### 核心操作流程

#### 代付流程
1. 进入"代付"页面
2. 输入汇出金额
3. 选择收款人（如无收款人，先添加）
4. 填写备注（可选）
5. 点击"提现继续"
6. 确认信息后提交

#### 换汇流程
1. 进入"换汇"页面
2. 选择源货币和目标货币
3. 输入兑换金额
4. 查看实时汇率和到账金额
5. 点击"立即兑换"
6. 确认后完成兑换

#### 收款人管理
1. 进入"收款人管理"页面
2. 点击"新增收款人"
3. 填写收款人信息：
   - 选择币种
   - 填写银行账户信息
   - 填写收款人地址
4. 保存收款人
5. 可随时编辑或删除

### 数据重置

如需重置所有数据，在浏览器控制台执行：
```javascript
resetAllData()
```

## 🎨 设计风格

### 颜色系统
- **主色调**：青蓝色 (#00D9FF)
- **次要色**：粉紫色 (#E91E63)
- **背景色**：深紫蓝渐变
- **文字色**：白色/浅灰色

### 玻璃态效果
- 半透明背景
- 毛玻璃模糊效果
- 渐变色卡片
- 柔和阴影

## 🔧 技术栈

- **前端**：HTML5、CSS3、JavaScript (ES6+)
- **数据存储**：LocalStorage
- **样式特性**：CSS Variables、Flexbox、Grid、Backdrop Filter
- **路由**：Hash-based SPA路由
- **图标**：Font Awesome 6.x

## 📝 注意事项

1. **数据存储**：所有数据存储在浏览器LocalStorage中，清除浏览器数据会丢失所有记录
2. **汇率数据**：使用固定汇率，可在`js/data.js`中修改
3. **浏览器兼容**：玻璃态效果需要浏览器支持`backdrop-filter`属性
4. **模拟延迟**：所有操作都有500ms模拟API延迟，提供真实感
5. **无后端**：纯前端实现，无需后端服务器

## 🐛 常见问题

### 页面无法加载？
- 确保使用本地服务器运行（不能直接双击HTML文件）
- 检查浏览器控制台是否有错误信息

### 玻璃态效果不显示？
- 检查浏览器是否支持`backdrop-filter`属性
- 更新浏览器到最新版本

### 数据丢失了？
- LocalStorage数据可能被清除
- 执行`initData()`或`resetAllData()`重新初始化

## 📄 许可证

本项目仅供学习和演示使用。

## 👨‍💻 开发者

开发完成日期：2026年1月

---

**提示**：这是一个高保真原型系统，所有功能均为模拟实现。在生产环境中使用需要连接真实的后端API服务。
