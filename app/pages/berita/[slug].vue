<template>
    <article class="space-y-8">
        <!-- Main 12-Column Grid -->
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-start">

            <!-- KOLOM KIRI: Detail Konten Berita (8 Kolom) -->
            <div class="lg:col-span-8 space-y-6">

                <!-- Breadcrumb & Kategori -->
                <div class="space-y-3">
                    <nav class="flex items-center gap-2 text-xs text-gray-500 font-sans">
                        <NuxtLink to="/" class="hover:text-[#A72185]">Beranda</NuxtLink>
                        <span>/</span>
                        <NuxtLink to="/kategori/pemerintahan" class="hover:text-[#A72185]">Pemerintahan</NuxtLink>
                        <span>/</span>
                        <NuxtLink to="/kategori/tata-ruang" class="hover:text-[#A72185]">Tata Ruang & Infrastruktur
                        </NuxtLink>
                        <span>/</span>
                        <span class="text-gray-400 truncate max-w-[180px]">Revitalisasi Kawasan Alun-Alun</span>
                    </nav>

                    <div class="flex items-center gap-2">
                        <span
                            class="bg-[#A72185] text-white text-[10px] font-bold px-2.5 py-0.5 rounded uppercase tracking-wider">PEMERINTAHAN</span>
                        <span
                            class="bg-emerald-600 text-white text-[10px] font-bold px-2.5 py-0.5 rounded uppercase tracking-wider">TATAR
                            GALUH TERKINI</span>
                    </div>
                </div>

                <!-- Judul Utama & Sub-Judul -->
                <div class="space-y-3">
                    <h1 class="text-2xl sm:text-3xl md:text-4xl font-serif font-bold text-gray-900 leading-tight">
                        Revitalisasi Kawasan Alun-Alun dan Masjid Agung Ciamis Resmi Dibuka, Dorong Pusat Ekonomi
                        Kreatif Warga
                    </h1>

                    <p class="text-sm sm:text-base text-gray-600 font-serif leading-relaxed">
                        Wajah baru jantung kota Ciamis hadir mengusung perpaduan harmoni arsitektur Sunda Galuh, ruang
                        publik ramah disabilitas, serta wadah inkubasi ratusan UMKM lokal pasca revitalisasi total.
                    </p>
                </div>

                <!-- Meta Penulis & Informasi Statistik -->
                <div
                    class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 py-3 border-y border-gray-100 text-xs font-sans">
                    <div class="flex items-center gap-3">
                        <div
                            class="w-10 h-10 rounded-full bg-[#A72185] text-white flex items-center justify-center font-bold text-sm shrink-0">
                            HW
                        </div>
                        <div>
                            <div class="font-bold text-gray-900 flex items-center gap-1.5">
                                <span>Hendra Wijaya <span class="text-gray-500 font-normal">(Biro Pemda
                                        Ciamis)</span></span>
                                <span class="text-gray-300">•</span>
                                <span class="text-gray-500 font-normal">Editor: Kang Asep Saepudin</span>
                            </div>
                            <div class="text-gray-400 text-[11px] mt-0.5">
                                Rabu, 29 Juli 2026 • 08:15 WIB
                            </div>
                        </div>
                    </div>

                    <div class="flex items-center gap-4 text-gray-500 text-[11px]">
                        <!-- Icon Views (Mata) -->
                        <span class="flex items-center gap-1">
                            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24">
                                <path d="M0 0h24v24H0z" fill="none" />
                                <g fill="none" stroke="#a72185" stroke-linecap="round" stroke-linejoin="round"
                                    stroke-width="2">
                                    <path
                                        d="M21.257 10.962c.474.62.474 1.457 0 2.076C19.764 14.987 16.182 19 12 19s-7.764-4.013-9.257-5.962a1.69 1.69 0 0 1 0-2.076C4.236 9.013 7.818 5 12 5s7.764 4.013 9.257 5.962" />
                                    <circle cx="12" cy="12" r="3" />
                                </g>
                            </svg>
                            4.8k
                        </span>

                        <!-- Icon Comments (Pesan) -->
                        <span class="flex items-center gap-1">
                            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 640 640">
                                <path d="M0 0h640v640H0z" fill="none" />
                                <path fill="#a72185"
                                    d="M64 304c0 54.4 19.3 104.6 51.9 144.9l-48.8 89.4c-2 3.7-3.1 7.9-3.1 12.2c0 14.1 11.4 25.5 25.5 25.5c4 0 7.8-.6 11.5-2.1L217.4 524c31.4 12.9 66.1 20 102.6 20c141.4 0 256-107.5 256-240S461.4 64 320 64S64 171.5 64 304m94 167.9c9.3-17.1 7.4-38.1-4.8-53.2C127.1 386.4 112 346.8 112 304c0-103.2 90.2-192 208-192s208 88.8 208 192s-90.2 192-208 192c-30.2 0-58.7-5.9-84.3-16.4c-11.9-4.9-25.3-4.8-37.1.3l-58.6 25zM208 336c17.7 0 32-14.3 32-32s-14.3-32-32-32s-32 14.3-32 32s14.3 32 32 32m144-32c0-17.7-14.3-32-32-32s-32 14.3-32 32s14.3 32 32 32s32-14.3 32-32m80 32c17.7 0 32-14.3 32-32s-14.3-32-32-32s-32 14.3-32 32s14.3 32 32 32" />
                            </svg>
                            42
                        </span>

                        <!-- Icon Share -->
                        <span class="flex items-center gap-1">
                            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24">
                                <path d="M0 0h24v24H0z" fill="none" />
                                <path fill="#a72185"
                                    d="M5.5 15a3.5 3.5 0 0 0 2.36-.93l6.26 3.58a3 3 0 0 0-.12.85a3.53 3.53 0 1 0 1.14-2.57l-6.26-3.58a2.7 2.7 0 0 0 .12-.76l6.15-3.52A3.49 3.49 0 1 0 14 5.5a3.4 3.4 0 0 0 .12.85L8.43 9.6A3.5 3.5 0 1 0 5.5 15m12 2a1.5 1.5 0 1 1-1.5 1.5a1.5 1.5 0 0 1 1.5-1.5m0-13A1.5 1.5 0 1 1 16 5.5A1.5 1.5 0 0 1 17.5 4m-12 6A1.5 1.5 0 1 1 4 11.5A1.5 1.5 0 0 1 5.5 10" />
                            </svg>
                            3.7k
                        </span>
                    </div>
                </div>

                <!-- Banner Verifikasi Media -->
                <div
                    class="bg-gray-50 border border-gray-200/80 rounded-md p-2.5 flex flex-col sm:flex-row sm:items-center justify-between gap-2 text-[11px] text-gray-600 font-sans">
                    <div class="flex items-center gap-2">
                        <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 1024 1024">
                            <path d="M0 0h1024v1024H0z" fill="none" />
                            <path fill="#009966"
                                d="M688 312v-48c0-4.4-3.6-8-8-8H296c-4.4 0-8 3.6-8 8v48c0 4.4 3.6 8 8 8h384c4.4 0 8-3.6 8-8m-392 88c-4.4 0-8 3.6-8 8v48c0 4.4 3.6 8 8 8h184c4.4 0 8-3.6 8-8v-48c0-4.4-3.6-8-8-8zm376 116c-119.3 0-216 96.7-216 216s96.7 216 216 216s216-96.7 216-216s-96.7-216-216-216m107.5 323.5C750.8 868.2 712.6 884 672 884s-78.8-15.8-107.5-44.5S520 772.6 520 732s15.8-78.8 44.5-107.5S631.4 580 672 580s78.8 15.8 107.5 44.5S824 691.4 824 732s-15.8 78.8-44.5 107.5M761 656h-44.3c-2.6 0-5 1.2-6.5 3.3l-63.5 87.8l-23.1-31.9a7.92 7.92 0 0 0-6.5-3.3H573c-6.5 0-10.3 7.4-6.5 12.7l73.8 102.1c3.2 4.4 9.7 4.4 12.9 0l114.2-158c3.9-5.3.1-12.7-6.4-12.7M440 852H208V148h560v344c0 4.4 3.6 8 8 8h56c4.4 0 8-3.6 8-8V108c0-17.7-14.3-32-32-32H168c-17.7 0-32 14.3-32 32v784c0 17.7 14.3 32 32 32h272c4.4 0 8-3.6 8-8v-56c0-4.4-3.6-8-8-8" />
                        </svg>
                        <span class="text-emerald-600 font-bold">PEMBERITAAN TERVERIFIKASI</span>
                        <span>— Mentaati Pedoman Pemberitaan Media Siber & Kode Etik Jurnalistik PWI/Dewan Pers</span>
                    </div>
                    <div class="text-gray-400">ID: 46211/DP/2026</div>
                </div>

                <!-- Tombol Bagikan -->
                <div class="flex items-center gap-2 text-xs font-sans">
                    <span class="font-bold text-gray-500 text-[11px] mr-1 uppercase">BAGIKAN:</span>
                    <button
                        class="bg-[#25D366] text-white px-3 py-1.5 rounded font-bold text-[11px] flex items-center gap-1.5 hover:opacity-90">
                        WhatsApp <span class="bg-white/20 px-1 rounded text-[10px]">2.1k</span>
                    </button>
                    <button class="bg-[#1877F2] text-white p-1.5 rounded hover:opacity-90">
                        <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24">
                            <path
                                d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z" />
                        </svg>
                    </button>
                    <button class="bg-black text-white p-1.5 rounded hover:opacity-90">
                        <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24">
                            <path
                                d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z" />
                        </svg>
                    </button>
                    <button class="bg-sky-500 text-white p-1.5 rounded hover:opacity-90">
                        <svg class="w-4 h-4 fill-current" viewBox="0 0 24 24">
                            <path
                                d="M12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zm5.894 8.221l-1.97 9.28c-.145.658-.537.818-1.084.508l-3-2.21-1.446 1.394c-.16.16-.295.295-.605.295l.213-3.053 5.56-5.023c.242-.213-.054-.333-.373-.121l-6.871 4.326-2.962-.924c-.643-.204-.657-.643.136-.953l11.57-4.458c.538-.196 1.006.128.832.941z" />
                        </svg>
                    </button>
                    <button
                        class="bg-gray-100 text-gray-700 px-2.5 py-1.5 rounded font-medium text-[11px] flex items-center gap-1 hover:bg-gray-200">
                        🔗 Salin Tautan
                    </button>
                </div>

                <!-- Gambar Utama / Featured Image -->
                <figure class="space-y-2">
                    <div class="relative rounded-lg overflow-hidden border border-gray-100">
                        <span
                            class="absolute top-3 left-3 bg-[#A72185] text-white text-[10px] font-bold px-2 py-0.5 rounded uppercase">IKONIK
                            TATAR GALUH</span>
                        <img src="https://ik.imagekit.io/tvlk/blog/2025/06/alun-alun-ciamis.jpg?tr=q-70,c-at_max,w-1000,h-600"
                            alt="Alun Alun Ciamis" class="w-full h-[380px] object-cover" />
                        <div
                            class="absolute bottom-2 right-2 bg-black/60 text-white text-[10px] px-2 py-1 rounded backdrop-blur-xs flex items-center gap-1.5">
                            <svg xmlns="http://www.w3.org/2000/svg" class="w-3.5 h-3.5 shrink-0"
                                viewBox="0 0 1024 1024">
                                <path d="M0 0h1024v1024H0z" fill="none" />
                                <path fill="#a72185"
                                    d="M864 248H728l-32.4-90.8a32.07 32.07 0 0 0-30.2-21.2H358.6c-13.5 0-25.6 8.5-30.1 21.2L296 248H160c-44.2 0-80 35.8-80 80v456c0 44.2 35.8 80 80 80h704c44.2 0 80-35.8 80-80V328c0-44.2-35.8-80-80-80m8 536c0 4.4-3.6 8-8 8H160c-4.4 0-8-3.6-8-8V328c0-4.4 3.6-8 8-8h186.7l17.1-47.8l22.9-64.2h250.5l22.9 64.2l17.1 47.8H864c4.4 0 8 3.6 8 8zM512 384c-88.4 0-160 71.6-160 160s71.6 160 160 160s160-71.6 160-160s-71.6-160-160-160m0 256c-53 0-96-43-96-96s43-96 96-96s96 43 96 96s-43 96-96 96" />
                            </svg>
                            <span style="margin-top:-2px;">Dok : Diskominfo Ciamis</span>
                        </div>
                    </div>
                    <figcaption class="text-[11px] text-gray-500 font-serif italic">
                        <strong class="font-sans font-bold text-gray-700">Sentral Kemegahan Tatar Galuh:</strong>
                        Suasana peresmian wajah baru kawasan sentral Alun-Alun Ciamis dan Masjid Agung yang dipadati
                        ribuan warga, komunitas pemuda, serta ratusan pelaku UMKM pada hari pembukaan resmi, Kamis
                        (24/10/2026). Foto: Diskominfo Ciamis / Hendra W.
                    </figcaption>
                </figure>

                <!-- Body Artikel Utama -->
                <div class="prose prose-sm max-w-none text-gray-800 space-y-5 leading-relaxed font-serif text-base">
                    <p>
                        <span
                            class="float-left text-5xl font-serif font-bold text-[#A72185] leading-none pr-2 pt-1">C</span>
                        <strong class="font-sans font-bold text-gray-900">IAMIS</strong> — Kawasan sentral Alun-Alun
                        Kabupaten Ciamis dan area pelataran Masjid Agung Ciamis kini resmi bertransformasi menjadi ruang
                        publik modern berwawasan kearifan lokal. Peresmian proyek revitalisasi yang memakan waktu
                        pengerjaan selama delapan bulan ini diresmikan langsung oleh jajaran Forkopimda bersama para
                        tokoh ulama, menandai babak baru penataan kota yang humanis, estetik, dan terintegrasi dengan
                        penguatan ekonomi kerakyatan.
                    </p>

                    <p>
                        Pembaruan lanskap yang mencakup penataan pedestrian granit bermotif batik Ciwulan, amfiteater
                        terbuka berundak, hingga instalasi pencahayaan tematik malam hari menghadirkan kenyamanan prima
                        bagi para pelancong dan warga lokal. Jalur pedestrian kini diperlebar hingga empat meter di
                        sekeliling masjid dan taman kota, dilengkapi jalur pemandu difabel (guiding block), bangku taman
                        kayu jati ramah cuaca, serta puluhan titik kanopi peneduh.
                    </p>

                    <!-- Highlight Blockquote Card -->
                    <blockquote
                        class="bg-purple-50/50 border-l-4 border-[#A72185] p-5 rounded-r-xl my-6 not-italic relative overflow-hidden">
                        <span class="absolute top-2 left-3 text-6xl text-[#A72185]/10 font-serif select-none">“</span>
                        <p
                            class="font-serif italic text-gray-800 text-sm sm:text-base leading-relaxed relative z-10 mb-4">
                            "Kawasan Alun-Alun bukan sekadar ruang publik terbuka hijau biasa, melainkan etalase
                            kebudayaan luhur Tatar Galuh dan roda penggerak denyut ekonomi masyarakat pasca pemulihan.
                            Kami mendesainnya agar Masjid Agung tetap menjadi episentrum spiritualitas, sementara
                            lingkar alun-alun menjadi simpul kreativitas pemuda serta rumah kehormatan bagi pelaku UMKM
                            Ciamis."
                        </p>
                        <div class="flex items-center gap-3 relative z-10">
                            <div
                                class="w-8 h-8 rounded-full bg-[#A72185] text-white flex items-center justify-center font-bold text-xs font-sans">
                                BC
                            </div>
                            <div>
                                <div class="font-sans font-bold text-xs text-gray-900">Dr. H. Herdiat Sunarya</div>
                                <div class="font-sans text-[10px] text-gray-500">Bupati Ciamis Periode 2019-2026</div>
                            </div>
                        </div>
                    </blockquote>

                    <h2 class="text-xl font-serif font-bold text-[#A72185] pt-2">
                        Sentralisasi UMKM dan Fasilitas Ramah Keluarga
                    </h2>

                    <p>
                        Salah satu terobosan paling signifikan dalam revitalisasi ini adalah pengelompokan zona kuliner
                        tradisional dan cenderamata khas Ciamis. Pemkab Ciamis bersama Paguyuban Pedagang Kreatif
                        Lapangan (PKL) menyepakati pemindahan lapak tenda acak ke dalam shelter tematik terpadu "Sentra
                        Niaga Pasundan" di sisi timur alun-alun.
                    </p>

                    <p>
                        Sebanyak 120 kios UMKM kini tertata higienis dengan sistem pembayaran digital QRIS binaan Bank
                        bjb dan Dinas KUKMP Ciamis. Pengunjung kini dapat mencicipi sajian legendaris seperti Galendo
                        khas Ciamis, Sale Pisang Manggu, dendeng sapi khas Tatar Sunda, serta beragam kopi robusta
                        Gunung Sawal dalam suasana santai tanpa mengganggu kenyamanan jamaah masjid maupun pejalan kaki.
                    </p>

                    <!-- Infografis Box Metric -->
                    <div
                        class="bg-gradient-to-br from-gray-50 to-purple-50/30 border border-gray-200 rounded-xl p-5 my-6 space-y-4 font-sans">
                        <div class="flex justify-between items-center border-b border-gray-200/80 pb-2">
                            <div>
                                <span
                                    class="text-[10px] font-bold text-[#A72185] uppercase tracking-wider block">RINGKASAN
                                    DATA & PEMBANGUNAN</span>
                                <h3 class="text-sm font-bold text-gray-900">Metrik Proyek Revitalisasi Alun-Alun 2026
                                </h3>
                            </div>
                        </div>

                        <div class="grid grid-cols-2 sm:grid-cols-4 gap-3">
                            <div class="bg-white p-3 rounded-lg border border-gray-100 shadow-2xs">
                                <div class="text-[10px] text-gray-500 font-medium uppercase">LUAS KAWASAN</div>
                                <div class="text-xl font-black text-gray-900 my-0.5">2,4 Ha</div>
                                <div class="text-[10px] text-gray-400">Zona hijau & pedestrian</div>
                            </div>
                            <div class="bg-white p-3 rounded-lg border border-gray-100 shadow-2xs">
                                <div class="text-[10px] text-gray-500 font-medium uppercase">KIOS UMKM</div>
                                <div class="text-xl font-black text-gray-900 my-0.5">120 Kios</div>
                                <div class="text-[10px] text-gray-400">Terverifikasi sistem QRIS</div>
                            </div>
                            <div class="bg-white p-3 rounded-lg border border-gray-100 shadow-2xs">
                                <div class="text-[10px] text-gray-500 font-medium uppercase">AKSESIBILITAS</div>
                                <div class="text-xl font-black text-gray-900 my-0.5">100%</div>
                                <div class="text-[10px] text-gray-400">Ramah lansia & disabilitas</div>
                            </div>
                            <div class="bg-white p-3 rounded-lg border border-gray-100 shadow-2xs">
                                <div class="text-[10px] text-gray-500 font-medium uppercase">WIFI PUBLIK</div>
                                <div class="text-xl font-black text-gray-900 my-0.5">24 Jam</div>
                                <div class="text-[10px] text-gray-400">Akses gratis berkecepatan tinggi</div>
                            </div>
                        </div>

                        <!-- Progress Bar Anggaran -->
                        <div class="space-y-1.5 pt-1">
                            <div class="flex justify-between text-[11px] font-bold">
                                <span class="text-gray-700">Realisasi Anggaran Terpadu APBD & Bantuan Provinsi Jawa
                                    Barat</span>
                                <span class="text-emerald-600">100% Tuntas Tepat Waktu</span>
                            </div>
                            <div class="w-full bg-gray-200 h-2 rounded-full overflow-hidden flex">
                                <div class="bg-[#A72185] h-full w-[65%]" title="Lanskap & Pedestrian (65%)"></div>
                                <div class="bg-purple-400 h-full w-[25%]" title="Sentra Niaga UMKM (25%)"></div>
                                <div class="bg-emerald-500 h-full w-[10%]" title="Smart Public Space (10%)"></div>
                            </div>
                            <div class="flex items-center gap-4 text-[10px] text-gray-500 pt-0.5">
                                <span class="flex items-center gap-1"><span
                                        class="w-2 h-2 rounded-full bg-[#A72185]"></span> Lanskap & Pedestrian
                                    (65%)</span>
                                <span class="flex items-center gap-1"><span
                                        class="w-2 h-2 rounded-full bg-purple-400"></span> Sentra Niaga UMKM
                                    (25%)</span>
                                <span class="flex items-center gap-1"><span
                                        class="w-2 h-2 rounded-full bg-emerald-500"></span> Smart Public Space
                                    (10%)</span>
                            </div>
                        </div>
                    </div>

                    <h2 class="text-xl font-serif font-bold text-[#A72185] pt-2">
                        Penerapan Konsep Smart Public Space
                    </h2>

                    <p>
                        Ketua Dewan Kemakmuran Masjid (DKM) Masjid Agung Ciamis, KH. Wawan Malik Marwan, mengapresiasi
                        tinggi sinergi antara pemerintah kabupaten dan kemakmuran masjid. Menurut beliau, penataan baru
                        ini sama sekali tidak mengurangi kekhusyukan ibadah di Masjid Agung berkapasitas 10.000 jamaah
                        tersebut, melainkan justru memperluas daya tampung shalat saat perayaan hari besar Islam.
                    </p>

                    <p>
                        "Pelataran utama kini terhubung mulus dengan Alun-Alun tanpa sekat dinding pembatas yang kaku.
                        Saat pelaksanaan Shalat Idulfitri atau pengajian akbar peringatan Maulid Nabi, ribuan jamaah
                        dapat memanfaatkan lapangan rumput sintetis dan plaza utama secara tertib," ungkap KH. Wawan
                        saat ditemui di serambi barat masjid.
                    </p>

                    <p>
                        Selain itu, Dinas Komunikasi dan Informatika (Diskominfo) Ciamis menyematkan delapan titik
                        kamera pengawas AI CCTV 360 derajat untuk memastikan keamanan pengunjung sepanjang waktu, serta
                        stasiun pengisian daya gawai (solar-powered charging station) di taman bermain anak yang
                        terletak di sisi utara.
                    </p>
                </div>

                <!-- Tag Terkait -->
                <div class="pt-4 border-t border-gray-100 flex flex-wrap items-center gap-1.5 text-xs font-sans">
                    <span class="font-bold text-gray-500 text-[11px] mr-1 uppercase">TOPIK TERKAIT BERITA :</span>
                    <NuxtLink
                        v-for="tag in ['#AlunAlunCiamis', '#MasjidAgungCiamis', '#TatarGaluh', '#WisataCiamis', '#EkonomiKreatif', '#BupatiCiamis', '#UMKMCiamis']"
                        :key="tag" to="#"
                        class="bg-gray-100 hover:bg-[#A72185] hover:text-white px-2.5 py-1 rounded text-gray-600 transition-colors font-medium text-[11px]">
                        {{ tag }}
                    </NuxtLink>
                </div>

                <!-- Profile Card Penulis/Jurnalis -->
                <div class="bg-gray-50 border border-gray-200/80 rounded p-3 flex items-center gap-4 font-sans">
                    <div
                        class="w-14 h-14 rounded-full bg-[#A72185] text-white flex items-center justify-center font-bold text-lg shrink-0">
                        HW
                    </div>
                    <div class="space-y-1 text-xs">
                        <div class="flex items-center gap-1">
                            <h4 class="font-bold text-gray-900 text-sm">Hendra Wijaya</h4>
                            <span style="margin-top: 3px;">
                                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16">
                                    <path d="M0 0h16v16H0z" fill="none" />
                                    <path fill="#006045"
                                        d="m11.335 2.065l.076.153l.577 1.533c.045.12.14.216.261.261l1.48.555c.65.244.999.938.826 1.595l-.042.13l-.688 1.523a.45.45 0 0 0 0 .37l.653 1.439a1.34 1.34 0 0 1-.543 1.711l-.153.076l-1.533.577a.45.45 0 0 0-.261.261l-.555 1.48a1.34 1.34 0 0 1-1.595.826l-.13-.042l-1.523-.688a.45.45 0 0 0-.37 0l-1.439.654a1.34 1.34 0 0 1-1.711-.544l-.076-.153l-.577-1.533a.45.45 0 0 0-.261-.261l-1.48-.555a1.34 1.34 0 0 1-.826-1.595l.042-.13l.689-1.523a.45.45 0 0 0 0-.37l-.654-1.439a1.34 1.34 0 0 1 .543-1.711l.153-.076l1.533-.577a.45.45 0 0 0 .261-.261l.555-1.48a1.34 1.34 0 0 1 1.595-.826l.13.042l1.523.689a.45.45 0 0 0 .37 0l1.439-.654a1.34 1.34 0 0 1 1.711.543m-1.171 3.64L6.978 9.348L5.816 8.184a.447.447 0 1 0-.632.632l1.5 1.5a.447.447 0 0 0 .652-.022l3.5-4a.447.447 0 0 0-.672-.588" />
                                </svg>
                            </span>
                        </div>
                        <p class="text-gray-600 leading-snug">
                            Reporter Biro Pemerintahan & Kebijakan Publik Ciamis News. Mengawal dinamika tata ruang,
                            infrastruktur pedesaan, dan transparansi kebijakan daerah Kabupaten Ciamis sejak 2017.
                        </p>
                        <div class="flex items-center gap-3 pt-1 text-[11px] text-[#A72185] font-semibold">
                            <NuxtLink to="#" class="hover:underline inline-flex items-center gap-1">
                                <span>Lihat 342 Artikel Lainnya</span>
                                <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4 shrink-0" viewBox="0 0 24 24">
                                    <path d="M0 0h24v24H0z" fill="none" />
                                    <path fill="none" stroke="#a72185" stroke-linecap="round" stroke-linejoin="round"
                                        stroke-width="2" d="M4 12h16m-7-7l7 7l-7 7" />
                                </svg>
                            </NuxtLink>
                            <!-- <span>•</span>
                            <a href="mailto:redaksi@ciamisnews.id" class="text-gray-500 hover:underline">✉ Surel
                                Redaksi</a> -->
                        </div>
                    </div>
                </div>

                <!-- Section Berita Terkait Grid 2x2 -->
                <div class="space-y-4 pt-4 font-sans">
                    <div class="flex justify-between items-center border-b-2 border-[#A72185] pb-2">
                        <h3 class="text-base font-bold text-gray-900 flex items-center gap-2">
                            <span class="w-2.5 h-4 bg-[#A72185] rounded-xs"></span>
                            Berita Terkait
                        </h3>
                        <NuxtLink to="/kategori/pemerintahan" class="text-xs text-[#A72185] font-bold hover:underline">
                            Arsip Berita ›</NuxtLink>
                    </div>

                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <!-- Item 1 -->
                        <div
                            class="bg-white border border-gray-100 rounded-lg overflow-hidden shadow-2xs hover:shadow-md transition">
                            <div class="relative h-36">
                                <span
                                    class="absolute top-2 left-2 bg-[#A72185] text-white text-[9px] font-bold px-2 py-0.5 rounded uppercase">Ekonomi
                                    & UMKM</span>
                                <img src="https://images.unsplash.com/photo-1590779033100-9f60a05a013d?q=80&w=400&auto=format&fit=crop"
                                    class="w-full h-full object-cover" alt="Kuliner Ciamis" />
                            </div>
                            <div class="p-3 space-y-1.5">
                                <div class="text-[10px] text-gray-400">23 Okt 2026 • 1.410x dibaca</div>
                                <h4
                                    class="text-xs font-bold text-gray-900 line-clamp-2 hover:text-[#A72185] cursor-pointer">
                                    Penataan Sentra Kuliner Galendo Khas Ciamis Siap Masuk Etalase Digital Nasional
                                </h4>
                                <p class="text-[11px] text-gray-500 line-clamp-2">
                                    Dinas KUKMP siapkan standardisasi higienitas dan kemasan modern agar camilan khas
                                    Galuh mampu menembus ritel...
                                </p>
                            </div>
                        </div>

                        <!-- Item 2 -->
                        <div
                            class="bg-white border border-gray-100 rounded-lg overflow-hidden shadow-2xs hover:shadow-md transition">
                            <div class="relative h-36">
                                <span
                                    class="absolute top-2 left-2 bg-[#A72185] text-white text-[9px] font-bold px-2 py-0.5 rounded uppercase">Tatar
                                    Galuh / Budaya</span>
                                <img src="https://images.unsplash.com/photo-1533105079780-92b9be482077?q=80&w=400&auto=format&fit=crop"
                                    class="w-full h-full object-cover" alt="Budaya Ciamis" />
                            </div>
                            <div class="p-3 space-y-1.5">
                                <div class="text-[10px] text-gray-400">22 Okt 2026 • 2.980x dibaca</div>
                                <h4
                                    class="text-xs font-bold text-gray-900 line-clamp-2 hover:text-[#A72185] cursor-pointer">
                                    Jadwal Rangkaian Parade Seni Musik Bambu Akhir Pekan di Taman Lokasana Ciamis
                                </h4>
                                <p class="text-[11px] text-gray-500 line-clamp-2">
                                    Menampilkan puluhan sanggar calung dan angklung cilik dari berbagai kecamatan
                                    se-Kabupaten Ciamis...
                                </p>
                            </div>
                        </div>

                        <!-- Item 3 -->
                        <div
                            class="bg-white border border-gray-100 rounded-lg overflow-hidden shadow-2xs hover:shadow-md transition">
                            <div class="relative h-36">
                                <span
                                    class="absolute top-2 left-2 bg-[#A72185] text-white text-[9px] font-bold px-2 py-0.5 rounded uppercase">Pemerintahan</span>
                                <img src="https://images.unsplash.com/photo-1544620347-c4fd4a3d5957?q=80&w=400&auto=format&fit=crop"
                                    class="w-full h-full object-cover" alt="Bus Listrik" />
                            </div>
                            <div class="p-3 space-y-1.5">
                                <div class="text-[10px] text-gray-400">20 Okt 2026 • 3.204x dibaca</div>
                                <h4
                                    class="text-xs font-bold text-gray-900 line-clamp-2 hover:text-[#A72185] cursor-pointer">
                                    Pemkab Ciamis Uji Coba Shuttle Bus Listrik Keliling Kawasan Pusat Pemerintahan
                                </h4>
                                <p class="text-[11px] text-gray-500 line-clamp-2">
                                    Langkah konkret mengurangi emisi gas buang karbon di sekitar lingkar Alun-Alun dan
                                    perkantoran bale kota...
                                </p>
                            </div>
                        </div>

                        <!-- Item 4 -->
                        <div
                            class="bg-white border border-gray-100 rounded-lg overflow-hidden shadow-2xs hover:shadow-md transition">
                            <div class="relative h-36">
                                <span
                                    class="absolute top-2 left-2 bg-[#A72185] text-white text-[9px] font-bold px-2 py-0.5 rounded uppercase">Wisata
                                    & Religi</span>
                                <img src="https://images.unsplash.com/photo-1564769625905-50e93615e769?q=80&w=400&auto=format&fit=crop"
                                    class="w-full h-full object-cover" alt="Masjid Agung" />
                            </div>
                            <div class="p-3 space-y-1.5">
                                <div class="text-[10px] text-gray-400">19 Okt 2026 • 4.110x dibaca</div>
                                <h4
                                    class="text-xs font-bold text-gray-900 line-clamp-2 hover:text-[#A72185] cursor-pointer">
                                    Eksplorasi Wisata Religi Masjid Agung Ciamis: Jejak Syiar Islam Abad ke-19 di Tatar
                                    Galuh
                                </h4>
                                <p class="text-[11px] text-gray-500 line-clamp-2">
                                    Mengulas ornamen khas Sunda di kubah utama dan kisah sejarah pembangunan yang
                                    diprakarsai oleh bupati terdahulu...
                                </p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Section Komentar Warga Lengkap -->
                <div class="bg-white border border-gray-200/80 rounded p-3 space-y-5 font-sans shadow-xs">
                    <div class="flex justify-between items-center border-b border-gray-100 pb-3">
                        <h3 class="text-base font-bold text-gray-900 flex items-center gap-2">
                            <span class="w-2.5 h-4 bg-[#A72185] rounded-xs"></span>
                            Komentar Warga Tatar Galuh
                        </h3>
                        <span class="bg-purple-100 text-[#A72185] text-xs font-bold px-2.5 py-0.5 rounded-full">42
                            Komentar</span>
                    </div>

                    <!-- Banner Ketentuan Diskusi -->
                    <div
                        class="bg-purple-50/60 border border-purple-100 p-3 rounded flex items-start gap-2.5 text-[11px] text-gray-600">
                        <div>
                            <strong class="text-gray-900 font-bold block">Ketentuan Diskusi Cerdas Ciamis News
                                :</strong>
                            Komentar dimoderasi secara aktif sebelum dipublikasikan sesuai Pedoman Pemberitaan Media
                            Siber Dewan Pers RI. Hindari ujaran kebencian, suku/agama/ras, hoaks, dan tautan promosi
                            liar.
                        </div>
                    </div>

                    <!-- Form Tanggapan -->
                    <form @submit.prevent class="space-y-3 bg-gray-50/50 p-4 rounded border border-gray-100">
                        <h4 class="text-xs font-bold text-gray-900 uppercase tracking-wider">Tulis Tanggapan & Suara
                            Anda</h4>

                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                            <div class="space-y-1">
                                <label class="text-[11px] font-bold text-gray-700">Nama Lengkap *</label>
                                <input type="text" placeholder="Contoh: Asep Kurniawan"
                                    class="bg-white border border-gray-200 rounded-lg px-3 py-2 text-xs w-full focus:outline-none focus:border-[#A72185]" />
                            </div>
                            <div class="space-y-1">
                                <label class="text-[11px] font-bold text-gray-700">Kecamatan Asal / Domisili *</label>
                                <select
                                    class="bg-white border border-gray-200 rounded-lg px-3 py-2 text-xs w-full focus:outline-none focus:border-[#A72185] text-gray-600">
                                    <option value="">Pilih Kecamatan di Kab. Ciamis</option>
                                    <option value="banjaranyar">Banjaranyar</option>
                                    <option value="banjarsari">Banjarsari</option>
                                    <option value="baregbeg">Baregbeg</option>
                                    <option value="ciamis">Ciamis</option>
                                    <option value="cidolog">Cidolog</option>
                                    <option value="cihaurbeuti">Cihaurbeuti</option>
                                    <option value="cijeungjing">Cijeungjing</option>
                                    <option value="cikoneng">Cikoneng</option>
                                    <option value="cimaragas">Cimaragas</option>
                                    <option value="cipaku">Cipaku</option>
                                    <option value="cisaga">Cisaga</option>
                                    <option value="jatinagara">Jatinagara</option>
                                    <option value="kawali">Kawali</option>
                                    <option value="lakbok">Lakbok</option>
                                    <option value="lumbung">Lumbung</option>
                                    <option value="pamarican">Pamarican</option>
                                    <option value="panawangan">Panawangan</option>
                                    <option value="panjalu">Panjalu</option>
                                    <option value="panumbangan">Panumbangan</option>
                                    <option value="purwadadi">Purwadadi</option>
                                    <option value="rajadesa">Rajadesa</option>
                                    <option value="rancah">Rancah</option>
                                    <option value="sadananya">Sadananya</option>
                                    <option value="sindangkasih">Sindangkasih</option>
                                    <option value="sukadana">Sukadana</option>
                                    <option value="sukamantri">Sukamantri</option>
                                    <option value="tambaksari">Tambaksari</option>
                                    <option value="lainnya">Luar Ciamis / Diaspora</option>
                                </select>
                            </div>
                        </div>

                        <div class="space-y-1">
                            <label class="text-[11px] font-bold text-gray-700">Surel / Email (Tidak akan dipublikasikan)
                                *</label>
                            <input type="email" placeholder="nama@email.com"
                                class="bg-white border border-gray-200 rounded-lg px-3 py-2 text-xs w-full focus:outline-none focus:border-[#A72185]" />
                        </div>

                        <div class="space-y-1">
                            <label class="text-[11px] font-bold text-gray-700">Isi Komentar / Aspirasi Warga *</label>
                            <textarea rows="3"
                                placeholder="Sampaikan apresiasi, saran fasilitas, atau masukan untuk pengelolaan Alun-Alun Ciamis..."
                                class="bg-white border border-gray-200 rounded-lg px-3 py-2 text-xs w-full focus:outline-none focus:border-[#A72185]"></textarea>
                        </div>

                        <div class="flex flex-col sm:flex-row items-center justify-between gap-3 pt-1">
                            <div
                                class="flex items-center gap-2 bg-white px-3 py-1.5 rounded-lg border border-gray-200 text-xs">
                                <span class="text-gray-600 font-medium inline-flex items-center gap-1.5">
                                    <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4 shrink-0"
                                        viewBox="0 0 24 24">
                                        <path d="M0 0h24v24H0z" fill="none" />
                                        <g fill="none" stroke="#a72185" stroke-width="1.5">
                                            <path stroke-linecap="round" stroke-linejoin="round"
                                                d="M2 20v-1a7 7 0 0 1 7-7v0" />
                                            <path
                                                d="M15.804 12.314a1.62 1.62 0 0 1 2.392 0c.325.356.79.549 1.272.526a1.62 1.62 0 0 1 1.692 1.692c-.023.481.17.947.526 1.272c.705.642.705 1.75 0 2.392c-.356.325-.549.79-.526 1.272a1.62 1.62 0 0 1-1.692 1.692a1.62 1.62 0 0 0-1.272.526a1.62 1.62 0 0 1-2.392 0a1.62 1.62 0 0 0-1.272-.526a1.62 1.62 0 0 1-1.692-1.692a1.62 1.62 0 0 0-.527-1.272a1.62 1.62 0 0 1 0-2.392c.357-.325.55-.79.527-1.272a1.62 1.62 0 0 1 1.692-1.692c.481.023.947-.17 1.272-.527Z" />
                                            <path stroke-linecap="round" stroke-linejoin="round"
                                                d="m15.364 17l1.09 1.09l2.182-2.18M9 12a4 4 0 1 0 0-8a4 4 0 0 0 0 8" />
                                        </g>
                                    </svg>
                                    <span>Verifikasi Ringan : 5 + 3 =</span>
                                </span>
                                <input type="text"
                                    class="w-10 border border-gray-300 rounded px-1.5 py-0.5 text-center font-bold focus:outline-none focus:border-[#A72185]"
                                    placeholder="?" />
                            </div>

                            <button
                                class="bg-[#A72185] text-white text-xs font-bold px-5 py-2.5 rounded-lg hover:bg-[#8e1b70] transition flex items-center gap-2 w-full sm:w-auto justify-center cursor-pointer">
                                <span><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                                        viewBox="0 0 16 16">
                                        <path d="M0 0h16v16H0z" fill="none" />
                                        <path fill="#fff"
                                            d="M15.854.146a.5.5 0 0 1 .11.54l-5.819 14.547a.75.75 0 0 1-1.329.124l-3.178-4.995L.643 7.184a.75.75 0 0 1 .124-1.33L15.314.037a.5.5 0 0 1 .54.11ZM6.636 10.07l2.761 4.338L14.13 2.576zm6.787-8.201L1.591 6.602l4.339 2.76z" />
                                    </svg>
                                </span> Kirim Komentar (Moderasi)
                            </button>
                        </div>
                    </form>

                    <!-- List Komentar Warga -->
                    <div class="space-y-3 pt-2">
                        <!-- Komentar 1 -->
                        <div class="bg-gray-50/80 p-4 rounded border border-gray-100 space-y-2">
                            <div class="flex items-center justify-between">
                                <div class="flex items-center gap-2.5">
                                    <div
                                        class="w-8 h-8 rounded-full bg-purple-700 text-white font-bold text-xs flex items-center justify-center">
                                        DN
                                    </div>
                                    <div>
                                        <div class="font-bold text-gray-900 text-xs flex items-center gap-1.5">
                                            <span>Dadan Nugraha</span>
                                        </div>
                                        <div class="text-[10px] text-gray-400 flex items-center gap-1 mt-0.5">
                                            <svg class="w-3 h-3 text-gray-400 shrink-0" fill="none"
                                                stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                                                <path stroke-linecap="round" stroke-linejoin="round"
                                                    d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                                                <path stroke-linecap="round" stroke-linejoin="round"
                                                    d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                                            </svg>
                                            <span>Warga Kec. Baregbeg • 4 jam yang lalu</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <p class="text-xs text-gray-700 leading-relaxed">
                                Alhamdulillah, bangga sekali melihat wajah baru Alun-Alun Ciamis. Kemarin malam sempat
                                berkunjung bersama keluarga, jalurnya sangat luas dan nyaman untuk kursi roda orang tua
                                saya. Mohon petugas Satpol PP dan dinas kebersihan konsisten menjaga ketertiban agar
                                tidak ada sampah berserakan.
                            </p>
                            <div class="flex items-center gap-4 text-[11px] text-gray-500 pt-1">
                                <button class="hover:text-[#A72185] font-medium flex items-center gap-1">
                                    <svg class="w-3.5 h-3.5 shrink-0" fill="none" stroke="currentColor" stroke-width="2"
                                        viewBox="0 0 24 24">
                                        <path stroke-linecap="round" stroke-linejoin="round"
                                            d="M14 10h4.764a2 2 0 011.789 2.894l-3.5 7A2 2 0 0115.263 21h-4.017c-.163 0-.326-.02-.485-.06L7 20m7-10V5a2 2 0 00-2-2h-.095c-.5 0-.905.405-.905.905 0 .714-.211 1.412-.608 2.006L7 11v9m7-10h-2M7 20H5a2 2 0 01-2-2v-6a2 2 0 012-2h2.5" />
                                    </svg>
                                    <span>28 Suka</span>
                                </button>
                                <button class="hover:text-[#A72185] font-medium flex items-center gap-1">
                                    <svg class="w-3.5 h-3.5 shrink-0" fill="none" stroke="currentColor" stroke-width="2"
                                        viewBox="0 0 24 24">
                                        <path stroke-linecap="round" stroke-linejoin="round"
                                            d="M3 10h10a8 8 0 018 8v2M3 10l6 6m-6-6l6-6" />
                                    </svg>
                                    <span>Balas</span>
                                </button>
                            </div>
                        </div>

                        <!-- Komentar 2 -->
                        <div class="bg-gray-50/80 p-4 rounded border border-gray-100 space-y-2">
                            <div class="flex items-center justify-between">
                                <div class="flex items-center gap-2.5">
                                    <div
                                        class="w-8 h-8 rounded-full bg-pink-700 text-white font-bold text-xs flex items-center justify-center">
                                        SR
                                    </div>
                                    <div>
                                        <div class="font-bold text-gray-900 text-xs flex items-center gap-1.5">
                                            <span>Siti Rahmawati</span>
                                        </div>
                                        <div class="text-[10px] text-gray-400 flex items-center gap-1 mt-0.5">
                                            <svg class="w-3 h-3 text-gray-400 shrink-0" fill="none"
                                                stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                                                <path stroke-linecap="round" stroke-linejoin="round"
                                                    d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                                                <path stroke-linecap="round" stroke-linejoin="round"
                                                    d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                                            </svg>
                                            <span>Warga Kec. Cihaurbeuti • 4 jam yang lalu</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <p class="text-xs text-gray-700 leading-relaxed">
                                Sebagai penjual Sale Pisang di area barat, kami sangat bersyukur ditata rapi seperti
                                ini. Pembeli jadi betah nongkrong, sistem pembayaran QRIS juga sangat membantu tanpa
                                ribet kembalian uang koin. Semoga Ciamis semakin maju dan wisatawan luar kota makin
                                ramai mampir!
                            </p>
                            <div class="flex items-center gap-4 text-[11px] text-gray-500 pt-1">
                                <button class="hover:text-[#A72185] font-medium flex items-center gap-1">
                                    <svg class="w-3.5 h-3.5 shrink-0" fill="none" stroke="currentColor" stroke-width="2"
                                        viewBox="0 0 24 24">
                                        <path stroke-linecap="round" stroke-linejoin="round"
                                            d="M14 10h4.764a2 2 0 011.789 2.894l-3.5 7A2 2 0 0115.263 21h-4.017c-.163 0-.326-.02-.485-.06L7 20m7-10V5a2 2 0 00-2-2h-.095c-.5 0-.905.405-.905.905 0 .714-.211 1.412-.608 2.006L7 11v9m7-10h-2M7 20H5a2 2 0 01-2-2v-6a2 2 0 012-2h2.5" />
                                    </svg>
                                    <span>45 Suka</span>
                                </button>
                                <button class="hover:text-[#A72185] font-medium flex items-center gap-1">
                                    <svg class="w-3.5 h-3.5 shrink-0" fill="none" stroke="currentColor" stroke-width="2"
                                        viewBox="0 0 24 24">
                                        <path stroke-linecap="round" stroke-linejoin="round"
                                            d="M3 10h10a8 8 0 018 8v2M3 10l6 6m-6-6l6-6" />
                                    </svg>
                                    <span>Balas</span>
                                </button>
                            </div>
                        </div>

                        <!-- Komentar 3 -->
                        <div class="bg-gray-50/80 p-4 rounded border border-gray-100 space-y-2">
                            <div class="flex items-center justify-between">
                                <div class="flex items-center gap-2.5">
                                    <div
                                        class="w-8 h-8 rounded-full bg-[#A72185] text-white font-bold text-xs flex items-center justify-center">
                                        WK
                                    </div>
                                    <div>
                                        <div class="font-bold text-gray-900 text-xs">Wawan Kuswandi</div>
                                        <div class="text-[10px] text-gray-400 flex items-center gap-1 mt-0.5">
                                            <svg class="w-3 h-3 text-gray-400 shrink-0" fill="none"
                                                stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                                                <path stroke-linecap="round" stroke-linejoin="round"
                                                    d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                                                <path stroke-linecap="round" stroke-linejoin="round"
                                                    d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                                            </svg>
                                            <span>Warga Kec. Kawali • 8 jam yang lalu</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <p class="text-xs text-gray-700 leading-relaxed">
                                Melihat foto udara di Ciamis News ini bikin rindu kampung halaman. Sangat megah berpadu
                                dengan arsitektur Masjid Agung. Akhir pekan ini rencana pulang kampung mau ajak
                                anak-anak main ke amfiteater barunya.
                            </p>
                            <div class="flex items-center gap-4 text-[11px] text-gray-500 pt-1">
                                <button class="hover:text-[#A72185] font-medium flex items-center gap-1">
                                    <svg class="w-3.5 h-3.5 shrink-0" fill="none" stroke="currentColor" stroke-width="2"
                                        viewBox="0 0 24 24">
                                        <path stroke-linecap="round" stroke-linejoin="round"
                                            d="M14 10h4.764a2 2 0 011.789 2.894l-3.5 7A2 2 0 0115.263 21h-4.017c-.163 0-.326-.02-.485-.06L7 20m7-10V5a2 2 0 00-2-2h-.095c-.5 0-.905.405-.905.905 0 .714-.211 1.412-.608 2.006L7 11v9m7-10h-2M7 20H5a2 2 0 01-2-2v-6a2 2 0 012-2h2.5" />
                                    </svg>
                                    <span>19 Suka</span>
                                </button>
                                <button class="hover:text-[#A72185] font-medium flex items-center gap-1">
                                    <svg class="w-3.5 h-3.5 shrink-0" fill="none" stroke="currentColor" stroke-width="2"
                                        viewBox="0 0 24 24">
                                        <path stroke-linecap="round" stroke-linejoin="round"
                                            d="M3 10h10a8 8 0 018 8v2M3 10l6 6m-6-6l6-6" />
                                    </svg>
                                    <span>Balas</span>
                                </button>
                            </div>
                        </div>

                        <!-- Tombol Muat Lebih Banyak -->
                        <div class="text-center pt-3">
                            <button
                                class="bg-gray-100 hover:bg-gray-200 text-gray-700 text-xs font-bold px-6 py-2.5 rounded-lg transition inline-flex items-center gap-2">
                                <svg class="w-4 h-4 shrink-0" fill="none" stroke="currentColor" stroke-width="2"
                                    viewBox="0 0 24 24">
                                    <path stroke-linecap="round" stroke-linejoin="round" d="M19 9l-7 7-7-7" />
                                </svg>
                                <span>Muat Komentar Lainnya (39 Tersisa)</span>
                            </button>
                        </div>
                    </div>
                </div>

            </div>

            <!-- KOLOM KANAN: Sticky Sidebar Widgets (4 Kolom) -->
            <aside class="lg:col-span-4 sticky top-6 space-y-5">
                <HomeSidebarWidgets />
            </aside>

        </div>
    </article>
</template>

<script setup>
import HomeSidebarWidgets from '~/components/home/SidebarWidget.vue'
</script>