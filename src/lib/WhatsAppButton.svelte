<script>
  import { business } from '$lib/data.js';

  /**
   * @typedef {{
   *   variant?: 'primary' | 'secondary' | 'light';
   *   size?: 'md' | 'lg';
   *   message?: string;
   *   children?: any;
   *   class?: string;
   * }} Props
   * @type {Props}
   */
  let {
    variant = 'primary',
    size = 'md',
    message,
    children,
    class: cls = ''
  } = $props();

  const text = message ?? business.whatsappMessage;
  const link = `https://wa.me/${business.phoneIntl}?text=${encodeURIComponent(text)}`;

  const variants = {
    primary:
      'bg-[#25D366] text-white hover:bg-[#1ebe5b] shadow-lg shadow-emerald-900/20 ring-1 ring-emerald-800/10',
    secondary:
      'bg-white text-emerald-700 hover:bg-emerald-50 ring-1 ring-emerald-200',
    light:
      'bg-emerald-50 text-emerald-800 hover:bg-emerald-100 ring-1 ring-emerald-200'
  };

  const sizes = {
    md: 'px-5 py-3 text-sm',
    lg: 'px-6 py-4 text-base'
  };
</script>

<a
  href={link}
  target="_blank"
  rel="noopener"
  class="inline-flex items-center justify-center gap-2 rounded-full font-semibold transition-all hover:-translate-y-0.5 active:translate-y-0 {variants[variant]} {sizes[size]} {cls}"
>
  <svg
    viewBox="0 0 32 32"
    aria-hidden="true"
    class="h-5 w-5 fill-current"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      d="M19.11 17.205c-.372 0-1.088 1.39-1.518 1.39a.63.63 0 0 1-.315-.1c-.802-.402-1.504-.817-2.163-1.447-.545-.516-1.146-1.29-1.46-1.963a.426.426 0 0 1-.073-.215c0-.33.99-.945.99-1.49 0-.143-.73-2.122-.832-2.367-.116-.282-.514-.397-.787-.397-.157 0-.358.04-.484.082-.728.245-1.222 1.03-1.222 1.853 0 .846.342 1.668.74 2.426 1.397 2.667 3.18 5.21 5.99 6.532.79.372 2.16.882 3.04.882.85 0 1.91-.42 2.27-1.27.156-.366.225-.766.225-1.156 0-.27-.024-.516-.16-.745-.16-.265-1.85-1.018-2.24-1.018zM16.045 6c-5.514 0-10.043 4.5-10.043 10.045 0 1.93.55 3.815 1.59 5.444L6 26.13l4.78-1.557a10.07 10.07 0 0 0 5.265 1.474h.005c5.514 0 10.045-4.5 10.045-10.045 0-2.69-1.05-5.215-2.945-7.115A10.077 10.077 0 0 0 16.045 6m0 18.4a8.34 8.34 0 0 1-4.255-1.165l-.305-.18-3.155 1.025 1.025-3.075-.2-.32a8.34 8.34 0 0 1-1.27-4.43c0-4.605 3.755-8.355 8.36-8.355 2.235 0 4.33.875 5.91 2.46a8.31 8.31 0 0 1 2.45 5.9c0 4.605-3.755 8.355-8.36 8.355"
    />
  </svg>
  {@render children?.()}
</a>
