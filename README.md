# Smart Link Opener

一个智能的浏览器用户脚本（UserScript），可以自动判断并在新标签页中打开网页链接。无需配置，即装即用，支持所有主流浏览器。


## ✨ 主要特点

- 🧠 **智能识别**：自动识别页面主要内容区域的链接
- 🎯 **精准控制**：智能排除导航栏、工具栏等功能区域的链接
- 🌐 **全站适配**：支持所有网站，无需针对特定网站配置
- ⚙️ **灵活定制**：提供丰富的配置选项，可根据需求自定义
- 🚀 **性能优化**：使用事件委托，资源占用极小
- 🔒 **安全可靠**：开源代码，无隐私泄露风险

## 📦 安装方法

### 1. 安装脚本管理器

选择适合你的浏览器的脚本管理器：

| 浏览器 | 推荐的脚本管理器 |
|-------|----------------|
| Chrome | [Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo) |
| Firefox | [Violentmonkey](https://addons.mozilla.org/firefox/addon/violentmonkey/) |
| Safari | [Stay](https://apps.apple.com/cn/app/stay-网页纵览/id1591620171) |
| Edge | [Tampermonkey](https://microsoftedge.microsoft.com/addons/detail/tampermonkey/iikmkjmpaadaobahmlepeloendndfphd) |

### 2. 安装脚本

方法一：点击下面的链接直接安装：
- 待更新

方法二：手动安装
1. 打开脚本管理器的管理面板
2. 创建新脚本
3. 复制 [smart-link-opener.js](./smart-link-opener.user.js) 中的代码
4. 粘贴到编辑器中并保存

## 🎯 使用场景

- 浏览新闻、博客时，点击文章链接自动在新标签页打开
- 逛论坛时，点击帖子链接自动在新标签页打开
- 浏览商品列表时，点击商品链接自动在新标签页打开

## ⚙️ 自定义配置

脚本提供了丰富的配置选项，你可以根据需要自定义：

```javascript
const config = {
    // 排除的容器
    excludeContainers: [
        'nav', 'navigation', 'navbar', 'header', 'footer',
        'sidebar', 'menu', 'toolbar', 'timeline', 'pagination',
        'breadcrumb', 'dropdown', 'modal', 'dialog'
    ],
    
    // 排除的链接类型
    excludeLinkTypes: [
        'menu-item', 'nav-item', 'button', 'tab', 'logo',
        'icon', 'avatar', 'profile', 'search', 'login',
        'signup', 'download'
    ],
    
    // 主要内容区域特征
    mainContentClasses: [
        'content', 'main', 'article', 'post', 'topic',
        'thread', 'list', 'body'
    ]
};
```

### 配置说明

1. **excludeContainers**：不需要新标签页打开的区域
   - 导航栏、页眉页脚
   - 侧边栏、菜单栏
   - 工具栏、时间轴等

2. **excludeLinkTypes**：不需要新标签页打开的链接类型
   - 功能按钮（登录、注册等）
   - 导航项（菜单项、标签等）
   - 用户相关（头像、个人资料等）

3. **mainContentClasses**：主要内容区域的特征类名
   - 文章内容区
   - 列表区域
   - 帖子内容等

## 📝 更新日志

### v2.0 (2024-02-17)
- ✨ 支持所有主流浏览器和脚本管理器
- 🎯 优化链接识别算法
- 🛠️ 增加更多自定义配置选项
- 🐞 修复已知问题

### v1.0 (2024-02-16)
- 🎉 首个版本发布

## 🤝 参与贡献

欢迎提交 Issue 和 Pull Request！


## 📄 开源协议

本项目基于 [MIT](./LICENSE) 协议开源。

## 🙏 鸣谢

感谢所有贡献者对本项目的支持！ 
