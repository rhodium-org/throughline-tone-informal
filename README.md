# throughline-tone-informal

The **informal register** of the **tone / register** content axis, expressed as a
[throughline](https://pypi.org/project/throughline/) **source** — a standalone,
grounded requirements graph that a consuming project composes with
[throughline-compose](https://github.com/rhodium-org/throughline-compose).

This repository holds no application code. It is a directory of small YAML items with
permanent UIDs, validated by `tl check`. Consumers import it under a namespace and
reference its rules as `tone:SR-0001` or its principles as `tone:UR-0001`.

## One orthogonal axis, one register

Tone is *how the writing sounds* relative to the reader relationship — distinct from
whether it is *understood* (readability) or *correctly spelled and punctuated*
(conventions). This source is **only** the tone axis, and **only** its **informal**
register: warm, personable and close to speech. It says nothing about:

- **readability** (word choice, sentence length, active voice) — `throughline-plain-language`
- **conventions** (spelling, punctuation, capitalisation, numbers) — `throughline-conventions-uk`
- **genre / purpose** (inform, instruct, persuade, negotiate)
- **medium / channel** (web page, email, microcopy, slide deck)
- **brand voice** (an organisation's own personality)

Registers are **mutually exclusive**: a piece of writing is formal *or* neutral *or*
informal, never several at once. So each register is a **sibling** source
(`throughline-tone-formal`, `throughline-tone-neutral`) and a consumer composes
exactly one under the `tone` namespace — swapping register is a one-line `url`/`ref`
change. A task like *"a plain, informal, UK-English community page"* becomes a
**compose** of `plain` + `conventions-uk` + `tone-informal`.

## What's in the graph

<!-- tl:count type == 'user_requirement' -->
5
<!-- tl:end --> principles as `user_requirement`s, each `derives_from` the root
intent, and
<!-- tl:count type == 'system_requirement' -->
11
<!-- tl:end --> rules as `system_requirement`s, each `implements` its principle. The
published spec is generated from the graph at [`docs/spec.md`](docs/spec.md).

## Source & licensing

The rules are original house tone guidance, licensed under Apache-2.0.
They reproduce no third-party standard. Each rule records its register and tone
dimension in `attrs.source_ref` and its owning principle in `attrs.principle`. See
[`NOTICE`](NOTICE).

## Extending the source

Items are hand-authored static YAML — one file per item, one permanent UID per file.
To add a rule, create the next `SR-00NN.yml` by hand (never renumber an existing one)
and link it with `implements` to its principle. Then:

```sh
tl check --strict      # the graph must stay sound
tl docs                # regenerate docs/spec.md + README.md
tl docs --check        # CI gate: docs must match the graph
```
