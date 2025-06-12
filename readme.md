# 小狼毫（单字）郑码码表

## 安装

若无 GUI 介面，建 `default.custom.yaml`

```yaml
patch:
  schema_list:
    - schema: zhengma
#### German Layout for Windows: ####
# key_binder:
#   bindings:
#     - { when: always, accept: y, send: z }
#     - { when: always, accept: z, send: y }
#     - { when: always, accept: backslash, send: '#' }
```

- 复制 `*.yaml` 文件到
  - `Windows`: `%APPDATA%\Rime`
  - `Linux` / `BSD`
  - `ibus`: `~/.config/ibus/rime`
  - `fcitx4`: `~/.config/fcitx/rime`
  - `fcitx5`: `~/.local/share/fcitx5/rime/`
- 取消控制台默认开启字母模式 (Windows) ：
  更改 `安装目录\data\weasel.yaml`　为

  ```yaml
  app_options:
    cmd.exe:
      ascii_mode: false
    conhost.exe:
      ascii_mode: false
  ```

## 备注

- `pinyin_simp.*.yaml` 作为反查(#键)拼音码表
- 德语键盘注删表[文件](replace-zh-kbd-by-de.reg)（更好方案为将所有中文输入法改为德语，而不仅限于该输入法）
