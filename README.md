# Smart Water Dispenser — Fitts' Law HCI Study

🔗 **[Try the Live Interactive Experiment Here](https://imasheaweed.github.io/water-dispenser-fitts-law/)**

---

## 📋 Scenario (The HCI Problem)
In daily life, people frequently multitask while using a water dispenser—such as holding a cup, bottle, or smartphone in one hand. Many modern dispensers feature automatic cup detection sensors, yet users must still manually select settings like water temperature or confirm pouring. Because one hand is occupied, having small buttons placed high above or far from the cup placement area forces awkward hand reaches, increasing movement time ($MT$) and error rates.

## 💡 Innovation (The Design Idea)
To solve this, we used Fitts' Law to evaluate and redesign the interface logic for single-handed dispenser operation. Instead of arbitrary button placement, our design innovation proposes bringing essential touch targets closer to the natural cup resting area (reducing distance $D$) and expanding the target contact zone (increasing width $W$). 

By simulating this interface in a web-based testing tool, we dynamically test 12 combinations of target size and vertical distance to scientifically identify the optimal layout for single-handed use.

## 🚀 Application (Real-World Use Cases)
- **Accessible & Single-Handed Interfaces:** Enhancing interface usability for individuals with limited mobility, parents holding children, or users carrying items.

---

## 📐 Fitts' Law Model & Custom Formula

### Theoretical Model
This experiment uses the Shannon formulation of Fitts' Law to calculate the Index of Difficulty ($ID$):

$$ID = \log_2\left(\frac{D}{W} + 1\right)$$

### Custom Empirical Formula
Based on regression analysis of our collected participant trial data, our empirically derived values for reaction/delay time ($a$) and movement speed penalty ($b$) yield the following predictive equation:

$$MT = a + b \cdot ID$$

*(Note: Replace **a** and **b** with your actual calculated numbers from your experimental data, e.g., $MT = 180 + 145 \cdot ID$.)*

---

## 📊 Experiment Parameters
- **Target Sizes ($W$):** 50px, 80px, 110px
- **Vertical Distances ($D$):** 100px, 150px, 200px, 300px
- **Data Collection:** Automated logging of 120 trials per participant with full CSV data export.
