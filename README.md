# MacCreateNewFile
--version 1.0

[简体中文](./README.md) | [English](./README_en.md)

使用方法：
1. 双击 shortcut 文件将其导入进快捷指令
2. 将快捷指令“添加到程序坞”，并找到 .app 文件
3. 将 .app 文件按住 cmd 键拖动到访达顶部
4. 将非纯文本文件的空白模板添加到模板目录 (默认为 ~/.Template)，并命名成 "Blank.xxx"
5. 点击访达顶部的按键，然后输入所需的文件名和后缀名

说明：

0. 此快捷指令为纯 zsh 脚本，响应迅速
1. 如果没有输入文件名，默认将新建 "Untitled.txt" 文件。如果 "Untitled.txt" 已存在，将新建 "Untitled 2.txt", "Untitled 3.txt" ...
2. 如果需要修改模板文件夹的路径，修改 `TEMPLATE_DIR="${HOME}/.Template"` 项
3. 对于纯文本文件，将使用 touch 命令新建
4. 对于非纯文本文件（如 .docx, .nd 等)，需要提前添加到模板文件夹中，使用 cp 命令在指定路径下仿制一个全新的文件
5. 虽然使用 touch 命令生成的 .docx 也能正常打开，但仍然建议使用 cp 的方法
