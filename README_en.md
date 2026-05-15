# Mac Create New File

--version 1.0

[English](./README_en.md) | [简体中文](./README.md) 

## How to Use

1. **Import:** Double-click the `.shortcut` file to import it into the Shortcuts app.
2. **Locate App:** Select "Add to Dock" within the shortcut settings, and locate the generated `.app` file.
3. **Add to Finder:** Hold down the **Cmd** key and drag the `.app` file onto the top toolbar of Finder.
4. **Set Up Templates:** Add blank templates for non-plain text files to your template directory (default is `~/.Template`) and name them `Blank.xxx`.
5. **Run:** Click the shortcut icon on the Finder toolbar, then input your desired file name and extension.

---

## Notes

0. This shortcut is powered entirely by a **zsh script**, ensuring a lightning-fast response time.
1. If no file name is provided, it defaults to creating `Untitled.txt`. If `Untitled.txt` already exists, it will sequentially create `Untitled 2.txt`, `Untitled 3.txt`, etc.
2. To change the path of your template folder, simply modify the line: `TEMPLATE_DIR="${HOME}/.Template"`.
3. For plain text files, the script utilizes the `touch` command for instant creation.
4. For non-plain text files (such as `.docx`, `.nd`, etc.), you need to add them to the template folder beforehand. The script will use the `cp` command to clone a fresh copy into your destination directory.
5. While `.docx` files generated using the `touch` command may open normally, using the template-based `cp` method is still highly recommended to prevent file corruption.
