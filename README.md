# Saltash WebAR Historical Tour

A professional, permanent website featuring an interactive augmented reality (AR) historical tour of Saltash, Cornwall. This project showcases the Royal Albert Bridge, Mary Newman's Bridge, and other historical landmarks through immersive AR technology.

## 🌐 Website Structure

The website consists of four main pages:

### 1. **Home Page** (`index.html`)
- Professional landing page with hero section
- Overview of historical landmarks
- Features and benefits of the AR tour
- Call-to-action buttons to start the experience
- Responsive design for all devices

### 2. **AR Tour Page** (`tour.html`)
- Interactive augmented reality experience
- Three AR markers for different landmarks:
  - **HIRO Marker**: Royal Albert Bridge
  - **KANJI Marker**: Mary Newman's Bridge
  - **LETTER A Marker**: Historic Saltash Town
- Real-time 3D model visualization
- Historical information panels
- Mobile-optimized interface

### 3. **Markers Guide** (`markers.html`)
- Complete guide to AR markers
- Download links for printable markers
- Setup and usage instructions
- Tips for best results
- Troubleshooting information

### 4. **Additional Resources**
- `README.md`: This file
- `package.json`: Project metadata

## 🎯 Features

✅ **Mobile-First Design**: Fully responsive and optimized for smartphones  
✅ **No App Required**: Access directly through a web browser  
✅ **Interactive 3D Models**: Animated AR representations of landmarks  
✅ **Rich Historical Content**: Detailed information about each landmark  
✅ **Easy to Use**: Simple marker-based AR detection  
✅ **Privacy-Focused**: All processing happens on the user's device  
✅ **Fast Performance**: Optimized for smooth AR experiences  
✅ **Educational**: Perfect for tourism, schools, and cultural exploration  

## 🚀 Deployment

### Option 1: Deploy to Netlify (Recommended)

1. **Create a Netlify account** at [netlify.com](https://netlify.com)
2. **Connect your repository** or drag and drop the project folder
3. **Configure build settings**:
   - Build command: (leave empty - static site)
   - Publish directory: `.` (root directory)
4. **Deploy** - Your site will be live with a permanent URL

### Option 2: Deploy to Vercel

1. **Create a Vercel account** at [vercel.com](https://vercel.com)
2. **Import your project** from GitHub or upload the folder
3. **Deploy** - Vercel will automatically configure it for static hosting

### Option 3: Deploy to GitHub Pages

1. **Create a GitHub repository** for the project
2. **Push all files** to the repository
3. **Enable GitHub Pages** in repository settings
4. **Select the main branch** as the source
5. Your site will be available at `https://yourusername.github.io/saltash-webar-tour`

### Option 4: Self-Hosted

1. **Upload files** to your web server via FTP/SSH
2. **Ensure HTTPS** is enabled (required for camera access)
3. **Configure** your web server to serve static files
4. Access via your domain

## 📋 Requirements

- **Browser Support**: Modern browsers with WebGL and WebRTC support
  - Chrome/Edge 60+
  - Firefox 55+
  - Safari 11+
- **Device**: Smartphone or tablet with a camera
- **Connection**: Internet access (for loading libraries)
- **Permissions**: Camera access (required for AR)

## 🎨 Customization

### Modify Landmark Information

Edit the `markerData` object in `tour.html`:

```javascript
const markerData = {
    'bridge-marker': {
        name: 'Royal Albert Bridge',
        title: '🌉 The Royal Albert Bridge',
        content: 'Your custom content here...'
    },
    // ... more landmarks
};
```

### Change Colors and Styling

Edit the CSS sections in each HTML file:

```css
/* Primary color */
--primary-color: #1e3c72;

/* Accent color */
--accent-color: #00d4ff;

/* Button color */
--button-color: #ff6b6b;
```

### Update 3D Models

Modify the A-Frame entities in `tour.html` to change the 3D representations:

```html
<a-box 
    position="0 0.5 0" 
    scale="2.5 0.6 0.15"
    color="#c0504d"
></a-box>
```

## 🔧 Technologies Used

- **A-Frame**: WebGL framework for building VR/AR experiences
- **AR.js**: Lightweight AR library for web
- **Three.js**: 3D graphics library
- **HTML5**: Semantic markup
- **CSS3**: Modern styling and animations
- **JavaScript**: Interactive functionality

## 📱 How to Use

### For Users

1. **Visit the website** on your smartphone
2. **Click "Start AR Tour"** on the home page
3. **Allow camera access** when prompted
4. **Download and print AR markers** from the Markers Guide page
5. **Point your camera** at the markers to see the AR experience
6. **Read the historical information** displayed on your screen

### For Developers

1. **Clone or download** the project files
2. **Open `index.html`** in a web browser to preview locally
3. **Modify content** as needed (see Customization section)
4. **Test on mobile** devices before deployment
5. **Deploy** using one of the methods above

## 🖨️ AR Markers

The tour uses three standard AR markers:

| Marker | Landmark | File |
|--------|----------|------|
| HIRO | Royal Albert Bridge | `hiro.jpg` |
| KANJI | Mary Newman's Bridge | `kanji.png` |
| LETTER A | Historic Saltash Town | `letterA.png` |

**Download links** are available on the Markers Guide page.

## 📊 Performance Optimization

- **Lazy loading**: Images and models load on demand
- **Minified CSS/JS**: Reduced file sizes
- **Optimized 3D models**: Simplified geometry for faster rendering
- **Responsive images**: Appropriate sizes for different devices
- **Caching**: Browser caching for faster repeat visits

## 🔒 Privacy & Security

- **No data collection**: All processing happens on the user's device
- **No tracking**: No analytics or user tracking
- **HTTPS ready**: Secure by default
- **Open source**: Transparent and auditable code

## 🐛 Troubleshooting

### AR not detecting markers
- Ensure good lighting conditions
- Print markers at larger size (15cm × 15cm+)
- Hold device 20-50cm from marker
- Point camera directly at marker

### Camera not working
- Grant camera permissions in browser settings
- Check if HTTPS is enabled (required)
- Try a different browser
- Restart your device

### 3D models not showing
- Clear browser cache
- Check internet connection
- Ensure WebGL is supported
- Try a different device

## 📞 Support & Contact

For issues, suggestions, or contributions:
- Check the troubleshooting section
- Review the markers guide
- Test on different devices and browsers

## 📄 License

This project is open source and available for educational and commercial use.

## 🙏 Credits

- **Isambard Kingdom Brunel**: Designer of the Royal Albert Bridge
- **A-Frame & AR.js**: Open source AR frameworks
- **Saltash Community**: Historical information and inspiration

## 🌟 Future Enhancements

Potential features for future versions:
- Location-based AR (GPS integration)
- Multiple language support
- User-generated content
- Social sharing features
- Advanced 3D models
- Audio narration
- Virtual tours
- Mobile app version

---

**Version**: 1.0.0  
**Last Updated**: June 2026  
**Status**: Production Ready ✅
