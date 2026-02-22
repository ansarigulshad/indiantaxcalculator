# 🇮🇳 India Income Tax Calculator

A comprehensive web-based Income Tax Calculator for Indian taxpayers to calculate their tax liability for Financial Year 2024-25 (Assessment Year 2025-26).

![Income Tax Calculator](https://img.shields.io/badge/Tax%20Calculator-India-orange)
![HTML](https://img.shields.io/badge/HTML-5-red)
![CSS](https://img.shields.io/badge/CSS-3-blue)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow)

## 🌟 Features

### Multiple Income Sources
- **Salary Income** - With automatic standard deduction (₹50,000)
- **Business/Professional Income** - For self-employed individuals
- **House Property Income** - Rental income after deductions
- **Short-Term Capital Gains (STCG)** - From equity and other investments
- **Long-Term Capital Gains (LTCG)** - With ₹1 lakh exemption
- **Dividend Income** - From shares and mutual funds
- **Interest Income** - From savings, FD, and bonds
- **F&O Trading Income/Loss** - Futures & Options trading results

### Tax Regime Support
- ✅ **New Tax Regime** (Default for FY 2024-25)
  - Updated slabs with higher exemption limits
  - Rebate up to ₹25,000 for income up to ₹7 lakh
- ✅ **Old Tax Regime**
  - Support for all deductions (80C, 80D, etc.)
  - Rebate up to ₹12,500 for income up to ₹5 lakh

### Advanced Calculations
- ✅ F&O loss set-off against other income (except salary)
- ✅ Automatic surcharge calculation based on income slabs
- ✅ Health & Education Cess (4%)
- ✅ Different tax rates for different income types
- ✅ Real-time calculations as you type

### User Experience
- 🎨 Modern, responsive design
- 📱 Mobile-friendly interface
- 💡 Helpful tooltips for guidance
- 🔢 Indian currency formatting
- ⚡ Instant calculations without page reload

## 🚀 Live Demo

**[View Live Calculator](https://yourusername.github.io/india-tax-calculator/)**

## 📊 Tax Slabs (FY 2024-25)

### New Tax Regime
| Income Range | Tax Rate |
|--------------|----------|
| Up to ₹3,00,000 | 0% |
| ₹3,00,001 - ₹7,00,000 | 5% |
| ₹7,00,001 - ₹10,00,000 | 10% |
| ₹10,00,001 - ₹12,00,000 | 15% |
| ₹12,00,001 - ₹15,00,000 | 20% |
| Above ₹15,00,000 | 30% |

### Old Tax Regime
| Income Range | Tax Rate |
|--------------|----------|
| Up to ₹2,50,000 | 0% |
| ₹2,50,001 - ₹5,00,000 | 5% |
| ₹5,00,001 - ₹10,00,000 | 20% |
| Above ₹10,00,000 | 30% |

### Surcharge Rates
| Total Income | Surcharge Rate |
|--------------|----------------|
| Up to ₹50,00,000 | 0% |
| ₹50,00,001 - ₹1,00,00,000 | 10% |
| ₹1,00,00,001 - ₹2,00,00,000 | 15% |
| ₹2,00,00,001 - ₹5,00,00,000 | 25% |
| Above ₹5,00,00,000 | 37% |

## 🛠️ Installation & Setup

### Option 1: Direct Use
1. Download the `index.html` file
2. Open it in any modern web browser
3. Start calculating your taxes!

### Option 2: GitHub Pages Deployment

1. **Fork this repository**
   ```bash
   # Click the 'Fork' button on GitHub
   ```

2. **Clone your fork**
   ```bash
   git clone https://github.com/yourusername/india-tax-calculator.git
   cd india-tax-calculator
   ```

3. **Enable GitHub Pages**
   - Go to repository Settings
   - Navigate to Pages section
   - Select source: `main` branch
   - Save and wait for deployment

4. **Access your calculator**
   ```
   https://yourusername.github.io/india-tax-calculator/
   ```

### Option 3: Local Development

```bash
# Clone the repository
git clone https://github.com/yourusername/india-tax-calculator.git

# Navigate to directory
cd india-tax-calculator

# Open in browser (or use any local server)
# For Python 3
python -m http.server 8000

# For Node.js
npx serve

# Then visit http://localhost:8000
```

## 📖 Usage Guide

### Basic Steps

1. **Select Tax Regime**
   - Choose between New Tax Regime or Old Tax Regime
   - New regime is default for FY 2024-25

2. **Enter Income Details**
   - Fill in all applicable income sources
   - Enter amounts in Indian Rupees (₹)
   - Use 0 for income sources you don't have

3. **F&O Trading**
   - Enter **positive values** for profits (e.g., 50000)
   - Enter **negative values** for losses (e.g., -30000)
   - Losses will automatically offset other income (except salary)

4. **Deductions** (Old Regime Only)
   - Enter total deductions under 80C, 80D, etc.
   - This field is only applicable for Old Tax Regime

5. **View Results**
   - Tax calculation updates automatically
   - Review detailed breakdown of all components
   - See final tax payable amount

### Example Scenarios

#### Scenario 1: Salaried Employee with Investments
```
Tax Regime: New Tax Regime
Salary: ₹12,00,000
LTCG: ₹2,00,000
Dividend: ₹50,000
```
**Result:** Tax breakdown with standard deduction, LTCG exemption applied

#### Scenario 2: Trader with F&O Loss
```
Tax Regime: New Tax Regime
Salary: ₹8,00,000
STCG: ₹1,50,000
F&O Trading Income/Loss: -50,000
```
**Result:** F&O loss offsets STCG, reducing taxable income

#### Scenario 3: Old Regime with Deductions
```
Tax Regime: Old Tax Regime
Salary: ₹10,00,000
Interest: ₹1,00,000
Deductions: ₹1,50,000
```
**Result:** Deductions reduce taxable income in old regime

## 🧮 Calculation Logic

### Income Computation
1. **Gross Total Income** = Sum of all income sources
2. **Standard Deduction** = ₹50,000 (from salary)
3. **Other Deductions** = 80C, 80D, etc. (Old Regime only)
4. **F&O Loss Set-off** = Against non-salary income only

### Tax Calculation
1. **Base Tax** = Calculated as per slab rates
2. **Special Rates**:
   - STCG: 20%
   - LTCG: 10% (on amount above ₹1 lakh)
3. **Surcharge** = Based on total income
4. **Health & Education Cess** = 4% on (Tax + Surcharge)
5. **Rebate** = If applicable based on income limit
6. **Final Tax** = Base Tax + Surcharge + Cess - Rebate

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/YourFeature
   ```
3. **Commit your changes**
   ```bash
   git commit -m "Add some feature"
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/YourFeature
   ```
5. **Open a Pull Request**

### Ideas for Contribution
- Add TDS calculator
- Include section 24 calculations for home loan interest
- Add comparison between old and new regime
- Export tax calculation as PDF
- Add more detailed tooltips
- Tax saving suggestions

## 📝 Disclaimer

**Important Notice:**

- This calculator is for **educational and estimation purposes only**
- Tax laws are subject to change; always verify with latest rules
- For accurate tax filing, consult a qualified Chartered Accountant (CA)
- The developer is not responsible for any financial decisions based on this calculator
- This tool does not constitute financial or legal advice

## 🐛 Known Limitations

- Does not handle all edge cases of income tax law
- Does not include agricultural income calculations
- Does not calculate advance tax or TDS
- Does not handle loss carry forward from previous years
- Simplified calculation for capital gains (doesn't differentiate between equity/debt/real estate)


## 👨‍💻 Author

**Gulshad**

- GitHub: [@gulshadansari](https://github.com/ansarigulshad/)
- Project Link: [indiantaxcalculator](https://ansarigulshad.github.io/indiantaxcalculator/)
