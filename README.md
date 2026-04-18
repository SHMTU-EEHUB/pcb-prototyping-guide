# PCB Prototyping Guide

上海海事大学 EEHUB 社团 **DM350 制板机** 使用指南，覆盖从 PCB 设计准备、导出 Gerber、刀路计算、到上机加工与关机的完整流程。

## 在线阅读

**<https://shmtu-eehub.github.io/pcb-prototyping-guide/>**

## 内容

- **准备 PCB** — 无电镀工艺下的设计规则与布线建议
- **导出 Gerber** — KiCad / 立创 EDA / Altium Designer
- **开机与预热** — DM350 + 气泵启动、软件预热
- **刀路计算** — CircuitCam7 导入、D 码还原、生成刀路、保存 LMD
- **制板准备** — 新建项目、垫板与铜板定位、导入刀路（含拼板、移动位置等可选项）
- **正式制板** — 钻孔、试刀、铣正反面与边框
- **关机** — 按顺序关闭软件、机床、气泵

## 本地预览

需要 Rust 工具链（`cargo`）。首次安装：

```bash
cargo install mdbook         --version '^0.4'  --locked
cargo install mdbook-admonish --version '^1.20' --locked
cargo install mdbook-mermaid  --version '^0.14' --locked
```

然后在仓库根目录：

```bash
mdbook serve --open
```

浏览器会自动打开预览，保存 md 后会实时刷新。

## 部署

push 到 `main` 会触发 `.github/workflows/deploy.yml`,自动构建并发布到 GitHub Pages。

## 许可

[CC BY-NC-SA 4.0](./LICENSE) — 署名 - 非商业性使用 - 相同方式共享 4.0 国际
