# 小狼毫郑码码表

## 改动

-   使用我自己维护的郑码单字码表
-   德语键盘注删表文件（更好方案为将所有中文输入法改为德语，而不仅限于该输入法） 

## 备注
-   安装：复制 `*.yaml` 文件到 `%APPDATA%\Rime`
-   `pinyin_simp.*.yaml` 作为反查(#键)拼音码表
-   取消控制台默认开启字母模式：
    更改 `安装目录\data\weasel.yaml`　为
```yaml
app_options:
  cmd.exe:
    ascii_mode: false
  conhost.exe:
    ascii_mode: false
```
-   Fix Windows IME list: https://github.com/rime/weasel/issues/479
