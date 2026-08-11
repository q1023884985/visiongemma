# VisionGemma - 本地图片识别 + AI 桌宠

在完全本地的 Windows 电脑上运行的开箱即用图片识别工具 + 趣味 AI 桌宠。基于 Google Gemma 3 4B 模型，**图片识别全程在本机完成，不上传任何数据**。

## 功能特性

- **本地图片识别**：基于 Gemma 3 4B，图片分析、OCR 文字提取、图表解读、场景描述全部在本机完成
- **Vulkan 加速**：支持 NVIDIA / AMD / Intel 显卡硬件加速；无独显时自动回退 CPU 运行
- **趣味 AI 桌宠**：托盘启动可爱桌宠，可对话、可识别屏幕/图片，互动陪伴
- **MCP 服务器模式**：可作为 MCP 服务器接入任意 AI 工具（ision_analyze 工具），让 AI 获得看图能力
- **隐私安全**：所有识别完全离线本地完成，不上传任何数据到云端
- **单文件免安装**：一个 exe 即完整运行，内置 Vulkan 引擎与桌宠

## 系统要求

- Windows 10/11 x64
- 显卡支持 Vulkan（NVIDIA / AMD / Intel 均可，推荐硬件加速）
- 无独显时自动回退 CPU 运行
- 磁盘剩余空间 >= 5GB（模型约 3.2GB）

## 下载

### GitHub Release（推荐）

[前往 Releases 页面下载 v1.0.0](https://github.com/q1023884985/visiongemma/releases)

> 安装包：VisionGemma-Vulkan.zip
> SHA256：1d61d205ed2308a0e2b9257f5775e7b1a2f75b45a126ca4af797ae5b2eb641c

### 夸克网盘镜像（国内用户加速）

[夸克网盘下载 VisionGemma-Vulkan.zip](https://pan.quark.cn/s/6148db284ee2)

## 快速开始

1. 解压压缩包，双击 VisionGemma-Vulkan.exe，首次运行自动打开配置向导
2. 向导引导从 ModelScope 下载模型（约 3.2GB，支持断点续传）
3. 下载完成后选择「开始 7 天试用」或「在线购买」

## 在线购买（永久授权，￥38）

1. 点击托盘「关于/激活状态」，打开「在线购买」窗口（￥38 永久使用）
2. 打开支付宝扫码支付 ¥38（支付页固定金额，请务必支付展示金额）
3. 支付成功后本机**自动检测并完成激活**，无需手动输入激活码

## 趣味桌宠

1. 右键托盘图标 →「趣味桌宠」，可快速启动桌宠，自动拉起本地识别引擎
2. 桌宠支持对话、选择主题等功能
3. 可通过托盘菜单设置开机自启

## 作为 MCP 服务器使用（接入 AI 工具）

在 AI 工具的 MCP 配置中加入：

\\json
{
  "mcpServers": {
    "vision-gemma": {
      "command": "VisionGemma-Vulkan.exe 完整路径",
      "args": ["--mcp"],
      "type": "stdio"
    }
  }
}
\
然后即可调用 ision_analyze 工具识别图片。

## 文件说明

- VisionGemma-Vulkan.exe 主程序（内置 Vulkan 引擎 + 桌宠，单文件免安装）
- 模型存放于 %LOCALAPPDATA%\VisionGemma\models

## 隐私说明

所有图片识别完全在本地完成，**不上传任何数据**。

## 售后支持

- QQ：1023884985
- 微信：13147295520
- 邮箱：1023884985@qq.com
