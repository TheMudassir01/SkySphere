# 3D Weather Website 🌍☀️🌧️

A 3D interactive weather visualization website built using **Three.js** and the **OpenWeatherMap API**. This project displays real-time weather data (e.g., temperature, wind speed, and weather conditions) for a specific location and renders corresponding 3D effects (e.g., rain, snow, or lightning).

![Demo](https://via.placeholder.com/800x400.png?text=3D+Weather+Website+Demo) <!-- Replace with an actual screenshot or GIF -->

---

## Features ✨
- **Real-time Weather Data**: Fetches weather information from OpenWeatherMap API.
- **3D Visualization**: Renders a 3D Earth model with weather effects (e.g., rain, snow, lightning).
- **Interactive**: Users can rotate the 3D Earth model using mouse drag.
- **Responsive Design**: Works on both desktop and mobile devices.

---

## Technologies Used 🛠️
- **Three.js**: For 3D rendering and animations.
- **OpenWeatherMap API**: For fetching real-time weather data.
- **GSAP**: For smooth animations (optional).
- **HTML/CSS/JavaScript**: For the website structure and styling.

---

## How to Use 🚀

### 1. **Set Up the Project**
- Clone this repository or download the `index.html` file.
- Open the `index.html` file in your browser to view the website.

### 2. **Replace the API Key**
- Get your **OpenWeatherMap API Key** from [OpenWeatherMap](https://openweathermap.org/api).
- Replace `YOUR_API_KEY` in the `index.html` file with your actual API key:
  ```javascript
  const apiKey = 'f0cdc9f0b5039240faf47f33f0df3fff'; // Replace with your API key
