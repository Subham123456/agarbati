<script lang="ts">
	import { onMount } from 'svelte';
	
	let mounted = false;
	let selectedCategory = 'all';
	
	onMount(() => {
		mounted = true;
	});
	
	const categories = [
		{ id: 'all', label: 'All Products', icon: '✨' },
		{ id: 'floral', label: 'Floral', icon: '🌸' },
		{ id: 'woody', label: 'Woody', icon: '🪵' },
		{ id: 'spicy', label: 'Spicy', icon: '🌶️' },
		{ id: 'herbal', label: 'Herbal', icon: '🌿' }
	];
	
	const products = [
		{
			id: 1,
			name: 'Mystic Sandalwood',
			category: 'woody',
			description: 'Rich, warm, and earthy aroma of pure sandalwood',
			price: '₹120',
			image: '🪵',
			gradient: 'from-amber-600 to-orange-700',
			burning: '45 minutes',
			sticks: '20 sticks'
		},
		{
			id: 2,
			name: 'Divine Jasmine',
			category: 'floral',
			description: 'Sweet and intoxicating jasmine flowers',
			price: '₹110',
			image: '🌸',
			gradient: 'from-pink-500 to-purple-600',
			burning: '40 minutes',
			sticks: '20 sticks'
		},
		{
			id: 3,
			name: 'Sacred Rose',
			category: 'floral',
			description: 'Elegant and romantic rose fragrance',
			price: '₹115',
			image: '🌹',
			gradient: 'from-rose-500 to-red-600',
			burning: '40 minutes',
			sticks: '20 sticks'
		},
		{
			id: 4,
			name: 'Holy Lotus',
			category: 'floral',
			description: 'Pure and serene lotus blossom scent',
			price: '₹130',
			image: '🪷',
			gradient: 'from-pink-400 to-indigo-500',
			burning: '45 minutes',
			sticks: '20 sticks'
		},
		{
			id: 5,
			name: 'Ancient Oud',
			category: 'woody',
			description: 'Deep, mysterious, and luxurious oud wood',
			price: '₹180',
			image: '🌳',
			gradient: 'from-gray-700 to-gray-900',
			burning: '50 minutes',
			sticks: '15 sticks'
		},
		{
			id: 6,
			name: 'Cedarwood Serenity',
			category: 'woody',
			description: 'Calming and grounding cedar essence',
			price: '₹125',
			image: '🎋',
			gradient: 'from-green-700 to-teal-800',
			burning: '45 minutes',
			sticks: '20 sticks'
		},
		{
			id: 7,
			name: 'Cinnamon Spice',
			category: 'spicy',
			description: 'Warm and comforting cinnamon blend',
			price: '₹105',
			image: '🌶️',
			gradient: 'from-orange-600 to-red-700',
			burning: '40 minutes',
			sticks: '20 sticks'
		},
		{
			id: 8,
			name: 'Clove Harmony',
			category: 'spicy',
			description: 'Rich and aromatic clove fragrance',
			price: '₹100',
			image: '🧄',
			gradient: 'from-amber-700 to-orange-900',
			burning: '40 minutes',
			sticks: '20 sticks'
		},
		{
			id: 9,
			name: 'Tulsi Sacred Basil',
			category: 'herbal',
			description: 'Holy basil with healing properties',
			price: '₹95',
			image: '🌿',
			gradient: 'from-green-500 to-emerald-700',
			burning: '35 minutes',
			sticks: '25 sticks'
		},
		{
			id: 10,
			name: 'Patchouli Earth',
			category: 'herbal',
			description: 'Earthy and musky patchouli essence',
			price: '₹115',
			image: '🍃',
			gradient: 'from-lime-600 to-green-800',
			burning: '45 minutes',
			sticks: '20 sticks'
		},
		{
			id: 11,
			name: 'Lavender Dreams',
			category: 'herbal',
			description: 'Soothing lavender for peaceful relaxation',
			price: '₹120',
			image: '💜',
			gradient: 'from-purple-400 to-violet-600',
			burning: '40 minutes',
			sticks: '20 sticks'
		},
		{
			id: 12,
			name: 'Mogra Bliss',
			category: 'floral',
			description: 'Enchanting Arabian jasmine fragrance',
			price: '₹125',
			image: '🌼',
			gradient: 'from-yellow-400 to-amber-500',
			burning: '45 minutes',
			sticks: '20 sticks'
		}
	];
	
	$: filteredProducts = selectedCategory === 'all' 
		? products 
		: products.filter(p => p.category === selectedCategory);
</script>

<svelte:head>
	<title>Catalogue - Agarbatti Premium Agarbatti</title>
	<meta name="description" content="Explore our complete range of premium handcrafted agarbatti. From sandalwood to jasmine, find your perfect fragrance." />
</svelte:head>

<!-- Hero Section -->
<section class="relative py-20 bg-gradient-to-br from-amber-50 via-orange-50 to-amber-100">
	<div class="container mx-auto px-4">
		<div class="text-center space-y-6" class:fade-in={mounted}>
			<h1 class="text-5xl md:text-6xl font-display font-bold gradient-text">
				Our Catalogue
			</h1>
			<p class="text-xl text-gray-600 max-w-2xl mx-auto">
				Discover our exquisite collection of handcrafted agarbatti, each carefully 
				created to bring divine fragrances to your space.
			</p>
		</div>
	</div>
</section>

<!-- Category Filter -->
<section class="py-8 bg-white sticky top-0 z-40 shadow-md">
	<div class="container mx-auto px-4">
		<div class="flex flex-wrap justify-center gap-4">
			{#each categories as category}
				<button
					class="btn px-6 py-3 rounded-full transition-all duration-300 flex items-center space-x-2"
					class:bg-gradient-to-r={selectedCategory === category.id}
					class:from-brand-primary={selectedCategory === category.id}
					class:to-amber-900={selectedCategory === category.id}
					class:text-white={selectedCategory === category.id}
					class:shadow-lg={selectedCategory === category.id}
					class:bg-gray-100={selectedCategory !== category.id}
					class:text-gray-700={selectedCategory !== category.id}
					class:hover:bg-gray-200={selectedCategory !== category.id}
					on:click={() => selectedCategory = category.id}
				>
					<span class="text-xl">{category.icon}</span>
					<span class="font-medium">{category.label}</span>
				</button>
			{/each}
		</div>
	</div>
</section>

<!-- Products Grid -->
<section class="py-16 bg-gradient-to-br from-white via-amber-50/30 to-white">
	<div class="container mx-auto px-4">
		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
			{#each filteredProducts as product, i}
				<div 
					class="card overflow-hidden hover:shadow-2xl transition-all duration-300 hover:-translate-y-2 bg-white slide-up group"
					style="animation-delay: {i * 0.05}s;"
				>
					<!-- Product Image -->
					<div class="h-56 bg-gradient-to-br {product.gradient} flex items-center justify-center relative overflow-hidden">
						<span class="text-8xl floating-animation group-hover:scale-110 transition-transform duration-500">
							{product.image}
						</span>
						<div class="absolute top-4 right-4 bg-white/90 backdrop-blur-sm px-3 py-1 rounded-full text-brand-primary font-semibold text-sm">
							{product.price}
						</div>
					</div>
					
					<!-- Product Details -->
					<div class="p-6 space-y-3">
						<h3 class="text-2xl font-display font-semibold text-brand-primary group-hover:text-brand-accent transition-colors">
							{product.name}
						</h3>
						<p class="text-gray-600 text-sm leading-relaxed">
							{product.description}
						</p>
						
						<!-- Product Info -->
						<div class="flex justify-between items-center text-xs text-gray-500 pt-2 border-t border-gray-200">
							<div class="flex items-center space-x-1">
								<span>⏱️</span>
								<span>{product.burning}</span>
							</div>
							<div class="flex items-center space-x-1">
								<span>📦</span>
								<span>{product.sticks}</span>
							</div>
						</div>
						
						<!-- Add to Cart Button -->
						<button class="w-full btn bg-gradient-to-r from-brand-primary to-amber-900 text-white py-3 rounded-lg hover:shadow-lg transition-all duration-300 hover:scale-105 font-medium">
							Add to Inquiry
						</button>
					</div>
				</div>
			{/each}
		</div>
		
		{#if filteredProducts.length === 0}
			<div class="text-center py-20">
				<p class="text-2xl text-gray-500 font-light">No products found in this category.</p>
			</div>
		{/if}
	</div>
</section>

<!-- Information Section -->
<section class="py-16 bg-gradient-to-r from-brand-primary via-amber-900 to-brand-primary text-white">
	<div class="container mx-auto px-4">
		<div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-center">
			<div class="space-y-3">
				<div class="text-5xl mb-2">🚚</div>
				<h3 class="text-xl font-semibold">Free Delivery</h3>
				<p class="text-amber-200">On orders above ₹500</p>
			</div>
			<div class="space-y-3">
				<div class="text-5xl mb-2">✨</div>
				<h3 class="text-xl font-semibold">Premium Quality</h3>
				<p class="text-amber-200">100% natural ingredients</p>
			</div>
			<div class="space-y-3">
				<div class="text-5xl mb-2">🛡️</div>
				<h3 class="text-xl font-semibold">Quality Guarantee</h3>
				<p class="text-amber-200">Satisfaction guaranteed</p>
			</div>
		</div>
	</div>
</section>

