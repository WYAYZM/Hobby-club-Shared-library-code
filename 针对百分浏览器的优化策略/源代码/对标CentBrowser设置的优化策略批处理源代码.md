对标CentBrowser设置的优化策略批处理源代码

@echo off

%1 mshta vbscript:CreateObject("Shell.Application").ShellExecute("cmd.exe","/c ""%~s0"" ::","","runas",0)(window.close)>nul 2>nul&&exit

>>"%Temp%\Reg2Temp.reg" echo Windows Registry Editor Version 5.00

>>"%Temp%\Reg2Temp.reg" echo.

>>"%Temp%\Reg2Temp.reg" echo [HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Policies\Google]

>>"%Temp%\Reg2Temp.reg" echo.

>>"%Temp%\Reg2Temp.reg" echo [HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Policies\Google\Chrome];针对百分浏览器设置的策略

>>"%Temp%\Reg2Temp.reg" echo.

>>"%Temp%\Reg2Temp.reg" echo ;1代表启用；0代表禁止

>>"%Temp%\Reg2Temp.reg" echo.

>>"%Temp%\Reg2Temp.reg" echo "BrowserThemeColor"="#000000"

>>"%Temp%\Reg2Temp.reg" echo ;浏览器主题颜色

>>"%Temp%\Reg2Temp.reg" echo "TaskManagerEndProcessEnabled"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;任务管理器结束进程已启用

>>"%Temp%\Reg2Temp.reg" echo "TranslateEnabled"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;翻译启用

>>"%Temp%\Reg2Temp.reg" echo "DefaultBrowserSettingEnabled"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;默认浏览器设置已启用

>>"%Temp%\Reg2Temp.reg" echo "SavingBrowserHistoryDisabled"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;保存浏览器历史记录已禁用

>>"%Temp%\Reg2Temp.reg" echo "ShowFullUrlsInAddressBar"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;在地址栏中显示完整网址

>>"%Temp%\Reg2Temp.reg" echo "SuppressUnsupportedOSWarning"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;抑制不支持的操作系统警告

>>"%Temp%\Reg2Temp.reg" echo "WPADQuickCheckEnabled"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;WPDA优化

>>"%Temp%\Reg2Temp.reg" echo "AllowDinosaurEasterEgg"=dword:00000000

>>"%Temp%\Reg2Temp.reg" echo ;允许恐龙复活节彩蛋 [百分浏览器自带的小恐龙游戏]

>>"%Temp%\Reg2Temp.reg" echo "BlockThirdPartyCookies"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;阻止第三方Cookie

>>"%Temp%\Reg2Temp.reg" echo "BackgroundModeEnabled"=dword:00000000

>>"%Temp%\Reg2Temp.reg" echo ;启用后台模式

>>"%Temp%\Reg2Temp.reg" echo "AutoplayAllowed"=dword:00000000

>>"%Temp%\Reg2Temp.reg" echo ;允许自动播放

>>"%Temp%\Reg2Temp.reg" echo "BrowserAddPersonEnabled"=dword:00000000

>>"%Temp%\Reg2Temp.reg" echo ;启用浏览器添加新的配置文件

>>"%Temp%\Reg2Temp.reg" echo "HardwareAccelerationModeEnabled"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;启用硬件加速模式

>>"%Temp%\Reg2Temp.reg" echo "BrowserGuestModeEnabled"=dword:00000000

>>"%Temp%\Reg2Temp.reg" echo ;启用浏览器访客模式

>>"%Temp%\Reg2Temp.reg" echo "AutofillAddressEnabled"=dword:00000000

>>"%Temp%\Reg2Temp.reg" echo ;启用自动填充地址

>>"%Temp%\Reg2Temp.reg" echo "BrowserSwitcherKeepLastChromeTab"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;在百分浏览器中保留最后一个标签打开

>>"%Temp%\Reg2Temp.reg" echo "SafeBrowsingProtectionLevel"=dword:00000002

>>"%Temp%\Reg2Temp.reg" echo ;安全浏览保护级别

>>"%Temp%\Reg2Temp.reg" echo "PasswordProtectionWarningTrigger"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;密码保护警告触发器

>>"%Temp%\Reg2Temp.reg" echo "PasswordManagerEnabled"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;启用密码管理器

>>"%Temp%\Reg2Temp.reg" echo "PasswordDismissCompromisedAlertEnabled"=dword:00000000

>>"%Temp%\Reg2Temp.reg" echo ;已启用密码接触妥协警报 [为输入的凭据启用解除密码泄漏警报]

>>"%Temp%\Reg2Temp.reg" echo "PasswordLeakDetectionEnabled"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;启用密码泄漏检测

>>"%Temp%\Reg2Temp.reg" echo "DefaultInsecureContentSetting"=dword:00000003

>>"%Temp%\Reg2Temp.reg" echo ;默认不安全内容设置 [控制不安全内容异常的使用]

>>"%Temp%\Reg2Temp.reg" echo "ShowHomeButton"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;显示主页按钮 [在工具栏上显示主页按钮]

>>"%Temp%\Reg2Temp.reg" echo "FullscreenAllowed"=dword:00000001

>>"%Temp%\Reg2Temp.reg" echo ;允许全屏模式

>>"%Temp%\Reg2Temp.reg" echo "HomepageLocation"="https://baidu.com"

>>"%Temp%\Reg2Temp.reg" echo ;配置主页URL

>>"%Temp%\Reg2Temp.reg" echo "SigninAllowed"=dword:00000000

>>"%Temp%\Reg2Temp.reg" echo ;允许登陆账户

>>"%Temp%\Reg2Temp.reg" echo.

>>"%Temp%\Reg2Temp.reg" echo [HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Policies\Google\Chrome\URLBlocklist];以下为阻止访问的网址，可自行添加

>>"%Temp%\Reg2Temp.reg" echo "1"="2345.com"

>>"%Temp%\Reg2Temp.reg" echo "2"="hao123.com"

>>"%Temp%\Reg2Temp.reg" echo "3"="www.laomaotao.net"

>>"%Temp%\Reg2Temp.reg" echo "4"="lmt.waclhzp.cn"

>>"%Temp%\Reg2Temp.reg" echo "5"="hcl.baidu.com"

>>"%Temp%\Reg2Temp.reg" echo "6"="lmt.qima1.top"

>>"%Temp%\Reg2Temp.reg" echo "7"="www.1zd1.com"

>>"%Temp%\Reg2Temp.reg" echo "8"="pe.wfhlwl.cn"

>>"%Temp%\Reg2Temp.reg" echo "9"="w.wxhse.cn"

>>"%Temp%\Reg2Temp.reg" echo "10"="dbc.hzfkznp.cn"

>>"%Temp%\Reg2Temp.reg" echo "11"="dbc.nxexvq.cn"

>>"%Temp%\Reg2Temp.reg" echo "12"="www.winbaicai.com"

>>"%Temp%\Reg2Temp.reg" echo "13"="www.dabaicai.com"

>>"%Temp%\Reg2Temp.reg" echo "14"="www.weipe.com"

>>"%Temp%\Reg2Temp.reg" echo "15"="www.uqitong.com"

>>"%Temp%\Reg2Temp.reg" echo "16"="www.uqitong.com"

>>"%Temp%\Reg2Temp.reg" echo "17"="www.uqitong.com"

>>"%Temp%\Reg2Temp.reg" echo "18"="lao9123.com"

>>"%Temp%\Reg2Temp.reg" echo "19"="www.bear20.com"

>>"%Temp%\Reg2Temp.reg" echo "20"="hbs.lzlcm.cn"

>>"%Temp%\Reg2Temp.reg" echo "21"="www.xiaobaixitong.com"

>>"%Temp%\Reg2Temp.reg" echo "22"="www.qihuys520.vip"

>>"%Temp%\Reg2Temp.reg" echo "23"="3721.com"

>>"%Temp%\Reg2Temp.reg" echo "24"="MOP.com"

>>"%Temp%\Reg2Temp.reg" echo "25"="Zhongsou.com"

>>"%Temp%\Reg2Temp.reg" echo "26"="Sougou.com"

>>"%Temp%\Reg2Temp.reg" echo "27"="51.com"

>>"%Temp%\Reg2Temp.reg" echo "28"="265.com"

>>"%Temp%\Reg2Temp.reg" echo "29"="Bokee.com"

>>"%Temp%\Reg2Temp.reg" echo "30"="Qyule.com"

>>"%Temp%\Reg2Temp.reg" echo "31"="9991.com"

>>"%Temp%\Reg2Temp.reg" echo "32"="yxtg.taojike.com.cn"

>>"%Temp%\Reg2Temp.reg" echo "33"="www.so.com"

>>"%Temp%\Reg2Temp.reg" echo "34"="hao.360.com"

>>"%Temp%\Reg2Temp.reg" echo "35"="tp.9377s.com"

>>"%Temp%\Reg2Temp.reg" echo "36"="www.code.91tw.net"

>>"%Temp%\Reg2Temp.reg" echo "37"="www.duba.com"

>>"%Temp%\Reg2Temp.reg" echo "38"="www.duba.com"

>>"%Temp%\Reg2Temp.reg" echo "39"="www.hao774.com"

;下面为自定义的屏蔽网址已经写好格式了，自己添加就好

>>"%Temp%\Reg2Temp.reg" echo ""=""
