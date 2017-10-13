### 代码注入、命令执行

	1.内置危险函数
	exec
	execfile
	eval
	
	2.标准库危险模块
	os
		os.popen() or subprocess.Popen(), and subprocess.check_output()
	sys
	subprocess
		subprocess.call(user_input, shell=True) : popen, subprocess.call等
	commands
	
	3.危险第三方库
	Template(user_input) : 模板注入(SSTI)所产生的代码执行
	subprocess32 
	
	4.反序列化
	marshal
	PyYAML
	pickle和cpickle
	shelve
	PIL
	unzip


[Python沙箱逃逸的n种姿势](https://xianzhi.aliyun.com/forum/read/2138.html)

[Python之数据序列化（json、pickle、shelve）](http://www.cnblogs.com/yyds/p/6563608.html)

[Exploiting Python PIL Module Command Execution Vulnerability](https://xianzhi.aliyun.com/forum/read/2163.html)

[Exploiting Python Code Injection in Web Applications](https://www.doyler.net/security-not-included/exploiting-python-code-injection)

[EXPLOITING PYTHON CODE INJECTION IN WEB APPLICATIONS](http://www.securitynewspaper.com/2016/11/12/exploiting-python-code-injection-web-applications/)

[Exploiting Python Code Injection in Web Applications](https://sethsec.blogspot.jp/2016/11/exploiting-python-code-injection-in-web.html)

[Python eval的常见错误封装及利用原理](http://xxlegend.com/2015/07/31/Python%20eval%E7%9A%84%E5%B8%B8%E8%A7%81%E9%94%99%E8%AF%AF%E5%B0%81%E8%A3%85%E5%8F%8A%E5%88%A9%E7%94%A8%E5%8E%9F%E7%90%86/)

[Exploiting Python’s Eval](http://www.floyd.ch/?p=584)

[Exploiting insecure file extraction in Python for code execution](https://ajinabraham.com/blog/exploiting-insecure-file-extraction-in-python-for-code-execution)

[掌阅iReader某站Python漏洞挖掘](https://www.leavesongs.com/PENETRATION/zhangyue-python-web-code-execute.html)

[Python Pickle的任意代码执行漏洞实践和Payload构造](http://www.code2sec.com/2017/03/22/python-pickle%E7%9A%84%E4%BB%BB%E6%84%8F%E4%BB%A3%E7%A0%81%E6%89%A7%E8%A1%8C%E6%BC%8F%E6%B4%9E%E5%AE%9E%E8%B7%B5%E5%92%8Cpayload%E6%9E%84%E9%80%A0/)

[Python PyYAML反序列化漏洞实验和payload构造](http://www.code2sec.com/2017/09/22/python-pyyaml%E5%8F%8D%E5%BA%8F%E5%88%97%E5%8C%96%E6%BC%8F%E6%B4%9E%E5%AE%9E%E9%AA%8C%E5%92%8Cpayload%E6%9E%84%E9%80%A0/)

[Exploiting Python Deserialization Vulnerabilities](https://crowdshield.com/blog.php?name=exploiting-python-deserialization-vulnerabilities)



### 代码审计

[Python安全编码和代码审计](http://xxlegend.com/2015/07/30/Python%E5%AE%89%E5%85%A8%E7%BC%96%E7%A0%81%E5%92%8C%E4%BB%A3%E7%A0%81%E5%AE%A1%E8%AE%A1/)

https://xianzhi.aliyun.com/forum/read/303.html
https://xianzhi.aliyun.com/forum/read/302.html
https://xianzhi.aliyun.com/forum/read/301.html
https://xianzhi.aliyun.com/forum/read/300.html
https://xianzhi.aliyun.com/forum/read/274.html

[廖新喜大佬的python代码审计工具](https://github.com/shengqi158/pyvulhunter)

[来自openstack安全团队的python代码静态审计工具](https://github.com/openstack/bandit)

[来自openstack安全团队的python代码静态审计工具2](https://github.com/openstack/syntribos)



### Django相关

[Django debug page XSS漏洞（CVE-2017-12794）分析](https://www.leavesongs.com/PENETRATION/django-debug-page-xss.html)

[Django DeleteView without confirmation template, but with CSRF attack](https://www.leavesongs.com/PYTHON/django-deleteView-without-confirmation-template.html)

[Django安全机制](http://xxlegend.com/2015/04/01/Django%E5%AE%89%E5%85%A8%E6%9C%BA%E5%88%B6/)

[从Django的SECTET_KEY到代码执行](http://xxlegend.com/2015/04/01/%E4%BB%8EDjango%E7%9A%84SECTET_KEY%E5%88%B0%E4%BB%A3%E7%A0%81%E6%89%A7%E8%A1%8C/)

[Django CSRF Bypass (CVE-2016-7401) 漏洞分析](https://paper.seebug.org/58/)

[Django的两个url跳转漏洞分析:CVE-2017-7233&7234](https://paper.seebug.org/274/)

[Python 格式化字符串漏洞（Django为例）](https://www.leavesongs.com/PENETRATION/python-string-format-vulnerability.html)

[Django 安全最佳实践](http://www.atjiang.com/2scoopsdjango1.8-26-security-best-practices/)

[从Pwnhub诞生聊Django安全编码](https://www.leavesongs.com/PYTHON/django-coding-experience-from-pwnhub.html)

[python和django的目录遍历漏洞(任意文件读取)](http://www.lijiejie.com/python-django-directory-traversal/)

[新型任意文件读取漏洞的研究](https://www.leavesongs.com/PENETRATION/arbitrary-files-read-via-static-requests.html)



### package钓鱼

[Package 钓鱼](https://paper.seebug.org/311/)

[被忽视的攻击面：Python package 钓鱼](https://paper.seebug.org/326/)

https://www.pytosquatting.org/



### LDAP注入

[Python安全编码之预防LDAP注入](http://xxlegend.com/2016/12/01/Python%E5%AE%89%E5%85%A8%E7%BC%96%E7%A0%81%E4%B9%8B%E9%A2%84%E9%98%B2LDAP%E6%B3%A8%E5%85%A5/)



### SSRF

[谈一谈如何在Python开发中拒绝SSRF漏洞](https://www.leavesongs.com/PYTHON/defend-ssrf-vulnerable-in-python.html)

[Python安全 - 从SSRF到命令执行惨案](https://www.leavesongs.com/PENETRATION/getshell-via-ssrf-and-redis.html)

[Splash SSRF 到获取内网服务器 ROOT 权限](https://xianzhi.aliyun.com/forum/read/1872.html)



### 其他

[如何判断目标站点是否为Django开发](https://www.leavesongs.com/PENETRATION/detect-django.html)

[Supervisord远程命令执行漏洞（CVE-2017-11610）](https://www.leavesongs.com/PENETRATION/supervisord-RCE-CVE-2017-11610.html)

[python富文本XSS过滤器](https://www.leavesongs.com/PYTHON/python-xss-filter.html)

[基于mezzanine的攻防比赛环境搭建及XXE漏洞构造/](http://xxlegend.com/2016/04/01/%E5%9F%BA%E4%BA%8Emezzanine%E7%9A%84%E6%94%BB%E9%98%B2%E6%AF%94%E8%B5%9B%E7%8E%AF%E5%A2%83%E6%90%AD%E5%BB%BA%E5%8F%8AXXE%E6%BC%8F%E6%B4%9E%E6%9E%84%E9%80%A0/)

[Python Waf黑名单过滤下的一些Bypass思路](http://www.0aa.me/index.php/archives/123/)

[Pwnhub Web题Classroom题解与分析](https://www.leavesongs.com/PENETRATION/pwnhub-web-classroom-django-sql-injection.html)



### 安全工具

[python正向连接后门](https://www.leavesongs.com/PYTHON/python-shell-backdoor.html)

[struts2 S2-016/S2-017 Python GetShell](https://www.leavesongs.com/PENETRATION/UseOfStruts.html)

[Python多线程端口扫描工具](https://www.leavesongs.com/PYTHON/PortScanner.html)

[Python JSON Fuzzer: PyJFuzz](https://n0where.net/python-json-fuzzer-pyjfuzz/)

https://github.com/smartFlash/pySecurity



### 对象注入

[DEFENCELY CLARIFIES PYTHON OBJECT INJECTION EXPLOITATION](https://defencely.com/blog/defencely-clarifies-python-object-injection-exploitation/)