<!-- Header -->
<div align="center">
  
```
 ████████╗ █████╗ ███╗   ██╗███╗   ███╗ █████╗ ██╗   ██╗
 ╚══██╔══╝██╔══██╗████╗  ██║████╗ ████║██╔══██╗╚██╗ ██╔╝
    ██║   ███████║██╔██╗ ██║██╔████╔██║███████║ ╚████╔╝ 
    ██║   ██╔══██║██║╚██╗██║██║╚██╔╝██║██╔══██║  ╚██╔╝  
    ██║   ██║  ██║██║ ╚████║██║ ╚═╝ ██║██║  ██║   ██║   
    ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═══╝╚═╝     ╚═╝╚═╝  ╚═╝   ╚═╝   
```

**Senior Data Scientist** · Building ML systems that make 50M+ decisions/day

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tanmay-sinnarkar/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:tanu.sinnarkar@gmail.com)
[![Location](https://img.shields.io/badge/NYC-FF6F00?style=for-the-badge&logo=google-maps&logoColor=white)]()

</div>

---

## The Problem I Solve

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                         │
│   User completes purchase                                               │
│            │                                                            │
│            ▼                                                            │
│   ┌─────────────────┐                                                   │
│   │  ~400ms window  │  ◄── This is where I live                        │
│   └─────────────────┘                                                   │
│            │                                                            │
│            ▼                                                            │
│   Show the right ad from 200+ campaigns                                 │
│            │                                                            │
│            ▼                                                            │
│   50M+ times per day                                                    │
│                                                                         │
└─────────────────────────────────────────────────────────────────────────┘
```

Get it wrong = wasted impression. Get it right = everyone wins.

---

## 🏗️ The System I Built

<table>
<tr>
<td width="50%">

### The Ranking Pipeline

```
                    ┌─────────────┐
   Session Data ───►│ Click Model │───► pCTR
                    │  (XGBoost)  │
                    └─────────────┘
                           │
                           │ parallel
                           │
                    ┌─────────────┐
   User Features ──►│ Conv Model  │───► pCVR
                    │  (XGBoost)  │
                    └─────────────┘
                           │
                           ▼
                    ┌─────────────┐
                    │   RANKER    │
                    │             │
                    │ RPI = pCTR  │
                    │    × bid    │
                    │ × (1-scrub) │
                    └─────────────┘
                           │
                           ▼
                    Sorted Creatives
```

</td>
<td width="50%">

### What Each Piece Does

**Click Model (pCTR)**
> *"Will this user engage?"*
> 
> 30+ features: demographics, behavior, context

**Conversion Model (pCVR)**
> *"Will they convert if they click?"*
> 
> Enables ML-driven bid pricing

**Ranker**
> *"Which creative maximizes value?"*
> 
> The equation that decides everything

Built from scratch. Took ownership from legacy platform. Now processes every ad decision.

</td>
</tr>
</table>

---

## 🔬 The Nerdy Details

<details>
<summary><b>📊 Feature Engineering (30+ signals)</b></summary>

```
┌──────────────────────────────────────────────────────────────┐
│                        FEATURE SPACE                         │
├──────────────────┬──────────────────┬───────────────────────┤
│   DEMOGRAPHIC    │    BEHAVIORAL    │      CONTEXTUAL       │
├──────────────────┼──────────────────┼───────────────────────┤
│ • Age            │ • Click history  │ • Hour of day         │
│ • Gender         │ • View recency   │ • Local hour          │
│ • Household $    │ • Campaign CTR   │ • Position (1-4)      │
│ • State (zip)    │ • Time since     │ • OS / Device         │
│ • Experian data  │   last action    │ • Creative ID         │
└──────────────────┴──────────────────┴───────────────────────┘
```

</details>

<details>
<summary><b>🔄 Model Evolution (8+ versions)</b></summary>

```
v1 ──► v2 ──► v3 ──► ... ──► v8
 │      │      │              │
 │      │      │              └─ Dynamic lookback windows
 │      │      └─ Geographic enrichment
 │      └─ Behavioral signals
 └─ Basic demographics

Each iteration: better features, lower log loss, same latency constraint
```

</details>

<details>
<summary><b>🎰 Exploration Framework (Thompson Sampling)</b></summary>

```
The Cold Start Problem:
━━━━━━━━━━━━━━━━━━━━━━━

New Campaign ──► No data ──► Show it anyway? ──► Risk revenue
                    │
                    └──► Don't show? ──► Never learn

Solution:
━━━━━━━━━

┌─────────────────────────────────────┐
│     Thompson Sampling + Bonuses     │
├─────────────────────────────────────┤
│  • Uncertainty quantification       │
│  • Recency weighting                │
│  • Trend detection                  │
│  • Fairness correction              │
│  • Creative refresh timing          │
└─────────────────────────────────────┘

Result: Find winners 3× faster while protecting baseline
```

</details>

---

## 🛠️ Tech Stack

<div align="center">

### Languages & ML
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat-square&logo=apache-spark&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)

### Frameworks
![XGBoost](https://img.shields.io/badge/XGBoost-337AB7?style=flat-square&logo=xgboost&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/sklearn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Prophet](https://img.shields.io/badge/Prophet-3B5998?style=flat-square&logo=meta&logoColor=white)

### Platforms
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta_Lake-00ADD8?style=flat-square&logo=delta&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=google-cloud&logoColor=white)

### Methods I Actually Use
```
Thompson Sampling · Multi-Armed Bandits · A/B Testing · Causal Inference · Time Series
```

</div>

---

## 📈 The Numbers

<div align="center">

| Metric | Value |
|:------:|:-----:|
| 💰 Revenue Impact | **$11M+** |
| 📊 Daily Impressions | **50M+** |
| 🎯 Campaigns Managed | **200+** |
| ⚡ Inference Latency | **<400ms** |
| 📈 RPS Improvement | **5.86%** |
| 🚀 Campaign Launch Speed | **3× faster** |

</div>

---

## 🕰️ Timeline

```
2024 ─────────────────────────────────────────────────────────► Present
  │
  ├── Ranker ownership (took over from Minion platform)
  ├── Conversion model → ML-driven bid pricing
  ├── Thompson Sampling framework
  ├── Audience Miner 2.0 (Databricks App)
  └── CI/CD pipeline for model deployment

2022 ─────────────────────────────────────────────────────────► 2024
  │
  ├── Click model v1 → v8 (built from scratch)
  ├── Feature engineering (30+ signals)
  ├── Session forecasting system
  └── A/B testing framework (50+ experiments/year)

2018 ─────────────────────────────────────────────────────────► 2022
  │
  └── Bed Bath & Beyond
      ├── Coupon propensity ($2-5M savings)
      ├── Store trade area analysis (800+ stores)
      └── Recommendation engine (50M+ transactions)
```

---

## 🧠 Currently Curious About

```diff
+ LLMs for ML debugging (talking to Claude about misbehaving models)
+ Feature stores that don't make you cry
! Whether causal inference can ever be simple (probably not)
- Overengineered solutions to simple problems (learning to avoid)
```

---

## ☕ Beyond the Terminal

<table>
<tr>
<td align="center" width="33%">
  
**Coffee**

```
   ( (
    ) )
  ........
  |      |]
  \      /
   `----'
```
Hunting NYC's<br/>best cortado

</td>
<td align="center" width="33%">

**Film**

```
  ┌───────────┐
  │ ▶ ││ ■ ◄◄ │
  └───────────┘
```
Analyzing narratives<br/>like ML architectures

</td>
<td align="center" width="33%">

**Languages**

```
  EN ████████░░
  HI ██████████
  MR ██████████
  PY ████████░░
```
Does Python count?

</td>
</tr>
</table>

---

<div align="center">

### Let's Talk

*Interested in production ML, exploration-exploitation tradeoffs,*
*or why your model works in staging but fails in prod.*

*Also coffee.*

---

<sub>If you're here from a recruiter search: yes, I know what a p-value is. No, I won't use one incorrectly.</sub>

</div>
