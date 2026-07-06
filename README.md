# 📋 月度考勤记录系统

一个专为手机端优化的移动版考勤记录 Web 应用，支持多人考勤登记、自动汇总统计、月度总结导出。

## ✨ 功能特性

| 功能 | 说明 |
|---|---|
| 👥 多人管理 | 支持杨建军、沈炜、郁启三位员工的考勤记录 |
| 📅 月份切换 | 自由切换查看/编辑不同月份的考勤数据 |
| 📆 日历视图 | 直观的月历网格，有记录的日子显示彩色圆点标识 |
| ➕ 快速登记 | 底部弹出面板，选择姓名+日期+考勤类型，一键添加 |
| 🗑️ 删除记录 | 每条记录支持单独删除，同一天可覆盖更新 |
| 📊 实时汇总 | 自动统计每人的出勤天数、迟到、早退、请假、缺勤 |
| 📋 月度总结 | 一键生成格式化的月度总结报告，支持复制到剪贴板 |
| 💾 本地存储 | 数据保存在浏览器 localStorage，关闭再打开数据不丢失 |
| 📱 移动适配 | 专为手机竖屏设计，触控友好，微信内可正常使用 |

## 🚀 快速部署（GitHub Pages）

### 1️⃣ Fork / 克隆本仓库

```bash
git clone https://github.com/你的用户名/attendance-system.git
cd attendance-system
```

### 2️⃣ 启用 GitHub Pages

1. 进入仓库 → **Settings** → 左侧 **Pages**
2. Source 选择 **Deploy from a branch**
3. Branch 选择 **main**，文件夹选 **/ (root)**
4. 点击 **Save**

### 3️⃣ 访问你的网站

等待约 1 分钟，即可通过以下链接访问：

```
https://你的用户名.github.io/attendance-system/
```

## 📁 项目结构

```
attendance-system/
├── index.html          # 主页面（移动端考勤系统）
├── README.md           # 项目说明文档
└── .github/
    └── workflows/
        └── deploy.yml  # GitHub Actions 自动部署配置（可选）
```

## 🔧 自定义配置

### 修改考勤人员

打开 `index.html`，找到第 15 行附近的 `PEOPLE` 数组：

```javascript
const PEOPLE = ['杨建军', '沈炜', '郁启'];
```

添加或修改为你的人员名单即可。

### 修改考勤类型

找到 `TYPE_CONFIG` 对象：

```javascript
const TYPE_CONFIG = {
    normal:   { label: '正常', color: '#07c160', bg: '#e8f8ef' },
    late:     { label: '迟到', color: '#faad14', bg: '#fffbe6' },
    early:    { label: '早退', color: '#ff8c00', bg: '#fff3e6' },
    leave:    { label: '请假', color: '#1890ff', bg: '#e6f7ff' },
    absent:   { label: '缺勤', color: '#ff4d4f', bg: '#fff1f0' },
};
```

可自由添加、修改类型和对应的颜色。

## 📱 使用说明

### 添加考勤记录
1. 选择目标月份（左上角可切换）
2. 点击底部「+ 添加考勤记录」
3. 选择姓名 → 选择日期 → 选择考勤类型
4. 点击「确认添加」

### 查看月度总结
1. 滚动到页面底部
2. 点击「📋 生成月度总结报告」
3. 报告自动生成并复制到剪贴板
4. 可粘贴到微信/邮件等任意地方

### 删除记录
- 在考勤明细表格中，点击记录右侧的 🗑️ 按钮即可删除

## ⚠️ 注意事项

- **数据存储**：数据保存在浏览器本地（localStorage），清除浏览器缓存会导致数据丢失
- **数据备份**：建议定期使用「月度总结」功能导出数据备份
- **多设备同步**：如需多设备同步数据，需要接入后端数据库（当前版本为纯前端实现）

## 🛠️ 技术栈

- **纯前端**：HTML5 + CSS3 + JavaScript（无框架依赖）
- **存储**：浏览器 localStorage
- **部署**：GitHub Pages / 任意静态网站托管服务

## 📄 License

MIT License — 自由使用、修改、分发

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！