# Smart Water Dispenser — Fitts' Law HCI Study

🔗 **[Try the Live Interactive Experiment Here](https://imasheaweed.github.io/water-dispenser-fitts-law/)**

---

## 📋 Scenario (The HCI Problem)
In daily life, these days people frequently multitask while using a water dispenser—such as holding a cup or bottle and also a smartphone or other things in other hand.  While many modern dispensers feature automatic cup detection sensors, yet users must still manually select settings like water temperature or confirm pouring. Because one hand is occupied, having small buttons placed high above or far from the cup placement area forces awkward hand reaches, increasing movement time ($MT$) and error rates.

---
## 📐 Fitts' Law Model & Custom Formula

### Theoretical Model
This experiment uses the Shannon formulation of Fitts' Law to calculate the Index of Difficulty ($ID$):

$$ID = \log_2\left(\frac{D}{W} + 1\right)$$

$$MT = a + b \cdot ID$$

*(Note: Replace **a** and **b** with your actual calculated numbers from your experimental data, e.g., $MT = 180 + 145 \cdot ID$.)*

---

## 📊 Experiment Parameters
- **Target Sizes ($W$):** 50px, 80px, 110px
- **Vertical Distances ($D$):** 100px, 150px, 200px, 300px
- **Data Collection:** Automated logging of 120 trials per participant with full CSV data export.
---
### 📊 Summary of Experimental Data
### 🎥 Demonstration
[Video Experiment Link](https://drive.google.com/file/d/1eVfIasHWV1cjwCF92E1LjUwwtHmGMnp1/view?usp=sharing)

| Condition | W (px) | D (px) | Index of Difficulty (ID) | Average Time (ms) | Total Misses | Error Rate (%) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| W110-D150 | 110 | 150 | 1.2410 | 793.34 | 1.00 | 10.00% |
| W110-D300 | 110 | 300 | 1.8981 | 773.18 | 1.00 | 10.00% |
| W80-D150 | 80 | 150 | 1.5236 | 835.41 | 1.00 | 10.00% |
| W110-D100 | 110 | 100 | 0.9329 | 624.23 | 0.00 | 0.00% |
| W80-D300 | 80 | 300 | 2.2479 | 1072.04 | 1.00 | 10.00% |
| W80-D100 | 80 | 100 | 1.1699 | 791.01 | 0.00 | 0.00% |
| W110-D200 | 110 | 200 | 1.4948 | 749.40 | 0.00 | 0.00% |
| W50-D300 | 50 | 300 | 2.8074 | 976.67 | 0.00 | 0.00% |
| W50-D200 | 50 | 200 | 2.3219 | 963.09 | 0.00 | 0.00% |
| W50-D150 | 50 | 150 | 2.0000 | 870.63 | 0.00 | 0.00% |
| W50-D100 | 50 | 100 | 1.5850 | 920.79 | 0.00 | 0.00% |
| W80-D200 | 80 | 200 | 1.8074 | 832.16 | 1.00 | 10.00% |

#### 📐 Regression Metrics
- **Slope ($b$):** $177.80$
- **Intercept ($a$):** $538.57$ 
- **$R^2$ (RSQ):** $0.6386$

Looking at the data from the 12 experimental conditions, there is a clear linear relationship between the Index of Difficulty ($ID$) and Movement Time ($MT$). 

Using linear regression ($y = mx + c$) to calculate the empirical Fitts' Law equation for this water dispenser interface:
$$MT = 538.57 + 177.80 \times ID$$

<p align="center">
  <img src="Scatter%20Plot%20Water%20Dispenser.png" alt="Fitts' Law Scatter Plot" width="600"/>
  <br>
  <em>Figure 1: Scatter plot showing Average Movement Time (ms) vs. Index of Difficulty (ID). Trendline equation: y = 177.8x + 538.57, with R² = 0.6386.</em>
</p>

#### Key Observations
Both target distance and button size had a clear impact on user performance. For instance, keeping the button size constant at $W = 110\text{ px}$, increasing the distance from $100\text{ px}$ to $300\text{ px}$ raised the index of difficulty from $0.93$ to $1.90\text{ bits}$, causing the average movement time to increase from $624.23\text{ ms}$ to $773.18\text{ ms}$. Similarly, shrinking the button size slowed down selection times significantly; at a fixed distance of $D = 300\text{ px}$, reducing $W$ from $110\text{ px}$ to $50\text{ px}$ increased difficulty to $2.81\text{ bits}$ and extended movement time to $976.67\text{ ms}$. We also observed $10\%$ error rates on conditions with smaller targets at longer distances ($W = 80\text{ px}$ and $W = 110\text{ px}$ at $D = 150\text{–}300\text{ px}$), which shows that single-handed operation suffers precision loss when targets are harder to reach

---

**####💡 Innovation - Design Implications for Smart Water Dispensers**

These results directly support our proposed layout for single-handed dispenser operation:

- **Warm & Cold Water Buttons:** 
  - **Design Choice:** Place these frequently used options **closer to the cup filling area ($D \downarrow$)** and make them **larger ($W \uparrow$)**.
  - **Why:** Keeping $ID \le 1.0\text{ bit}$ allows users to make quick selections (~$600\text{–}700\text{ ms}$) with $0\%$ errors, making it effortless when holding a bottle or phone in one hand.

- **Hot Water Button (Safety Design):**
  - **Design Choice:** Intentionally make the Hot Water button **smaller ($W \downarrow$)** and place it **higher up ($D \uparrow$)**.
  - **Why:** By intentionally raising difficulty to $2.5\text{–}3.0\text{ bits}$, selection time slows down to around ~$950\text{–}1000\text{ ms}$ and requires more focus. This deliberate delay acts as a built-in safety measure to prevent accidental scalding misclicks during single-handed use.


## 🚀 Application (Real-World Use Cases)
- **Accessible & Single-Handed Interfaces:** Enhancing interface usability for individuals with limited mobility, parents holding children, outpatients holding documents or users carrying items.
