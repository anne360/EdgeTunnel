This is a script based on the CF Worker platform. It modifies the original version to display the VLESS configuration information converted to subscription content. With this script, you can easily convert the VLESS configuration information to tools such as Clash or Singbox using online configuration.

Basic deployment video tutorial: https://www.youtube.com/watch?v=LeT4jQUh8ok
Quick deployment video tutorial: https://www.youtube.com/watch?v=59THrmJhmAw Best recommendation!!!
Advanced use video tutorial: https://www.youtube.com/watch?v=s91zjpw3-P8
From entry to mastery tutorial: https://www.youtube.com/watch?v=oRYnrp5rQSc Must-see content! Must-see content! Must-see content!!!

Telegram communication group: @CMLiussss, thanks to Alice Networks for providing cloud servers to maintain CM subscription conversion services!
Disclaimer

This disclaimer applies to the "edgetunnel" project on GitHub (hereinafter referred to as "this project"), the project link is: https://github.com/cmliu/edgetunnel .
Purpose

This project is designed and developed for educational, research and security testing purposes only. It aims to provide a tool for security researchers, academics and technology enthusiasts to explore and practice network communication technologies.
Legality

When downloading and using the code of this project, you must comply with the laws and regulations applicable to the user. The user is responsible for ensuring that his or her behavior complies with the legal framework, rules and regulations and other relevant regulations in the region.
Disclaimer

As the secondary developer of this project (hereinafter referred to as "the author"), I cmliu emphasize that this project should only be used for legal, ethical and educational purposes.
The author does not approve, support or encourage any form of illegal use. If it is found that this project is used for any illegal or unethical activities, the author will strongly condemn it.
The author is not responsible for any illegal activities carried out by any person or organization using the code of this project. Any consequences arising from the use of the code of this project shall be borne by the user.
The author is not responsible for any direct or indirect damages that may arise from the use of this project code.
To avoid any unexpected consequences or legal risks, users should delete the code within 24 hours after using this project code.
By using this project code, users understand and agree to all the terms of this disclaimer. If users do not agree to these terms, they should immediately stop using this project.

The author reserves the right to update this disclaimer at any time without further notice. The latest version of the disclaimer will be published on the GitHub page of this project.
Risk Warning

Avoid node configuration information leakage by submitting false node configuration to the subscription service.
In addition, you can also choose to deploy the WorkerVless2sub subscription generation service yourself, so that you can take advantage of the convenience of the subscription generator.

Workers deployment method video tutorial
「Workers deployment text tutorial」

Pages upload deployment method best recommendation!!! video tutorial
「Pages upload file deployment text tutorial」

Pages GitHub deployment method video tutorial
「Pages GitHub deployment text tutorial」

Variable description
Variable name Example Required Notes YT
UUID 90cd4a77-141a-43c9-991b-08263cfe9c10 ✅ Powershell -NoExit -Command "[guid]::NewGuid()" Video
KEY token ❌ Dynamic UUID secret key, when using variable KEY, variable UUID will no longer be enabled
TIME 7 ❌ Dynamic UUID validity period (unit: day)
UPTIME 3 ❌ Dynamic UUID update time (default: updated at 3:00 Beijing time)
PROXYIP proxyip.fxxk.dedyn.io:443 ❌ Alternative proxy node for accessing CFCDN sites (supports custom ProxyIP port, supports multiple ProxyIPs, use between ProxyIPs, or line breaks as intervals) Video
SOCKS5 user:password@127.0.0.1:1080 ❌ Prioritize as a SOCKS5 proxy for accessing CFCDN sites (supports multiple socks5, use between socks5, or line breaks as intervals) Video
GO2SOCKS5 blog.cmliussss.com,*.ip111.cn,*google.com ❌ After setting the SOCKS5 variable, you can set a mandatory socks5 access list (* can be used as a wildcard, line breaks as multiple element intervals)
ADD icook.tw:2053#Official preferred domain name ❌ Local preferred TLS domain name/preferred IP (supports multiple elements, or line breaks as intervals)
ADDAPI https://raw.github.../addressesapi.txt ❌ API address of preferred IP (supports multiple elements, or line breaks as intervals)
ADDNOTLS icook.hk:8080#Official preferred domain name ❌ Local preferred noTLS domain name/preferred IP (supports multiple elements, or line breaks as intervals)
ADDNOTLSAPI https://raw.github.../addressesapi.txt ❌ API address of preferred IP (supports multiple elements, or line breaks as intervals)
ADDCSV https://raw.github.../addressescsv.csv ❌ iptest speed test results (supports multiple elements, use of elements as intervals)
DLS 8 ❌ ADDCSV speed test results meet the speed limit
TGTOKEN 6894123456:XXXXXXXXXX0qExVsBPUhHDAbXXX ❌ Robot token for sending TG notifications
TGID 6946912345 ❌ Account digital ID for receiving TG notifications
SUB VLESS.fxxk.dedyn.io ❌ Subscription generator address with built-in domain name and IP node information Video
SUBAPI SUBAPI.fxxk.dedyn.io ❌ Subscription conversion backend such as clash and singbox Video
SUBCONFIG https://raw.github.../ACL4SSR_Online_Full_MultiMode.ini ❌ Subscription conversion configuration file such as clash and singbox Video
SUBNAME edgetunnel ❌ Subscription name
RPROXYIP false ❌ Set to true to force the acquisition of the ProxyIP assigned by the subscriber (subscriber support required) Video
URL302 https://t.me/CMLiussss ❌ Home page 302 jump (supports multiple URLs, use between URLs, or line breaks as intervals, don't use it if you are new)
URL https://blog.cmliussss.com ❌ Homepage anti-genuine camouflage (supports multiple URLs, use between URLs, or use line breaks as intervals. Random settings can easily trigger anti-fraud)
CFEMAIL admin@gmail.com ❌ CF account email (after filling in both CFKEY, the subscription information will display the request usage, so don’t use it if you’re new to it)
CFKEY c6a944b5c956b6c18c2352880952bced8b85e ❌ CF account Global API Key (after filling in both CFEMAIL, the subscription information will display the request usage, so don’t use it if you’re new to it)
CFPORTS 2053,2096,8443 ❌ CF account standard port list

Note: UUID will no longer be enabled after filling in KEY! Please choose one of the two! ! !

After filling in KEY, the permanent subscription address is https://[YOUR-URL]/[YOUR-KEY];
After filling in KEY, the temporary subscription address is https://[YOUR-URL]/[YOUR-UUID];
The subscription usage time of dynamic UUID is 1 TIME valid time period;
The node usage time of dynamic UUID is 2 TIME valid time periods (that is, if the dynamic UUID expires, the node can continue to be used for one period, but the subscription cannot be updated);

Note: After filling in SOCKS5, PROXYIP will no longer be enabled! Please choose one of the two! ! !

Note: After filling in SUB, the subscription content generated by ADD* class variables will no longer be enabled! Please choose one of the two! ! !

Note: Filling in CFEMAIL and CFKEY at the same time will enable the display of request usage, but it is not recommended! There is no need to give a Worker project such a high authority! You are at your own risk! ! !

Practical tips

The subscription deployed by this project can quickly change the preferred subscription generator by adding the sub key value!

For example, https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10 is your universal adaptive subscription address

Quickly change the subscriber to the subscription address of VLESS.fxxk.dedyn.io

https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sub=VLESS.fxxk.dedyn.io

The nodes deployed in this project can use the specified PROXYIP or SOCKS5 through the node PATH (path) method! ! !

Specifying PROXYIP example

/proxyip=proxyip.fxxk.dedyn.io
/?proxyip=proxyip.fxxk.dedyn.io
/proxyip.fxxk.dedyn.io (limited to domain names starting with 'proxyip.')

Specifying SOCKS5 Case

/socks5=user:password@127.0.0.1:1080
/?socks5=user:password@127.0.0.1:1080
/socks://dXNlcjpwYXNzd29yZA==@127.0.0.1:1080
/socks5://user:password@127.0.0.1:1080

When your ADDAPI can be used as a PROXYIP, you can add?proxyip=true at the end of the ADDAPI variable, and then use the preferred IP itself as the PROXYIP when generating nodes

Specify ADDAPI as a PROXYIP case

https://raw.githubusercontent.com/cmliu/WorkerVless2sub/main/addressesapi.txt?proxyip=true

Star Stars Go

Stargazers over time
Adapted client
Windows

v2rayN
clash.meta (FlClash, clash-verge-rev, Clash Nyanpasu)

IOS

Surge, Little Rocket
sing-box (SFI)

Android

clash.meta (ClashMetaForAndroid, FlClash)
sing-box (SFA)

MacOS

clash.meta (FlClash)

Thanks
zizifn, 3Kmfi6HP, Stanley-baby, ACL4SSR, SHIJS1999, Alice Networks LTD,