# Asthma Risk Factor Analysis: Interaction Effects and Model Evaluation
# 喘息リスク因子の多変量解析とモデル評価

---

## 🇬🇧 English Section: Executive Summary

### 📊 Executive Summary
This project investigates the multifaceted risk factors associated with asthma diagnosis using multivariable logistic regression. By integrating statistical modeling in Python with interactive visualizations in Power BI, this analysis aims to inform strategic patient sampling for future clinical trials.

### 💡 Key Findings
*   **Potential Synergistic Effects:** The interaction plot revealed crossing trend lines between smoking habits and hay fever. Although the interaction term was not statistically significant ($p=0.170$), the adjusted odds ratio exceeding 1.0 suggests a targeted clinical hypothesis: the impact of allergies on asthma risk may vary significantly depending on smoking status.
*   **Model Performance & Limitations:** The model yielded an AUC of 0.556. While discriminative power is currently limited, this finding provides a critical, evidence-based rationale for incorporating higher-resolution environmental covariates (such as pollution exposure) in subsequent research phases.
*   **Strategic Impact:** The identified risk trends within specific subgroups (e.g., smokers with hay fever) offer a data-driven foundation for more efficient and strategic patient recruitment in future observational studies.
*   Asthma_Hay_Fever.pbix: An interactive dashboard built with Power BI.

### 🛠️ Methodology
*   **Statistical Modeling:** Multivariable logistic regression adjusting for age, BMI, and physical activity.
*   **Validation:** Rigorous multicollinearity checks using Variance Inflation Factor (VIF).
*   **Evaluation:** Receiver Operating Characteristic (ROC) curve and Area Under the Curve (AUC) analysis to assess model discrimination.
*   **Visualization:** Interactive interaction plots built in Power BI to bridge complex statistics with intuitive data storytelling.

---

## 🇯🇵 日本語セクション: プロジェクト概要 (IMRaD形式)

### 🔬 背景 (Introduction)
喘息の発症には、個人の属性や生活習慣、環境要因など、複雑な交絡因子が関与している。特に、気道に直接的な負荷を与える「喫煙」と、アレルギー反応である「花粉症」の複合的な影響を定量的に理解することは、より精緻なリスク評価と層別化において臨床的に重要である。

### 🎯 目的 (Objective)
多変量ロジスティック回帰モデルを用い、基本的な背景因子で調整した上で、喫煙習慣と花粉症の「交互作用（Interaction）」を評価する。また、ROC曲線およびAUCを用いて予測モデルとしての識別能を検証し、今後の臨床研究に向けた課題を抽出する。

### ⚙️ 手法 (Methods)
*   **解析モデル:** 年齢、BMI、身体活動量を共変量に含めた多変量ロジスティック回帰分析。
*   **統計的妥当性の確認:** VIF（分散拡大係数）を算出し、多重共線性の影響が排除されていることを確認。
*   **交互作用の可視化:** Pythonで算出した予測確率をPower BIに連携し、層別の交互作用プロットを作成。
*   **精度評価:** ROC曲線の描画およびAUCによるモデルの客観的評価。

### 📈 結果 (Results)
1.  **交互作用項の評価:** 喫煙と花粉症の交互作用項のP値は0.170であり、有意水準5%で統計的に有意な相乗効果は認められなかった。しかし、可視化されたプロットにおいては2本のトレンドラインが交差し、特定の条件下における非線形なリスク変動が観察された。
2.  **モデルの識別能:** 現行の変数を投入したモデルのAUCは0.556であった。
3.  Asthma_Hay_Fever.pbixはPower BIによるダッシュボードである。

### 🧠 考察 (Discussion)
統計的に有意な交互作用は確認されなかったものの、トレンドラインの交差は、喫煙習慣の有無によってアレルギー疾患が喘息リスクに与える影響が異なる可能性を示唆している。この知見は、次相の臨床試験において、リスク変動が顕著な層に焦点を当てる「戦略的サンプリング」の基礎資料として有用である。
また、AUCが0.556に留まったことは、既存の個人属性データのみでは喘息の病態を十分に説明できないという科学的事実を示している。今後は、大気汚染（Pollution Exposure）などの高解像度な環境データや、遺伝的素因といった未観測の交絡因子をモデルに組み込むことが必須の課題である。
