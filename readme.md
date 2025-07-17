# 小狼毫（单字）郑码码表

## 安装

若无 GUI 介面，建 `default.custom.yaml`

```yaml
patch:
  schema_list:
    - schema: zhengma
  app_options:
    cmd.exe:
      ascii_mode: false
    conhost.exe:
      ascii_mode: false
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
- Add to other languages, en-US:409 en-UK:809 en-CA:1009 de-DE:407
  ```
  set LANGID=0x00000409
  set BASEKEY=HKLM\SOFTWARE\Microsoft\CTF\TIP\{A3F4CDED-B1E9-41EE-9CA6-7B4D0DE6CB0A}\LanguageProfile\%LANGID%
  set SUBKEY=%BASEKEY%\{3D02CAB6-2B8E-4781-BA20-1C9267529467}
  reg add "%BASEKEY%" /f
  rem Add values to the subkey
  reg add "%SUBKEY%" /v Description /t REG_SZ /d "Weasel" /f
  reg add "%SUBKEY%" /v IconFile /t REG_SZ /d "C:\\WINDOWS\\system32\\weasel.dll" /f
  reg add "%SUBKEY%" /v IconIndex /t REG_DWORD /d 0 /f
  reg add "%SUBKEY%" /v Enable /t REG_DWORD /d 1 /f
  ```
