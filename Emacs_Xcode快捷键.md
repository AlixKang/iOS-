# Emacs笔记 部分适用于Xcode
<br>

---
* ### 与文件操作有关的命令

| 键盘操作 | 命令名称 | 说明  |
| ------  | -----  | -----|
| `C-x C-f` | find-file | 查找文件并在一个新缓冲区里打开它 相当于 `Files -> Open File`
| `C-x C-v` | find-alternate-file | 读入另外一个文件替换掉用'C-x C-f'读入的文件
| `C-x i` | insert-file | 把文件插入到光标的当前位置 相关于`Files -> Insert File`
| `C-x C-s` | save buffer | 保存文件
| `C-x C-w` | write file | 把缓冲区内容写入一个文件 相关于`Files -> Save Buffer As`
| `C-x C-c` | save buffers kill emacs | 退出Emacs 相关于`Files -> Exit Emacs`
| `C-h` | help command | 进入Emacs的在线帮助系统 
| `C-h f` | describe-function | 给出某个给定命令名的在线帮助信息 相当于`Help -> Describe Function`
| `C-h k` | describe-key | 给出某个给定击键序列在帮助信息 相当于`Help -> Describe Key`
| `C-h i` | info goto emacs command mode | 启用Info文档阅读器 相当于`Help -> Brower Manuals`


<br>

---
* ### 移动光标

| 键盘操作 | 命令名称 | 说明  |
| ------  | -----  | -----|
| `C-f` | farward char | 光标前移一个字符(右)
| `C-b` | backward char | 光标后移一个字符(左)
| `C-p` | previous line | 光标前移一行(上)
| `C-n` | next line | 光标后移一行(下)
| `ESC f` | forward word | 光标前移一个单词
| `ESC b` | backward word | 光标后移一个单词
| `C-a` | beginning of line | 光标移到行首
| `C-e` | end of line |  光标移到行尾
| `ESC e` | forward sentence | 光标前移一个句子
| `ESC a` | backward sentence | 光标后移一个句子
| `ESC }` | forward paragraph | 光标前移一个段落
| `ESC {` | backward paragraph | 光标后移一个段落 
| `C-v` | scroll up | 屏幕上翻一屏
| `ESC v` | scroll down | 屏幕下翻一屏
| `C-x ]` | forward page | 光标前移一页
| `C-x [` | backward page | 光标后移一页
| `ESC <` | beginning of buffer | 光标称到文件头
| `ESC >` | end of buffer | 光标移到文件尾
| `ESC-x goto-line` | goto-line | 光标前进到文件的第n行
| `ESC-x goto-char` | goto-char | 光标前进到文件的第n个字符
| `C-l` | recenter | 重新绘制屏显画面, 肖前行放在画面中心处
| `ESC n` | digit-argument | 重复执行n次后续命令
| `C-u n` | universal-argument | 重复执行n次后续命令(`省略时重复4次`)

<br>

----
* ### 文本操作(Copy/Cut/Paste/Delete/Undo/Redo/Replace)

| 键盘操作 | 命令名称 | 说明  |
| ------  | -----  | -----|
| `C-d` | delete char | 删除光标位置 上的字符
| `DEL` | delete backward char | 删除光标前面的字符 
| `ESC d` | kill word | 删除光标后面的单词
| `ESC DEL` | backward kill word | 删除光标后面的单词
| `C-k` | kill line | 从光标位置删除到行尾
| `ESC k` | kill sentence | 删除光标后面的句子
| `C-x DEL` | backward kill sentence | 删除光标前面的句子
| `C-y` | yank | 恢复被删除的文本 相关于`Edit -> Paste Most Recent`
| `C-w` | kill region | 删除文本块 相关于`Edit -> Cut`
| `ESC-x kill-paragraph` | kill paragraph | 删除光标后面的段落
| `ESC-x backward-kill-paragraph` | backward kill paragraph | 删除光标前面的段落
| `C-@ 或 C-SPACE` | set mark command | 标记文本块的开始(或结束)位置
| `C-x C-x` | exchange point and mark | 互换插入点和文本标记的位置
| `ESC w 或 C-INSERT` | kill ring save | 复制文本块(以便用`C-y`命令来粘贴它)
| `ESC h` | mark paragraph | 标记段落
| `C-x C-p` | mark page | 标记页面
| `C-x h` | mark whole buffer | 标记整个缓冲区
| `ESC y` | yank pop | 在用过`C-y`命令以后粘贴更早删除的文本 相当于`Edit -> Select and Paste`
| `C-t` | transpose chars | 交换两个字符的位置 
| `ESC t` | transpose words | 交换两个单词的位置 
| `C-x C-t` | transpose lines | 交换两个文本行的位置 
| `ESC-x transpose-sentences` | transpose sentences | 交换两个句子的位置 
| `ESC-x transpose-paragraphs` | transpose paragraphs | 交换两个段落的位置
| `ESC c` | capitalize word | 把单词的首字母改为大写
| `ESC u` | upcase word | 把单词的字母全部改为大写
| `ESC l` | downcase word | 把单词的字母全部改为小写
| `ESC ESC c` | negtive argument; capitalize word | 把前一个单词的首字母改为大写
| `ESC ESC u` | negtive argument; upcase word | 把前一个单词的字母全部改为大写
| `ESC ESC l` | negtive argument; downcase word | 把前一个单词的字母全部改为小写
| `ESC-x overwrite-mode` | overwrite mode | 改写模式
| `C-g` | keyboard quit | 放弃当前命令
| `C-x u` | advertised-undo | 撤消上一次编辑(可重复使用)
| `C-_或C-/` | undo | 撤消上一次编辑 相当于`Edit -> Undo`
| `ESC-x revert-buffer` | revert buffer | 把缓冲区恢复到上次对文件进行存盘(或者自动存盘)时的状态








