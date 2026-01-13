# 🚀 Quick Start Guide - Agarbatti Website

## Running the Website

### Development Mode (with hot reload)
```bash
npm run dev
```
Then open your browser to: **http://localhost:5173**

### Production Build
```bash
npm run build
npm run preview
```

---

## 📁 Project Structure

```
Agarbatti/
├── src/
│   ├── routes/
│   │   ├── +page.svelte           ← Home page
│   │   ├── +layout.svelte         ← Navigation & Footer
│   │   ├── catalogue/
│   │   │   └── +page.svelte       ← Catalogue page
│   │   └── about/
│   │       └── +page.svelte       ← About page
│   ├── app.html                   ← HTML template
│   └── app.postcss                ← Global styles & animations
├── static/                        ← Static assets (images, favicon)
├── package.json
├── tailwind.config.ts             ← Tailwind & brand colors
└── README.md
```

---

## 🎨 Key Files to Customize

### **1. Brand Colors** (`tailwind.config.ts`)
```typescript
colors: {
  'brand-primary': '#8B4513',    // Change main color
  'brand-secondary': '#D4AF37',  // Change accent color
  'brand-accent': '#FF6B35'      // Change highlight color
}
```

### **2. Products** (`src/routes/catalogue/+page.svelte`)
Look for the `products` array around line 20:
```typescript
const products = [
  {
    id: 1,
    name: 'Product Name',
    category: 'floral', // floral, woody, spicy, herbal
    description: 'Description',
    price: '₹120',
    // ... more fields
  }
];
```

### **3. Contact Info** (`src/routes/+layout.svelte` and `src/routes/about/+page.svelte`)
Search for:
- Email: `contact@Agarbatti.com`
- Phone: `+91 98765 43210`
- Location: `Mumbai, Maharashtra`

### **4. Brand Name** 
Search and replace `Agarbatti` across all files if you want to change it.

---

## 🎯 Page URLs

- **Home**: http://localhost:5173/
- **Catalogue**: http://localhost:5173/catalogue
- **About**: http://localhost:5173/about

---

## ✨ Features You Get

### Home Page
- ✅ Beautiful hero section with animated logo
- ✅ Feature cards (4 key benefits)
- ✅ Popular products preview
- ✅ Call-to-action sections

### Catalogue Page
- ✅ 12 products across 4 categories
- ✅ Category filtering (All, Floral, Woody, Spicy, Herbal)
- ✅ Product cards with hover effects
- ✅ Price, burning time, and quantity info

### About Page
- ✅ Brand mission and story
- ✅ Company values (4 cards)
- ✅ Timeline (company history)
- ✅ Contact information
- ✅ Customer testimonials

### Global Features
- ✅ Responsive navigation (desktop + mobile)
- ✅ Beautiful footer with links
- ✅ Smooth animations throughout
- ✅ Mobile-responsive design
- ✅ Custom scrollbar styling

---

## 🎨 Design Highlights

### Animations
- **Floating**: Logo and icons gently float up and down
- **Fade-in**: Content fades in smoothly on page load
- **Slide-up**: Cards slide up with staggered timing
- **Hover effects**: Cards lift and scale on hover

### Color Scheme
- Warm brown tones (traditional, earthy)
- Gold accents (premium, quality)
- Orange highlights (energy, warmth)
- Gradient effects throughout

### Typography
- **Playfair Display**: Elegant serif for headings
- **Inter**: Clean sans-serif for body text

---

## 📱 Mobile Responsive

The site automatically adapts to:
- 📱 **Mobile phones** (< 768px): 1 column, hamburger menu
- 📱 **Tablets** (768px - 1024px): 2 columns
- 💻 **Desktop** (> 1024px): 3-4 columns, full navigation

---

## 🔧 Making Changes

### To add a new product:
1. Open `src/routes/catalogue/+page.svelte`
2. Add to the `products` array
3. Choose a category: `floral`, `woody`, `spicy`, or `herbal`
4. Pick an emoji for the `image` field
5. Set a gradient (e.g., `from-pink-500 to-purple-600`)

### To change animations:
1. Open `src/app.postcss`
2. Modify the `@keyframes` sections
3. Adjust timing, distance, or easing

### To add a new page:
1. Create a new folder in `src/routes/`
2. Add a `+page.svelte` file
3. It will automatically be routed!

---

## 🛠️ Troubleshooting

### Port already in use?
```bash
# Change port in package.json or use:
npm run dev -- --port 3000
```

### Dependencies issues?
```bash
# Clean install
rm -rf node_modules package-lock.json
npm install
```

### Build errors?
```bash
# Check syntax and run:
npm run check
```

---

## 📚 Learn More

- **SvelteKit Docs**: https://kit.svelte.dev/
- **Skeleton UI**: https://skeleton.dev/
- **Tailwind CSS**: https://tailwindcss.com/

---

## 🎉 You're All Set!

Just run `npm run dev` and start exploring your beautiful new website!

**Need help?** Check the `DESIGN_GUIDE.md` for detailed information about every design element.

---

**Happy coding! 🚀**

