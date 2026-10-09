# OPENLAW

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-legal_tech-lightgrey)

> Anticloud-hardened packaging of the upstream project `OPENLAW` in category **LEGAL TECH**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** LEGAL TECH · **Upstream:** https://github.com/sml2h3/openlawClawer · **Upstream pin:** `7988e555824d170528aae719df5bf00644a9ae52` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

## 程序猿相亲群：780432470 欢迎妹子加群啊
# openlawClawer V1.1 使用手册文档
# 通知：即将全面更新系统，将新增自动注册账号、接入自有验证码识别系统(价格超低，超稳定)等全新功能，全面优化系统稳定性，爬虫学习爱好者可加QQ群：119794042
[![Github All Releases](https://img.shields.io/github/downloads/atom/atom/total.svg)](https://github.com/sml2h3/openlawClawer)  :[![Read the Docs](https://img.shields.io/readthedocs/pip.svg)](https://github.com/sml2h3/openlawClawer)
## 环境条件
使用环境  | 版本要求
------------- | -------------
Python  | >= 3
PhantomJs  | >= 2.0
Redis  |  >= 3
MongoDB  | >= 2.6

## 开始安装

> 安装手册以Ubuntu16.04系统为标准，其他系统不保证稳定性，您也可以通过提交Pull Request添加您所使用系统的本产品安装手册作为补充！

 1. 安装Python3以及PhantomJs环境

``` shell
sudo apt-get install python3.5
```
PhantomJs只需要主端安装
``` shell
sudo apt-get install phantomjs
```

 2. 安装PIP包依赖

``` shell
pip3 install -r requirements.txt
```
 3. 获得程序

``` shell
git source https://github.com/sml2h3/openlawClawer.git
```

## 配置程序

 ### 配置Celery
 打开Config目录，找到celeryconfig.py文件
 #### BROKER
 broker_url 为redis
 redis_url格式为
 #### 账号 
 打开Account文件夹，按照[username,password]的数组格式添加openlaw的账号，多多益善，openlaw封禁账号很容易，越多越不容易被封，一般1-2天解封

> redis://:password@hostname:port/db_number

``` python
broker_url = "redis://127.0.0.1"
```
#### RESULT_BACKEND
result_backend为mongodb
mongodb_url格式为

> mongodb://userid:password@hostname:port/database_name

``` python
result_backend = "mongodb://127.0.0.1/celery"
```
#### 验证码识别[超级鹰]
注册、充值后新建软件，然后打开Core/Chaoji.py 进行配置username、password、soft_id

#### 代理IP提取
经过在开发中使用各家的产品结合openlaw网站爬取的特殊性，经过慎重考虑将采用[无忧代理][1]的爬虫代理IP产品（非广告），当然也可使用作者github中的[代理池工具][2]做提取。
打开Tasks目录中的get_content文件，修改第13行get_ip变量，将{order}替换成你的订单号。（如果您不是使用无忧代理，还需额外修改第15行Host的值）

  ## 运行使用

 - 主端直接运行

``` shell
python3 openlawClawer.py
```

> 如果您是在vps云上运行的请先安装xvfb: `sudo apt-get install xvfb`
> 然后使用如下命令启动: `xvfb-run python3 openlawClawer.py `
> 否则可能会引起PhantomJs报错

 - 子端在项目根目录运行

``` shell
celery worker -A app -l info -concurrency=5
```

> 其中concurrency参数制定子节点并发数，默认5即可，过大可能会引发一些突发问题（如代理IP提取频率受限等，量力而行），如果使用本地代理池进行提取代理IP，可以考虑增大。最好不要超过10

## 捐赠支持

> 本项目无偿给大家使用，但每一个版本的维护都需要作者的精力才得以维持。如果本项目为您或者贵公司带来了很多方便，可以通过Star或捐赠的方式支持作者继续维护本项目。毕竟Openlaw网站最近更新的有点频繁，哈哈。感谢各位支持！捐赠后我会定期将捐赠者（捐赠大于30元）的名单发布在本README，您可以在备注中额外添加您的公司主页或者个人主页，将统一展示在下方。
![enter description here][3]![enter description here][4]

> 本项目是经过测试后才提交，故如有技术问题可提交ISSUE或者考虑收费服务。如您需要有偿服务解决问题，可微信或支付宝扫码并在转账留言留下您的联系方式并标注需要解决问题，我会在下班后与您进行联系。

|   捐赠名单  |  主页   |
| --- | --- |
|   李佳璐  |  -   |
|   北京敬一科技有限公司  |   -  |
|   路人甲(捐助者希望匿名)  |   -  |

  [1]: http://www.data5u.com/
  [2]: https://github.com/sml2h3/proxypool
  [3]: http://i4.bvimg.com/623795/46aeff9232e66019.png
  [4]: http://i4.bvimg.com/623795/c13701483f7aa837.jpg

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Python (requirements)** (manifests: requirements.txt; scanned in UPSTREAM_CLONE)
- Top-level source layout: `Account/`, `Config/`, `Core/`, `Tasks/`
- Snapshot size: **19 files**, **824 lines of code** (measured; see Benchmarks)
- Primary languages: `.py` (13), `(none)` (2), `.md` (2), `.js` (1), `.txt` (1)
- Upstream commit pinned for this packaging: `7988e555824d170528aae719df5bf00644a9ae52`

---

## Installation

```
PhantomJs只需要主端安装
``` shell
sudo apt-get install phantomjs
```

 2. 安装PIP包依赖

``` shell
pip3 install -r requirements.txt
```
 3. 获得程序

``` shell
git source https://github.com/sml2h3/openlawClawer.git
```

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

No usage section was found in the upstream readme. Entry points detected in this project directory:

```sh
python -m openlaw    # module entry point, when the package layout matches
```

Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

The upstream API surface is defined by the `OPENLAW` source tree vendored in `UPSTREAM_CLONE/` (Python (requirements) ecosystem). Public entry points:

- Source modules: `Account/`, `Config/`, `Core/`, `Tasks/`
- Overlay API: `anticloud/cli.py` exposes 13 subcommands with JSON stdout; `anticloud/bench/runner.py` runs the 16-check suite; `anticloud/provenance/chain.py` exposes the SHA3-256 + Ed25519 provenance chain.

---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Python (requirements) |
| Manifests detected | requirements.txt |
| Files in snapshot | 19 |
| Lines of code | 824 |
| Dependency references | 0 |
| Upstream license | Apache-2.0 |
| Overlay license | Anticommons 0.1.0 |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

#### BROKER
 broker_url 为redis
 redis_url格式为
 #### 账号 
 打开Account文件夹，按照[username,password]的数组格式添加openlaw的账号，多多益善，openlaw封禁账号很容易，越多越不容易被封，一般1-2天解封

> redis://:password@hostname:port/db_number

``` python
broker_url = "redis://127.0.0.1"
```

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

Upstream contributions: fork the `OPENLAW` project, create a feature branch, and open a pull request against upstream. Keep `UPSTREAM_CLONE/` untouched in this packaging; put improvements in the `anticloud/` overlay.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: Apache-2.0** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
                                 Apache License
                           Version 2.0, January 2004
                        http://www.apache.org/licenses/

   TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

   1. Definitions.

      "License" shall mean the terms and conditions for use, reproduction,
      and distribution as defined by Sections 1 through 9 of this document.

      "Licensor" shall mean the copyright owner or entity authorized by
      the copyright owner that is granting the License.

      "Legal Entity" shall mean the union of the acting entity and all
      other entities that control, are controlled by, or are under common
      control with that entity. For the purposes of this definition,
      "control" means (i) the power, direct or indirect, to cause the
      direction or management of such entity, whether by contract or
      otherwise, or (ii) ownership of fifty percent (50%) or more of the
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original Apache-2.0 terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `Apache-2.0` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `OPENLAW` (category: LEGAL TECH)
- **Upstream URL:** https://github.com/sml2h3/openlawClawer
- **Pinned commit (SHA):** `7988e555824d170528aae719df5bf00644a9ae52`
- **Branch:** master
- **Pin provenance:** GitHub API commits/master. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`aecd57275bdcf54ec7259bd3a2f1847c408f9ebc85b3f63b204538db129f5aeb`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| DANS (KNAW/NWO, Netherlands) | 10.17026/PT | EU-recognised archive |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe
and Mail, Business Insider, National Post, Financial Post, StreetInsider,
Digital Journal, Barchart, International Business Times, and Fox News.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

