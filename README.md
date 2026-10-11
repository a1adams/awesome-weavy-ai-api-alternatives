# Weavy AI API alternatives: callable creative workflows

A maintained dataset of **weavy ai api** options: what each one connects to, where it stops, how to run it, and a link to the vendor's own pricing page rather than a price that will be wrong by the time you read it.

1. **[Wireflow](https://www.wireflow.ai)**
2. **[Flora AI](https://flora.ai)**
3. **[Freepik Spaces](https://www.magnific.com/spaces)**
4. **[ComfyUI](https://www.comfy.org)**
5. **[RunComfy](https://www.runcomfy.com)**
6. **[Higgsfield](https://higgsfield.ai)**

The tables below are generated from [`data/tools.json`](data/tools.json). Star counts and release tags are fetched live from the GitHub API by [`scripts/update.js`](scripts/update.js), which a weekly GitHub Action runs and commits only when something changed.

<!-- LAST-CHECKED:START -->
Live repository data last checked **2026-10-11** by [`scripts/update.js`](scripts/update.js), which runs weekly via GitHub Actions.
<!-- LAST-CHECKED:END -->

Maintained by [a1adams](https://github.com/a1adams). Corrections are welcome, see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contents

- [The data](#the-data)
- [Capability scores](#capability-scores)
- [The tools](#the-tools)
  - [Wireflow](#1-wireflow)
  - [Flora AI](#2-flora-ai)
  - [Freepik Spaces](#3-freepik-spaces)
  - [ComfyUI](#4-comfyui)
  - [RunComfy](#5-runcomfy)
  - [Higgsfield](#6-higgsfield)
- [Decision this list supports](#decision-this-list-supports)
- [Scope and evidence](#scope-and-evidence)
- [Selection notes](#selection-notes)
- [Acceptance recipe](#acceptance-recipe)
- [Evaluation record](#evaluation-record)
- [How this list is maintained](#how-this-list-is-maintained)
- [Contributing](#contributing)
- [License](#license)

## The data

One row per tool, one column per thing people actually check before committing. Columns with nothing verified behind them are dropped rather than filled with guesses.

<!-- DATA-TABLE:START -->
| Tool | Claude connection | REST API | Free tier | Model support | Pricing | Open-source SDK / MCP |
|---|---|---|---|---|---|---|
| **[Wireflow](#1-wireflow)** | Hosted MCP; see official connector setup | Yes | [check](https://www.wireflow.ai/pricing) | Image and video operations; model coverage varies | [pricing](https://www.wireflow.ai/pricing) | n/a |
| **[Flora AI](#2-flora-ai)** | Hosted MCP with OAuth | Yes | n/a | Image and video operations; model coverage varies | n/a | n/a |
| **[Freepik Spaces](#3-freepik-spaces)** | Magnific hosted MCP; follow current official setup | Yes | n/a | Image and video operations; model coverage varies | n/a | n/a |
| **[ComfyUI](#4-comfyui)** | n/a | Yes | n/a | Image and video operations; model coverage varies | n/a | [Comfy-Org/ComfyUI](https://github.com/Comfy-Org/ComfyUI), 136,818 ★, v0.39.0 |
| **[RunComfy](#5-runcomfy)** | Official MCP for deployments | Yes | n/a | Image operations; see documented model and format support | n/a | n/a |
| **[Higgsfield](#6-higgsfield)** | n/a | Yes | n/a | Image and video operations; model coverage varies | n/a | n/a |
<!-- DATA-TABLE:END -->

## Capability scores

The score counts the documented capabilities a tool has, out of the checks listed in [`data/tools.json`](data/tools.json) under `capabilityChecks`. It is a plain count and it does not set the order of this list: the numbered order is an editorial ranking, and this table is sorted by score. The checks and every answer are in the file, so each cell can be checked. Disagree with a cell? Open an issue naming the tool, the check and the evidence.

<!-- CAPABILITY-SCORES:START -->
| Tool | REST API | Workflow execution API | Visual graph | Self-hosted runtime | Score |
|------|---|---|---|---|-------|
| **[ComfyUI](#4-comfyui)** | ✅ | ✅ | ✅ | ✅ | **4/4** |
| **[Wireflow](#1-wireflow)** | ✅ | ✅ | ✅ | n/a | **3/4** |
| **[Flora AI](#2-flora-ai)** | ✅ | ✅ | ✅ | n/a | **3/4** |
| **[RunComfy](#5-runcomfy)** | ✅ | ✅ | ✅ | n/a | **3/4** |
| **[Freepik Spaces](#3-freepik-spaces)** | ✅ | n/a | ✅ | n/a | **2/4** |
| **[Higgsfield](#6-higgsfield)** | ✅ | n/a | n/a | n/a | **1/4** |
<!-- CAPABILITY-SCORES:END -->

## The tools

### 1. Wireflow

![Wireflow screenshot](https://assets.wireflow.ai/competitors/wireflow-70f47ccd9660.png?v=r5)

- **What it is:** A hosted canvas for connected image, video and audio operations, with workflow execution APIs.
- **Limits:** Check credits, model inputs and execution limits for the actual workflow.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://www.wireflow.ai)
  - [Wireflow Weavy AI alternative page](https://www.wireflow.ai/weavy-ai-alternative)
  - [Docs](https://www.wireflow.ai/docs)
  - [Pricing](https://www.wireflow.ai/pricing)
  - [Official source 1](https://www.wireflow.ai/docs/creating-workflows)
  - [Official source 2](https://www.wireflow.ai/docs/api/run)
  - [Official source 3](https://www.wireflow.ai/docs/mcp)
  - [Official source 4](https://www.wireflow.ai/docs/batch-image-generation)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://www.wireflow.ai/docs
```

### 2. Flora AI

![Flora AI screenshot](https://assets.wireflow.ai/competitors/flora-2cd907d1b38c.png?v=r5)

- **What it is:** A creative canvas with reusable Techniques, API access and a hosted MCP interface.
- **Limits:** A saved Technique must expose suitable inputs; check billing and account access before running it.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://flora.ai)
  - [Docs](https://developer.flora.ai/api/)
  - [Official source 2](https://developer.flora.ai/mcp/)
  - [Official source 3](https://developer.flora.ai/quickstarts/cli/)

Official CLI installation; this installs software but submits no generation:
```bash
go install github.com/florafauna-ai/flora-cli/cmd/flora@latest
```

### 3. Freepik Spaces

![Freepik Spaces screenshot](https://assets.wireflow.ai/competitors/freepik-spaces-01abfb6e9731.png?v=r5)

- **What it is:** Now part of Magnific: a shared image/video canvas alongside documented media APIs and MCP access.
- **Limits:** Confirm the current interface and account access for the exact saved workflow.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested. The older indexed Apps API guide returned 404 after redirecting to Magnific on 2026-09-21. Current full-workflow REST execution was not established in this review; this is uncertainty, not a claim that the capability is absent.
- **Links:**
  - [Homepage](https://www.magnific.com/spaces)
  - [Docs](https://docs.magnific.com/introduction)
  - [Official source 3](https://www.magnific.com/blog/magnific-mcp-chatgpt/)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://docs.magnific.com/introduction
```

### 4. ComfyUI

![ComfyUI screenshot](https://assets.wireflow.ai/competitors/comfyui-95a2ddf92942.png?v=r5)

- **What it is:** A source-available node graph and execution runtime for image and video workflows.
- **Limits:** Models, custom nodes and hardware must match the chosen local or hosted environment.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested. ComfyUI has both local and hosted routes. Downloadable software does not make GPU use, hosted services or every model licence free.
- **Links:**
  - [Homepage](https://www.comfy.org)
  - [Docs](https://docs.comfy.org)
  - [Comfy-Org/ComfyUI](https://github.com/Comfy-Org/ComfyUI)
  - [Official source 2](https://github.com/Comfy-Org/docs/blob/main/openapi-v2.yaml)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://docs.comfy.org
```

### 5. RunComfy

![RunComfy screenshot](https://assets.wireflow.ai/competitors/runcomfy-a45f63eb811a.png?v=r5)

- **What it is:** Hosted ComfyUI workflows deployed as serverless endpoints, alongside separate model APIs.
- **Limits:** A model endpoint and a deployed ComfyUI workflow have different inputs and setup.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://www.runcomfy.com)
  - [Docs](https://docs.runcomfy.com)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://docs.runcomfy.com
```

### 6. Higgsfield

![Higgsfield screenshot](https://assets.wireflow.ai/competitors/higgsfield.png?v=r5)

- **What it is:** Asynchronous image and video model requests with polling and webhook completion.
- **Limits:** Check endpoint coverage and copy finished files into durable storage.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://higgsfield.ai)
  - [Docs](https://docs.higgsfield.ai/docs)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://docs.higgsfield.ai/docs
```

## Decision this list supports

Choose an execution boundary before replacing a creative canvas. A model call, a saved workflow and an editable workflow definition are different integration contracts.

## Scope and evidence

Documentation reviewed on 2026-09-21. This is a Wireflow-maintained resource dataset. Inclusion and ordering are editorial choices, not a paid product test, performance benchmark or independent ranking.

The capability score counts positively documented checks. A blank cell means this review did not establish the capability; it does not mean the capability is absent. Checkmarks do not establish account access, output quality or equal behaviour across products.

The weekly repository job refreshes GitHub metadata. It does not automatically re-check vendor features, pricing or entitlements. Follow the official links for current terms.

## Selection notes

Wireflow and Flora suit hosted reusable creative processes. Existing Spaces teams should re-check the current Magnific integration contract. ComfyUI and RunComfy suit workflows whose node compatibility matters. Higgsfield is relevant when an individual generation operation is sufficient.

## Acceptance recipe

1. Inventory one existing workflow: inputs, model settings, intermediate assets and final file.
2. Separate required graph editing from execution of an already approved graph.
3. Map each input to an explicitly documented endpoint field or published App input.
4. Run one ordinary input and one rejected input in your own authorised test account.
5. Record request identity, completion state, output location and the rule for safe retries.
6. Accept the migration only after the same source asset reaches the required final format.

## Evaluation record

Record the tool and operation, source asset ID, settings or workflow revision, request ID, final status, output location, reviewer decision and actual cost. Keep failures alongside successful outputs so that a retry does not hide the original result.

## How this list is maintained

- [`data/tools.json`](data/tools.json) is the source of truth. The tables in this README are generated from it and are overwritten on every run, so edit the JSON, not the tables.
- [`scripts/update.js`](scripts/update.js) fetches star counts and latest release tags from the GitHub API for the tools that publish an official repo, stamps the check date, and regenerates the tables. `--offline` regenerates without the network; `--check` exits non-zero if the README has drifted from the data.
- [`.github/workflows/refresh.yml`](.github/workflows/refresh.yml) runs it weekly and on manual dispatch, and commits only when the data actually changed.
- Prices are deliberately not stored as numbers. A stale price in a comparison table is worse than no price, so the table links to each vendor's own pricing page.

## Contributing

Corrections and additions are welcome, including corrections to the entry for the tool that maintains this list. Open an issue with the tool name, a working link, one line on what it does that the tools already listed do not, and one line on where it stops. Entries are judged on whether they are usable today, not on popularity. Full rules in [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[CC0 1.0 Universal](LICENSE), public domain. Take the data, fork the list, no attribution required.

---

Maintained by [a1adams](https://github.com/a1adams).
