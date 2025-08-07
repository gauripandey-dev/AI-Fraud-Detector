# AI Fraud Detection System

A modern, interactive web application that uses advanced algorithms to analyze and detect potentially fraudulent transactions in real-time. Built with React and featuring a cyberpunk-inspired UI with smooth animations and visual effects.

## ✨ Features

### 🔍 **Real-time Fraud Analysis**
- Advanced risk scoring algorithm
- Multi-factor analysis including amount, location, merchant type, and timing
- Instant risk assessment with detailed recommendations

### 🎨 **Modern Cyberpunk UI**
- Glassmorphism design elements
- Animated scanning effects and pulse glows
- Responsive grid layout with floating animations
- Dynamic color-coded risk indicators

### 📊 **Interactive Dashboard**
- Transaction input form with validation
- Real-time risk score visualization
- Recent transactions history
- Detailed analysis results panel

### 🚀 **Performance Features**
- Smooth animations and transitions
- Loading states with scanning effects
- Responsive design for all screen sizes
- No external dependencies (self-contained)

## 🏗️ Architecture

### **Frontend Technologies**
- **React 18**: Modern React with hooks for state management
- **Tailwind CSS**: Utility-first CSS framework via CDN
- **Babel Standalone**: In-browser JSX compilation
- **Custom CSS**: Advanced animations and glassmorphism effects

### **Risk Analysis Algorithm**
The fraud detection algorithm evaluates multiple factors:

1. **Transaction Amount Risk**
   - High amounts (>$5,000): +40 risk points
   - Medium amounts ($1,000-$5,000): +20 risk points
   - Low amounts ($500-$1,000): +10 risk points

2. **Location-based Risk**
   - Unknown locations: +30 risk points
   - Foreign locations: +25 risk points

3. **Merchant Type Risk**
   - Unknown merchants: +35 risk points
   - ATM transactions: +15 risk points

4. **Time-based Risk**
   - Late night transactions (11 PM - 5 AM): +15 risk points

5. **Card Pattern Analysis**
   - Incomplete card numbers: +20 risk points

### **Risk Classification**
- **HIGH RISK** (70-100%): Block transaction immediately
- **MEDIUM RISK** (40-69%): Requires additional verification
- **LOW RISK** (0-39%): Approve transaction

## 🚀 Getting Started

### **Prerequisites**
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No additional installations required

### **Installation**
1. **Download the HTML file**
   ```bash
   # Clone or download the project
   git clone [your-repo-url]
   cd ai-fraud-detection-system
   ```

2. **Open in browser**
   ```bash
   # Simply open the HTML file in any modern browser
   open index.html
   # or
   double-click the HTML file
   ```

### **Alternative Setup with Local Server**
```bash
# Using Python (recommended for local development)
python -m http.server 8000

# Using Node.js
npx http-server

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000`

## 📖 Usage Guide

### **Basic Transaction Analysis**

1. **Enter Transaction Details**
   - **Amount**: Enter the transaction amount in USD
   - **Location**: Specify transaction location (e.g., "New York", "Foreign", "Unknown")
   - **Merchant Type**: Select from dropdown (Retail, Restaurant, ATM, etc.)
   - **Card Number**: Enter the full card number or last 4 digits
   - **Transaction Time**: Set the transaction timestamp

2. **Run Analysis**
   - Click "ANALYZE FRAUD RISK" button
   - Watch the AI processing animation (3-second simulation)
   - Review the comprehensive risk assessment

3. **Interpret Results**
   - **Risk Score**: Percentage-based risk indicator (0-100%)
   - **Risk Level**: Color-coded classification (Low/Medium/High)
   - **Recommendation**: Action guidance (Approve/Verify/Block)
   - **Details**: Explanation of risk factors detected

### **Dashboard Features**

- **Recent Transactions**: View history of analyzed transactions
- **Real-time Updates**: New analyses automatically appear in history
- **Visual Indicators**: Color-coded risk levels throughout the interface

## 🎨 Customization

### **Styling Customization**
```css
/* Modify color scheme */
:root {
  --primary-cyan: #00f5ff;
  --primary-purple: #8b5cf6;
  --danger-red: #ff073a;
  --success-green: #39ff14;
}

/* Adjust animation speeds */
.animate-pulse-glow {
  animation-duration: 2s; /* Modify glow speed */
}

.scan-line {
  animation-duration: 3s; /* Modify scan speed */
}
```

### **Risk Algorithm Modification**
```javascript
// Adjust risk factors in calculateRiskScore function
const calculateRiskScore = (data) => {
  let score = 0;
  
  // Modify thresholds and weights
  const amount = parseFloat(data.amount) || 0;
  if (amount > 10000) score += 60; // Increase high-amount threshold
  // ... other modifications
  
  return Math.min(score, 100);
};
```

## 🔧 Technical Details

### **Performance Optimizations**
- CSS animations use `transform` and `opacity` for GPU acceleration
- React state management minimizes re-renders
- Efficient gradient and backdrop-filter usage
- Optimized loading states and transitions

### **Browser Compatibility**
- **Chrome**: Full support (recommended)
- **Firefox**: Full support
- **Safari**: Full support (iOS 14+)
- **Edge**: Full support
- **IE**: Not supported (uses modern CSS features)

### **Responsive Design**
- Mobile-first approach with Tailwind CSS
- Breakpoints: `sm` (640px), `md` (768px), `lg` (1024px), `xl` (1280px)
- Fluid typography and spacing
- Touch-friendly interactive elements

## 🧪 Testing

### **Manual Testing Scenarios**

1. **High Risk Transaction**
   ```
   Amount: $8000
   Location: Unknown
   Merchant: Unknown
   Time: 2:00 AM
   Expected: High risk (70%+)
   ```

2. **Medium Risk Transaction**
   ```
   Amount: $1500
   Location: New York
   Merchant: Electronics Store
   Time: 3:00 PM
   Expected: Medium risk (40-69%)
   ```

3. **Low Risk Transaction**
   ```
   Amount: $25
   Location: Local
   Merchant: Grocery Store
   Time: 12:00 PM
   Expected: Low risk (0-39%)
   ```

## 🤝 Contributing

### **Development Setup**
1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Make your changes
4. Test thoroughly across different browsers
5. Submit a pull request

### **Contribution Guidelines**
- Maintain the existing code style and structure
- Ensure responsive design compatibility
- Test animations across different devices
- Update documentation for new features
- Follow semantic versioning for releases

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **React Team**: For the amazing React library
- **Tailwind CSS**: For the comprehensive utility framework
- **Design Inspiration**: Cyberpunk and modern fintech aesthetics
- **Community**: For feedback and feature suggestions

## 📞 Support

For questions, issues, or feature requests:
- Create an issue in the GitHub repository
- Contact the development team
- Check the documentation for common solutions

---

**Built with ❤️ for modern fraud detection and prevention**