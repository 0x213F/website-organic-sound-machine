# Organic Sound Machine Website

## Project Overview
A marketing website for "Organic Sound Machine," a contemporary organ trio based in San Francisco. The band plays funky jazz with a modern twist, targeting both jazz musicians and general audiences.

## Band Information
- **Name**: Organic Sound Machine
- **Location**: San Francisco, CA
- **Format**: Hammond organ trio (organ, electric guitar, drums)
- **Style**: Contemporary jazz with funky arrangements, transforms pop songs into jazz arrangements
- **Target Audience**: Jazz musicians for jam sessions, wedding/corporate events, general music lovers

## Website Features

### Design & Aesthetics
- **Color Scheme**: Vibrant gradient themes with modern lava lamp aesthetic
- **Header**: Animated gradient background (chillGradient animation, 25-second cycle)
- **Typography**: Helvetica Neue for modern, clean look
- **Layout**: Full-width sections spanning entire viewport height
- **Responsive**: Mobile-optimized with appropriate breakpoints

### Interactive Elements

#### Header Section
- **Animated Background**: Slow-morphing gradient with floating orbs
- **"Listen to Us" Button**: Primary CTA that triggers video auto-play and smooth scroll
- **Scroll Indicator**: Clickable animated arrows encouraging exploration

#### Hero Section (2nd section)
- **Layout**: 2-column grid (5fr text, 7fr image)
- **Headline**: "This Jazz Trio Makes Billie Jean Sound Like You've Never Heard It Before"
- **Content**: Single paragraph describing band's approach
- **Photo**: White background placeholder for band photo (600x450px)

#### Interactive Setlist
- **Location**: Below hero content in 2-column grid
- **Songs**: 6 mystery tracks with play buttons
- **Functionality**: 5-second delay before revealing song names
- **Song List**:
  1. Superstition (Stevie Wonder)
  2. Cantaloupe Island (Herbie Hancock)
  3. Billie Jean (Michael Jackson)
  4. Chameleon (Herbie Hancock)
  5. Use Me (Bill Withers)
  6. Cissy Strut (The Meters)

#### Video Section
- **YouTube Integration**: Embedded video with auto-play functionality
- **Video ID**: -TKUNBVlq4w
- **Aspect Ratio**: Strict 16:9 format
- **Auto-play**: Triggered by "Listen to Us" button with immediate response

#### Additional Sections
- **About**: Streamlined content about the band
- **Contact**: Email CTA (booking@organicsoundmachine.com)
- **Jam Session**: Targets jazz musicians for house band bookings

### Technical Implementation

#### Key JavaScript Functions
```javascript
// Video auto-play with immediate trigger
function scrollToVideo() {
    const iframe = document.getElementById('youtube-video');
    const src = iframe.src;
    if (!src.includes('autoplay=1')) {
        iframe.src = src + '&autoplay=1';
    }
    const videoSection = document.getElementById('video-section');
    videoSection.scrollIntoView({ behavior: 'smooth', block: 'center' });
}

// Mystery track functionality with 5-second reveal
function playSong(audioId, songName, button) {
    // Play audio and set 5-second timeout to reveal song name
}
```

#### CSS Animations
- **chillGradient**: 25-second header background animation
- **gentleOrbs**: 30-second floating orb animation
- **scrollBounce**: 2-second scroll indicator animation
- **pulse**: Play button animation when active

### Deployment
- **Platform**: GitHub Pages
- **Repository**: https://github.com/0x213F/website-organic-sound-machine
- **Live URL**: https://0x213f.github.io/website-organic-sound-machine/
- **Files**: index.html and styles.css in root directory (required for GitHub Pages)

### Development Commands
```bash
# Local development
yarn start  # Runs Express server on localhost:3000

# Deployment
git add .
git commit -m "commit message"
git push  # Auto-deploys to GitHub Pages
```

### File Structure
```
website-organic-sound-machine/
├── index.html              # Main website file
├── styles.css             # All styling and animations
├── server.js              # Local development server
├── package.json           # Node dependencies
├── .github/workflows/deploy.yml  # GitHub Pages deployment
└── CLAUDE.md              # This documentation file
```

### Content Strategy
- **Click-bait headline** to grab attention
- **Mystery tracks** to engage users interactively
- **Dual targeting**: serious jazz musicians + casual listeners
- **San Francisco identity** emphasized throughout
- **Professional booking focus** for revenue generation

### Future Considerations
- Replace placeholder audio files with actual song previews
- Update band photo placeholder with professional photos
- Consider adding more interactive elements
- Potential integration with streaming platforms
- SEO optimization for local San Francisco searches

### Known Technical Details
- YouTube iframe requires enablejsapi=1 for auto-play control
- Video auto-play triggered immediately on button click (no delay)
- Setlist uses glassmorphism design with backdrop-filter
- Mobile responsive with single-column layouts
- All gradients use modern CSS techniques for smooth performance

### Brand Voice & Messaging
- Professional but approachable
- Emphasizes versatility (jazz purists + casual listeners)
- Highlights transformation of familiar songs
- San Francisco music scene connection
- Technical proficiency balanced with fun factor