<script>
  /**
   * @typedef {{ name: string; class?: string }} Props
   * @type {Props}
   */
  let { name, class: cls = 'h-7 w-7' } = $props();
</script>

{#if name === 'car'}
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round" class={cls}>
    <path d="M5 17h14"/>
    <path d="M5 17v2a1 1 0 001 1h2a1 1 0 001-1v-2"/>
    <path d="M15 17v2a1 1 0 001 1h2a1 1 0 001-1v-2"/>
    <path d="M3 13l1.5-4A3 3 0 017.4 7h9.2a3 3 0 012.9 2l1.5 4"/>
    <path d="M3 13h18v4H3z"/>
    <circle cx="7.5" cy="15" r=".7" fill="currentColor"/>
    <circle cx="16.5" cy="15" r=".7" fill="currentColor"/>
  </svg>
{:else if name === 'key-immo'}
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round" class={cls}>
    <rect x="6" y="4" width="12" height="14" rx="3"/>
    <circle cx="12" cy="9" r="1.4" fill="currentColor"/>
    <path d="M12 12v3"/>
    <path d="M9 18v2"/>
    <path d="M15 18v2"/>
  </svg>
{:else if name === 'motor'}
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round" class={cls}>
    <circle cx="5.5" cy="16" r="3"/>
    <circle cx="18.5" cy="16" r="3"/>
    <path d="M5.5 16L9 9h4l3 4"/>
    <path d="M16 13l2.5 3"/>
    <path d="M11 9V6h2"/>
  </svg>
{:else if name === 'home'}
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round" class={cls}>
    <path d="M3 11l9-7 9 7"/>
    <path d="M5 10v10h14V10"/>
    <circle cx="14" cy="15" r="1.2" fill="currentColor"/>
    <path d="M14 16.2V18"/>
  </svg>
{:else if name === 'safe'}
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round" class={cls}>
    <rect x="3" y="4" width="18" height="16" rx="2"/>
    <circle cx="11" cy="12" r="3.5"/>
    <path d="M11 8.5v-1"/>
    <path d="M11 15.5v1"/>
    <path d="M14.5 12h1"/>
    <path d="M7.5 12h-1"/>
    <path d="M18 11v2"/>
  </svg>
{:else if name === 'install'}
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round" class={cls}>
    <path d="M14.7 6.3a4 4 0 015.6 5.6l-2.1 2.1-5.6-5.6 2.1-2.1z"/>
    <path d="M12.6 8.4l-7.3 7.3a2 2 0 000 2.8l.2.2a2 2 0 002.8 0l7.3-7.3"/>
    <path d="M9 16l-1.5 1.5"/>
  </svg>
{:else if name === 'shield'}
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round" class={cls}>
    <path d="M12 3l8 3v6c0 5-3.5 8-8 9-4.5-1-8-4-8-9V6l8-3z"/>
    <path d="M9.5 12.5l2 2 3.5-3.5"/>
  </svg>
{:else if name === 'clock'}
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round" class={cls}>
    <circle cx="12" cy="12" r="9"/>
    <path d="M12 7v5l3 2"/>
  </svg>
{:else if name === 'pin'}
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round" class={cls}>
    <path d="M12 22s7-7.5 7-12a7 7 0 10-14 0c0 4.5 7 12 7 12z"/>
    <circle cx="12" cy="10" r="2.5"/>
  </svg>
{:else if name === 'phone'}
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round" class={cls}>
    <path d="M5 4h3l2 5-2.5 1.5a11 11 0 005 5L14 13l5 2v3a2 2 0 01-2 2A14 14 0 013 6a2 2 0 012-2z"/>
  </svg>
{:else if name === 'check'}
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class={cls}>
    <path d="M5 12.5l4 4L19 7"/>
  </svg>
{:else if name === 'star'}
  <svg viewBox="0 0 24 24" fill="currentColor" class={cls}>
    <path d="M12 2.5l2.95 6 6.55.95-4.75 4.6 1.12 6.5L12 17.6l-5.87 3 1.12-6.5L2.5 9.45 9.05 8.5z"/>
  </svg>
{:else if name === 'plus'}
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" class={cls}>
    <path d="M12 5v14M5 12h14"/>
  </svg>
{:else if name === 'minus'}
  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" class={cls}>
    <path d="M5 12h14"/>
  </svg>
{:else if name === 'lightning'}
  <svg viewBox="0 0 24 24" fill="currentColor" class={cls}>
    <path d="M13 2L4 14h7l-1 8 9-12h-7l1-8z"/>
  </svg>
{/if}
