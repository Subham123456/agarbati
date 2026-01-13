<script lang="ts">
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import { page } from '$app/stores';
	
	let mobileMenuOpen = false;
	
	const navItems = [
		{ label: 'Home', href: '/' },
		{ label: 'Catalogue', href: '/catalogue' },
		{ label: 'About', href: '/about' }
	];
	
	function toggleMobileMenu() {
		mobileMenuOpen = !mobileMenuOpen;
	}
</script>

<AppShell>
	<svelte:fragment slot="header">
		<AppBar background="bg-gradient-to-r from-brand-primary via-amber-900 to-brand-primary shadow-xl">
			<svelte:fragment slot="lead">
				<a href="/" class="flex items-center space-x-3 group">
					<div class="w-12 h-12 bg-brand-secondary rounded-full flex items-center justify-center transform group-hover:rotate-12 transition-transform duration-300">
						<span class="text-2xl">🕉️</span>
					</div>
					<div class="flex flex-col">
						<strong class="text-2xl font-display text-brand-secondary tracking-wide">Agarbatti</strong>
						<span class="text-xs text-amber-200 tracking-widest">PREMIUM AGARBATTI</span>
					</div>
				</a>
			</svelte:fragment>
			
			<svelte:fragment slot="trail">
				<!-- Desktop Navigation -->
				<nav class="hidden md:flex items-center space-x-8">
					{#each navItems as item}
						<a 
							href={item.href} 
							class="relative text-lg font-medium text-white hover:text-brand-secondary transition-colors duration-300 group"
							class:text-brand-secondary={$page.url.pathname === item.href}
						>
							{item.label}
							<span class="absolute bottom-0 left-0 w-0 h-0.5 bg-brand-secondary group-hover:w-full transition-all duration-300"></span>
						</a>
					{/each}
				</nav>
				
				<!-- Mobile Menu Button -->
				<button 
					class="btn btn-sm md:hidden text-white"
					on:click={toggleMobileMenu}
					aria-label="Toggle menu"
				>
					<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						{#if mobileMenuOpen}
							<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
						{:else}
							<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
						{/if}
					</svg>
				</button>
			</svelte:fragment>
		</AppBar>
		
		<!-- Mobile Menu -->
		{#if mobileMenuOpen}
			<div class="md:hidden bg-brand-primary border-t border-brand-secondary/20 slide-up">
				<nav class="flex flex-col p-4 space-y-2">
					{#each navItems as item}
						<a 
							href={item.href} 
							class="text-white hover:text-brand-secondary p-3 rounded-lg transition-all {$page.url.pathname === item.href ? 'bg-white/10 text-brand-secondary' : 'hover:bg-white/10'}"
							on:click={toggleMobileMenu}
						>
							{item.label}
						</a>
					{/each}
				</nav>
			</div>
		{/if}
	</svelte:fragment>
	
	<!-- Page Content -->
	<main class="min-h-screen">
		<slot />
	</main>
	
	<!-- Footer -->
	<svelte:fragment slot="pageFooter">
		<footer class="bg-gradient-to-r from-gray-900 via-gray-800 to-gray-900 text-white py-12 mt-20">
			<div class="container mx-auto px-4">
				<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
					<!-- Brand Section -->
					<div class="space-y-4">
						<div class="flex items-center space-x-3">
							<div class="w-10 h-10 bg-brand-secondary rounded-full flex items-center justify-center">
								<span class="text-xl">🕉️</span>
							</div>
							<h3 class="text-2xl font-display text-brand-secondary">Agarbatti</h3>
						</div>
						<p class="text-gray-400 text-sm leading-relaxed">
							Premium handcrafted agarbatti bringing divine fragrances to your home. 
							Made with natural ingredients and ancient traditions.
						</p>
					</div>
					
					<!-- Quick Links -->
					<div class="space-y-4">
						<h4 class="text-lg font-semibold text-brand-secondary">Quick Links</h4>
						<ul class="space-y-2">
							{#each navItems as item}
								<li>
									<a href={item.href} class="text-gray-400 hover:text-brand-secondary transition-colors">
										{item.label}
									</a>
								</li>
							{/each}
						</ul>
					</div>
					
					<!-- Contact Info -->
					<div class="space-y-4">
						<h4 class="text-lg font-semibold text-brand-secondary">Contact Us</h4>
						<ul class="space-y-2 text-gray-400 text-sm">
							<li class="flex items-center space-x-2">
								<span>📧</span>
								<span>contact@Agarbatti.com</span>
							</li>
							<li class="flex items-center space-x-2">
								<span>📱</span>
								<span>+91 98765 43210</span>
							</li>
							<li class="flex items-center space-x-2">
								<span>📍</span>
								<span>Mumbai, Maharashtra, India</span>
							</li>
						</ul>
					</div>
				</div>
				
				<div class="border-t border-gray-700 mt-8 pt-8 text-center">
					<p class="text-gray-400 text-sm">
						© {new Date().getFullYear()} Agarbatti. All rights reserved. Crafted with 💝 and devotion.
					</p>
				</div>
			</div>
		</footer>
	</svelte:fragment>
</AppShell>

