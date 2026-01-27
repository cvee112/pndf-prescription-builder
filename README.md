# 🇵🇭 PNDF Prescription Builder & Price Estimator

A web-based prescription builder for Philippine healthcare providers, featuring drugs from the **Philippine National Drug Formulary (PNDF)** with pricing from the **Drug Price Reference Index (DPRI) October 2025**.

![PNDF Prescription Builder](https://img.shields.io/badge/DPRI-October%202025-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Features

### 📋 Smart Prescription Building
- **Search 747+ PNDF drugs** with real-time autocomplete
- Automatic price lookup using highest DPRI reference prices
- Copy-paste ready prescription output format

### 💊 Intelligent Dosing Calculator
- **Fixed Dose Mode**: Direct mg/mL input
- **Weight-Based Dosing (mg/kg/dose)**: Per-dose calculation
- **Weight-Based Dosing (mg/kg/day)**: Daily dose with automatic division
- Automatic mL conversion for liquid formulations
- Automatic frequency inference (e.g., 4 doses → "every 6 hours")

### 👶 Pediatric Support
- Auto-detects pediatric patients (age < 18 years or in months)
- Weight-based dosing enabled by default
- Uses "Give" instead of "Take" in instructions

### 💰 Cost Estimation
- Real-time cost calculation per medication
- Automatic quantity computation from duration
- Accounts for bottle volumes for liquid medications
- Running total for entire prescription

### 🎨 Accessible Design
- Filipino-inspired color scheme (Philippine flag colors)
- High contrast for accessibility
- Mobile-responsive layout
- Collapsible medication cards for long prescriptions

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ 
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/pndf-prescription-builder.git
cd pndf-prescription-builder

# Install dependencies
npm install

# Start development server
npm run dev
```

The app will be available at `http://localhost:5173`

### Build for Production

```bash
npm run build
```

The built files will be in the `dist/` folder.

## 🌐 Deployment

### Vercel (Recommended)
1. Push to GitHub
2. Import project in [Vercel](https://vercel.com)
3. Deploy with default settings

### Netlify
1. Push to GitHub
2. Import in [Netlify](https://netlify.com)
3. Build command: `npm run build`
4. Publish directory: `dist`

### GitHub Pages
1. Update `vite.config.js`:
   ```js
   export default defineConfig({
     base: '/pndf-prescription-builder/',
     // ...
   })
   ```
2. Run `npm run build`
3. Deploy `dist/` folder to GitHub Pages

## 📊 Data Source

Drug data is sourced from the **Drug Price Reference Index (DPRI) October 2025**, published by the Department of Health (DOH) Philippines. The dataset includes:

- 747 drugs from the Philippine National Drug Formulary
- Lowest, Median, and Highest reference prices
- Concentration and formulation information

**Note:** This tool uses the **highest** DPRI price for cost estimation as a conservative reference.

## ⚠️ Disclaimer

This tool is for **reference and educational purposes only**. 

- Drug data is exclusively from the PNDF as listed in DPRI October 2025
- Prices shown are reference prices; actual pharmacy prices may vary
- Always verify prescriptions clinically before dispensing
- This tool does not replace professional medical judgment

## 🛠️ Tech Stack

- **React 18** - UI framework
- **Vite** - Build tool
- **Vanilla CSS** - Styling (no external CSS framework)

## 📁 Project Structure

```
pndf-prescription-builder/
├── index.html
├── package.json
├── vite.config.js
├── src/
│   ├── main.jsx
│   └── App.jsx        # Main application component with embedded drug data
└── README.md
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Department of Health (DOH) Philippines for the DPRI data
- Philippine National Drug Formulary (PNDF)
- Healthcare providers who inspired this tool

---

Made with 🇵🇭 for Filipino healthcare providers
