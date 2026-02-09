# 🚀 FRONTEND QUICK START GUIDE

## ✅ Prerequisites Checklist

Before starting, make sure you have:
- [x] Node.js installed (v14+)
- [x] Backend server running on http://localhost:5000
- [x] npm installed (comes with Node.js)
- [x] VS Code or any code editor

## 📦 Step-by-Step Setup

### Step 1: Extract Files
Extract the `salon-booking-frontend` folder to your project directory.

### Step 2: Open in VS Code
```bash
cd salon-booking-frontend
code .
```

### Step 3: Install Dependencies
Open terminal in VS Code (Ctrl + `) and run:
```bash
npm install
```

**This will take 2-3 minutes. You should see:**
```
added 1500+ packages in 2m
```

### Step 4: Verify .env File
Make sure `.env` file exists with:
```
REACT_APP_API_URL=http://localhost:5000/api
```

### Step 5: Start the Server
```bash
npm start
```

**The browser should automatically open to:**
```
http://localhost:3000
```

## ✅ Verify It's Working

### 1. Homepage Loads
You should see:
- Purple gradient header
- "Welcome to Premium Salon" title
- Login and Register buttons

### 2. Test Navigation
Click around:
- Home
- Services
- Login
- Register

### 3. Try Logging In
Use test account:
- Email: `john@example.com`
- Password: `password123`

If login works, you should:
- See your name in navbar
- Have access to "My Appointments"
- Can book appointments

## 🎯 What Each File Does

```
salon-booking-frontend/
├── package.json           → Dependencies list
├── .env                   → Backend URL configuration
├── public/
│   └── index.html         → HTML template
└── src/
    ├── index.js           → React entry point
    ├── App.js             → Main app with routing
    ├── components/        → All UI components
    ├── context/           → Authentication state
    └── services/          → API calls to backend
```

## 🔧 Common Commands

```bash
# Start development server
npm start

# Stop the server
Ctrl + C

# Install new package
npm install package-name

# Clear cache and reinstall
rm -rf node_modules package-lock.json
npm install
```

## 🐛 Troubleshooting

### Problem: npm install fails
**Solution:**
```bash
# Try with legacy peer deps
npm install --legacy-peer-deps
```

### Problem: Port 3000 already in use
**Solution:**
```bash
# Option 1: Kill the process
# Windows: taskkill /F /IM node.exe
# Mac/Linux: killall node

# Option 2: Use different port
PORT=3001 npm start
```

### Problem: "Cannot connect to backend"
**Solution:**
1. Is backend running? Check http://localhost:5000
2. Is .env correct? Check REACT_APP_API_URL
3. CORS enabled in backend? (Already done in our code)

### Problem: Blank white page
**Solution:**
1. Check browser console (F12) for errors
2. Check terminal for compilation errors
3. Try: `rm -rf node_modules && npm install`

### Problem: Changes not showing
**Solution:**
1. Hard refresh: Ctrl + Shift + R
2. Clear browser cache
3. Restart npm start

## 📱 Test on Mobile

### Option 1: Same Network
1. Find your computer's IP address
   - Windows: `ipconfig`
   - Mac/Linux: `ifconfig`
2. Open on phone: `http://YOUR_IP:3000`

### Option 2: Chrome DevTools
1. F12 → Toggle device toolbar
2. Test different screen sizes

## 🎨 Customization Tips

### Change Colors:
Edit CSS files in `src/components/`
- Look for `#667eea` (purple)
- Replace with your color

### Add New Page:
1. Create `NewPage.js` in `components/`
2. Add route in `App.js`:
```javascript
<Route path="/new" element={<NewPage />} />
```
3. Add link in `Navbar.js`

### Modify Styles:
Each component has its own CSS file:
- `Navbar.css` → Navigation styling
- `Home.css` → Homepage styling
- `Auth.css` → Login/Register styling
- etc.

## 📊 Project Progress Tracker

### Basic Setup ✅
- [x] npm install completed
- [x] Server starts successfully
- [x] Homepage loads correctly

### Authentication ⏳
- [ ] Can register new user
- [ ] Can login successfully
- [ ] Can logout
- [ ] Token persists on refresh

### Services ⏳
- [ ] Services display correctly
- [ ] Can view service details
- [ ] Book button works

### Appointments ⏳
- [ ] Can create appointment
- [ ] Can view appointments
- [ ] Can cancel appointment
- [ ] Status updates work

### Admin ⏳
- [ ] Admin login works
- [ ] Can add services
- [ ] Can delete services
- [ ] Can manage appointments

## 🎓 Learning Path

### Day 1: Setup & Basics
- Install and run the app
- Explore the homepage
- Test login/register
- Understand file structure

### Day 2: Components
- Study each component file
- Understand how they work
- Try modifying text/colors
- Learn about props and state

### Day 3: Routing
- Understand React Router
- See how pages connect
- Try adding a new route
- Learn protected routes

### Day 4: API Integration
- Study api.js file
- Understand axios calls
- See how data flows
- Try adding a new API call

### Day 5: State Management
- Learn AuthContext
- Understand useState
- Learn useEffect
- Practice with forms

## 💡 Pro Tips

1. **Keep Backend Running**
   - Frontend needs backend to work
   - Run both simultaneously

2. **Use Browser DevTools**
   - F12 is your best friend
   - Check Console for errors
   - Check Network for API calls
   - Check Application → Local Storage for token

3. **Read Error Messages**
   - They tell you exactly what's wrong
   - Google the error if stuck
   - Check line numbers

4. **Save Often**
   - React auto-reloads on save
   - Ctrl + S after every change

5. **One Change at a Time**
   - Make small changes
   - Test immediately
   - Easier to find bugs

## 🆘 Getting Help

### Error in Terminal?
1. Read the error message
2. Check which file and line
3. Look for typos
4. Google the error

### Error in Browser?
1. Open console (F12)
2. Read the error
3. Click the error to see file
4. Fix and save

### Still Stuck?
1. Check README.md
2. Search Stack Overflow
3. Review the working example
4. Take a break and come back

## 🎯 Success Criteria

You know it's working when:

✅ npm start runs without errors
✅ Homepage loads in browser
✅ Can click around without errors
✅ Can login successfully
✅ Can see services
✅ Can book appointment
✅ Admin dashboard works

## 📞 Quick Reference

**Start Server:** `npm start`
**Stop Server:** `Ctrl + C`
**Backend URL:** `http://localhost:5000`
**Frontend URL:** `http://localhost:3000`
**Browser Console:** `F12`
**Save File:** `Ctrl + S`

---

## ⚡ Ready to Start?

1. ✅ Install dependencies: `npm install`
2. ✅ Start server: `npm start`
3. ✅ Open browser: `http://localhost:3000`
4. ✅ Start coding! 🚀

**You've got this! Happy coding! 🎉**

