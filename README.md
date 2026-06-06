# 💰 Loan Management System

A modern, user-friendly web application for managing and tracking loans with monthly payments and interest tracking.

## ✨ Features

- **Create Loans**: Add new loans with borrower details, amounts, and payment schedules
- **Track Payments**: Monitor monthly interest payments with checkbox tracking
- **Edit Loans**: Modify loan details including amount, interest rate, and status
- **Loan Summary**: View complete overview with loan amount, expected, received, and pending amounts
- **Status Management**: Change loan status between Active and Closed
- **Payment Tracking**: Auto-calculated total received and pending amounts
- **Local Storage**: All data is automatically saved in browser storage - no internet required after loading
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Beautiful UI**: Modern gradient design with smooth animations

## 📱 Application Structure

The app has three main tabs:

### 🏠 Home Tab
- View all loans in a card-based list view
- Select a loan to see detailed information
- View loan summary with financial breakdown
- Edit loan details
- Delete loans

### ➕ New Tab
- Create new loans with the following fields:
  - Borrower Name (required)
  - Loan Amount (required)
  - Monthly Interest (required)
  - Total Agreement Months (required)
  - Start Date (required)
  - Notes (optional)

### ⚙️ Settings Tab
- Learn about all features
- Quick reference guide for functionality

## 🚀 Getting Started

### Desktop Version
Open **`index.html`** in your web browser
- Full-featured desktop experience
- Optimized for larger screens
- All features available

### Mobile Version
Open **`mobile.html`** in your web browser
- Mobile-optimized interface
- Touch-friendly buttons and controls
- Perfect for on-the-go loan management
- Can be added to home screen (iOS & Android)

### Create Your First Loan
1. Click on the "➕ New" tab
2. Fill in all required fields
3. Click "✅ Create" button

### Track Payments
1. Go to "🏠 Home" tab
2. Click on a loan card to view details
3. Check boxes to mark monthly interest as received

### Manage Loans
- Edit borrower name, loan amount, interest rate, or notes
- Change loan status (Active/Closed)
- Delete loans permanently

## 💾 Data Storage

All data is stored locally in your browser using `localStorage`:
- **loans**: Array of loan objects
- **payments**: Array of payment tracking records

Data persists across browser sessions and requires no internet connection after first load.

## 🎨 Technology Stack

- **HTML5**: Structure and semantic markup
- **CSS3**: Responsive design with gradients and animations
- **Vanilla JavaScript**: No frameworks or dependencies

## 📊 Loan Object Structure

```javascript
{
  id: "LOAN_timestamp",
  borrowerName: "John Doe",
  loanAmount: 50000,
  monthlyInterest: 5000,
  numberOfMonths: 12,
  startDate: "2024-06-06",
  notes: "Notes about the loan",
  status: "Active", // or "Closed"
  totalExpected: 60000, // monthlyInterest * numberOfMonths
  totalReceived: 0,
  createdAt: "ISO timestamp"
}
```

## 📅 Payment Object Structure

```javascript
{
  id: "PAY_LOAN_ID_month",
  loanId: "LOAN_timestamp",
  month: 1,
  expectedAmount: 5000,
  collected: 0, // or expectedAmount if paid
  collectionDate: ""
}
```

## 🎯 Key Features Explained

### Monthly Payment Tracking
- Each loan automatically generates monthly payment records
- Check the checkbox when payment is received
- System auto-updates total received amount

### Loan Summary
- **Loan Amount**: Original loan principal
- **Total Expected**: Sum of all monthly interest payments
- **Received**: Total amount received so far
- **Pending**: Remaining amount to be collected

### Status Management
- **Active**: Loan is ongoing and can be edited
- **Closed**: Loan is completed and can be deleted

### Auto Calculation
- Total Expected = Monthly Interest × Number of Months
- Total Received = Sum of all checked monthly payments
- Pending = Total Expected - Total Received

## 📝 Usage Tips

1. **Start Date**: Set the date when the loan agreement begins
2. **Monthly Interest**: Enter the amount due each month
3. **Agreement Duration**: Specify how many months the loan will run
4. **Notes Field**: Add any special terms or reminders about the loan
5. **Payment Tracking**: Check boxes as you receive monthly payments

## 🔒 Data Security

- All data is stored locally in your browser
- No data is sent to any server
- You have complete control over your data
- Clear browser data will delete all loan records

## 🛠️ Customization

You can easily customize:
- Colors: Modify the gradient in CSS (`.header`, `.summary-card`)
- Currency: Change `₹` to your preferred currency symbol
- Font: Adjust `font-family` in the `body` CSS rule
- Layout: Modify grid and flex properties in CSS

## 📱 Browser Support

Works on all modern browsers:
- Chrome/Chromium
- Firefox
- Safari
- Edge
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📄 File Structure

```
loan-management-system/
├── index.html          # Desktop version
├── mobile.html         # Mobile-optimized version
├── README.md           # This file
└── .gitignore          # Git configuration
```

## 🎓 Learning Resources

This project demonstrates:
- HTML5 form handling
- CSS3 animations and gradients
- Vanilla JavaScript DOM manipulation
- Local Storage API usage
- Responsive design principles

## 👨‍💻 Author

Created by: Naveen Gowda

## 🤝 Contributing

Feel free to fork this repository and submit pull requests for any improvements.

## 📞 Support

For issues or questions, please create an issue in the repository.

---

**Made with ❤️ for managing loans efficiently**
