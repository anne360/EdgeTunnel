# EdgeTunnel (VLESS Config for V2ray)
This is a script based on the CF Worker platform. It modifies the original version to display VLESS configuration information and convert it into subscription content. Using this script, you can easily convert VLESS configuration information to tools such as Clash or Singbox using online configuration.

- Basic deployment video tutorial: https://www.youtube.com/watch?v=LeT4jQUh8ok
- Quick deployment video tutorial: https://www.youtube.com/watch?v=59THrmJhmAw ***Best recommendation!!!***
- Advanced use video tutorial: https://www.youtube.com/watch?v=s91zjpw3-P8
- **From entry to mastery** tutorial: https://www.youtube.com/watch?v=oRYnrp5rQSc ***Must-see content! Must-see content! Must-see content!!!***

Telegram communication group: [@CMLiussss](https://t.me/CMLiussss), **Thanks to [Alice Networks](https://url.cmliussss.com/alice) for providing cloud servers to maintain [CM subscription conversion service](https://sub.fxxk.dedyn.io/)! **

# Disclaimer

This disclaimer applies to the "edgetunnel" project on GitHub (hereinafter referred to as "this project"), the project link is: https://github.com/cmliu/edgetunnel .

### Purpose
This project is designed and developed for educational, research and security testing purposes only. It aims to provide a tool for security researchers, academics and technology enthusiasts to explore and practice network communication technologies.

### Legality
When downloading and using the code of this project, you must comply with the laws and regulations applicable to the user. The user is responsible for ensuring that his or her behavior complies with the legal framework, rules and regulations and other relevant regulations in the region.

### Disclaimer
1. As the **secondary development author** of this project (hereinafter referred to as "the author"), I **cmliu** emphasize that this project should only be used for legal, ethical and educational purposes.
2. The author does not endorse, support or encourage any form of illegal use. If it is found that this project is used for any illegal or unethical activities, the author will strongly condemn it.
3. The author is not responsible for any illegal activities carried out by any person or organization using the code of this project. Any consequences arising from the use of this project code shall be borne by the user.
4. The author is not responsible for any direct or indirect damages that may be caused by the use of this project code.
5. To avoid any unexpected consequences or legal risks, users should delete the code within 24 hours after using this project code.

By using this project code, users understand and agree to all the terms of this disclaimer. If users do not agree to these terms, they should immediately stop using this project.

The author reserves the right to update this disclaimer at any time without further notice. The latest version of the disclaimer will be published on the GitHub page of this project.

## Risk Warning
- Avoid node configuration information leakage by submitting false node configuration to the subscription service.
- In addition, you can also choose to deploy [WorkerVless2sub Subscription Generation Service](https://github.com/cmliu/WorkerVless2sub) by yourself, so that you can take advantage of the convenience of the subscription generator.

## Workers deployment method [video tutorial](https://www.youtube.com/watch?v=LeT4jQUh8ok&t=83s)

<details>
<summary><code><strong>「 Workers deployment text tutorial 」</strong></code></summary>

1. Deploy CF Worker:
- Create a new Worker in the CF Worker console.
- Paste the contents of [worker.js](https://github.com/cmliu/edgetunnel/blob/main/_worker.js) into the Worker editor.
- Change line 7 `userID` to your own **UUID**.

2. Access subscription content:
- Visit `https://[YOUR-WORKERS-URL]/[UUID]` to get subscription content.
- For example, `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` is your universal adaptive subscription address.
- For example, `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sub` Base64 subscription format, suitable for PassWall, SSR+, etc.
- For example, `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?clash` Clash subscription format, suitable for OpenClash, etc.
- For example, `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sb` singbox subscription format, suitable for singbox, etc.

3. Bind custom domains to workers:
- In the `Trigger` tab of the workers console, click `Add custom domain` below.
- Fill in the subdomain name you have transferred to the CF domain name resolution service, for example: `vless.google.com`, then click `Add custom domain` and wait for the certificate to take effect.
- **If you are a novice, you can take off now, no need to read on! ! ! **

4. Subscription content using your own `preferred domain name`/`preferred IP`:
- If you want to use your own preferred domain name or your own preferred IP, you can refer to the deployment instructions in the [WorkerVless2sub GitHub repository](https://github.com/cmliu/WorkerVless2sub) to build it yourself.
- Open the [worker.js](https://github.com/cmliu/edgetunnel/blob/main/_worker.js) file, find the `sub` variable in line 12, and modify it to the subscription generator address you deployed. For example, `let sub = 'sub.cmliussss.workers.dev';`, be careful not to include protocol information and symbols such as https.
- Note that if you use your own subscription address, the `sub` domain name of the subscription generator and the domain name of `[YOUR-WORKER-URL]` must not belong to the same top-level domain name, otherwise an exception will occur. You can assign the domain name assigned to workers.dev to the `sub` variable.

</details>

## Pages upload deployment method **Best recommendation!!!** [Video tutorial](https://www.youtube.com/watch?v=59THrmJhmAw)

<details>
<summary><code><strong>「 Pages upload file deployment text tutorial 」</strong></code></summary>

1. Deploy CF Pages:
- Download the [main.zip](https://github.com/cmliu/edgetunnel/archive/refs/heads/main.zip) file and click Star!!!
- After selecting `Upload assets` in the CF Pages console, name your project and click `Create Project`, then upload the downloaded [main.zip](https://github.com/cmliu/edgetunnel/archive/refs/heads/main.zip) file and click `Deploy site`.
- After the deployment is complete, click `Continue processing site`, select `Settings` > `Environment variables` > **Make** define variables for production environment > `Add variable`.
Fill in **UUID** for the variable name and your UUID for the value, then click `Save`.
- Return to the `Deployment` tab, click `Create new deployment` in the lower right corner, re-upload the [main.zip](https://github.com/cmliu/edgetunnel/archive/refs/heads/main.zip) file, and click `Save and deploy`.

2. Access subscription content:
- Visit `https://[YOUR-PAGES-URL]/[YOUR-UUID]` to get the subscription content.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` is your universal adaptive subscription address.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sub` Base64 subscription format, suitable for PassWall, SSR+, etc.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?clash` Clash subscription format, suitable for OpenClash, etc.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sb` singbox subscription format, suitable for singbox, etc.

3. Bind a CNAME custom domain to Pages: [Video tutorial](https://www.youtube.com/watch?v=LeT4jQUh8ok&t=851s)
- In the `Custom Domains` tab of the Pages console, click `Set Custom Domain` at the bottom.
- Fill in your custom subdomain name, and be careful not to use your root domain name, for example:
If the domain name you are assigned is `fuck.cloudns.biz`, then add a custom domain and fill in `lizi.fuck.cloudns.biz`;
- According to the requirements of CF, your domain name DNS service provider will be returned. After adding the CNAME record `edgetunnel.pages.dev` of the custom domain `lizi`, click `Activate Domain`.
- **If you are a novice, then your pages can be directly launched after binding the `custom domain`, no need to read on! ! ! **

4. Subscriptions using your own `preferred domain name`/`preferred IP`:
- If you want to use your own preferred domain name or your own preferred IP, you can refer to the deployment instructions in the [WorkerVless2sub GitHub repository](https://github.com/cmliu/WorkerVless2sub) to build it yourself.
- In the `Settings` tab of the Pages console, select `Environment variables` > `Make` > `Edit variables` > `Add variable`;
- Set the variable name to `SUB`, and the corresponding value is the address of the subscription generator you deployed. For example, `sub.cmliussss.workers.dev`, and then click **Save**.
- Then in the `Deployment` tab of the Pages console, select `All deployments` > `Latest deployment rightmost ...` > `Retry deployment`, and that's it.
- Note that if you use your own subscription address, the `SUB` domain name of the subscription generator and the domain name of `[YOUR-PAGES-URL]` must not belong to the same top-level domain name, otherwise an exception will occur. You can assign the domain name assigned to Pages.dev to the `SUB` variable.

</details>

## Pages GitHub deployment method [video tutorial](https://www.youtube.com/watch?v=LeT4jQUh8ok&t=560s)

<details>
<summary><code><strong>「 Pages GitHub deployment text tutorial 」</strong></code></summary>

1. Deploy CF Pages:
- Fork this project on Github and click Star!!!- In the CF Pages console, select `Connect to Git`, select the `edgetunnel` project and click `Start Setup`.
- Under the `Set up build and deployment` page, select `Environment variables (advanced)` and `Add variable`
Fill in **UUID** as the variable name and your UUID as the value, then click `Save and deploy`.

2. Access subscription content:
- Visit `https://[YOUR-PAGES-URL]/[YOUR-UUID]` to get the subscription content.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` is your universal adaptive subscription address.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sub` Base64 subscription format, suitable for PassWall, SSR+, etc.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?clash` Clash subscription format, suitable for OpenClash, etc.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sb` singbox subscription format, suitable for singbox, etc.

3. Bind a CNAME custom domain to Pages: [Video tutorial](https://www.youtube.com/watch?v=LeT4jQUh8ok&t=851s)
- In the `Custom Domains` tab of the Pages console, click `Set Custom Domain` at the bottom.
- Fill in your custom subdomain name, and be careful not to use your root domain name, for example:
If the domain name you are assigned is `fuck.cloudns.biz`, then add a custom domain and fill in `lizi.fuck.cloudns.biz`;
- According to the requirements of CF, your domain name DNS service provider will be returned. After adding the CNAME record `edgetunnel.pages.dev` of the custom domain `lizi`, click `Activate Domain`.
- **If you are a novice, then your pages can be directly launched after binding the `custom domain`, no need to read on! ! ! **

4. Subscriptions using your own `preferred domain name`/`preferred IP`:
- If you want to use your own preferred domain name or your own preferred IP, you can refer to the deployment instructions in the [WorkerVless2sub GitHub repository](https://github.com/cmliu/WorkerVless2sub) to build it yourself.
- In the `Settings` tab of the Pages console, select `Environment variables` > `Make` > `Edit variables` > `Add variable`;
- Set the variable name to `SUB`, and the corresponding value is the address of the subscription generator you deployed. For example, `sub.cmliussss.workers.dev`, and then click **Save**.
- Then in the `Deployment` tab of the Pages console, select `All deployments` > `Latest deployment rightmost ...` > `Retry deployment`, that's it.
- Note that if you use your own subscription address, the `SUB` domain name of the subscription generator and the domain name of `[YOUR-PAGES-URL]` must not belong to the same top-level domain name, otherwise an exception will occur. You can assign the domain assigned to Pages.dev to the `SUB` variable.

</details>

# Variable description
| Variable name | Example | Required | Notes | YT |
|--------|---------|-|-----|-----|
| UUID | `90cd4a77-141a-43c9-991b-08263cfe9c10` |✅| Powershell -NoExit -Command "[guid]::NewGuid()"| [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=72s) |
| KEY | `token` |❌| Dynamic UUID key. When using variable `KEY`, variable `UUID` will no longer be enabled| |
| TIME | `7` |❌| Dynamic UUID validity period (unit: day)| |
| UPTIME | `3` |❌| Dynamic UUID update time (default: update at `3` Beijing time) | |
| PROXYIP | `proxyip.fxxk.dedyn.io:443` |❌| Alternative proxy node for accessing CFCDN sites (supports custom ProxyIP port, supports multiple ProxyIPs, and uses `,` or `newline` as a separator between ProxyIPs) | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=166s) |
| SOCKS5 | `user:password@127.0.0.1:1080` |❌| Prioritize as a SOCKS5 proxy for accessing CFCDN sites (supports multiple socks5, and uses `,` or `newline` as a separator between socks5) | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=826s) |
| GO2SOCKS5 | `blog.cmliussss.com`,`*.ip111.cn`,`*google.com` |❌| After setting the `SOCKS5` variable, you can set the mandatory use of socks5 access list (`*` can be used as a wildcard, `newline` as a multiple-element separator) ||
| ADD | `icook.tw:2053#Official preferred domain name` |❌| Local preferred TLS domain name/preferred IP (supports `,` or `newline` as separators between multiple elements) ||
| ADDAPI | [https://raw.github.../addressesapi.txt](https://raw.githubusercontent.com/cmliu/WorkerVless2sub/main/addressesapi.txt) |❌| Preferred IP API address (supports `,` or newline as separators between multiple elements) ||
| ADDNOTLS | `icook.hk:8080#Official preferred domain name` |❌| Local preferred noTLS domain name/preferred IP (supports `,` or `newline` as separator between multiple elements) ||
| ADDNOTLSAPI | [https://raw.github.../addressesapi.txt](https://raw.githubusercontent.com/cmliu/CFcdnVmess2sub/main/addressesapi.txt) |❌| API address of preferred IP (supports `,` or newline as separator between multiple elements) ||
| ADDCSV | [https://raw.github.../addressescsv.csv](https://raw.githubusercontent.com/cmliu/WorkerVless2sub/main/addressescsv.csv) |❌| iptest speed test results (supports multiple elements, `,` is used as separator between elements) ||
| DLS | `8` |❌| `ADDCSV` speed test results meet the speed limit ||
| TGTOKEN | `6894123456:XXXXXXXXXX0qExVsBPUhHDAbXXX` |❌| Robot token for sending TG notifications |
| TGID | `6946912345` |❌| Account digital ID for receiving TG notifications |
| SUB | `VLESS.fxxk.dedyn.io` | ❌ | Subscription generator address for built-in domain name and IP node information | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=1193s) |
| SUBAPI | `SUBAPI.fxxk.dedyn.io` |❌| Subscription conversion backend for clash, singbox, etc. | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=1446s) |
| SUBCONFIG | [https://raw.github.../ACL4SSR_Online_Full_MultiMode.ini](https://raw.githubusercontent.com/cmliu/ACL4SSR/main/Clash/config/ACL4SSR_Online_Full_MultiMode.ini) |❌| clash, singbox, etc. Subscription conversion configuration files | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=1605s) |
| SUBNAME | `edgetunnel` |❌| Subscription name | |
| RPROXYIP | `false` |❌| Set to true to force the acquisition of the ProxyIP assigned by the subscriber (subscriber support required) | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=1816s) |
| URL302 | `https://t.me/CMLiussss` |❌| Home page 302 redirect (supports multiple URLs, use `,` or `newline` as a separator between URLs, don't use it if you're new to this) | |
| URL | `https://blog.cmliussss.com` |❌| Home page anti-genuine camouflage (supports multiple URLs, use `,` or `newline` as a separator between URLs, random settings can easily trigger anti-fraud) | |
| CFEMAIL | `admin@gmail.com` |❌| CF account email (after filling in `CFKEY`, the subscription information will display the request usage, don't use it if you're new to this) | |
| CFKEY | `c6a944b5c956b6c18c2352880952bced8b85e` |❌| CF account Global API Key (after filling in `CFEMAIL`, the subscription information will display the request usage, don't use it if you're new to this) | |
| CFPORTS | `2053`,`2096`,`8443` |❌| CF account standard port list | |

**Note: `UUID` will no longer be enabled after filling in `KEY`! Please choose one of the two! ! ! **
1. After filling in `KEY`, the permanent subscription address is `https://[YOUR-URL]/[YOUR-KEY]`;
2. After filling in `KEY`, the temporary subscription address is `https://[YOUR-URL]/[YOUR-UUID]`;
3. The subscription usage time of **dynamic UUID** is **1** `TIME` valid time period;
4. The node usage time of **dynamic UUID** is **2** `TIME` valid time periods (that is, if the dynamic UUID expires, the node can continue to be used for one period, but the subscription cannot be updated);

**Note: After filling in `SOCKS5`, `PROXYIP` will no longer be enabled! Please choose one of the two! ! ! **

**Note: After filling in `SUB`, the subscription content generated by the `ADD*` class variable will no longer be enabled! Please choose one of the two! ! ! **

**Note: Filling in `CFEMAIL` and `CFKEY` at the same time will enable the display of request usage, but it is not recommended! There is no need to give a Worker project such high permissions! You are at your own risk! ! ! **

## Practical tips

**The subscription deployed by this project can quickly change the preferred subscription generator by adding the `sub` key value! **
> For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` is your universal adaptive subscription address

- Quickly change the subscription address of the subscriber to `VLESS.fxxk.dedyn.io`

```url
https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sub=VLESS.fxxk.dedyn.io
```

**The nodes deployed by this project can be accessed through the node PATH (path) method, use the specified `PROXYIP` or `SOCKS5`! ! ! **

- Example of specifying `PROXYIP`
```url
/proxyip=proxyip.fxxk.dedyn.io
/?proxyip=proxyip.fxxk.dedyn.io
/proxyip.fxxk.dedyn.io (only for domains starting with 'proxyip.')
```

- Example of specifying `SOCKS5`
```url
/socks5=user:password@127.0.0.1:1080
/?socks5=user:password@127.0.0.1:1080
/socks://dXNlcjpwYXNzd29yZA==@127.0.0.1:1080
/socks5://user:password@127.0.0.1:1080
```

**When your `ADDAPI` can be used as a `PROXYIP`, you can add `?proxyip=true` to the end of the `ADDAPI` variable, and then use the preferred IP itself as the `PROXYIP` when generating nodes**
- Specify `ADDAPI` as a `PROXYIP` example
```url
https://raw.githubusercontent.com/cmliu/WorkerVless2sub/main/addressesapi.txt?proxyip=true
```

## Star Stars Go
[![Stargazers over time](https://starchart.cc/cmliu/edgetunnel.svg?variant=adaptive)](https://starchart.cc/cmliu/edgetunnel)

## Adapted Clients
### Windows
- [v2rayN](https://github.com/2dust/v2rayN)
- clash.meta ([FlClash](https://github.com/chen08209/FlClash), [clash-verge-rev](https://github.com/clash-verge-rev/clash-verge-rev), [Clash Nyanpasu](https://github.com/keiko233/clash-nyanpasu)) ### IOS - Surge, little rocket - sing-box（[SFI](https://sing-box.sagernet.org/zh/clients/apple/)） ### Android - clash.meta ([ClashMetaForAndroid](https://github.com/MetaCubeX/ClashMetaForAndroid), [FlClash](https://github.com/chen08209/FlClash)) - sing-box ([SFA](https://github.com/SagerNet/sing-box)) ### MacOS - clash.meta（[FlClash](https://github.com/chen08209/FlClash)）

# grateful [zizifn](https://github.com/zizifn/edgetunnel), [3Kmfi6HP](https://github.com/3Kmfi6HP/EDtunnel), [Stanley-baby](https://github.com/Stanley-baby) ,[ACL4SSR](https://github.com/ACL4SSR/ACL4SSR/tree/master/Clash/config),[SHIJS1999](https://github.com/SHIJS1999/cloudflare-worker-vless-ip),<a href="https://url.cmliussss.com/alice"><img src="https://alicenetworks.net/templates/lagom2/assets/img/logo/logo_big.194980063.png" width="150" height="75" alt="Alice Networks LTD"/></a>,
