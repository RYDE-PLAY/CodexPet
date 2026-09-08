# CodexPet

Codex 自定义宠物。当前宠物：**牛来**（`niulai`）。

## 安装

下载 `pets/niulai/`，保持下面两个文件在同一个目录中：

```text
niulai/
├── pet.json
└── spritesheet.webp
```

将它复制到 Codex 宠物目录：

```bash
CODEX_PETS_DIR="${CODEX_HOME:-$HOME/.codex}/pets"
mkdir -p "$CODEX_PETS_DIR"
cp -R pets/niulai "$CODEX_PETS_DIR/niulai"
```

复制完成后重启或重新加载 Codex。

使用宠物只需要 `pets/niulai/`；仓库中的其他文件是说明、许可或本地制作工具，不是运行牛来所必需的。

## 添加更多宠物

每个宠物放在 `pets/<pet-id>/` 下，并在目录中提供 `pet.json` 和 `spritesheet.webp`。

## 许可

MIT License
