<script lang="ts">
    import { Sparkles, Phone, Clock, Shirt } from "@lucide/svelte";

    const scrollToSection = (id: string) => {
        const element = document.getElementById(id);
        if (element) {
            element.scrollIntoView({ behavior: "smooth" });
        }
    };
</script>

<!-- Hero Section -->
<section
    id="hero"
    class="pt-16 sm:pt-20 min-h-screen flex items-center bg-linear-to-br from-[#33A1E0]/10 to-[#FFF9AF]/20"
>
    <div class="container mx-auto px-4 py-12 sm:py-16 md:py-20">
        <div
            class="grid grid-cols-1 lg:grid-cols-2 gap-8 md:gap-12 items-center"
        >
            <!-- Text Content -->
            <div class="space-y-4 sm:space-y-6 text-center lg:text-left">
                <div
                    class="inline-block bg-[#FFF9AF] px-3 sm:px-4 py-1.5 sm:py-2 rounded-full"
                >
                    <span
                        class="text-[#252525] font-medium text-sm sm:text-base"
                        >✨ บริการซักรีดคุณภาพ</span
                    >
                </div>
                <h1
                    class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-bold text-[#252525] leading-tight"
                >
                    Smith Laundary
                </h1>
                <p
                    class="text-base sm:text-lg md:text-xl text-[#252525]/80 leading-relaxed max-w-2xl mx-auto lg:mx-0"
                >
                    ร้านซักรีดเสื้อผ้าที่ให้บริการด้วยความใส่ใจ ผ้าสะอาด หอม
                    นุ่ม พร้อมส่งมอบความสดใสให้กับทุกชิ้นผ้าของคุณ
                </p>
                <div
                    class="flex flex-col sm:flex-row gap-3 sm:gap-4 justify-center lg:justify-start"
                >
                    <button
                        onclick={() => scrollToSection("pricing")}
                        class="bg-[#33A1E0] text-white px-6 sm:px-8 py-3 sm:py-4 rounded-lg hover:bg-[#2a8bc7] transition-all hover:shadow-lg font-medium text-base sm:text-lg w-full sm:w-auto"
                    >
                        ดูราคาบริการ
                    </button>
                    <button
                        onclick={() => scrollToSection("contact")}
                        class="bg-white text-[#33A1E0] px-6 sm:px-8 py-3 sm:py-4 rounded-lg hover:bg-[#FFF9AF] transition-all hover:shadow-lg font-medium text-base sm:text-lg border-2 border-[#33A1E0] w-full sm:w-auto"
                    >
                        ติดต่อเรา
                    </button>
                </div>
                <div
                    class="flex flex-col sm:flex-row flex-wrap gap-4 sm:gap-8 pt-4 sm:pt-6 justify-center lg:justify-start"
                >
                    <div
                        class="flex items-center gap-2 justify-center lg:justify-start"
                    >
                        <Clock
                            class="w-4 h-4 sm:w-5 sm:h-5 text-[#33A1E0] shrink-0"
                        />
                        <span class="text-[#252525]/70 text-sm sm:text-base"
                            >เปิดทุกวัน 08:00-21:00</span
                        >
                    </div>
                    <div
                        class="flex items-center gap-2 justify-center lg:justify-start"
                    >
                        <Phone
                            class="w-4 h-4 sm:w-5 sm:h-5 text-[#33A1E0] shrink-0"
                        />
                        <span class="text-[#252525]/70 text-sm sm:text-base"
                            >063-657-0399</span
                        >
                    </div>
                </div>
            </div>

            <!-- Image Placeholder -->
            <div class="relative order-first lg:order-last">
                <div
                    class="aspect-square bg-linear-to-br from-[#33A1E0] to-[#2a8bc7] rounded-2xl sm:rounded-3xl shadow-2xl flex items-center justify-center"
                >
                    <div class="text-center text-white p-4 sm:p-8">
                        <Shirt
                            class="w-20 h-20 sm:w-24 md:w-32 sm:h-24 md:h-32 mx-auto mb-2 sm:mb-4 opacity-50"
                        />
                        <p class="text-base sm:text-xl font-medium">
                            รูปภาพร้านซักรีด
                        </p>
                        <p class="text-xs sm:text-sm opacity-80 mt-1 sm:mt-2">
                            (แทนด้วยรูปจริง)
                        </p>
                    </div>
                </div>
                <!-- Floating Elements -->
                <div
                    class="absolute -top-4 -right-4 sm:-top-6 sm:-right-6 bg-[#FFF9AF] w-16 h-16 sm:w-24 sm:h-24 rounded-full animate-bounce-slow shadow-lg hidden sm:block"
                ></div>
                <div
                    class="absolute -bottom-4 -left-4 sm:-bottom-6 sm:-left-6 bg-[#33A1E0]/20 w-20 h-20 sm:w-32 sm:h-32 rounded-full animate-pulse hidden sm:block"
                ></div>
            </div>
        </div>
    </div>
</section>

<!-- Services Section -->
<section id="services" class="py-12 sm:py-16 md:py-20 bg-white">
    <div class="container mx-auto px-4">
        <div class="text-center mb-10 sm:mb-12 md:mb-16">
            <h2
                class="text-3xl sm:text-4xl md:text-5xl font-bold text-[#252525] mb-3 sm:mb-4"
            >
                บริการของเรา
            </h2>
            <p class="text-base sm:text-lg md:text-xl text-[#252525]/70">
                เลือกบริการที่ตรงกับความต้องการของคุณ
            </p>
        </div>

        <div
            class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 sm:gap-8"
        >
            {#each [{ icon: Sparkles, title: "ซัก + รีด", description: "บริการซักและรีดผ้าครบวงจร ผ้านุ่ม หอม สะอาด" }, { icon: Shirt, title: "รีดอย่างเดียว", description: "บริการรีดผ้าเรียบร้อย ดูดี พร้อมใส่" }, { icon: Clock, title: "ซักอย่างเดียว", description: "บริการซักผ้าเฉพาะ สะอาดหมดจด" }] as service}
                <div
                    class="bg-white rounded-xl sm:rounded-2xl shadow-lg hover:shadow-2xl transition-all duration-300 overflow-hidden group hover:-translate-y-2"
                >
                    <div class="p-6 sm:p-8">
                        <div
                            class="bg-[#33A1E0]/10 w-12 h-12 sm:w-16 sm:h-16 rounded-full flex items-center justify-center mb-4 sm:mb-6 group-hover:bg-[#33A1E0] transition-colors"
                        >
                            <svelte:component
                                this={service.icon}
                                class="w-6 h-6 sm:w-8 sm:h-8 text-[#33A1E0] group-hover:text-white transition-colors"
                            />
                        </div>
                        <h3
                            class="text-xl sm:text-2xl font-bold text-[#252525] mb-2 sm:mb-3"
                        >
                            {service.title}
                        </h3>
                        <p
                            class="text-sm sm:text-base text-[#252525]/70 leading-relaxed"
                        >
                            {service.description}
                        </p>
                    </div>
                    <div
                        class="h-1.5 sm:h-2 bg-linear-to-r from-[#33A1E0] to-[#2a8bc7]"
                    ></div>
                </div>
            {/each}
        </div>
    </div>
</section>

<style>
    @keyframes bounce-slow {
        0%,
        100% {
            transform: translateY(0);
        }
        50% {
            transform: translateY(-20px);
        }
    }

    .animate-bounce-slow {
        animation: bounce-slow 3s ease-in-out infinite;
    }
</style>
