# TTFHW-OmniOperator

本项目用于通过 GitHub Actions 自动化构建 [OmniOperator](https://gitcode.com/openeuler/OmniOperator.git) 的容器镜像。

## 项目概述

OmniOperator 是 openEuler 社区的项目，本项目提供自动化构建流水线，支持：

- **多平台构建**：支持 `linux/amd64` 和 `linux/arm64` 架构
- **原生 ARM 构建**：使用 ARM Runner 无需 QEMU 模拟，构建速度更快
- **安全扫描**：集成 Trivy 进行镜像安全扫描
- **SBOM 生成**：自动生成软件物料清单

## 触发方式

- **定时触发**：每天 UTC 2:00 (北京时间 10:00) 自动构建
- **手动触发**：通过 GitHub Actions 界面手动执行
- **配置变更触发**：当 `config/` 目录下的配置文件变更时自动触发

## 配置说明

镜像构建配置位于 `config/` 目录，采用 YAML 格式。参考 `config/example-images.yml` 了解配置结构。

## 相关链接

- 源码仓库：[https://gitcode.com/openeuler/OmniOperator](https://gitcode.com/openeuler/OmniOperator)
- 镜像仓库：`ghcr.io/computing-ttfhw/`

## License

本项目遵循相关开源协议。