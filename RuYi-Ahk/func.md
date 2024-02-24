---
layout: default
title: 如意百宝箱-Ahk
description: 如意百宝箱-Ahk 内置函数
---

[返回主页](index.md)

# [](#header-2) 内置函数

如意中内置的函数(包括标签). 支持传入[变量](./var.md).  

| 序号 | 动作 | 参数 | 说明 | 示例用法 |
| ----------- | ----------- | ----------- | ----------- | ----------- | 
|1|CF_AlwaysOnTop|(WinId)|传入窗口句柄, 使窗口置顶|[动作1049](/Actions/1049.md): canfunc&#124;CF_AlwaysOnTop&#124;%Windy_CurWin_id%|
|2|CF_CloseScreen|()|关闭显示器, 使其黑屏|[动作1168](/Actions/1168.md): canfunc&#124;CF_CloseScreen|
|3|CF_FileDelete|(sfile)|传入文件路径, 删除该文件, FileDelete 命令函数化|[动作1073](/Actions/1073.md): canfunc&#124;CF_FileDelete&#124;%CandySel%|
|4|CF_FileGetShortcut|(LinkFile, OutValue := 1, clip := 1)|FileGetShortcut 命令函数化, OutValue 为要得到值的序号(1-7)|[动作1149](/Actions/1149.md): Canfunc&#124;CF_FileGetShortcut&#124;%CandySel%|
|5|CF_FileMoveToFolder|(sfile, targetFolderName := "新建文件夹")|将选中文件移动到同级指定文件夹中,如果没有指定文件夹则默认为新建文件夹|[动作1267](/Actions/1267.md): canfunc&#124;CF_FileMoveToFolder&#124;%CandySel%|
|6|CF_FileRecycleEmpty|(DriveLetter := "")|清空回收站|[动作1362](/Actions/1362.md): canfunc&#124;CF_FileRecycleEmpty|
|7|CF_FileRemoveBlankDir|(sfolder)|删除指定文件夹下的所有空目录(每个文件夹只循环一次)|[动作1077](/Actions/1077.md): canfunc&#124;CF_FileRemoveBlankDir&#124;%Windy_CurWin_FolderPath%|
|8|CF_FileShortcutTarget|(sfile)|打开指定lnk快捷方式文件目标所在目录|[动作1053](/Actions/1053.md): CanFunc&#124;CF_FileShortcutTarget&#124;%CandySel%|
|9|CF_FileShortcutToDesk|(sfile)|创建指定文件的快捷方式到桌面|[动作1085](/Actions/1085.md): canfunc&#124;CF_FileShortcutToDesk&#124;%CandySel%|
|10|CF_FileToClip|(sfile)|复制指定文本文件的内容到剪贴板|动作1170: canfunc&#124;CF_FileToClip&#124;%CandySel%|
|11|CF_OpenProp|(sfile)|打开指定文件系统属性对话框|[动作1421](/Actions/1421.md): CanFunc&#124;CF_OpenProp&#124;%CandySel%|
|12|CF_ProcessClose|(WinPid := "")|强制结束指定进程|[动作1244](/Actions/1244.md): canfunc&#124;CF_ProcessClose&#124;%Windy_CurWin_Pid%|
|13|CF_restartexplorer|()|强制重新打开资源管理器|[动作1124](/Actions/1124.md): canfunc&#124;CF_restartexplorer|
|14|CF_WinKill|(WinId := "")|强制结束指定进程|[动作1243](/Actions/1243.md): canfunc&#124;CF_WinKill&#124;%Windy_CurWin_id%|
|15|CF_WinMinimizeAll|CF_WinMinimizeAll(mode := 1)|最小化所有窗口或还原|[动作1361](/Actions/1361.md): canfunc&#124;CF_WinMinimizeAll|
|16|CF_WinRemoveTaskbarButton|(WinId := "")|移除或恢复指定窗口在任务栏的按钮|[动作1241](/Actions/1241.md): canfunc&#124;CF_WinRemoveTaskbarButton&#124;%Windy_CurWin_id%|
|17|CF_WinSetTransparent|(N, WinId:="")|设置指定窗口的透明度|[动作1068](/Actions/1068.md): canfunc&#124;CF_WinSetTransparent&#124;128|
|18|CF_关机或重启|(num:=9)|Shutdown 命令的函数化|[动作1356](/Actions/1356.md): canfunc&#124;CF_关机或重启|
|19|CF_静音|(mode := "+1")|SoundSet 命令的函数化|[动作1353](/Actions/1353.md): canfunc&#124;CF_静音|
|20|ExecSend|(ByRef StringToSend, Title := "AnyToAhk ahk_class AutoHotkey", wParam := 0, Msg := 0x4a, Idc := "")|像 ATA 或外部脚本发送消息|[动作1102](/Actions/1102.md): canfunc&#124;ExecSend&#124;%CandySel%&#124;MD5验证 ahk_class AutoHotkeyGUI|
|21|ExecSendToDll|(ByRef StringToSend:="", Title:="AutoHotkey.dll ahk_class AutoHotkey", wParam := 0, Msg:=0x4a, Idc:="")|像如意的内置的插件脚本发送消息|动作1209: canfunc&#124;ExecSendToDll&#124;%CandySel%|
|22|PostMessToAhk|(wParam, winid)|固定消息号为 0x111,像指定 Ahk 脚本窗口发送消息 wParam|[动作1253](/Actions/1253.md): canfunc&#124;PostMessToAhk&#124;65300&#124;%Windy_CurWin_id%|
|23|SendTo32770|(Val, key := "")|设置对话框窗口中的 Edit1 控件的值, 并发送指定的按键|动作1547: canfunc&#124;SendTo32770&#124;%CandySel%&#124;{Enter}|
|24|ShowDBData|(Dtype := "execcount", Stype := "面板", Dnum := 12)|以面板或菜单形式显示动作数据库中运行次数或最近运行的动作|[动作1193](/Actions/1193.md): canfunc&#124;ShowDBData&#124;execcount&#124;菜单|
|25|ABBReSet|字符串: 按钮动作编号|接收外部脚本函数 ExecSendToRuyi 发送来的字符串, 重置额外任务栏上按钮的颜色|Cando&#124;ABBReSet|
|26|ABBSetColor|字符串: 按钮动作编号|背景色|文本颜色|接收外部脚本函数 ExecSendToRuyi 发送来的字符串, 设置额外任务栏上按钮的颜色|Cando&#124;ABBSetColor|
|27|ABTSetTextAndColor|字符串: 文本|颜色|接收外部脚本函数 ExecSendToRuyi 发送来的字符串, 设置额外任务栏顶部区域的文字和颜色|Cando&#124;ABTSetTextAndColor|
|28|ActionSR||显示搜索和运行动作的界面|[动作1233](/Actions/1233.md): Cando&#124;ActionSR|
|29|AddToCustomA|选中内容|将指定内容(文件,文件夹,文本) 添加为自定义动作|[动作1536](/Actions/1536.md): Cando&#124;AddToCustomA|
|30|addToLnkFolder|选中文件|发送指定文件的快捷方式到如意的 Lnk 文件夹|Cando&#124;addToLnkFolder|
|31|AddtoMenu||打开如意资源管理器选中右键菜单管理设置界面|[动作1342](/Actions/1342.md): Cando&#124;AddtoMenu|
|32|CreateAppBar||打开额外任务栏|[动作1523](/Actions/1523.md): Cando&#124;CreateAppBar|
|33|DarkTheme||打开系统深色模式|[动作1512](/Actions/1512.md): Cando&#124;DarkTheme|
|34|hotstrM||打开热字串管理界面|Cando&#124;hotstrM|
|35|LightTheme||打开系统浅色模式|[动作1511](/Actions/1511.md): Cando&#124;LightTheme|
|36|ScriptManager||Ahk 脚本管理器|Cando&#124;ScriptManager|
|37|TimingActionM||打开定时动作管理界面|[动作1414](/Actions/1414.md): Cando&#124;TimingActionM|
|38|TM_ActionM||打开如意动作管理界面|[动作1192](/Actions/1192.md): Cando&#124;TM_ActionM|
|39|TM_BoardM||打开如意面板管理界面|[动作1263](/Actions/1263.md): Cando&#124;TM_BoardM|
|40|TM_Exit||退出如意|Cando&#124;TM_Exit|
|41|TM_Pause||暂停如意|Cando&#124;TM_Pause|
|42|TM_Reload||重启如意|Cando&#124;TM_Reload|
|43|TM_SettingsM||打开如意设置界面|[动作1413](/Actions/1413.md): Cando&#124;TM_SettingsM|
|44|TM_show||显示如意的托盘菜单|Cando&#124;TM_show|
|45|TM_ShowMG||显示如意主面板|Cando&#124;TM_ShowMG|
|46|窗口最大化||最大化鼠标下的窗口|[动作1191](/Actions/1191.md): Cando&#124;窗口最大化|
|47|窗口最小化||最小化鼠标下的窗口|[动作1190](/Actions/1190.md): Cando&#124;窗口最小化|
|48|冻结到单元格|WPS 表格||Cando&#124;冻结到单元格|
|49|关闭窗口||关闭鼠标下窗口|[动作1187](/Actions/1187.md): Cando&#124;关闭窗口|
|50|获取鼠标下文本||获取任意窗口鼠标下的文本(例如 任务管理器的命令行)|[动作1082](/Actions/1082.md): cando&#124;获取鼠标下文本|
|51|全部边框|WPS 表格||Cando&#124;全部边框|
|52|输入为数值|WPS 表格||Cando&#124;输入为数值|
|53|右半前进||浏览器发送前进快捷键, 其他窗口为移到右半屏幕|[动作1189](/Actions/1189.md): Cando&#124;右半前进|
|54|粘贴为数值|WPS 表格||Cando&#124;粘贴为数值|
|55|左半后退||浏览器发送后退快捷键, 其他窗口为移到左半屏幕|[动作1188](/Actions/1188.md): Cando&#124;左半后退|