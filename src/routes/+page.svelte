<script></script>

<div class="mx-auto max-w-5xl pt-28 text-center text-[#0D494E]">
	<!-- Hero Section -->
	<section class="hero rounded-lg bg-base-200 p-8 shadow-lg">
		<div class="hero-content flex flex-col lg:flex-row-reverse">
			<img
				src="/images/product-4.jpg"
				class="max-w-xs rounded-lg shadow-2xl"
				alt="Featured Product"
			/>
			<div>
				<h1 class="text-5xl font-bold">Shop Our Latest Collection!</h1>
				<p class="py-4">Discover high-quality products tailored to your needs.</p>
				<button class="btn bg-green-400 text-[#0D494E] hover:bg-[#0D494E] hover:text-[white]"
					>Shop Now</button
				>
			</div>
		</div>
	</section>

	<!-- Featured Products Section -->
	<section class="my-5 text-[#0D494E]">
		<h2 class="my-5 text-2xl font-bold">Featured Products</h2>
		<div class="grid grid-cols-1 gap-4 md:grid-cols-3 lg:grid-cols-4">
			<!-- Mockup Product Cards (Replace with dynamic product data) -->
			{#each Array(4) as _, i}
				<div
					class="card bg-[#f5fffe] text-[#0D494E] shadow-md transition-shadow duration-300 hover:shadow-lg"
				>
					<figure>
						<img src={`/images/product-${i + 1}.jpg`} alt="Product" class="h-60 w-full" />
					</figure>
					<div class="card-body">
						<h2 class="card-title">Product {i + 1}</h2>
						<p class="text-start">₦2,999</p>
						<button class="btn bg-green-400 text-[#0D494E] hover:bg-[#0D494E] hover:text-[white]"
							>Add to Cart</button
						>
					</div>
				</div>
			{/each}
		</div>
	</section>

	<!-- Categories Section -->
	<section class="py-8">
		<h2 class="mb-4 text-2xl font-bold">Categories</h2>
		<div class="flex flex-wrap gap-4">
			{#each ['Market Errands', 'Party Packs', 'Local Snacks'] as category}
				<div class="btn btn-outline border-green-400 text-[#0D494E] hover:bg-[#0D494E]">
					{category}
				</div>
			{/each}
		</div>
	</section>

	<!-- Testimonials Section -->
	<section class="rounded-lg bg-base-100 p-6 shadow">
		<h2 class="mb-4 text-2xl font-bold">Customer Testimonials</h2>
		<div class="flex flex-row gap-10">
			<div
				class="card bg-[#f5fffe] text-[#0D494E] shadow-md transition-shadow duration-300 hover:shadow-lg"
			>
				<figure><img src="/images/bm_review.jpg" alt="Product" class="h-60 w-full" /></figure>
				<div class="card-body">
					<blockquote class="italic">"... I was impressed when I received your goods. Neat and hygienically packaged..." - Amazing customer</blockquote>
				</div>
			</div>
			<div
				class="card bg-[#f5fffe] text-[#0D494E] shadow-md transition-shadow duration-300 hover:shadow-lg"
			>
				<figure><img src="/images/bm_review_2.jpg" alt="Product" class="h-60 w-full" /></figure>
				<div class="card-body">
					<blockquote class="italic">"Amazing products and great service!" - Amazing customer</blockquote>
				</div>
			</div>
            <div
				class="card bg-[#f5fffe] text-[#0D494E] shadow-md transition-shadow duration-300 hover:shadow-lg"
			>
				<figure><img src="/images/bm_review_2.jpg" alt="Product" class="h-60 w-full" /></figure>
				<div class="card-body">
					<blockquote class="italic">"very okay, neatly packed so I love it" - Amazing Customer</blockquote>
				</div>
			</div>
		</div>
	</section>
</div>
