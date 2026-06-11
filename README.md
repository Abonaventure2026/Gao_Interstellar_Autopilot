# Gao_Interstellar_Autopilot

[![License](https://img.shields.io/badge/License-Commercial%20Proprietary-red.svg)](LICENSE)
[![C++](https://img.shields.io/badge/C%2B%2B-20-blue.svg)](https://isocpp.org/)
[![Version](https://img.shields.io/badge/version-5.0.0-brightgreen.svg)](.version)

Gao_Interstellar_Autopilot 是 4A 系统的星际空间分支，专为轨道飞行器、行星巡视器、深空探测器等航天器设计。

## 支持构型
- I-1 轨道飞行：二体轨道递推 + J2 摄动 + PID 轨道控制
- I-2 行星表面移动：轮式滑移运动学（参考陆地分支 T-1），低重力适配
- I-3 星际巡航：质点动力学 + 速度跟踪控制

## 依赖
- Gao_4A_Autopilot（基座）

## 构建与运行
```bash
./build_all.sh
./build/gao_autopilot
```

## 切换构型
修改 `edge/config/morphology.yaml` 文件，例如：
```yaml
morphology: "I-2"   # I-1, I-2, I-3
```
## 目录结构
```text
edge/
├── morphologies/I-1/  # 轨道动力学与控制器
├── morphologies/I-2/  # 巡视器动力学与控制器
├── morphologies/I-3/  # 巡航动力学与控制器
├── shared/            # 轨道递推、深空导航、辐射容错
├── safety/            # 单粒子翻转、通信中断安全模式
└── hardware/          # 星敏感器、推进器驱动抽象
```

## 许可证
商业专有。

## 作者
Yongji Gao
Email: bonaventure@163.com
