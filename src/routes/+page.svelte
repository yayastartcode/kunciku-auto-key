<script>
  import {
    business,
    services,
    trust,
    process,
    testimonials,
    gallery,
    faqs
  } from '$lib/data.js';
  import WhatsAppFloat from '$lib/WhatsAppFloat.svelte';
  import WhatsAppButton from '$lib/WhatsAppButton.svelte';
  import Icon from '$lib/Icon.svelte';

  let openFaq = $state(0);
  function toggle(i) {
    openFaq = openFaq === i ? -1 : i;
  }

  const telLink = `tel:+${business.phoneIntl}`;
  const mapsLink = `https://www.google.com/maps/search/?api=1&query=${encodeURIComponent(business.mapsQuery)}`;
</script>

<svelte:head>
  <title>Kunciku Auto Key - Ahli Kunci Pekanbaru 24 Jam | Buka Kunci Mobil, Motor, Rumah</title>
</svelte:head>

<WhatsAppFloat />

<!-- ==================== TOP BAR ==================== -->
<header class="sticky top-0 z-40 backdrop-blur bg-white/80 border-b border-slate-200/70">
  <div class="mx-auto max-w-6xl px-4 sm:px-6 h-14 flex items-center justify-between">
    <a href="#top" class="flex items-center gap-2 font-bold tracking-tight">
      <span class="grid place-items-center h-8 w-8 rounded-lg bg-gradient-to-br from-brand-400 to-brand-600 text-white shadow">
        <Icon name="key-immo" class="h-4 w-4" />
      </span>
      <span class="text-slate-900">Kunciku Auto Key</span>
    </a>

    <nav class="hidden md:flex items-center gap-7 text-sm font-medium text-slate-600">
      <a href="#layanan" class="hover:text-slate-900">Layanan</a>
      <a href="#proses" class="hover:text-slate-900">Cara Kerja</a>
      <a href="#galeri" class="hover:text-slate-900">Galeri</a>
      <a href="#testimoni" class="hover:text-slate-900">Testimoni</a>
      <a href="#faq" class="hover:text-slate-900">FAQ</a>
      <a href="#kontak" class="hover:text-slate-900">Kontak</a>
    </nav>

    <a
      href={telLink}
      class="hidden sm:inline-flex items-center gap-2 rounded-full bg-slate-900 text-white px-4 py-2 text-xs font-semibold hover:bg-slate-800"
    >
      <Icon name="phone" class="h-4 w-4" />
      {business.phone}
    </a>
  </div>
</header>

<main id="top">
  <!-- ==================== HERO ==================== -->
  <section class="relative overflow-hidden bg-slate-900 text-white">
    <div class="absolute inset-0 bg-grid opacity-40"></div>
    <div
      class="absolute -top-40 -right-32 w-[36rem] h-[36rem] rounded-full bg-brand-500/30 blur-3xl"
    ></div>
    <div
      class="absolute -bottom-40 -left-20 w-[30rem] h-[30rem] rounded-full bg-emerald-500/20 blur-3xl"
    ></div>

    <div class="relative mx-auto max-w-6xl px-4 sm:px-6 pt-12 pb-16 md:pt-20 md:pb-24">
      <div class="grid md:grid-cols-12 gap-10 items-center">
        <div class="md:col-span-7 animate-fade-up">
          <span
            class="inline-flex items-center gap-2 rounded-full bg-emerald-500/15 ring-1 ring-emerald-400/40 text-emerald-300 px-3 py-1 text-xs font-semibold"
          >
            <span class="relative flex h-2 w-2">
              <span class="absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75 animate-[pulse-ring_1.6s_ease-out_infinite]"></span>
              <span class="relative inline-flex rounded-full h-2 w-2 bg-emerald-400"></span>
            </span>
            Online sekarang - Siap dipanggil 24 jam
          </span>

          <h1 class="mt-5 text-4xl sm:text-5xl md:text-6xl font-extrabold leading-[1.05] tracking-tight">
            Ahli Kunci <span class="text-brand-300">Pekanbaru</span>,
            datang ke lokasi
            <span class="relative inline-block">
              <span class="relative z-10">tanpa rusak</span>
              <span class="absolute inset-x-0 bottom-1 h-3 bg-brand-500/40 rounded-sm -z-0"></span>
            </span>
            pintu.
          </h1>

          <p class="mt-5 text-lg text-slate-300 max-w-xl">
            Mobil terkunci? Kunci motor patah? Rumah atau brankas tidak bisa
            dibuka? Tim Kunciku Auto Key bantu Anda di Panam, Pekanbaru, dan
            sekitar Riau. Cepat, aman, bergaransi.
          </p>

          <div class="mt-7 flex flex-col sm:flex-row gap-3">
            <WhatsAppButton size="lg" variant="primary">
              Chat WhatsApp Sekarang
            </WhatsAppButton>
            <a
              href={telLink}
              class="inline-flex items-center justify-center gap-2 rounded-full bg-white/10 ring-1 ring-white/20 backdrop-blur px-6 py-4 text-base font-semibold text-white hover:bg-white/15"
            >
              <Icon name="phone" class="h-5 w-5" />
              Telepon {business.phone}
            </a>
          </div>

          <div class="mt-8 flex flex-wrap items-center gap-x-6 gap-y-3 text-sm text-slate-300">
            <div class="inline-flex items-center gap-2"><Icon name="clock" class="h-4 w-4 text-brand-300"/>Buka 24 jam</div>
            <div class="inline-flex items-center gap-2"><Icon name="shield" class="h-4 w-4 text-brand-300"/>Bergaransi</div>
            <div class="inline-flex items-center gap-2"><Icon name="pin" class="h-4 w-4 text-brand-300"/>Panam, Pekanbaru</div>
          </div>
        </div>

        <!-- Hero card -->
        <div class="md:col-span-5 animate-fade-up delay-2">
          <div class="relative">
            <div
              class="absolute -inset-4 rounded-3xl bg-gradient-to-br from-brand-400/40 via-brand-500/20 to-emerald-500/30 blur-2xl"
            ></div>
            <div
              class="relative rounded-3xl bg-white/95 text-slate-900 shadow-2xl ring-1 ring-white/20 p-6 sm:p-7"
            >
              <div class="flex items-center justify-between">
                <div class="flex items-center gap-2">
                  <span class="grid place-items-center h-10 w-10 rounded-xl bg-brand-500 text-white">
                    <Icon name="lightning" class="h-5 w-5"/>
                  </span>
                  <div>
                    <p class="text-xs uppercase tracking-wider text-slate-500 font-semibold">Estimasi tiba</p>
                    <p class="text-lg font-bold">15-30 menit di Panam</p>
                  </div>
                </div>
                <span class="text-xs font-semibold text-emerald-700 bg-emerald-50 ring-1 ring-emerald-200 rounded-full px-3 py-1">
                  Aktif
                </span>
              </div>

              <ul class="mt-5 space-y-3 text-sm">
                {#each ['Buka kunci tanpa merusak pintu/jok', 'Estimasi biaya transparan via WhatsApp', 'Teknisi berseragam & beralat lengkap', 'Garansi pekerjaan & kuitansi resmi'] as item}
                  <li class="flex items-start gap-2.5">
                    <span class="mt-0.5 grid place-items-center h-5 w-5 rounded-full bg-emerald-500 text-white">
                      <Icon name="check" class="h-3.5 w-3.5" />
                    </span>
                    <span>{item}</span>
                  </li>
                {/each}
              </ul>

              <div class="mt-6 grid grid-cols-2 gap-3">
                <WhatsAppButton variant="primary" size="md" message="Halo, saya butuh bantuan ahli kunci darurat. Lokasi saya:">
                  Bantuan Darurat
                </WhatsAppButton>
                <WhatsAppButton variant="light" size="md" message="Halo, saya mau tanya estimasi harga untuk:">
                  Tanya Harga
                </WhatsAppButton>
              </div>

              <p class="mt-4 text-[11px] text-slate-500">
                Mengirim pesan akan membuka WhatsApp ke nomor {business.phone}.
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- Trust strip -->
      <div class="mt-12 grid grid-cols-2 sm:grid-cols-4 gap-3 sm:gap-6">
        {#each trust as t, i}
          <div class="rounded-2xl bg-white/5 ring-1 ring-white/10 backdrop-blur px-4 py-4 sm:px-5 sm:py-5 animate-fade-up" style="animation-delay: {0.1 * i}s">
            <p class="text-2xl sm:text-3xl font-extrabold text-brand-300">{t.value}</p>
            <p class="mt-1 text-xs sm:text-sm text-slate-300">{t.label}</p>
          </div>
        {/each}
      </div>
    </div>
  </section>

  <!-- ==================== EMERGENCY STRIP ==================== -->
  <section class="relative bg-brand-500 text-white">
    <div class="mx-auto max-w-6xl px-4 sm:px-6 py-4 flex flex-col sm:flex-row items-center justify-between gap-3 text-sm">
      <p class="font-semibold flex items-center gap-2">
        <Icon name="lightning" class="h-4 w-4"/>
        Mobil/rumah terkunci sekarang? Telepon langsung lebih cepat.
      </p>
      <a href={telLink} class="inline-flex items-center gap-2 rounded-full bg-white text-brand-700 px-4 py-2 font-bold hover:bg-brand-50">
        <Icon name="phone" class="h-4 w-4"/>
        {business.phone}
      </a>
    </div>
  </section>

  <!-- ==================== SERVICES ==================== -->
  <section id="layanan" class="py-16 sm:py-24">
    <div class="mx-auto max-w-6xl px-4 sm:px-6">
      <div class="max-w-2xl">
        <p class="text-xs uppercase tracking-[0.2em] font-bold text-brand-600">Layanan</p>
        <h2 class="mt-2 text-3xl sm:text-4xl font-extrabold tracking-tight text-slate-900">
          Apa pun masalah kunci Anda, kami bantu di lokasi.
        </h2>
        <p class="mt-3 text-slate-600">
          Spesialisasi ahli kunci dan duplikat kunci untuk kendaraan, rumah,
          kantor, dan brankas di Pekanbaru.
        </p>
      </div>

      <div class="mt-10 grid sm:grid-cols-2 lg:grid-cols-3 gap-4 sm:gap-5">
        {#each services as s, i}
          <article
            class="group relative rounded-2xl bg-white ring-1 ring-slate-200 p-6 hover:ring-brand-300 hover:-translate-y-0.5 transition-all shadow-sm hover:shadow-md"
          >
            <div
              class="grid place-items-center h-12 w-12 rounded-xl bg-gradient-to-br from-brand-400 to-brand-600 text-white shadow"
            >
              <Icon name={s.icon} class="h-6 w-6" />
            </div>
            <h3 class="mt-5 text-lg font-bold text-slate-900">{s.title}</h3>
            <p class="mt-2 text-sm text-slate-600">{s.desc}</p>
            <ul class="mt-4 space-y-1.5 text-sm text-slate-600">
              {#each s.bullets as b}
                <li class="flex items-start gap-2">
                  <Icon name="check" class="h-4 w-4 text-emerald-600 mt-0.5 flex-none"/>
                  <span>{b}</span>
                </li>
              {/each}
            </ul>
            <div class="mt-5">
              <WhatsAppButton variant="light" size="md" message={`Halo, saya butuh bantuan: ${s.title}. Bisa bantu?`}>
                Tanya {s.title}
              </WhatsAppButton>
            </div>
          </article>
        {/each}
      </div>
    </div>
  </section>

  <!-- ==================== PROCESS ==================== -->
  <section id="proses" class="relative py-16 sm:py-24 bg-slate-50">
    <div class="mx-auto max-w-6xl px-4 sm:px-6">
      <div class="max-w-2xl">
        <p class="text-xs uppercase tracking-[0.2em] font-bold text-brand-600">Cara Kerja</p>
        <h2 class="mt-2 text-3xl sm:text-4xl font-extrabold tracking-tight text-slate-900">
          4 langkah cepat sampai kunci beres.
        </h2>
        <p class="mt-3 text-slate-600">
          Tanpa drama, tanpa biaya tersembunyi. Anda tahu persis estimasi biaya
          sebelum teknisi berangkat.
        </p>
      </div>

      <div class="mt-10 grid sm:grid-cols-2 lg:grid-cols-4 gap-4">
        {#each process as p, i}
          <div class="relative rounded-2xl bg-white ring-1 ring-slate-200 p-6 shadow-sm">
            <div class="flex items-center gap-3">
              <span class="grid place-items-center h-10 w-10 rounded-full bg-slate-900 text-white font-bold">
                {p.step}
              </span>
              <h3 class="font-bold text-slate-900">{p.title}</h3>
            </div>
            <p class="mt-3 text-sm text-slate-600">{p.desc}</p>
            {#if i < process.length - 1}
              <span class="hidden lg:block absolute top-10 -right-3 w-6 h-px bg-slate-300"></span>
            {/if}
          </div>
        {/each}
      </div>
    </div>
  </section>

  <!-- ==================== TESTIMONIALS ==================== -->
  <section id="testimoni" class="py-16 sm:py-24">
    <div class="mx-auto max-w-6xl px-4 sm:px-6">
      <div class="flex flex-col sm:flex-row sm:items-end sm:justify-between gap-4">
        <div class="max-w-2xl">
          <p class="text-xs uppercase tracking-[0.2em] font-bold text-brand-600">Testimoni</p>
          <h2 class="mt-2 text-3xl sm:text-4xl font-extrabold tracking-tight text-slate-900">
            Pelanggan Pekanbaru sudah membuktikan.
          </h2>
        </div>
        <div class="flex items-center gap-2">
          {#each Array(5) as _, i}
            <Icon name="star" class="h-5 w-5 text-amber-400" />
          {/each}
          <span class="text-sm text-slate-600 ml-1">Rata-rata 5/5</span>
        </div>
      </div>

      <div class="mt-10 grid md:grid-cols-3 gap-5">
        {#each testimonials as t}
          <figure class="rounded-2xl bg-white ring-1 ring-slate-200 p-6 shadow-sm">
            <div class="flex items-center gap-1">
              {#each Array(t.rating) as _}
                <Icon name="star" class="h-4 w-4 text-amber-400" />
              {/each}
            </div>
            <blockquote class="mt-3 text-slate-700 text-sm leading-relaxed">
              "{t.quote}"
            </blockquote>
            <figcaption class="mt-4 flex items-center gap-3">
              <span
                class="grid place-items-center h-10 w-10 rounded-full bg-gradient-to-br from-brand-300 to-brand-500 text-white font-bold"
              >
                {t.name.split(' ').slice(-1)[0][0]}
              </span>
              <div>
                <p class="font-semibold text-slate-900 text-sm">{t.name}</p>
                <p class="text-xs text-slate-500">{t.location}</p>
              </div>
            </figcaption>
          </figure>
        {/each}
      </div>
    </div>
  </section>

  <!-- ==================== GALLERY ==================== -->
  <section id="galeri" class="py-16 sm:py-24">
    <div class="mx-auto max-w-6xl px-4 sm:px-6">
      <div class="flex flex-col sm:flex-row sm:items-end sm:justify-between gap-4">
        <div class="max-w-2xl">
          <p class="text-xs uppercase tracking-[0.2em] font-bold text-brand-600">Galeri</p>
          <h2 class="mt-2 text-3xl sm:text-4xl font-extrabold tracking-tight text-slate-900">
            Dokumentasi pekerjaan & toko kami.
          </h2>
          <p class="mt-3 text-slate-600">
            Foto teknisi, alat, dan hasil kerja Kunciku Auto Key di Pekanbaru.
          </p>
        </div>
        <WhatsAppButton variant="light" size="md" message="Halo, boleh minta foto contoh hasil kerja sebelumnya?">
          Tanya foto lain
        </WhatsAppButton>
      </div>

      <div class="mt-10 grid grid-cols-2 md:grid-cols-3 gap-3 sm:gap-4">
        {#each gallery as g, i}
          <figure
            class="group relative overflow-hidden rounded-2xl ring-1 ring-slate-200 bg-slate-100 aspect-[4/3]"
          >
            <img
              src={g.src}
              alt={g.alt}
              loading={i < 2 ? 'eager' : 'lazy'}
              decoding="async"
              class="absolute inset-0 h-full w-full object-cover transition duration-500 group-hover:scale-105"
            />
            <figcaption
              class="absolute inset-x-0 bottom-0 bg-gradient-to-t from-slate-950/85 via-slate-950/40 to-transparent p-3 sm:p-4 text-white"
            >
              <p class="text-xs sm:text-sm font-semibold drop-shadow">{g.caption}</p>
            </figcaption>
          </figure>
        {/each}
      </div>

      <p class="mt-6 text-xs text-slate-500">
        Foto ditampilkan sebagai placeholder ilustratif. Foto asli pekerjaan & toko akan menyusul.
      </p>
    </div>
  </section>

  <!-- ==================== FAQ ==================== -->
  <section id="faq" class="py-16 sm:py-24 bg-slate-50">
    <div class="mx-auto max-w-3xl px-4 sm:px-6">
      <div class="text-center">
        <p class="text-xs uppercase tracking-[0.2em] font-bold text-brand-600">FAQ</p>
        <h2 class="mt-2 text-3xl sm:text-4xl font-extrabold tracking-tight text-slate-900">
          Pertanyaan yang sering ditanya.
        </h2>
      </div>

      <div class="mt-10 space-y-3">
        {#each faqs as f, i}
          <div class="rounded-2xl bg-white ring-1 ring-slate-200 overflow-hidden">
            <button
              type="button"
              class="w-full flex items-start gap-3 text-left px-5 py-4 hover:bg-slate-50"
              aria-expanded={openFaq === i}
              onclick={() => toggle(i)}
            >
              <span class="flex-1 font-semibold text-slate-900">{f.q}</span>
              <span class="mt-1 grid place-items-center h-7 w-7 rounded-full bg-slate-100 text-slate-700 flex-none">
                <Icon name={openFaq === i ? 'minus' : 'plus'} class="h-4 w-4"/>
              </span>
            </button>
            {#if openFaq === i}
              <div class="px-5 pb-5 -mt-1 text-slate-600 text-sm leading-relaxed">
                {f.a}
              </div>
            {/if}
          </div>
        {/each}
      </div>
    </div>
  </section>

  <!-- ==================== CONTACT / FINAL CTA ==================== -->
  <section id="kontak" class="relative py-16 sm:py-24 bg-slate-900 text-white overflow-hidden">
    <div class="absolute inset-0 bg-grid opacity-30"></div>
    <div class="absolute -top-32 -left-32 w-[28rem] h-[28rem] rounded-full bg-brand-500/30 blur-3xl"></div>

    <div class="relative mx-auto max-w-6xl px-4 sm:px-6 grid md:grid-cols-2 gap-10 items-center">
      <div>
        <h2 class="text-3xl sm:text-4xl font-extrabold tracking-tight">
          Butuh ahli kunci sekarang? Kami siap berangkat.
        </h2>
        <p class="mt-4 text-slate-300">
          Chat WhatsApp lebih cepat. Kirim lokasi & jenis kunci, kami beri
          estimasi biaya & waktu sebelum tim berangkat.
        </p>

        <div class="mt-6 flex flex-col sm:flex-row gap-3">
          <WhatsAppButton size="lg" variant="primary">
            Chat WhatsApp
          </WhatsAppButton>
          <a
            href={telLink}
            class="inline-flex items-center justify-center gap-2 rounded-full bg-white/10 ring-1 ring-white/20 px-6 py-4 font-semibold hover:bg-white/15"
          >
            <Icon name="phone" class="h-5 w-5"/>
            {business.phone}
          </a>
        </div>
      </div>

      <div class="rounded-2xl bg-white/5 ring-1 ring-white/10 backdrop-blur p-6 sm:p-7">
        <h3 class="font-bold text-lg">Toko & Kontak</h3>
        <ul class="mt-5 space-y-4 text-sm">
          <li class="flex items-start gap-3">
            <span class="grid place-items-center h-9 w-9 rounded-lg bg-brand-500/20 text-brand-300 flex-none">
              <Icon name="pin" class="h-5 w-5"/>
            </span>
            <div>
              <p class="font-semibold">Alamat Toko</p>
              <p class="text-slate-300 mt-0.5">{business.address}</p>
              <a href={mapsLink} target="_blank" rel="noopener" class="inline-block mt-1 text-brand-300 hover:text-brand-200 underline-offset-2 hover:underline">
                Lihat di Google Maps
              </a>
            </div>
          </li>
          <li class="flex items-start gap-3">
            <span class="grid place-items-center h-9 w-9 rounded-lg bg-brand-500/20 text-brand-300 flex-none">
              <Icon name="phone" class="h-5 w-5"/>
            </span>
            <div>
              <p class="font-semibold">WhatsApp & Telepon</p>
              <p class="text-slate-300 mt-0.5">{business.phone}</p>
            </div>
          </li>
          <li class="flex items-start gap-3">
            <span class="grid place-items-center h-9 w-9 rounded-lg bg-brand-500/20 text-brand-300 flex-none">
              <Icon name="clock" class="h-5 w-5"/>
            </span>
            <div>
              <p class="font-semibold">Jam Operasional</p>
              <p class="text-slate-300 mt-0.5">{business.hours}</p>
            </div>
          </li>
          <li class="flex items-start gap-3">
            <span class="grid place-items-center h-9 w-9 rounded-lg bg-brand-500/20 text-brand-300 flex-none">
              <Icon name="shield" class="h-5 w-5"/>
            </span>
            <div>
              <p class="font-semibold">Area Layanan</p>
              <p class="text-slate-300 mt-0.5">{business.serviceArea}</p>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>

  <!-- ==================== FOOTER ==================== -->
  <footer class="bg-slate-950 text-slate-400 text-sm">
    <div class="mx-auto max-w-6xl px-4 sm:px-6 py-8 flex flex-col md:flex-row items-center justify-between gap-3">
      <p>&copy; {new Date().getFullYear()} {business.name}. Semua hak dilindungi.</p>
      <p>Ahli kunci panggilan Pekanbaru &middot; {business.phone}</p>
    </div>
  </footer>
</main>
