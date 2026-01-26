# MTeam FREE 种子提取器

自动识别 MTeam 页面上所有标记为 "FREE" 的种子，并通过 API 批量获取下载链接。

## 功能特点

- 🔍 自动识别页面上的 FREE 标记种子
- 🚀 并发处理，提高获取速度（默认5个并发）
- 📋 自动复制下载链接到剪贴板
- 📊 实时显示处理进度
- ⚙️ 支持自定义 API 配置

## 配置方法

1. 访问 MTeam 网站后，在页面右下角找到"获取FREE种子"按钮
2. **右键点击**按钮，打开设置面板
3. 填写配置信息：
   - **API Endpoint**: `https://api.m-team.cc/api/torrent/genDlToken`
   - **API Key (x-api-key)**: 输入你的 API Key
4. 点击"保存"

## 使用方法

1. 打开包含 FREE 种子的页面
2. 点击页面右下角的**"获取FREE种子"**按钮
3. 等待处理完成（按钮会显示进度，如：`处理中... 5/10`）
4. 完成后，下载链接已自动复制到剪贴板

## 按钮状态

- **获取FREE种子**: 初始状态
- **处理中... 5/10**: 正在处理
- **11/11 成功 已复制到剪贴板**: 处理完成
- **未找到**: 页面上没有 FREE 种子
- **请配置API**: 需要先配置 API

## 控制台命令

```javascript
getAllFreeTorrentIds()        // 获取所有 FREE 种子 ID
getMTeamConfig()              // 查看当前配置
showMTeamSettings()           // 显示设置面板
window.freeTorrentDownloadLinksArray  // 下载链接数组
```

## 常见问题

**Q: 找不到 FREE 种子？**  
A: 确保页面已完全加载，刷新后重试。

**Q: API 调用失败？**  
A: 检查 API Endpoint 和 API Key 是否正确，查看控制台错误信息。

**Q: 下载链接未复制？**  
A: 检查浏览器剪贴板权限，或从控制台复制：`window.freeTorrentDownloadLinksArray`
