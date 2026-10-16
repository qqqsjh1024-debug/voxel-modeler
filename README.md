# 图片转体素模型

> **3D立体像素风格，把喜欢的东西随手拍下来，建模成3D立体图形，实现赛博永生。**

一个让 Codex 根据你上传的照片，制作体素 3D 模型的技能。

上传一张食物、玩具、相机、宠物或其他物件的照片，调用 `$voxel-modeler`，即可将主要物体建成由小方块组成的可旋转模型，并生成便于预览和导入的文件。

## 生成内容

- 参数化体素模型源码，方便继续修改形状和配色。
- 独立的浏览器预览页，支持旋转及触屏操作。
- JSON 体素坐标、颜色与材质分区。
- 自包含 GLB 三维网格，可导入 Blender 等 3D 软件。

模型的主体轮廓、关键部件与主色彩会以参考照片为准。对于被固定游戏色板限制的 JSON 颜色，技能会说明与照片原色的差异。

## 安装

把本仓库克隆到 Codex 的个人技能目录：

```powershell
$skillsDir = Join-Path $env:USERPROFILE '.codex\skills'
New-Item -ItemType Directory -Path $skillsDir -Force | Out-Null
git clone https://github.com/qqqsjh1024-debug/voxel-modeler.git (Join-Path $skillsDir 'voxel-modeler')
```

也可以只在一个项目中使用：把仓库内容放入该项目的 `.agents/skills/voxel-modeler/`。

重启或刷新 Codex 后，该技能会自动匹配图片建模请求，也可以在消息中显式调用：

```text
$voxel-modeler 按这张参考图生成 3D 体素模型
```

## 许可证

本项目使用 MIT License。详见 [LICENSE](LICENSE)。
