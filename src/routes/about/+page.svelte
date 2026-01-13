<script lang="ts">
	import { onMount } from 'svelte';
	
	let mounted = false;
	
	onMount(() => {
		mounted = true;
	});
	
	const values = [
		{
			icon: '🌿',
			title: 'Natural & Pure',
			description: 'We use only the finest natural ingredients, free from harmful chemicals and synthetic fragrances.'
		},
		{
			icon: '🙏',
			title: 'Traditional Craftsmanship',
			description: 'Our agarbatti are handcrafted using ancient techniques passed down through generations.'
		},
		{
			icon: '♻️',
			title: 'Sustainable',
			description: 'We are committed to eco-friendly practices and sustainable sourcing of all ingredients.'
		},
		{
			icon: '💝',
			title: 'Made with Love',
			description: 'Every stick is crafted with devotion and care to bring peace to your sacred space.'
		}
	];
	
	const timeline = [
		{
			year: '1985',
			title: 'The Beginning',
			description: 'Started as a small family business with a passion for creating authentic incense.'
		},
		{
			year: '2000',
			title: 'Expansion',
			description: 'Expanded our range to include various traditional and exotic fragrances.'
		},
		{
			year: '2015',
			title: 'Going Premium',
			description: 'Launched our premium line focusing on highest quality natural ingredients.'
		},
		{
			year: '2025',
			title: 'Today',
			description: 'Serving thousands of happy customers across India with our divine fragrances.'
		}
	];
</script>

<svelte:head>
	<title>About Us - Agarbatti Premium Agarbatti</title>
	<meta name="description" content="Learn about Agarbatti's journey in crafting premium handcrafted agarbatti with natural ingredients and traditional methods." />
</svelte:head>

<!-- Hero Section -->
<section class="relative py-20 bg-gradient-to-br from-amber-50 via-orange-50 to-amber-100">
	<div class="container mx-auto px-4">
		<div class="text-center space-y-6" class:fade-in={mounted}>
			<div class="inline-block mb-4 floating-animation">
				<div class="w-24 h-24 bg-gradient-to-br from-brand-secondary to-brand-primary rounded-full flex items-center justify-center shadow-2xl">
					<span class="text-5xl">🕉️</span>
				</div>
			</div>
			<h1 class="text-5xl md:text-6xl font-display font-bold gradient-text">
				Our Story
			</h1>
			<p class="text-xl text-gray-600 max-w-3xl mx-auto leading-relaxed">
				A journey of devotion, tradition, and the pursuit of creating the perfect 
				fragrance to elevate your spiritual experience.
			</p>
		</div>
	</div>
</section>

<!-- Mission Section -->
<section class="py-20 bg-white">
	<div class="container mx-auto px-4">
		<div class="max-w-4xl mx-auto">
			<div class="text-center mb-12 slide-up">
				<h2 class="text-4xl md:text-5xl font-display font-bold text-brand-primary mb-6">
					Our Mission
				</h2>
				<div class="w-24 h-1 bg-gradient-to-r from-brand-secondary to-brand-accent mx-auto rounded-full mb-8"></div>
			</div>
			
			<div class="prose prose-lg max-w-none slide-up">
				<p class="text-gray-700 text-lg leading-relaxed mb-6">
					At <span class="font-semibold text-brand-primary">Agarbatti</span>, we believe that fragrance has 
					the power to transform spaces and elevate spiritual experiences. For over three decades, 
					we have been dedicated to crafting premium agarbatti that honors ancient traditions while 
					meeting modern standards of quality and purity.
				</p>
				<p class="text-gray-700 text-lg leading-relaxed mb-6">
					Every stick of incense we create is a labor of love, carefully handcrafted using time-honored 
					techniques and the finest natural ingredients sourced from across India. We refuse to compromise 
					on quality, ensuring that each fragrance is authentic, long-lasting, and free from harmful chemicals.
				</p>
				<p class="text-gray-700 text-lg leading-relaxed">
					Our commitment goes beyond creating exceptional products. We strive to preserve traditional 
					craftsmanship, support local artisans, and maintain sustainable practices that respect both 
					our heritage and our environment.
				</p>
			</div>
		</div>
	</div>
</section>

<!-- Values Section -->
<section class="py-20 bg-gradient-to-br from-amber-50 to-orange-50">
	<div class="container mx-auto px-4">
		<div class="text-center mb-16 slide-up">
			<h2 class="text-4xl md:text-5xl font-display font-bold text-brand-primary mb-4">
				Our Values
			</h2>
			<div class="w-24 h-1 bg-gradient-to-r from-brand-secondary to-brand-accent mx-auto rounded-full"></div>
		</div>
		
		<div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-5xl mx-auto">
			{#each values as value, i}
				<div 
					class="card p-8 bg-white hover:shadow-2xl transition-all duration-300 hover:-translate-y-2 slide-up"
					style="animation-delay: {i * 0.1}s;"
				>
					<div class="text-6xl mb-4 floating-animation" style="animation-delay: {i * 0.5}s;">
						{value.icon}
					</div>
					<h3 class="text-2xl font-semibold text-brand-primary mb-3">
						{value.title}
					</h3>
					<p class="text-gray-600 leading-relaxed">
						{value.description}
					</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- Timeline Section -->
<section class="py-20 bg-white">
	<div class="container mx-auto px-4">
		<div class="text-center mb-16 slide-up">
			<h2 class="text-4xl md:text-5xl font-display font-bold text-brand-primary mb-4">
				Our Journey
			</h2>
			<div class="w-24 h-1 bg-gradient-to-r from-brand-secondary to-brand-accent mx-auto rounded-full"></div>
		</div>
		
		<div class="max-w-4xl mx-auto">
			<div class="space-y-12">
				{#each timeline as event, i}
					<div class="flex gap-8 slide-up" style="animation-delay: {i * 0.15}s;">
						<div class="flex-shrink-0 w-32 text-right">
							<span class="text-3xl font-display font-bold gradient-text">
								{event.year}
							</span>
						</div>
						<div class="flex-shrink-0 w-4 relative">
							<div class="w-4 h-4 bg-gradient-to-br from-brand-secondary to-brand-accent rounded-full border-4 border-white shadow-lg"></div>
							{#if i < timeline.length - 1}
								<div class="absolute top-4 left-1/2 w-0.5 h-full bg-gradient-to-b from-brand-secondary to-brand-accent transform -translate-x-1/2"></div>
							{/if}
						</div>
						<div class="flex-grow pb-12">
							<h3 class="text-2xl font-semibold text-brand-primary mb-2">
								{event.title}
							</h3>
							<p class="text-gray-600 leading-relaxed">
								{event.description}
							</p>
						</div>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>

<!-- Contact Section -->
<section class="py-20 bg-gradient-to-r from-brand-primary via-amber-900 to-brand-primary text-white">
	<div class="container mx-auto px-4">
		<div class="max-w-4xl mx-auto text-center">
			<h2 class="text-4xl md:text-5xl font-display font-bold mb-6">
				Get in Touch
			</h2>
			<p class="text-xl mb-12 text-amber-100">
				Have questions about our products or want to place a bulk order? We'd love to hear from you!
			</p>
			
			<div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-12">
				<div class="space-y-2">
					<div class="text-4xl mb-2">📧</div>
					<h3 class="text-lg font-semibold">Email</h3>
					<p class="text-amber-200">contact@Agarbatti.com</p>
					<p class="text-amber-200">orders@Agarbatti.com</p>
				</div>
				<div class="space-y-2">
					<div class="text-4xl mb-2">📱</div>
					<h3 class="text-lg font-semibold">Phone</h3>
					<p class="text-amber-200">+91 98765 43210</p>
					<p class="text-amber-200">+91 98765 43211</p>
				</div>
				<div class="space-y-2">
					<div class="text-4xl mb-2">📍</div>
					<h3 class="text-lg font-semibold">Location</h3>
					<p class="text-amber-200">Mumbai, Maharashtra</p>
					<p class="text-amber-200">India - 400001</p>
				</div>
			</div>
			
			<div class="flex flex-col sm:flex-row gap-4 justify-center">
				<a 
					href="mailto:contact@Agarbatti.com" 
					class="btn bg-white text-brand-primary px-8 py-4 rounded-full hover:scale-105 transition-transform duration-300 shadow-xl font-semibold"
				>
					Send us an Email
				</a>
				<a 
					href="/catalogue" 
					class="btn bg-brand-secondary text-white px-8 py-4 rounded-full hover:scale-105 transition-transform duration-300 shadow-xl font-semibold"
				>
					View Catalogue
				</a>
			</div>
		</div>
	</div>
</section>

<!-- Testimonials Section -->
<section class="py-20 bg-gradient-to-br from-white via-amber-50/30 to-white">
	<div class="container mx-auto px-4">
		<div class="text-center mb-16 slide-up">
			<h2 class="text-4xl md:text-5xl font-display font-bold text-brand-primary mb-4">
				What Our Customers Say
			</h2>
			<div class="w-24 h-1 bg-gradient-to-r from-brand-secondary to-brand-accent mx-auto rounded-full"></div>
		</div>
		
		<div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-6xl mx-auto">
			{#each [
				{ name: 'Priya Sharma', text: 'The best agarbatti I have ever used! The fragrances are divine and long-lasting.', rating: 5 },
				{ name: 'Rajesh Kumar', text: 'Pure quality and authentic scents. Highly recommend for daily puja and meditation.', rating: 5 },
				{ name: 'Anjali Desai', text: 'Love the natural ingredients and the beautiful packaging. Perfect for gifting too!', rating: 5 }
			] as testimonial, i}
				<div class="card p-6 bg-white hover:shadow-xl transition-all duration-300 slide-up" style="animation-delay: {i * 0.1}s;">
					<div class="flex items-center space-x-1 mb-4">
						{#each Array(testimonial.rating) as _}
							<span class="text-brand-secondary text-xl">⭐</span>
						{/each}
					</div>
					<p class="text-gray-600 italic mb-4 leading-relaxed">
						"{testimonial.text}"
					</p>
					<p class="font-semibold text-brand-primary">
						— {testimonial.name}
					</p>
				</div>
			{/each}
		</div>
	</div>
</section>

