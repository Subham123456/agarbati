# Agarbatti - Premium Agarbatti Website

A beautiful, modern 3-page website showcasing premium handcrafted agarbatti (incense sticks) with artistic design elements and smooth animations.

## 🌟 Features

- **Modern Design**: Beautiful gradients, animations, and artistic effects
- **Responsive**: Fully responsive design that works on all devices
- **3 Main Pages**:
  - **Home**: Artistic hero section with brand showcase and featured products
  - **Catalogue**: Complete product collection with category filtering
  - **About**: Brand story, timeline, values, and contact information
- **Skeleton UI**: Utilizing @skeletonlabs/skeleton for consistent, beautiful components
- **Smooth Animations**: Floating animations, fade-ins, and slide-ups
- **Custom Branding**: Brand colors, custom fonts (Playfair Display & Inter)

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ installed
- npm or pnpm package manager

### Installation

1. Install dependencies:
```bash
npm install
```

### Development

Start the development server:
```bash
npm run dev
```

The site will be available at `http://localhost:5173`

### Build

Build for production:
```bash
npm run build
```

Preview the production build:
```bash
npm run preview
```

## 🎨 Design Features

### Color Palette
- **Brand Primary**: #8B4513 (Rich brown)
- **Brand Secondary**: #D4AF37 (Gold)
- **Brand Accent**: #FF6B35 (Warm orange)

### Typography
- **Display Font**: Playfair Display (Headings)
- **Body Font**: Inter (Body text)

### Animations
- Floating animations for decorative elements
- Fade-in effects for page content
- Slide-up animations for cards and sections
- Smooth hover transitions on interactive elements

## 📁 Project Structure

```
Agarbatti/
├── src/
│   ├── routes/
│   │   ├── +layout.svelte       # Main layout with navigation
│   │   ├── +page.svelte          # Home page
│   │   ├── catalogue/
│   │   │   └── +page.svelte      # Catalogue page
│   │   └── about/
│   │       └── +page.svelte      # About page
│   ├── app.html                  # HTML template
│   └── app.postcss               # Global styles
├── static/                       # Static assets
├── package.json
├── svelte.config.js
├── tailwind.config.ts
└── tsconfig.json
```

## 🛠️ Technologies Used

- **SvelteKit**: Modern web framework
- **TypeScript**: Type-safe JavaScript
- **Tailwind CSS**: Utility-first CSS framework
- **Skeleton UI**: Pre-built Svelte components
- **Vite**: Fast build tool

## 📦 Product Catalogue

The website features 12 premium agarbatti varieties across 4 categories:
- **Floral**: Jasmine, Rose, Lotus, Mogra
- **Woody**: Sandalwood, Oud, Cedarwood
- **Spicy**: Cinnamon, Clove
- **Herbal**: Tulsi, Patchouli, Lavender

## 📝 License

This project is created for Agarbatti brand.

## 🤝 Contributing

This is a proprietary project. For any questions or contributions, please contact the development team.

---

**Crafted with 💝 and devotion**

