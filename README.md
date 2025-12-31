# 💰 Personal Expense Tracker

A comprehensive personal finance management tool to track income, expenses, and visualize spending patterns. Take control of your finances with real-time statistics, category tracking, and interactive charts.

<img width="1239" height="998" alt="image" src="https://github.com/user-attachments/assets/3d28aa0f-fc30-4ac3-869b-7322fb8d171f" />

## ✨ Features

### Core Functionality
- **Income & Expense Tracking** - Record all financial transactions
- **Category Organization** - 8 predefined categories with emoji icons
- **Real-Time Statistics** - Live updates of income, expenses, balance, and monthly spending
- **Date Tracking** - Record when each transaction occurred
- **Detailed Descriptions** - Add notes about each transaction
- **Easy Management** - Add, view, and delete transactions effortlessly

### Visualization
- **Interactive Doughnut Chart** - Visual breakdown of expenses by category
- **Color-Coded Categories** - Easy identification at a glance
- **Monthly Overview** - Track current month spending separately

### Data Management
- **Persistent Storage** - Automatic saving to browser localStorage
- **Transaction History** - Scrollable list of all transactions
- **Filter Options** - View all, expenses only, or income only
- **Instant Updates** - Real-time recalculation of all metrics

## 🚀 Quick Start

### Local Setup
1. Download `expense-tracker.html`
2. Double-click to open in any web browser
3. Start adding your transactions!

### Online Hosting
Compatible with all static hosting services:
- GitHub Pages (free)
- Netlify (free tier available)
- Vercel (free for personal projects)
- CodePen (for demos)

## 💻 How to Use

### Adding a Transaction

1. **Select Type** - Choose "Expense" or "Income"
2. **Enter Description** - e.g., "Grocery shopping at Whole Foods"
3. **Enter Amount** - Input the dollar amount (accepts decimals)
4. **Choose Category** - Select from 8 categories:
   - 🍔 Food & Dining
   - 🚗 Transportation
   - 🛍️ Shopping
   - 🎬 Entertainment
   - 💡 Bills & Utilities
   - ⚕️ Healthcare
   - 💼 Salary
   - 📌 Other
5. **Select Date** - Defaults to today
6. **Click "Add Transaction"**

### Viewing Your Finances

**Summary Dashboard:**
- **Total Income** - All-time income (green)
- **Total Expenses** - All-time expenses (red)
- **Balance** - Income minus expenses (blue)
- **This Month** - Current month expenses only (purple)

**Transaction List:**
- Chronological order (newest first)
- Filter by type using dropdown
- Swipe or click to delete

**Category Chart:**
- Visual breakdown of expense distribution
- Hover for exact amounts
- Automatically updates with new transactions

### Managing Transactions

- **Delete** - Click the 🗑️ icon next to any transaction
- **Filter** - Use dropdown to show all, expenses, or income
- **Review** - Scroll through transaction history

## 📊 Understanding Your Data

### Categories Explained

| Category | Icon | Examples |
|----------|------|----------|
| Food & Dining | 🍔 | Restaurants, groceries, coffee shops |
| Transportation | 🚗 | Gas, car payments, public transit, Uber |
| Shopping | 🛍️ | Clothing, electronics, home goods |
| Entertainment | 🎬 | Movies, concerts, subscriptions, hobbies |
| Bills & Utilities | 💡 | Rent, electricity, internet, phone |
| Healthcare | ⚕️ | Doctor visits, prescriptions, insurance |
| Salary | 💼 | Paychecks, bonuses, freelance income |
| Other | 📌 | Miscellaneous expenses or income |

### Key Metrics

**Total Income**: Sum of all income transactions  
**Total Expenses**: Sum of all expense transactions  
**Balance**: Net worth change (Income - Expenses)  
**This Month**: Expenses for current calendar month only

## 🛠️ Technical Stack

**Front-End:**
- HTML5 (semantic markup)
- Tailwind CSS (utility-first styling via CDN)
- Vanilla JavaScript (ES6+)

**Data Visualization:**
- Chart.js (doughnut chart)

**Storage:**
- Browser localStorage API

**No backend required** - fully client-side application

## 🔧 Technical Implementation

### Data Structure
```javascript
{
  id: 1640000000000,           // Timestamp
  type: "expense",             // "expense" or "income"
  description: "Groceries",    // User description
  amount: 45.67,               // Number with decimals
  category: "food",            // Category key
  date: "2025-12-31"          // ISO date string
}
```

### Storage Strategy
- All transactions stored as JSON array in localStorage
- Automatic saving on every change
- No server calls needed
- Data persists across browser sessions

### Chart Implementation
- Uses Chart.js library
- Dynamically updates on transaction changes
- Aggregates expenses by category
- Responsive and interactive

## 🎨 Customization

### Adding New Categories
1. Add option to category select:
```html
<option value="newcat">🎨 New Category</option>
```

2. Add icon to categoryIcons object:
```javascript
const categoryIcons = {
  newcat: '🎨',
  // ... existing categories
};
```

3. Chart will automatically include new category

### Changing Colors
Modify Tailwind classes in summary cards:
```html
<!-- Income card -->
<div class="bg-white rounded-lg shadow p-4">
  <p class="text-green-600">Total Income</p>    <!-- Change green-600 -->
  <p class="text-3xl font-bold text-green-600">  <!-- Change green-600 -->
```

### Modifying Chart Colors
Update Chart.js backgroundColor array:
```javascript
backgroundColor: [
  '#EF4444',  // Red
  '#F59E0B',  // Amber
  '#10B981',  // Green
  // Add more colors
]
```

## 📱 Responsive Design

**Desktop (1024px+):**
- Three-column layout
- Large chart display
- Full statistics dashboard

**Tablet (768px-1023px):**
- Adaptive grid layout
- Readable transaction list
- Optimized chart size

**Mobile (<768px):**
- Single-column stack
- Touch-friendly buttons
- Scrollable transaction list

## 🎯 Use Cases

Perfect for:
- **Personal Budgeting** - Track daily spending
- **Monthly Planning** - Monitor expenses by month
- **Category Analysis** - Identify spending patterns
- **Income Tracking** - Record all income sources
- **Financial Goals** - Measure progress toward saving targets
- **Tax Preparation** - Organized transaction records

## 🚀 Performance

- **Fast Loading** - Lightweight HTML file
- **Instant Updates** - Real-time calculations
- **Smooth Animations** - CSS transitions
- **Efficient Storage** - Minimal localStorage usage
- **No API Calls** - Works offline

## 🔐 Privacy & Security

- ✅ All data stored locally
- ✅ No external servers
- ✅ No account required
- ✅ No data transmission
- ✅ Works completely offline
- ⚠️ Data tied to browser/device

**Note:** Clearing browser data will delete all transactions. Export important data before clearing cache.

## 📊 Sample Use Case

**Monthly Budget Tracking:**
1. Set monthly budget goal
2. Add all income at month start
3. Record expenses as they occur
4. Monitor "This Month" metric
5. Review category chart at month end
6. Adjust spending for next month

## 🐛 Troubleshooting

**Data not saving:**
- Ensure localStorage is enabled
- Check browser privacy settings
- Try different browser

**Chart not displaying:**
- Verify Chart.js CDN is loading
- Check browser console for errors
- Add at least one expense to generate chart

**Amounts showing incorrectly:**
- Use decimal point (.) not comma
- Enter numbers only (no $ symbol)
- Verify amount is greater than 0

## 📈 Future Enhancements

Potential features:
- [ ] Budget limits per category
- [ ] Recurring transactions
- [ ] Multiple accounts support
- [ ] Export to CSV/PDF
- [ ] Monthly/yearly reports
- [ ] Budget vs actual comparison
- [ ] Receipt photo uploads
- [ ] Multi-currency support
- [ ] Cloud sync option
- [ ] Spending trends analysis
- [ ] Bill reminders

## 🤝 Project Purpose

This project demonstrates:
- **Full CRUD Operations** - Create, Read, Update, Delete
- **Data Visualization** - Chart.js integration
- **State Management** - LocalStorage implementation
- **Responsive Design** - Mobile-first approach
- **UI/UX Design** - Intuitive financial interface
- **Real-World Application** - Solves actual user problems

## 📄 License

Open source and free for personal and educational use.

## 👤 Author

Built as a portfolio project showcasing full-stack web development capabilities and practical problem-solving skills.

## 🌟 Why This Project Stands Out

1. **Practical Utility** - Solves real financial tracking needs
2. **Visual Appeal** - Clean, modern interface
3. **Data Visualization** - Interactive charts
4. **Complete Feature Set** - Production-ready functionality
5. **No Dependencies** - Pure JavaScript implementation
6. **Responsive Design** - Works on all devices

---

**Take Control of Your Finances** 💰

*Track every dollar, understand your spending, achieve your financial goals.*
