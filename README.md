<div align="center">

<img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=500&size=24&pause=1000&color=6B7280&center=true&vCenter=true&random=false&width=435&lines=tanmay+sinnarkar" alt="name" />

**data scientist · nyc**

*ranking systems · exploration problems · ml in production*

<br/>

[<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" height="25"/>](https://www.linkedin.com/in/tanmay-sinnarkar/)
&nbsp;
[<img src="https://img.shields.io/badge/email-%23EA4335.svg?&style=for-the-badge&logo=gmail&logoColor=white" height="25"/>](mailto:tanu.sinnarkar@gmail.com)

</div>

<br/>

## · what i work on ·

<table>
<tr>
<td width="55%">

```
    user finishes checkout
             │
             ▼
    ╭─────────────────╮
    │  which ad next? │
    ╰─────────────────╯
             │
             ▼
    somewhere here, our
    ranking system runs
             │
             ▼
    (harder than it sounds)
```

</td>
<td width="45%">

Ad ranking for post-transaction placements.

The interesting part isn't predicting clicks—it's everything around it: exploration vs exploitation, feedback loops, knowing when to retrain.

</td>
</tr>
</table>

<br/>

## · problems i find interesting ·

<table>
<tr>
<td width="50%">

### 🎰 exploration vs exploitation

new campaigns have no data. show them and risk revenue, or don't and never learn.

our team uses thompson sampling—balancing this is more art than science.

</td>
<td width="50%">

### 🔄 feedback loops

today's training data was shaped by yesterday's model. the ads users saw were already filtered.

untangling this is humbling.

</td>
</tr>
<tr>
<td width="50%">

### 🧹 boring > clever

spent weeks on fancy architectures. adding `local_hour_of_day` helped more.

simple features usually win.

</td>
<td width="50%">

### ⏱️ when to retrain

too often = chasing noise  
too rarely = drift

still iterating on this.

</td>
</tr>
</table>

<br/>

## · currently learning ·

<div align="center">

```
                    ╭──────────────────────────────────────────╮
                    │         where my head is at              │
                    ╰──────────────────────────────────────────╯
                                       │
          ┌────────────────────────────┼────────────────────────────┐
          │                            │                            │
          ▼                            ▼                            ▼
   ╭─────────────╮            ╭─────────────╮            ╭─────────────╮
   │  LLMs &     │            │   Causal    │            │  Online     │
   │  Gen AI     │            │  Inference  │            │  Learning   │
   ╰─────────────╯            ╰─────────────╯            ╰─────────────╯
          │                            │                            │
          ▼                            ▼                            ▼
    · prompt eng          · uplift modeling         · contextual bandits
    · RAG pipelines       · counterfactuals         · continuous adaptation
    · agents              · beyond A/B tests        · reward shaping
    · function calling
```

</div>

<br/>

<details>
<summary><b>📚 reading & experimenting</b></summary>

<br/>

<table>
<tr>
<td width="50%">

**on the nightstand**

```
◦ designing ml systems
  chip huyen

◦ causal inference in statistics  
  judea pearl

◦ bandit algorithms
  lattimore & szepesvári

◦ papers on llm evaluation
  & alignment
```

</td>
<td width="50%">

**hands-on lately**

```
◦ langchain / llamaindex
  for doc retrieval

◦ claude api
  for workflow tools

◦ llm-assisted debugging
  (asking ai why my model broke)

◦ small rag experiments
  on internal docs
```

</td>
</tr>
</table>

</details>

<br/>

## · lessons learned ·

<details>
<summary><b>on features</b></summary>

<br/>

```
    ✓ worked                              ✗ didn't
    ─────────────────────────             ─────────────────────────
    position (1 vs 4 is huge)             day of week (too noisy)
    local hour (not utc!)                 exact age (buckets better)
    campaign recency signals              most third-party enrichment
    state-level geo                       zip code (too sparse)
```

</details>

<details>
<summary><b>on systems</b></summary>

<br/>

```
    ◦ simple models + good features  >  complex models + mediocre features
    ◦ logging is the actual hard part
    ◦ "works on my machine" is a lifestyle
    ◦ most ml problems are data problems wearing a trench coat
```

</details>

<details>
<summary><b>on learning</b></summary>

<br/>

```
    ◦ reading papers is good, implementing is better
    ◦ the tutorial → production gap is where learning happens  
    ◦ explaining simply = understanding deeply
    ◦ staying curious > staying current
```

</details>

<br/>

## · tools ·

<div align="center">

<br/>

`python` · `pyspark` · `sql` · `xgboost` · `databricks` · `mlflow`

<br/>

<sub>exploring: `langchain` · `huggingface` · `anthropic/openai apis`</sub>

<br/>

</div>

<br/>

## · background ·

```
now         ╭────────────────────────────────────────────╮
  │         │  fluent · data scientist                   │
  │         │  ad ranking · exploration · ml systems     │
  │         ╰────────────────────────────────────────────╯
  │
  │         ╭────────────────────────────────────────────╮
2022        │  bed bath & beyond · data scientist        │
  │         │  targeting · store analytics · recs        │
  │         ╰────────────────────────────────────────────╯
  │
2018        ╭────────────────────────────────────────────╮
            │  stevens institute · ms information systems│
            ╰────────────────────────────────────────────╯
```

<br/>

## · outside work ·

<div align="center">

<table>
<tr>
<td align="center">
<br/>
☕<br/>
<sub>coffee</sub><br/>
<sub><sup>still chasing the</sup></sub><br/>
<sub><sup>perfect cortado</sup></sub>
<br/><br/>
</td>
<td align="center">
<br/>
🎬<br/>
<sub>films</sub><br/>
<sub><sup>narrative structure</sup></sub><br/>
<sub><sup>is just architecture</sup></sub>
<br/><br/>
</td>
<td align="center">
<br/>
📚<br/>
<sub>reading</sub><br/>
<sub><sup>ml papers, sci-fi,</sup></sub><br/>
<sub><sup>occasional philosophy</sup></sub>
<br/><br/>
</td>
<td align="center">
<br/>
🎤<br/>
<sub>singing</sub><br/>
<sub><sup>badly, but</sup></sub><br/>
<sub><sup>enthusiastically</sup></sub>
<br/><br/>
</td>
<td align="center">
<br/>
🗣️<br/>
<sub>languages</sub><br/>
<sub><sup>english · hindi</sup></sub><br/>
<sub><sup>marathi</sup></sub>
<br/><br/>
</td>
</tr>
</table>

</div>

<br/>

---

<div align="center">

<sub>happy to chat about ranking systems, bandits, llms, or coffee</sub>

</div>
