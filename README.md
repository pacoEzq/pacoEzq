# Francisco Ezquerra Larrodé

**CFD engineer. Simulation automation, postprocessing, and making solver output legible to language models.**

Technical Community Manager at Siemens Digital Industries Software, working on the
Simcenter STAR-CCM+ user community and educational content. Over 25 years in
computational fluid dynamics, with a focus on simulation automation, user-solver
customization, and programming. Lately most of my writing sits at the point where
CFD meets large language models.

---

## The Simulation Capsule

A Simulation Capsule is a self-contained, token-budgeted distillation of a
simulation case, designed to be consumed by a language model.

A Simulation Capsule is to a CFD case what `llms.txt` is to a website.

The problem it addresses is mundane and everywhere. A finished CFD case is
gigabytes of cells, fields, reports and scenes. A language model reads a context
window. Handing the model a raw export wastes the budget on structure it cannot
use; handing it a screenshot throws away everything a number could have said. The
capsule is the artifact in between: a fixed directory of small files, each one an
answer to a question somebody would actually ask, all of it nondimensional by
default so the numbers mean the same thing in every case.

```
capsule_<alias>/
├── summary.json        global scalars
├── planes/             plane sections, CSV and image in pairs
├── samples.csv         importance-weighted volume sample
├── features.json       named flow features
├── views/              renders answering declared questions
├── diff/               image differences between capsules
├── run_macro.java      reproduction
├── manifest.json       seeds, colorbar ranges, versions
├── signals/            time series and spectra
├── modes/              POD and DMD decomposition
└── disclosure.json     what is safe to send outside
```

Specification, example capsules and tooling: **[simulation-capsule](https://github.com/pacoEzq/simulation-capsule)**

---

## Preparing CFD Output for Large Language Models

A ten-part tutorial series on the Simcenter community forum. Each part introduces
exactly one new idea, produces one concrete artifact, and uses a reference case
chosen so the technique reveals something the case would not otherwise show.
Recipes are Simcenter STAR-CCM+; the principles are solver-agnostic and
model-agnostic.

| # | Part | Reference case |
|---|------|----------------|
| 1 | [What Does an LLM Consume Well?](https://community.sw.siemens.com/s/question/0D5Vb00001OziUAKAZ/preparing-cfd-output-for-large-language-models-110-what-does-an-llm-consume-well) | mixed |
| 2 | [Global Anchoring, the Case Summary in 50 Scalars](https://community.sw.siemens.com/s/question/0D5Vb00001Q4J4rKAF/preparing-cfd-output-for-large-language-models-210-global-anchoring-the-case-summary-in-50-scalars) | NACA 0012 |
| 3 | [Sections and Planes, the CSV plus Image Pair](https://community.sw.siemens.com/s/question/0D5Vb00001QuRzDKAV/preparing-cfd-output-for-large-language-models-310-sections-and-planes-the-csv-plus-image-pair) | cube wake, Re 200 |
| 4 | [Volumetric Importance-Based Sampling](https://community.sw.siemens.com/s/question/0D5Vb00001RmgOaKAJ/preparing-cfd-output-for-large-language-models-410-volumetric-importancebased-sampling) | jet in crossflow |
| 5 | [Semantic Feature Extraction](https://community.sw.siemens.com/s/question/0D5Vb00001SkKCtKAN/preparing-cfd-output-for-large-language-models-510-semantic-feature-extraction) | delta wing |
| 6 | [Visualizations Designed for LLMs](https://community.sw.siemens.com/s/question/0D5Vb00001WjpY0KAJ/preparing-cfd-output-for-large-language-models-610-visualizations-designed-for-llms) | Ahmed body |
| 7 | Automation: the reproducible capsule | cube wake |
| 8 | Transient fields I: time as statistics | cylinder, Re 100 |
| 9 | Transient fields II: modes | cylinder, Re 100 |
| 10 | Confidentiality: what leaves the building | Ahmed body |

A parallel part covers case comparison by image differencing.

Parts 1 to 6 are published. The rest are in progress.

---

## Also on the Simcenter community forum

- [Making AI Understand Your CFD Simulations (Simcenter STAR-CCM+ to LLM)](https://community.sw.siemens.com/s/question/0D5Vb0000181bwjKAA/making-ai-understand-your-cfd-simulations-simcenter-starccm-llm)
- [Five Ways AI Can Review Your CFD Simulation Setup](https://community.sw.siemens.com/s/question/0D5Vb00001BCuhHKAT/five-ways-ai-can-review-your-cfd-simulation-setup-simcenter-starccm)
- [Simcenter STAR-CCM+ Macros with AI: the full series, six parts](https://community.sw.siemens.com/s/question/0D5Vb00001NTdzhKAD/simcenter-starccm-macros-with-ai-the-full-series-parts-1-to-6)
- [Simcenter STAR-CCM+ Custom Menus: the full series, ten parts](https://community.sw.siemens.com/s/question/0D5Vb00001Kl8z1KAB/simcenter-starccm-custom-menus-1010-branding-shipping-your-module)

## On the Simcenter blog

- [AI-accelerated CFD](https://blogs.sw.siemens.com/simcenter/ai-accelerated-cfd/)
- [The Simcenter CFD community](https://blogs.sw.siemens.com/simcenter/cfd-simcenter-community/)
- [Free CFD training](https://blogs.sw.siemens.com/simcenter/free-cfd-training/)

---

## About this account

Personal account. The tutorial series it accompanies is published on the Simcenter
community forum. Views are my own.
