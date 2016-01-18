# tmux

tmux结构: server-session-window-pane
一个tmux服务管理多个会话，一个会话可以有多个窗口，一个窗口可以有对个面板

alias t='tmux -2'

t              #创建新的会话
t new -s name  #创建新的会话
t ls           #查看所有会话
t a            #attach到上次detach的会话
t a -t n       #attach到编号为n的会话
t a -t name    #attach到name会话
C-d            #关闭当前会话
C-x a          #打开会话列表，上下键选择
C-x d          #detach当前会话

C-x ?          #帮助
C-x t          #时间

C-x c          #创建新的窗口
C-x n          #下一个窗口
C-x p          #上一个窗口
C-x w          #打开窗口列表，上下键选择
C-x n          #跳转到编号为n的窗口
C-x ,          #修改当前窗口名字

C-x s          #在当前窗口，水平分割出一个面板
C-x v          #在当前窗口，垂直分割出一个面板
C-x h/j/k/l    #上下左右切换面板
C-x C-方向键   #调整面板大小
C-x q          #显示面板编号
C-x x          #关闭当前面板

#复制模式
C-x [          #进去复制模式（或者C-x pageup/pagedown），可以使用vi快捷键翻页、跳转、搜索等
space          #开始复制，移动光标选择复制区域
Enter          #复制并退出copy-mode
C-x ]          #粘贴
