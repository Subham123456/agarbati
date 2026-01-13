# Agarbatti Website - Design & Features Guide

## 🎨 Design Philosophy

This website showcases **Agarbatti** - a premium agarbatti (incense stick) brand with an emphasis on traditional craftsmanship and modern aesthetics. The design combines:

- **Traditional Elements**: Sacred symbols (🕉️), warm earthy tones
- **Modern UI/UX**: Smooth animations, gradient effects, responsive design
- **Artistic Effects**: Floating animations, dynamic backgrounds, elegant transitions

---

## 📄 Page Overview

### 1. **Home Page** (`/`)

The landing page creates an immersive first impression with multiple sections:

#### **Hero Section**
- Full-screen gradient background (amber to orange tones)
- Animated floating background orbs
- Centered brand logo with floating animation
- Large gradient text for brand name
- Call-to-action buttons with hover effects
- Animated scroll indicator

#### **Features Section**
- 4 feature cards in responsive grid
- Individual floating animations for icons
- Hover effects (lift and shadow enhancement)
- Cards feature: Natural Ingredients, Traditional Methods, Premium Quality, Variety

#### **Popular Fragrances Preview**
- 3 featured products with gradient backgrounds
- Product cards with emoji icons
- Floating animations on product icons
- Link to full catalogue

#### **Call to Action Section**
- Full-width gradient banner
- Animated background elements
- Clear CTAs for engagement

---

### 2. **Catalogue Page** (`/catalogue`)

A complete product showcase with filtering capabilities:

#### **Category Filter Bar**
- Sticky navigation (stays visible on scroll)
- 5 categories: All, Floral, Woody, Spicy, Herbal
- Active state highlighting with gradient background
- Emoji icons for each category

#### **Product Grid**
- 12 unique agarbatti products
- Responsive grid (1-4 columns based on screen size)
- Each product card includes:
  - Gradient background with emoji icon
  - Product name and description
  - Price tag overlay
  - Burning time and stick count
  - "Add to Inquiry" button
- Hover effects: lift animation, shadow, scale

#### **Product Categories**
- **Floral**: Jasmine, Rose, Lotus, Mogra
- **Woody**: Sandalwood, Oud, Cedarwood
- **Spicy**: Cinnamon, Clove
- **Herbal**: Tulsi, Patchouli, Lavender

#### **Information Banner**
- Service highlights: Free delivery, Premium quality, Quality guarantee
- Gradient background with white text

---

### 3. **About Page** (`/about`)

Brand story and company information:

#### **Hero Section**
- Brand logo with floating animation
- Mission statement introduction

#### **Mission Section**
- Detailed company story
- Three paragraphs explaining values and commitment
- Clean typography with ample spacing

#### **Values Grid**
- 4 core values in 2x2 grid
- Icons with floating animations
- Values: Natural & Pure, Traditional Craftsmanship, Sustainable, Made with Love

#### **Timeline Section**
- Visual timeline with 4 milestones
- Years: 1985, 2000, 2015, 2025
- Connected timeline dots
- Gradient year numbers

#### **Contact Section**
- Full-width gradient banner
- Contact details: Email, Phone, Location
- CTA buttons for email and catalogue
- Grid layout for contact info

#### **Testimonials**
- 3 customer testimonials
- 5-star ratings
- Hover effects on cards

---

## 🎯 Design Features

### **Color Palette**
```css
Brand Primary:   #8B4513 (Saddle Brown)
Brand Secondary: #D4AF37 (Metallic Gold)
Brand Accent:    #FF6B35 (Orange Red)
Background:      Amber/Orange gradients
```

### **Typography**
- **Display Font**: Playfair Display (elegant serif for headings)
- **Body Font**: Inter (clean sans-serif for readability)

### **Animations**

#### 1. **Floating Animation**
- Used for: Logo, product icons, decorative elements
- Effect: Gentle up-down movement
- Duration: 6 seconds, infinite loop

#### 2. **Fade In**
- Used for: Page content on load
- Effect: Opacity 0 to 1
- Duration: 1 second

#### 3. **Slide Up**
- Used for: Cards, sections
- Effect: Slides up while fading in
- Duration: 0.8 seconds
- Staggered delays for multiple items

#### 4. **Hover Effects**
- Cards lift up (-translate-y-2)
- Enhanced shadows
- Scale transformations (scale-105)
- Color transitions

### **Responsive Design**
- Mobile-first approach
- Breakpoints:
  - Mobile: < 768px (single column, mobile menu)
  - Tablet: 768px - 1024px (2 columns)
  - Desktop: > 1024px (3-4 columns)

---

## 🧭 Navigation

### **Desktop Navigation**
- Horizontal menu bar in header
- Active page highlighting with underline animation
- Smooth color transitions

### **Mobile Navigation**
- Hamburger menu button
- Slide-down mobile menu
- Active page highlighting

### **Footer**
- Three-column layout (Brand, Quick Links, Contact)
- Social responsibility message
- Copyright information

---

## ✨ Special Effects

### 1. **Gradient Text**
- Brand name and headings use gradient clipping
- Colors: Secondary → Accent → Primary

### 2. **Gradient Backgrounds**
- Hero sections use multi-stop gradients
- Product cards have unique gradient colors
- CTA sections use brand color gradients

### 3. **Background Orbs**
- Large blurred circular shapes
- Floating animations
- Low opacity for subtle effect

### 4. **Custom Scrollbar**
- Styled in brand colors
- Smooth appearance

---

## 🚀 Interactive Elements

### **Buttons**
- Primary: Gradient background (brown to amber)
- Secondary: White with brand-colored border
- All buttons have:
  - Rounded corners
  - Hover scale effect
  - Shadow enhancement
  - Smooth transitions

### **Product Cards**
- Interactive hover states
- Information overlays
- Action buttons

### **Category Filters**
- Toggle between categories
- Smooth transitions
- Visual feedback for active state

---

## 📱 Mobile Experience

### **Optimizations**
- Touch-friendly button sizes
- Simplified layouts for small screens
- Hamburger menu navigation
- Stacked sections
- Responsive font sizes
- Optimized images and animations

---

## 🎭 Brand Identity

### **Visual Identity**
- **Sacred Symbol**: Om (🕉️) as primary brand icon
- **Color Psychology**: Earthy browns (trust, stability), Gold (premium, quality), Orange (warmth, energy)
- **Typography**: Classic serif for tradition, modern sans-serif for clarity
- **Imagery**: Emojis used artistically for product representation

### **Brand Voice**
- Spiritual and devotional
- Premium and quality-focused
- Traditional yet modern
- Welcoming and warm

---

## 🔧 Technical Implementation

### **Built With**
- **Framework**: SvelteKit 2.0
- **Styling**: Tailwind CSS 3.4 + Skeleton UI 2.9
- **Language**: TypeScript
- **Build Tool**: Vite 5.0

### **Key Dependencies**
```json
{
  "@skeletonlabs/skeleton": "^2.9.0",
  "@sveltejs/kit": "^2.0.0",
  "tailwindcss": "^3.4.1",
  "typescript": "^5.0.0"
}
```

### **Performance Features**
- Server-side rendering (SSR)
- Static site generation support
- Optimized bundle sizes
- Lazy loading
- Responsive images

---

## 🎨 Customization Guide

### **Changing Brand Colors**
Edit `tailwind.config.ts`:
```typescript
colors: {
  'brand-primary': '#8B4513',    // Main brown
  'brand-secondary': '#D4AF37',  // Gold
  'brand-accent': '#FF6B35'      // Orange
}
```

### **Modifying Animations**
Edit `src/app.postcss`:
```css
@keyframes floating {
  /* Adjust timing and distance */
}
```

### **Adding Products**
Edit `src/routes/catalogue/+page.svelte`:
```typescript
const products = [
  {
    id: 1,
    name: 'Product Name',
    category: 'floral',
    // ... other properties
  }
];
```

---

## 📊 Content Structure

### **Home Page Sections**
1. Hero (Full screen)
2. Features (4 cards)
3. Popular Products (3 items)
4. CTA Banner

### **Catalogue Page Sections**
1. Hero Banner
2. Category Filter
3. Product Grid (12 items)
4. Information Banner

### **About Page Sections**
1. Hero Banner
2. Mission Statement
3. Core Values (4 items)
4. Timeline (4 milestones)
5. Contact Information
6. Testimonials (3 reviews)

---

## 🌟 Best Practices Implemented

- ✅ **Semantic HTML**: Proper use of sections, headers, navigation
- ✅ **Accessibility**: Aria labels, keyboard navigation
- ✅ **SEO**: Meta tags, semantic structure, descriptive content
- ✅ **Performance**: Optimized animations, efficient CSS
- ✅ **Responsive**: Mobile-first, flexible layouts
- ✅ **User Experience**: Clear CTAs, intuitive navigation, feedback
- ✅ **Visual Hierarchy**: Proper heading levels, spacing, contrast
- ✅ **Brand Consistency**: Unified color scheme, typography, voice

---

## 🎬 Getting Started

1. **Install**: `npm install`
2. **Develop**: `npm run dev` (opens at http://localhost:5173)
3. **Build**: `npm run build`
4. **Preview**: `npm run preview`

---

**Crafted with care to showcase the divine essence of Agarbatti** ✨

