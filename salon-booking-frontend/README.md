# 🎨 Salon Booking System - Frontend (React)

Complete React.js frontend for the salon booking system with modern UI/UX.

## 🌟 Features

### User Features
- ✅ Beautiful, responsive design
- ✅ User authentication (Login/Register)
- ✅ Browse services with pricing
- ✅ Book appointments online
- ✅ View and manage appointments
- ✅ Cancel appointments
- ✅ Real-time status updates

### Admin Features
- ✅ Admin dashboard with statistics
- ✅ Manage services (Add/Edit/Delete)
- ✅ View all appointments
- ✅ Confirm/Complete appointments
- ✅ Revenue tracking

## 🚀 Quick Start

### Prerequisites
- Node.js (v14 or higher)
- Backend server running on http://localhost:5000

### Installation

1. **Navigate to frontend folder:**
```bash
cd frontend
```

2. **Install dependencies:**
```bash
npm install
```

3. **Configure environment:**
- Make sure `.env` file exists with:
```
REACT_APP_API_URL=http://localhost:5000/api
```

4. **Start the development server:**
```bash
npm start
```

The app will open at `http://localhost:3000`

## 📁 Project Structure

```
src/
├── components/
│   ├── Navbar.js              # Navigation bar
│   ├── Navbar.css
│   ├── Home.js                # Landing page
│   ├── Home.css
│   ├── Login.js               # Login page
│   ├── Register.js            # Registration page
│   ├── Auth.css               # Login/Register styles
│   ├── ServiceList.js         # Services catalog
│   ├── ServiceList.css
│   ├── BookAppointment.js     # Booking form
│   ├── BookAppointment.css
│   ├── AppointmentList.js     # User appointments
│   ├── AppointmentList.css
│   ├── AdminDashboard.js      # Admin panel
│   └── AdminDashboard.css
├── context/
│   └── AuthContext.js         # Authentication state
├── services/
│   └── api.js                 # API calls
├── App.js                     # Main app with routing
├── App.css                    # Global styles
├── index.js                   # Entry point
└── index.css                  # Base styles
```

## 🎯 Pages & Routes

| Route | Component | Access | Description |
|-------|-----------|--------|-------------|
| `/` | Home | Public | Landing page |
| `/login` | Login | Public | User login |
| `/register` | Register | Public | User registration |
| `/services` | ServiceList | Public | Browse services |
| `/book-appointment` | BookAppointment | Protected | Book appointment |
| `/appointments` | AppointmentList | Protected | User appointments |
| `/admin` | AdminDashboard | Admin Only | Admin panel |

## 🔐 Authentication Flow

1. **User Registration:**
   - Fill registration form
   - Backend creates user and returns JWT token
   - Token stored in localStorage
   - User redirected to home page

2. **User Login:**
   - Enter email and password
   - Backend validates and returns token
   - Token stored and user logged in

3. **Protected Routes:**
   - Check if user is authenticated
   - Redirect to login if not
   - Admin routes check admin role

## 🎨 Components Overview

### Navbar
- Responsive navigation
- Shows different options based on login status
- Role-based menu items

### Home
- Hero section with call-to-action
- Features showcase
- Services preview
- Welcome banner for logged-in users

### ServiceList
- Grid layout of all services
- Category icons
- Price and duration display
- Book now buttons

### BookAppointment
- Service selection
- Staff selection
- Date picker
- Time slot selection
- Auto-calculated end time
- Special notes field

### AppointmentList
- All user appointments
- Status badges (pending/confirmed/cancelled/completed)
- Cancel appointment option
- Responsive card layout

### AdminDashboard
- Statistics cards
- Services management table
- Add new services
- Delete services
- All appointments view
- Confirm/Complete appointments

## 🔧 API Integration

All API calls are centralized in `src/services/api.js`:

```javascript
// Authentication
authAPI.register(userData)
authAPI.login(credentials)
authAPI.getCurrentUser()

// Services
servicesAPI.getAll()
servicesAPI.create(serviceData)
servicesAPI.delete(id)

// Appointments
appointmentsAPI.getAll()
appointmentsAPI.create(appointmentData)
appointmentsAPI.update(id, data)
appointmentsAPI.cancel(id)
```

## 🎨 Styling

- **CSS Modules:** Component-specific styles
- **Color Scheme:** Purple gradient theme (#667eea to #764ba2)
- **Responsive:** Mobile-first design
- **Animations:** Smooth transitions and hover effects

### Main Colors:
```css
Primary: #667eea
Secondary: #764ba2
Success: #4caf50
Error: #f44336
Warning: #ffa500
```

## 🧪 Testing the Frontend

### 1. Test Registration
1. Go to `/register`
2. Fill in all fields
3. Click "Register"
4. Should redirect to home page logged in

### 2. Test Login
1. Go to `/login`
2. Use test credentials:
   - Email: john@example.com
   - Password: password123
3. Should login successfully

### 3. Test Services
1. Go to `/services`
2. Should see all services
3. Click "Book Now" (must be logged in)

### 4. Test Booking
1. Login first
2. Go to `/book-appointment`
3. Select service, staff, date, time
4. Submit form
5. Should redirect to appointments page

### 5. Test Admin
1. Login as admin (admin@salon.com / password123)
2. Go to `/admin`
3. Try adding a service
4. Try confirming an appointment

## 🐛 Troubleshooting

### Issue: "Network Error"
**Solution:** 
- Check if backend is running on port 5000
- Verify REACT_APP_API_URL in .env
- Check browser console for CORS errors

### Issue: "Cannot read property of undefined"
**Solution:**
- Check if backend returned expected data
- Verify API response structure matches code
- Add null checks: `appointment.service?.name`

### Issue: Routes not working
**Solution:**
- Make sure react-router-dom is installed
- Check Route paths match Link paths
- Verify BrowserRouter wraps Routes

### Issue: Authentication not persisting
**Solution:**
- Check localStorage has token
- Verify token is being sent in headers
- Check token expiration in backend

## 📱 Responsive Design

Breakpoints:
- Mobile: < 768px
- Tablet: 768px - 1024px
- Desktop: > 1024px

All components are fully responsive with:
- Flexible grid layouts
- Mobile-optimized navigation
- Touch-friendly buttons
- Readable text sizes

## ✨ Future Enhancements

- [ ] Email/SMS notifications
- [ ] Payment integration
- [ ] Calendar view for appointments
- [ ] Customer reviews
- [ ] Image upload for staff
- [ ] Real-time chat support
- [ ] Push notifications
- [ ] Dark mode

## 🔄 Available Scripts

```bash
# Start development server
npm start

# Build for production
npm run build

# Run tests
npm test

# Eject (one-way operation)
npm run eject
```

## 📦 Dependencies

```json
{
  "react": "^18.2.0",
  "react-dom": "^18.2.0",
  "react-router-dom": "^6.20.0",
  "axios": "^1.6.0",
  "react-scripts": "5.0.1"
}
```

## 🌐 Environment Variables

Create `.env` file in frontend root:

```env
REACT_APP_API_URL=http://localhost:5000/api
```

For production:
```env
REACT_APP_API_URL=https://your-backend-url.com/api
```

## 🚀 Deployment

### Build for production:
```bash
npm run build
```

This creates an optimized production build in the `build/` folder.

### Deploy to:
- **Netlify:** Drag and drop `build` folder
- **Vercel:** Connect GitHub repo
- **GitHub Pages:** Use `gh-pages` package
- **Firebase Hosting:** Use Firebase CLI

## 💡 Tips for Beginners

1. **Start with Login/Register**
   - Test authentication first
   - Make sure tokens work

2. **Use Browser DevTools**
   - F12 to open console
   - Check Network tab for API calls
   - View localStorage for tokens

3. **Component Development**
   - Build one component at a time
   - Test each component separately
   - Use console.log() to debug

4. **State Management**
   - Understand useState and useEffect
   - Learn about Context API
   - Practice with forms

## 📚 Learning Resources

- React Docs: https://react.dev/
- React Router: https://reactrouter.com/
- Axios: https://axios-http.com/
- CSS Grid: https://css-tricks.com/snippets/css/complete-guide-grid/

## 🆘 Common Errors

**Error:** "Module not found"
```bash
npm install
```

**Error:** "Port 3000 already in use"
```bash
# Kill process on port 3000
# Or start on different port:
PORT=3001 npm start
```

**Error:** "Failed to compile"
- Check syntax errors
- Missing imports
- Incorrect component names

## 🎓 Code Examples

### Making an API Call:
```javascript
const fetchServices = async () => {
  try {
    const response = await servicesAPI.getAll();
    setServices(response.data);
  } catch (error) {
    console.error('Error:', error);
  }
};
```

### Using Auth Context:
```javascript
const { user, isAuthenticated, logout } = useAuth();
```

### Protected Route:
```javascript
{isAuthenticated ? (
  <Link to="/appointments">My Appointments</Link>
) : (
  <Link to="/login">Login</Link>
)}
```

---

**Built with React ⚛️ for the Salon Booking System**

**Happy Coding! 🚀**
