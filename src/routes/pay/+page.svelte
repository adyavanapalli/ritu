<script lang="ts">
  import { page } from "$app/state";

  const params = $derived(page.url.searchParams);
  const upiUrl = $derived(`upi://pay?${params.toString()}`);
</script>

<svelte:head>
  <title>RITU - Pay via UPI</title>
</svelte:head>

<main class="grid min-h-dvh place-items-center p-4">
  <div
    class="flex w-full max-w-sm flex-col gap-8 rounded-2xl border border-ctp-surface1 bg-ctp-mantle p-8 text-center"
  >
    {#if params.get("am")}
      <p class="text-4xl font-bold text-ctp-text">
        {params.get("cu") ?? "INR"} {params.get("am")}
      </p>
    {/if}

    {#if params.get("pa") || params.get("pn") || params.get("tn")}
      <dl
        class="grid grid-cols-[auto_1fr] items-baseline gap-x-6 gap-y-1 text-left"
      >
        {#if params.get("pn")}
          <dt class="text-sm text-ctp-overlay1">To</dt>
          <dd class="font-medium text-ctp-subtext1">{params.get("pn")}</dd>
        {/if}
        {#if params.get("pa")}
          <dt class="text-sm text-ctp-overlay1">UPI ID</dt>
          <dd class="break-all font-medium text-ctp-subtext1">{params.get("pa")}</dd>
        {/if}
        {#if params.get("tn")}
          <dt class="text-sm text-ctp-overlay1">Note</dt>
          <dd class="font-medium text-ctp-subtext1">{params.get("tn")}</dd>
        {/if}
      </dl>
    {/if}

    <a
      href={upiUrl}
      class="block rounded-xl bg-ctp-green px-4 py-3.5 text-lg font-semibold text-ctp-crust no-underline"
    >
      Pay via UPI
    </a>
  </div>
</main>
