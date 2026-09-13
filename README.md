# Weather Dashboard

A responsive, real-time weather dashboard that fetches data from the OpenWeatherMap API. Display current weather, hourly forecasts, 5-day forecasts, and detailed weather metrics.

## ✨ Features

🌡️ **Current Weather Display**
- Real-time temperature, weather conditions, and location
- Weather emoji icons
- Feels-like temperature
- Wind speed and humidity at a glance

⏱️ **Hourly Forecast**
- Next 24 hours of weather predictions
- Hourly temperature and conditions
- Interactive hover effects

📅 **5-Day Forecast**
- Daily weather predictions
- High/low temperatures
- Weather descriptions and icons

📊 **Detailed Weather Information**
- Feels-like temperature
- Humidity percentage
- Wind speed (km/h)
- Atmospheric pressure (hPa)
- UV index
- Visibility distance (km)

🌍 **Location Features**
- Search weather by city name
- Geolocation support (use your current location)
- Display city name and country code
- Real-time data updates

🎨 **Responsive Design**
- Works on desktop, tablet, and mobile
- Modern gradient backgrounds
- Smooth animations and transitions
- Interactive hover effects on cards
- Mobile-optimized layout

## 🚀 Quick Start

### 1. Get Your API Key

1. Visit [OpenWeatherMap API](https://openweathermap.org/api)
2. Sign up for a free account
3. Generate a free API key (includes access to current weather and forecasts)
4. Copy your API key

### 2. Configure the Application

1. Open `app.js`
2. Find this line:
   ```javascript
   const API_KEY = 'YOUR_API_KEY_HERE';
   ```
3. Replace `YOUR_API_KEY_HERE` with your actual API key:
   ```javascript
   const API_KEY = 'abc123def456ghi789jkl';
   ```

### 3. Run the Application

#### Option A: Direct File
Simply open `index.html` in your web browser

#### Option B: Local Server
```bash
# Using Python 3
python -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js (with http-server)
npx http-server
```

Then navigate to `http://localhost:8000`

## 📖 Usage

### Search by City
- Type a city name in the search box
- Click "Search" or press Enter
- Weather data updates automatically

### Use Your Location
- Click the 📍 button to get weather for your current location
- Your browser will ask for location permission
- Grant permission to fetch local weather

### View Forecasts
- Scroll down to see hourly and daily forecasts
- Hover over cards for interactive effects
- View detailed weather metrics below

## 🔌 API Endpoints Used

This dashboard uses the OpenWeatherMap API with these endpoints:

1. **Current Weather**
   ```
   GET /weather?q={city}&units=metric&appid={API_KEY}
   ```

2. **One Call API** (Hourly & Daily Forecasts)
   ```
   GET /onecall?lat={lat}&lon={lon}&units=metric&exclude=minutely,alerts&appid={API_KEY}
   ```

## 📋 Free API Tier Limitations

The free OpenWeatherMap API includes:
- ✅ Current weather data
- ✅ 5-day forecast
- ✅ Hourly data
- ⏱️ 60 calls/minute limit
- 📊 1,000 calls/day limit

For higher usage, consider upgrading to a paid plan.

## 🌐 Browser Compatibility

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)

### Geolocation Support
- Available in all modern browsers
- Requires HTTPS for production use (HTTP works for localhost)
- User must grant location permission

## 🎯 Customization

### Change Temperature Units to Fahrenheit

In `app.js`, replace all instances of `units=metric` with `units=imperial`

### Change Default City

In `app.js`, around line 170:
```javascript
fetchWeatherByCity('London'); // Change 'London' to your preferred city
```

### Modify Colors

In `styles.css`, update the CSS variables at the top:
```css
:root {
    --primary-color: #3498db;      /* Change this */
    --secondary-color: #2c3e50;    /* And this */
    --accent-color: #e74c3c;       /* And this */
    /* ... */
}
```

### Change Forecast Duration

In `app.js`, adjust the slice values:
```javascript
hourlyData.slice(0, 24)  // Show 24 hours (change to any number)
dailyData.slice(0, 5)    // Show 5 days (change to any number)
```

## 🔧 Troubleshooting

### "Failed to fetch weather" / API Error
- ✅ Check that your API key is correct and active
- ✅ Verify you have internet connection
- ✅ Check [OpenWeatherMap API status](https://status.openweathermap.org/)
- ✅ Ensure city name spelling is correct
- ✅ Check browser console for detailed errors (Press F12)

### Location Button Not Working
- ✅ Check that you granted location permission
- ✅ Ensure your browser supports geolocation
- ✅ For production, use HTTPS (localhost works with HTTP)
- ✅ Check browser permissions settings

### Blank Weather Data
- ✅ Wait a few seconds for the API to respond
- ✅ Try refreshing the page
- ✅ Check browser console for errors (F12 → Console tab)
- ✅ Verify your API key is valid

### CORS Errors
- The OpenWeatherMap API supports CORS from browsers
- If you still get errors, ensure you're using the correct API key
- Try accessing from a different browser or clearing cache

## 📁 Project Structure

```
weather-dashboard/
├── index.html          # HTML structure
├── styles.css          # Styling and responsive design
├── app.js              # JavaScript logic and API calls
└── README.md           # Documentation
```

## 🚀 Future Enhancements

- [ ] Add weather alerts and warnings
- [ ] Store search history in localStorage
- [ ] Add air quality index (AQI)
- [ ] Support multiple languages
- [ ] Add radar/satellite map integration
- [ ] Save favorite cities
- [ ] Dark/Light theme toggle
- [ ] Export weather data to CSV/PDF
- [ ] Weekly forecast extension
- [ ] Weather comparison between cities

## 📄 License

This project is open source and available under the MIT License.

## 📚 Resources

- [OpenWeatherMap API Documentation](https://openweathermap.org/api)
- [MDN: Geolocation API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API)
- [CSS Grid Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)
- [Fetch API Documentation](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)

## 💬 Support

For issues or questions:
1. Check the Troubleshooting section above
2. Review [OpenWeatherMap API documentation](https://openweathermap.org/api)
3. Check browser console for error messages (Press F12)
4. Open an issue on GitHub

## 🎓 Learning Resources

This project demonstrates:
- Fetching data from REST APIs
- Working with async/await in JavaScript
- DOM manipulation and event handling
- Responsive CSS Grid and Flexbox layouts
- Geolocation API usage
- Error handling and user feedback

---

**Built with ❤️ using OpenWeatherMap API**

*Happy weather checking! ☀️🌧️⛈️*