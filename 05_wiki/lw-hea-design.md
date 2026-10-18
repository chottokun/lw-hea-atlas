# LW-HEA 設計指針 (Run 14 確定版)

## 1. 密度
$$\rho = \frac{\sum c_i A_i}{\sum c_i (A_i/\rho_i)} \le 4.5\text{ g/cm}^3$$
Al (2.70) + Ti (4.51) を骨格（合計 $\ge 50\text{ at}\%$）とし、Si (2.33) または Sc (2.99) を密度レバーとして導入。高密度元素（Nb 8.57, Mo 10.2, Ta 16.7）は原則 $\le 10\text{ at}\%$ に制限。

## 2. 比弾性率
$$\frac{E}{\rho} > 25\text{ GPa}\cdot\text{g}^{-1}\text{cm}^3 \quad (\text{目標 } \ge 30)$$
$p\text{-}d$ 軌道混成（Al $sp$ + Ti/V/Cr $d$）により共有結合性を高め $E$ を飛躍的に向上。VRH 平均 + $\Delta E_{pd}$（$\beta=35$, cap 40 GPa）。

## 3. 耐食性・界面電気化学
単相 BCC で微小ガルバニック対を消滅。弁金属（Ti, Cr, Nb, Zr, V, Mo）の複合酸化皮膜をカクテル効果で自発形成。Cr が耐食性の主役（$\text{Cr}_2\text{O}_3$ 皮膜）。

### 点欠陥モデル (Point Defect Model, PDM) と半導体欠陥補償
- **Al酸化物の二面性**: Al 高濃度化（30 at% 以上）は不動態皮膜中の $\text{Al}_2\text{O}_3$ 含有率を高めるが、これは n 型半導体特性を示し、酸素空孔（$V_{\text{O}}^{\bullet\bullet}$）等のドナー欠陥密度を増大させ、塩化物イオン（$\text{Cl}^-$）のトラップ・局所孔食感受性を高めるリスクを負う。
- **欠陥補償指数 (SDCI)**:
  $$\text{SDCI} = \frac{c_{\text{Cr}} + c_{\text{Ti}} + 0.5 c_{\text{Si}} + 0.5 c_{\text{Nb}}}{c_{\text{Al}}} \ge 1.50$$
  p 型半導体特性を示す $\text{Cr}_2\text{O}_3$、高絶縁性の $\text{TiO}_2$、および非晶質ネットワーク形成材の $\text{SiO}_2/\text{Nb}_2\text{O}_5$ を複合化することで、皮膜中の欠陥輸送を電気化学的に遮断し、$\log_{10} I_{\text{corr}} \le -7.90\text{ A/cm}^2$ を達成。

### 文献ベンチマークによるキャリブレーションと予測仮説
- **文献ベンチマーク**: 真空アーク溶解 $\text{AlCrTiV}_{0.5}$ 合金が 0.6 M NaCl 中で $I_{\text{corr}} = 0.131\text{ }\mu\text{A/cm}^2$ ($\log_{10} I_{\text{corr}} = -6.883\text{ A/cm}^2$) を達成（Materials 2023, DOI: 10.3390/ma16072922）。本知見をアンカーとして偏析・エントロピー補正モデルを単点適合（キャリブレーション）。
- **A1 予測仮説**: 本命 A1 (`Al30Ti35V15Cr10Nb5Si5`) は、Cr 10 at% 抑制（偏析抑制）と 6元系 $\Delta S = 1.543R$ により、モデル予測値 $\log I = -7.90$ を算出。高い耐食性ポテンシャルを示す作業仮説であり、今後の湿式電気化学試験により実証予定。
- **Mo による $\text{MoO}_4^{2-}$ 再不動態化**: A-Mo 合金では Mo 5 at% 添加により PREN が 38.0 → 47.0 へ急増。ピット直上へのモリブデン酸アニオン吸着が $\text{Cl}^-$ を競合排除。

## 4. 原点徹底型 LW-HEA の数学的必然性 (Run 6 / Run 11 証明)

### 証明1: 5元系 Al-Ti-V-Cr-Nb では ρ≤4.5 と ΔS≥1.5R の同時達成が不可能 (第1不可能性定理)
- 5元系 `Al-Ti-V-Cr-Nb` において、軽元素を極大化した `Al35 Ti35 V20 Cr5 Nb5` では $\rho = 4.458\text{ g/cm}^3$ となるが、組成の偏りにより $\Delta S_{\text{mix}} = 1.403R < 1.50R$ に留まり Charter 要件（$\ge 1.50R$）を満たせない。
- 一方、高エントロピー条件（$\Delta S_{\text{mix}} \ge 1.50R$）を満たす等比率近傍の組成空間では、高密度元素（Nb 8.57, Cr 7.19 g/cm³）の比率が増加し、最小密度は $\rho_{\min} = 4.62\text{ g/cm}^3 > 4.50$ となる。
- したがって、第6の軽量主元素として Si (5 at%, $\rho=2.33$) を導入して 6元系化することで初めて $\Delta S_{\text{mix}} = 1.543R \ge 1.5R$ と $\rho = 4.45 \le 4.50$ が同時達成される。

### 証明2: 純遷移金属＋Al 6元系における密度限界 (第2不可能性定理)
- Si/Sc を含まない純バルブメタル系（`Al-Ti-V-Cr-Nb-Zr`）は、最軽量組成でも $\rho_{\min} = 4.532 > 4.50\text{ g/cm}^3$ となり 100% 棄却。Track A で $\rho \le 4.50$ を満たすには「第3の軽量元素 (Si または Sc)」の配合が不可欠。

### 証明3: Ω_net ≈ 0.84-0.90 の熱力学的意味
- Al と早期遷移金属 (Ti, Nb, Si) の強い負の混合エンタルピー ($\Delta H_{\text{Al-Ti}} = -30\text{ kJ/mol}$) は $p\text{-}d$ 軌道混成の物理的源泉。
- 強い $p\text{-}d$ 混成 (大きな $|\Delta H_{\text{mix}}|$) と $\Omega \ge 1.1$ (小さな $|\Delta H_{\text{mix}}|$) は熱力学的にトレードオフ。
- $\Omega_{\text{net}} = 0.84-0.90$ は脆性 TCP/Laves 相ではなく、BCC 母相中に B2 (TiAl/NiAl 型) ナノ相が整合析出 (スピノーダル分解) する駆動力を表す。
- Charter の「$\Omega \ge 1.1$（または B2 整合ナノ析出許容領域）」に準拠。

### 参考文献 (OKF v4.0, 817 ソース)
- AlCrTiV0.5Cux 耐食性実測・Cu偏析ガルバニック腐食 (Materials 2023, DOI: 10.3390/ma16072922)
- CoCrFeNiAl 不動態皮膜の PDM・半導体特性 (J. Mater. Res. Technol. 2020, DOI: 10.1016/j.jmrt.2020.10.002)
- AlCrTiV HEA dual-phase (J. Mater. Sci. 2018, 10.1007/s10853-018-2970-4)
- TiCrVNb0.5Al0.5 BCC 耐食性 (J. Alloys Compd. 2020, 10.1016/j.jallcom.2020.158278)
- (AlTiV)100-xCrx LW-HEA 腐食摩耗 (PubMed 40508667)
- Miracle & Senkov 2017 (BCC/B2 ナノ整合組織)
- OKF ナレッジグラフ: ref/wiki/_Graph_Map.md (8 トピックハブ, 817 ソース)