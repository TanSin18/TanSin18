<div align="center">

<img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=500&size=24&pause=1000&color=6B7280&center=true&vCenter=true&random=false&width=435&lines=tanmay+sinnarkar" alt="name" />

**senior data scientist · nyc**

*ranking · audience optimization · ml in production*

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
   user completes a transaction
              │
              ▼
       ranker fires
              │
   ┌──────────┼──────────┐
   ▼          ▼          ▼
  pCTR    bid scale   diversity
  model   + segments   overrides
   │          │          │
   └──────────┼──────────┘
              ▼
       impression served
              │
              ▼
       (we learn from
        what happens)
```

</td>
<td width="45%">

ranking and audience systems for post-transaction ad placements at fluent.

the interesting part isn't predicting clicks — it's the loop around it. exploration vs. exploitation, keeping the ranker from collapsing into a few advertisers, figuring out what a placement is worth when the training data was shaped by yesterday's model.

</td>
</tr>
</table>

<br/>

## · what i've built ·

<table>
<tr>
<td width="50%">

### audience miner
fluent's first databricks app. decision trees over 87 experian attributes → converting segments + calibrated bids. day-long workflow → minutes. now wraps a llama 3.3 agent with a sql tool layer.

</td>
<td width="50%">

### diversity engine
post-ranker override system. structured exposure for non-tier-1 campaigns without bleeding revenue. position tolerances, segment-level quality gates, mlflow artifact loading.

</td>
</tr>
<tr>
<td width="50%">

### structural risk dashboard
15+ queries collapsed into one cte-based master query. tracks rpi distance, bid density, and tier-1 concentration with thresholds by placement.

</td>
<td width="50%">

### dynamic lookback v2
24 → 59 features in the click ranker. latency was the gate, not accuracy. held to 1.24× v1 baseline (p50 86ms).

</td>
</tr>
</table>

<br/>

## · interests ·

<table>
<tr>
<td width="50%">

### exploration vs exploitation
new campaigns have no data. setting the exploration *budget* — and measuring whether it's paying off — is the hard part.

</td>
<td width="50%">

### feedback loops
training data was filtered by yesterday's model. features look stationary; the distribution isn't.

</td>
</tr>
<tr>
<td width="50%">

### calibration > cleverness
well-calibrated model + thoughtful features beats complex model + mediocre inputs. `local_hour` (not utc) helped more than most architecture changes.

</td>
<td width="50%">

### structural limits
when one `bid_scale` compresses bids globally, per-segment pricing isn't really achievable without model-level changes.

</td>
</tr>
</table>

<br/>

## · stack ·

<div align="center">

<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" height="28"/>
<img src="https://img.shields.io/badge/Apache%20Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white" height="28"/>
<img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white" height="28"/>
<img src="https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white" height="28"/>
<img src="https://img.shields.io/badge/Delta%20Lake-00ADD4?style=for-the-badge&logo=delta&logoColor=white" height="28"/>
<img src="https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white" height="28"/>
<img src="https://img.shields.io/badge/XGBoost-006ACC?style=for-the-badge&logo=scikitlearn&logoColor=white" height="28"/>
<img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" height="28"/>

<br/><br/>

<sub>exploring</sub>

<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" height="24"/>
<img src="https://img.shields.io/badge/Anthropic%20API-D97757?style=for-the-badge&logo=anthropic&logoColor=white" height="24"/>
<img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" height="24"/>

</div>

<br/>

## · background ·

```
now    fluent · senior data scientist
       adflow commerce media · ranking, audience, ml systems

2022   bed bath & beyond · data scientist
       targeting, store analytics, recommendations

2018   stevens institute of technology · ms, information systems
       university of pune · be, computer science
```

<br/>

## · outside work ·

<div align="center">

coffee · films · book club · english / hindi / marathi

</div>

<br/>

---

<div align="center">

<sub>happy to talk ranking systems, bandits, or llms in production.</sub>

</div>
