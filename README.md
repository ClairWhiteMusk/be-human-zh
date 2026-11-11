# stop-slop-zh

[English](#english) | 中文

本專案改編自 [Hardik Pandya](https://hvpandya.com) 的 [stop-slop](https://github.com/hardikpandya/stop-slop)，針對繁體中文（台灣用語）重寫。

這是一個給 Claude 用的技能（skill）。Claude 寫中文或改中文稿時會讀這份規則，刪掉常見的 AI 腔。

## 裡面寫了什麼

`SKILL.md` 一個檔案，分成六部分：

| 部分 | 內容 |
|------|------|
| 核心規則 | 九條寫作原則，例如刪套話、去翻譯腔、講具體的事 |
| 交稿前檢查 | 十三項檢查清單 |
| 評分 | 直接、節奏、信任、人味、密度，各 10 分，低於 35 分重改 |
| 要刪的詞句 | 開場白、總結語、摘要標籤、空洞強調、企業套話、連接詞 |
| 要避免的句型 | 對比公式、翻譯腔、排比、設問、沒有人的句子、標點 |
| 台灣用語與範例 | 中國用語對照表，六組改寫前後範例 |

## 會處理的常見用語

| 類型 | 例子 | 改法 |
|------|------|------|
| 開場白 | 「在當今…的時代」「值得注意的是」「眾所周知」 | 刪掉，從重點開始 |
| 總結語 | 「總而言之」「綜上所述」「希望這對你有幫助」 | 刪掉 |
| 摘要標籤 | 「一句話解釋」「一句話總結」 | 改成「內文大意」，寫出具體結論 |
| 空洞強調 | 「至關重要」「扮演著重要角色」「非常」「真正」 | 刪掉，或換成具體事實 |
| 企業套話 | 「賦能」「打造」「落地」「痛點」 | 換成平常的說法 |
| 對比公式 | 「不是 X，而是 Y」「不僅 X，更 Y」 | 直接講 Y |
| 翻譯腔 | 「進行討論」「做出決定」「被」字句 | 討論、決定，找出是誰做的 |
| 排比 | 「更快、更穩、更安全」 | 留一兩項 |
| 自問自答 | 「為什麼會這樣？因為…」 | 直接給答案 |
| 中國用語 | 質量、信息、視頻、默認 | 品質、資訊、影片、預設 |

改寫範例：

> 前：我們對這個方案進行了深入的討論，並做出了暫緩上線的決定。
>
> 後：我們討論後決定暫緩上線。

## 和原版的差異

原版的規則針對英文，有些搬到中文不適用。本版調整如下：

- **新增「翻譯腔」一節。** 處理「進行」「做出」「被」字句和連續的「的」。
- **新增「摘要標籤」規則。** 不用「一句話解釋」，改用「內文大意」，並要求內容講出具體結論、數字或建議。
- **新增台灣用語對照表。**
- **拿掉「刪除所有副詞」。** 改成只刪「非常」「十分」「真正」這類空洞的程度詞。
- **拿掉英文專屬規則。** 例如 Wh- 開頭句、-ly 結尾的字。
- **範例全部用中文重寫。**
- **把原版的四個檔案合併成一個。**

## 安裝

Claude Code：

```
git clone https://github.com/ClairWhiteMusk/be-human-zh.git ~/.claude/skills/stop-slop-zh
```

更新時在該資料夾執行 `git pull`。

Claude app：把這個 repo 的連結貼給 Claude，請它安裝。

## 授權

MIT。原作版權屬於 Hardik Pandya，見 [LICENSE](LICENSE)。

---

<a name="english"></a>

# stop-slop-zh (English)

This project adapts [stop-slop](https://github.com/hardikpandya/stop-slop) by [Hardik Pandya](https://hvpandya.com) for Traditional Chinese as written in Taiwan.

It is a skill for Claude. Claude reads these rules when it writes or edits Chinese text and removes common AI writing patterns.

## What it contains

One file, `SKILL.md`, in six parts:

| Part | Content |
|------|---------|
| Core rules | Nine writing principles, such as cutting filler and naming specifics |
| Pre-delivery checks | A thirteen-item checklist |
| Scoring | Directness, rhythm, trust, authenticity, density. Ten points each. Revise below 35. |
| Phrases to remove | Openers, closers, summary labels, empty emphasis, corporate jargon, connectives |
| Structures to avoid | Contrast formulas, translationese, parallel triplets, rhetorical questions, sentences with no actor, punctuation |
| Taiwan usage and examples | A table of Mainland terms with Taiwan equivalents, and six before/after rewrites |

## Phrases it handles

| Type | Examples | Fix |
|------|----------|-----|
| Openers | 「在當今…的時代」 (in today's era of...), 「值得注意的是」 (it is worth noting) | Delete. Start with the point. |
| Closers | 「總而言之」 (in conclusion), 「希望這對你有幫助」 (hope this helps) | Delete. |
| Summary labels | 「一句話解釋」 (explained in one sentence) | Use 「內文大意」 (gist) and state the conclusion. |
| Empty emphasis | 「至關重要」 (crucial), 「非常」 (very) | Delete, or give a fact. |
| Corporate jargon | 「賦能」 (empower), 「落地」 (land), 「痛點」 (pain point) | Use plain words. |
| Contrast formulas | 「不是 X，而是 Y」 (not X, but Y) | State Y. |
| Translationese | 「進行討論」 (conduct a discussion), passive 「被」 | Use the verb. Name the actor. |
| Triplets | 「更快、更穩、更安全」 (faster, steadier, safer) | Keep one or two. |
| Self-answered questions | 「為什麼會這樣？因為…」 (Why? Because...) | Give the answer. |
| Mainland terms | 質量, 信息, 視頻, 默認 | 品質, 資訊, 影片, 預設 |

## Changes from the original

The original targets English. Some rules do not carry over to Chinese. This version makes these changes:

- **Adds a translationese section.** It covers 「進行」, 「做出」, passive 「被」, and stacked 「的」.
- **Adds a summary-label rule.** It bans 「一句話解釋」, uses 「內文大意」, and requires a concrete conclusion, number, or recommendation.
- **Adds a Taiwan usage table.**
- **Drops "kill all adverbs".** It cuts empty intensifiers such as 「非常」 and 「真正」 and keeps other adverbs.
- **Drops English-only rules**, such as Wh- sentence starters and -ly words.
- **Rewrites every example in Chinese.**
- **Merges the original four files into one.**

## Install

Claude Code:

```
git clone https://github.com/ClairWhiteMusk/be-human-zh.git ~/.claude/skills/stop-slop-zh
```

Run `git pull` in that folder to update.

Claude app: paste this repo's link to Claude and ask it to install the skill.

## License

MIT. Hardik Pandya holds the copyright on the original work. See [LICENSE](LICENSE).
