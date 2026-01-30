<svelte:head>
	<title>RITU - Redirect Intent To UPI</title>
</svelte:head>

<main class="mx-auto flex h-dvh max-w-2xl flex-col justify-center gap-8 px-6">
	<header class="text-center">
		<h1 class="mb-1 text-5xl font-bold text-ctp-text">RITU</h1>
		<p class="text-ctp-subtext0">
			<strong class="text-ctp-mauve">R</strong>edirect
			<strong class="text-ctp-mauve">I</strong>ntent
			<strong class="text-ctp-mauve">T</strong>o
			<strong class="text-ctp-mauve">U</strong>PI
		</p>
	</header>

	<section>
		<h2 class="mb-2 text-xl font-semibold text-ctp-text">What is this?</h2>
		<p class="text-ctp-subtext1">
			RITU turns a regular HTTPS link into a
			<code class="rounded bg-ctp-surface0 px-1.5 py-0.5 text-sm text-ctp-peach">upi://</code>
			deep link that opens your UPI app directly. Share payment links over SMS, email, or
			anywhere that doesn't support custom URI schemes.
		</p>
	</section>

	<section>
		<h2 class="mb-2 text-xl font-semibold text-ctp-text">Parameters</h2>
		<div class="overflow-x-auto rounded-lg border border-ctp-surface1">
			<table class="w-full text-left text-sm">
				<thead class="border-b border-ctp-surface1 bg-ctp-mantle">
					<tr>
						<th class="px-4 py-2.5 font-medium text-ctp-subtext0">Param</th>
						<th class="px-4 py-2.5 font-medium text-ctp-subtext0">Description</th>
					</tr>
				</thead>
				<tbody class="divide-y divide-ctp-surface0">
					<tr>
						<td class="px-4 py-2 font-mono text-ctp-peach">pa</td>
						<td class="px-4 py-2 text-ctp-subtext1">Payee UPI address (e.g. <code class="text-ctp-overlay2">ritu@ybl</code>)</td>
					</tr>
					<tr>
						<td class="px-4 py-2 font-mono text-ctp-peach">pn</td>
						<td class="px-4 py-2 text-ctp-subtext1">Payee name</td>
					</tr>
					<tr>
						<td class="px-4 py-2 font-mono text-ctp-peach">am</td>
						<td class="px-4 py-2 text-ctp-subtext1">Amount (up to 2 decimal places)</td>
					</tr>
					<tr>
						<td class="px-4 py-2 font-mono text-ctp-peach">tn</td>
						<td class="px-4 py-2 text-ctp-subtext1">Transaction note (max 80 chars)</td>
					</tr>
				</tbody>
			</table>
		</div>
	</section>

	<section>
		<h2 class="mb-2 text-xl font-semibold text-ctp-text">Example</h2>
		<p class="mb-3 text-ctp-subtext1">
			Pay <strong class="text-ctp-text">Ritu</strong> ₹50 for coffee:
		</p>
		<a
			href="https://payviaupi.link/pay?pa=ritu@ybl&pn=Ritu&am=50&tn=coffee"
			class="block break-all rounded-lg border border-ctp-surface1 bg-ctp-mantle px-4 py-3 text-sm text-ctp-blue hover:text-ctp-sapphire"
		>
			https://payviaupi.link/pay?pa=ritu@ybl&amp;pn=Ritu&amp;am=50&amp;tn=coffee
		</a>
		<p class="mt-3 text-sm text-ctp-overlay1">
			On a phone, this opens the UPI app chooser with the payee, amount, and note pre-filled.
		</p>
	</section>
</main>
