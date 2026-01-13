<script lang="ts">
	import { onMount } from 'svelte';
	
	let mounted = false;
	
	onMount(() => {
		mounted = true;
	});
	
	const features = [
		{
			icon: '🌿',
			title: 'Natural Ingredients',
			description: 'Made with pure herbs, essential oils, and natural resins'
		},
		{
			icon: '🙏',
			title: 'Traditional Methods',
			description: 'Handcrafted using ancient techniques passed through generations'
		},
		{
			icon: '✨',
			title: 'Premium Quality',
			description: 'Long-lasting fragrances that create divine atmosphere'
		},
		{
			icon: '🌸',
			title: 'Variety of Scents',
			description: 'From sandalwood to jasmine, find your perfect fragrance'
		}
	];
</script>

<svelte:head>
	<title>Agarbatti - Premium Agarbatti & Incense Sticks</title>
	<meta name="description" content="Discover premium handcrafted agarbatti with divine fragrances. Made with natural ingredients using traditional methods." />
</svelte:head>

<!-- Hero Section -->
<section class="relative h-screen flex items-center justify-center overflow-hidden bg-gradient-to-br from-amber-50 via-orange-50 to-amber-100">
	<!-- Animated background elements -->
	<div class="absolute inset-0 opacity-10">
		<div class="absolute top-20 left-20 w-72 h-72 bg-brand-primary rounded-full blur-3xl floating-animation"></div>
		<div class="absolute bottom-20 right-20 w-96 h-96 bg-brand-accent rounded-full blur-3xl floating-animation" style="animation-delay: -3s;"></div>
	</div>
	
	<div class="container mx-auto px-4 z-10">
		<div class="text-center space-y-8" class:fade-in={mounted}>
			<!-- Brand Logo -->
			<div class="inline-block mb-6 floating-animation">
				<div class="w-32 h-32 bg-gradient-to-br from-brand-secondary to-brand-primary rounded-full flex items-center justify-center shadow-2xl">
					<span class="text-6xl">🕉️</span>
				</div>
			</div>
			
			<!-- Main Heading -->
			<h1 class="text-6xl md:text-8xl font-display font-bold gradient-text leading-tight">
				Agarbatti
			</h1>
			
			<p class="text-2xl md:text-3xl text-gray-700 font-light tracking-wide">
				Premium Handcrafted Agarbatti
			</p>
			
			<p class="text-lg md:text-xl text-gray-600 max-w-2xl mx-auto leading-relaxed">
				Experience the divine fragrance of tradition. Our premium incense sticks are 
				handcrafted with natural ingredients, bringing serenity to your sacred space.
			</p>
			
			<!-- CTA Buttons -->
			<div class="flex flex-col sm:flex-row gap-4 justify-center items-center pt-6">
				<a 
					href="/catalogue" 
					class="btn bg-gradient-to-r from-brand-primary to-amber-900 text-white px-8 py-4 text-lg rounded-full hover:scale-105 transition-transform duration-300 shadow-xl hover:shadow-2xl"
				>
					Explore Catalogue
				</a>
				<a 
					href="/about" 
					class="btn bg-white text-brand-primary border-2 border-brand-primary px-8 py-4 text-lg rounded-full hover:bg-brand-primary hover:text-white transition-all duration-300 shadow-lg"
				>
					Our Story
				</a>
			</div>
		</div>
	</div>
	
	<!-- Scroll indicator -->
	<div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce">
		<svg class="w-6 h-6 text-brand-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24">
			<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
		</svg>
	</div>
</section>

<!-- Features Section -->
<section class="py-20 bg-white">
	<div class="container mx-auto px-4">
		<div class="text-center mb-16 slide-up">
			<h2 class="text-4xl md:text-5xl font-display font-bold text-brand-primary mb-4">
				Why Choose Agarbatti?
			</h2>
			<div class="w-24 h-1 bg-gradient-to-r from-brand-secondary to-brand-accent mx-auto rounded-full"></div>
		</div>
		
		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
			{#each features as feature, i}
				<div 
					class="card p-8 text-center hover:shadow-2xl transition-all duration-300 hover:-translate-y-2 bg-gradient-to-br from-white to-amber-50 border-2 border-transparent hover:border-brand-secondary slide-up"
					style="animation-delay: {i * 0.1}s;"
				>
					<div class="text-6xl mb-4 inline-block floating-animation" style="animation-delay: {i * 0.5}s;">
						{feature.icon}
					</div>
					<h3 class="text-xl font-semibold text-brand-primary mb-3">
						{feature.title}
					</h3>
					<p class="text-gray-600 leading-relaxed">
						{feature.description}
					</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- Featured Products Preview -->
<section class="py-20 bg-gradient-to-br from-amber-50 to-orange-50">
	<div class="container mx-auto px-4">
		<div class="text-center mb-16">
			<h2 class="text-4xl md:text-5xl font-display font-bold text-brand-primary mb-4">
				Popular Fragrances
			</h2>
			<div class="w-24 h-1 bg-gradient-to-r from-brand-secondary to-brand-accent mx-auto rounded-full mb-6"></div>
			<p class="text-gray-600 text-lg">Discover our most beloved scents</p>
		</div>
		
		<div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-12">
			{#each [
				{ name: 'Mystic Sandalwood', image: '🪵', color: 'from-amber-600 to-orange-700' },
				{ name: 'Divine Jasmine', image: '🌸', color: 'from-pink-500 to-purple-600' },
				{ name: 'Sacred Rose', image: '🌹', color: 'from-rose-500 to-red-600' }
			] as product, i}
				<div class="card overflow-hidden hover:shadow-2xl transition-all duration-300 hover:-translate-y-2 slide-up" style="animation-delay: {i * 0.15}s;">
					<div class="h-48 bg-gradient-to-br {product.color} flex items-center justify-center">
						<span class="text-8xl floating-animation">{product.image}</span>
					</div>
					<div class="p-6 bg-white">
						<h3 class="text-2xl font-semibold text-brand-primary mb-2">{product.name}</h3>
						<p class="text-gray-600 mb-4">Experience the divine essence</p>
					</div>
				</div>
			{/each}
		</div>
		
		<div class="text-center">
			<a 
				href="/catalogue" 
				class="btn bg-gradient-to-r from-brand-primary to-amber-900 text-white px-10 py-4 text-lg rounded-full hover:scale-105 transition-transform duration-300 shadow-xl inline-flex items-center space-x-2"
			>
				<span>View All Products</span>
				<svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6"></path>
				</svg>
			</a>
		</div>
	</div>
</section>

<!-- Call to Action Section -->
<section class="py-20 bg-gradient-to-r from-brand-primary via-amber-900 to-brand-primary text-white relative overflow-hidden">
	<div class="absolute inset-0 opacity-10">
		<div class="absolute top-0 left-0 w-96 h-96 bg-white rounded-full blur-3xl floating-animation"></div>
		<div class="absolute bottom-0 right-0 w-96 h-96 bg-brand-secondary rounded-full blur-3xl floating-animation" style="animation-delay: -2s;"></div>
	</div>
	
	<div class="container mx-auto px-4 text-center relative z-10">
		<h2 class="text-4xl md:text-5xl font-display font-bold mb-6">
			Transform Your Space with Divine Fragrances
		</h2>
		<p class="text-xl mb-8 max-w-2xl mx-auto opacity-90">
			Join thousands of satisfied customers who have made Agarbatti their choice for premium incense.
		</p>
		<a 
			href="/about" 
			class="btn bg-white text-brand-primary px-10 py-4 text-lg rounded-full hover:scale-105 transition-transform duration-300 shadow-xl inline-flex items-center space-x-2 font-semibold"
		>
			<span>Learn More About Us</span>
			<svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6"></path>
			</svg>
		</a>
	</div>
</section>

