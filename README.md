# CodexPet

可安装到 Codex 的自定义宠物集合。每个宠物都放在 `pets/<pet-id>/` 独立目录中，方便继续加入更多宠物。

## 安装

给其他人使用时，只需要复制某个宠物目录中的两个文件：

```text
pets/niulai/
├── pet.json
└── spritesheet.webp
```

复制到本机的 Codex 宠物目录：

```bash
CODEX_PETS_DIR="${CODEX_HOME:-$HOME/.codex}/pets"
mkdir -p "$CODEX_PETS_DIR"
cp -R pets/niulai "$CODEX_PETS_DIR/niulai"
```

如果设置了 `CODEX_HOME`，上面的路径会随之变化。`pet.json` 与 `spritesheet.webp` 必须保持在同一个宠物目录中；安装后重启或重新加载 Codex 即可让应用重新读取宠物文件。

## 当前宠物

### 牛来（`niulai`）

圆滚滚的金色牛角小怪兽，带着半睁眼和紫粉色口鼻的毛绒 Codex 宠物。

当前版本沿用已经验证过的 Codex 8×9 图集格式：`1536×1872`，单格 `192×208`。这是可直接使用的旧版 v1 包，因此没有人为添加 `spriteVersionNumber: 2`；v2 图集需要另外生成 8×11、`1536×2288` 的完整素材。

## 仓库结构

```text
.
├── pets/                  # 面向使用者的宠物包
│   └── niulai/             # 牛来；后续宠物继续按 id 建目录
├── hatch-pet/              # 可选的制作/验证工具与说明
└── output/                 # 本地生成与 QA 缓存，不提交到 Git
```

制作工具不是安装宠物的必需依赖；分发时只需复制目标宠物目录。

## 参考素材

- [三视图](https://holopix.cn/image/16037)
- [3D 模型参考](https://www.meshy.ai/zh-Hant/3d-models/Golden-Grumble-Goblin-01a01939-431a-7cab-80e4-27e9d884e44e)

仓库不重复提交这些外部参考文件。

## 许可

仓库根目录采用 MIT License；`hatch-pet/` 目录保留其自身的 Apache-2.0 许可文件。
