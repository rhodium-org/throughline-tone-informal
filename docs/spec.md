# Tone — Informal register — throughline source

This document is **generated from the graph** by `tl docs`; `tl docs --check` gates
it in CI. The prose headings are hand-owned — everything between `tl:*` markers is
injected from the YAML items, so the published spec can never drift from the graph.

This source is the **tone / register axis** for one register: **informal**. It governs
how the writing *sounds* relative to the reader relationship — not readability,
spelling, punctuation, genre, medium or brand voice, each of which is its own
throughline source. Register variants are mutually exclusive: **formal**, **neutral**
and **informal** are sibling sources and a consumer composes exactly one under the
`tone` namespace. Every principle is a `user_requirement`; every rule is a
`system_requirement` that `implements` its principle. The throughline UIDs are this
source's own and immutable — a consumer cites a rule as `tone:SR-0001`.

It carries
<!-- tl:count type == 'user_requirement' -->
5
<!-- tl:end --> principles and
<!-- tl:count type == 'system_requirement' -->
11
<!-- tl:end --> rules.

## Purpose

<!-- tl:item INT-0001 -->
**INT-0001 — Text sounds consistently warm and informal** — `intent`, status `approved`

> An informal register is warm, personable and close to speech. It suits community, lifestyle, consumer and internal-team writing, where a friendly, human voice builds rapport and the reader would find stiffness off-putting. This axis governs register — how the writing sounds relative to the reader relationship — not readability, spelling or punctuation, each of which is a separate source. Register variants are mutually exclusive: a consumer composes exactly one of the formal, neutral or informal sibling sources.

**source_ref**: TBS Tone — Informal register
<!-- tl:end -->

## 1. Contract freely, as people speak

<!-- tl:item UR-0001 -->
**UR-0001 — Contract freely, as people speak** — `user_requirement`, status `approved`

> Use contractions throughout so the writing sounds spoken.

*Derives from:* INT-0001

**source_ref**: TBS Tone — Informal register — Contractions
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0001' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0001 | system_requirement | approved | Use contractions throughout |
| SR-0002 | system_requirement | approved | Everyday shortenings are fine where they aid flow |
<!-- tl:end -->

## 2. Address the reader like a familiar peer

<!-- tl:item UR-0002 -->
**UR-0002 — Address the reader like a familiar peer** — `user_requirement`, status `approved`

> Be warm and personal in how you greet and name the reader.

*Derives from:* INT-0001

**source_ref**: TBS Tone — Informal register — Address and greeting
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0002' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0003 | system_requirement | approved | Open with a warm, casual greeting |
| SR-0004 | system_requirement | approved | Use the reader's first name naturally |
| SR-0011 | system_requirement | approved | Close with a warm, casual sign-off |
<!-- tl:end -->

## 3. Use warm, conversational vocabulary

<!-- tl:item UR-0003 -->
**UR-0003 — Use warm, conversational vocabulary** — `user_requirement`, status `approved`

> Everyday, expressive language is welcome where it aids connection.

*Derives from:* INT-0001

**source_ref**: TBS Tone — Informal register — Vocabulary register
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0003' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0005 | system_requirement | approved | Conversational words and common idiom are welcome |
| SR-0006 | system_requirement | approved | Expressive intensifiers are fine in moderation |
<!-- tl:end -->

## 4. Be direct but relaxed

<!-- tl:item UR-0004 -->
**UR-0004 — Be direct but relaxed** — `user_requirement`, status `approved`

> Give friendly, plain steers; asides are fine.

*Derives from:* INT-0001

**source_ref**: TBS Tone — Informal register — Directness
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0004' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0007 | system_requirement | approved | Use friendly imperatives and invitations |
| SR-0008 | system_requirement | approved | Rhetorical questions and asides are welcome |
<!-- tl:end -->

## 5. Be warm, personable and encouraging

<!-- tl:item UR-0005 -->
**UR-0005 — Be warm, personable and encouraging** — `user_requirement`, status `approved`

> Use genuine warmth, encouragement and gentle humour.

*Derives from:* INT-0001

**source_ref**: TBS Tone — Informal register — Warmth and social signals
<!-- tl:end -->

<!-- tl:table attrs.get('principle') == 'UR-0005' -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0009 | system_requirement | approved | Use warmth and encouragement freely |
| SR-0010 | system_requirement | approved | Gentle, inclusive humour is welcome |
<!-- tl:end -->
