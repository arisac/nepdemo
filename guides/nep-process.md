---
title: NEP Process
weight: 21
description: How NEP is proccessed and status is changed during the process
---

{{< hint info >}}
This doc was originally from https://github.com/newtonproject/NEPs/wiki, and should be added to a NEP as reference.
{{< /hint >}}

## General NEP Flow

### Submit a NEP for the first time

**Draft** > `pr` > assign NEP number > JUDGE > `merge` > complete

{{< details "Flowchart" open>}}
{{<mermaid class="text-center">}}
graph TD
userDraft[NEP-X Draft] --> |PR to NEPs repo| DraftPR[NEP-X Draft]
DraftPR --> |Assign NEP number| Draft[NEP-N Draft]
Draft --> JUDGE{JUDGE}
JUDGE --> |pass| Merge[Merged to NEPs repo]
JUDGE --> |not pass| Draft
{{</mermaid >}}
{{< /details >}}

### Update a NEP Draft

**Draft** > `pr` > JUDGE > `merge` > complete

### Make a NEP Draft to NEP Final

**Draft** > `issue` > JUDGE > **Public Call** > **Final / Active** > complete

## NEP Status

### Flowchart

{{<mermaid class="text-center">}}
graph TD
WIP --> |PR| Draft
subgraph "NEP Review Process"
Draft --> Abandoned
Draft --> Rejected
Draft --> PublicCall[Public Call]
end

      PublicCall --> Draft
      PublicCall --> Final
      PublicCall --> Active

      subgraph "Status Change on Conditions"
        Final -->  Deferred
        Deferred --> Implemented
        Final -->  Implemented
        Implemented --> Replaced[Replaced / Superseded]
        Final -->  Replaced
      end

{{</mermaid >}}

<details><summary>General NEP Flow</summary>

## General NEP Flow

### 1. Submit a NEP for the first time

**Draft** > `pr` > assign NEP number > JUDGE > `merge` > complete

### 2. Update a NEP Draft

**Draft** > `pr` > JUDGE > `merge` > complete

### 3. Make a NEP Draft to NEP Final

**Draft** > `issue` > JUDGE > **Public Call** > **Final / Active** > complete

</details>

<details><summary>Status Flow</summary>

## Status Flow Chart

http://processon.com/chart_image/5e9edf235653bb6efc60d7e8.png the flow chart below is updated from time to time. the browser may display from browser/github cache instead the latest one. visit url to view the latest.
![status flow](https://processon.com/chart_image/5e9edf235653bb6efc60d7e8.png#update8)

</details>

<details><summary>Roles & Responsibilities</summary>

## Main responsibilities for each role during a NEP review

**Champion(Lead) & Authors**

- answer questions

**Bots**

- multiple bots may be required to perform different tasks with different permissions
- PR Format Check
  - check header
  - check format
  - check URLs
- Advanced Functions
  - NLP check (offensive words, non-sense descriptions etc.)
  - check required fields for each category & type
  - check forbidden assets
  - run code test
- Repo Maintenances
  - merge if passed bots & editor review
  - update NEPs TOC files after merge/status change
- Messenger/Notify
  - notify editors & review board members after merge/status change
- Webhooks
  - performing tasks for other services e.g. test bots/services, html formatter bots/services
  - notify newton website server to update NEPs list on website

**NEP Editors**

- check descriptions in each part
- check if duplicate
- check if not obey newton principle
- simple code check
- assign number

**Review Board**

- anything

**Public**

- anything

</details>

## First NEP Draft Review

Since a new NEP Draft is just a start and it may needs improvements later in the future updates.
We should help a new NEP to pass as easy as possible as long as it's not fundamentally incorrect.

As long as no Board Member says it's fundamentally incorrect. A 50% approval will result the NEP Draft goes into our NEPs repo.

Voting process for NEP approval should happen on NewChain:

For each vote to start, a NEP Editor should make a transaction to NEP New Address, indicates the topic for voting and end time.

For Board Members to vote, Members should make a transaction to NEP New Address, leaving their decisions in the transaction notes.

NEP Editors should count the vote and make the

## NEP Editors

The current NEP editors are:

| GitHub ID                                      | NEW Address                             |
| ---------------------------------------------- | --------------------------------------- |
| [@arisac](https://github.com/arisac)           | NEW182LTNoiufc9tiveZdno3HXH5yEmUURKUiac |
| [@liuyong5653](https://github.com/liuyong5653) | NEW182VbmZs3TyC268wz7Kq4Cznssv7WzRPDq7j |
| [@weixuefeng](https://github.com/weixuefeng)   | NEW182PdJBJoMnGAub6KJ6YrhSPHWrFE9RSBmGE |
| [@zhouxiqiao](https://github.com/zhouxiqiao)   | NEW182Vzd7pgjGjNCKVB7831yFCT5yuhSfRnfgA |

## Review Board

The current Review Board members are:

| Display Name | GitHub ID                                          | NEW Address                             |
| ------------ | -------------------------------------------------- | --------------------------------------- |
| Mr. Koo      | [@benkoo](https://github.com/benkoo)               | NEW182XacauX8woduncHaXTzNGCFnk7B15z34hi |
| Evan Liu     | [@evanliuchina](https://github.com/evanliuchina)   | NEW182Jqu3ok6ZnjkLAyhpSw9WEJXhEwUYX4jLR |
| Qu Jianwei   | [@i29](https://github.com/i29)                     | NEW182TpZToiXBk1SkR1bMJLUxguPxFsZciz123 |
| Jiang Tao    | [@jiangtao-tang](https://github.com/jiangtao-tang) | NEW182XmN8jkgnkW8rtu9jRriQJjnEBXSbZZuHJ |
| Lee Willson  | [@leewillson](https://github.com/leewillson)       | NEW182ZheiEbSBW3SbtETmXEgdG5X9GvFuLRun2 |
| VieYang      | [@VieYang](https://github.com/VieYang)             | NEW182bMUiAM1nXMjcwri8zNrgZftcnPJc1uVie |
| xiawu        | [@xiawu](https://github.com/xiawu)                 | NEW182Kt8siZGciPGBss3rg7GmJqfZ7CUafVUHH |
| Xu Jizhe     | [@xujizhe](https://github.com/xujizhe)             | unregistered                            |
| zqy15789     | [@zqy15789](https://github.com/zqy15789)           | NEW182EFjxZjxRJcfBdJBHEuMTYNsK7RLTFeiiJ |

## Reference

- [NEP/EIP/BIP/PEP Comparison](https://github.com/arisac/newton-general/blob/master/D-02.proposal-comparison.md)
