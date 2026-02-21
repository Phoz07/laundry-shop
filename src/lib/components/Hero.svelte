<script lang="ts">
    import { Sparkles, Phone, Clock, Shirt } from "@lucide/svelte";
    import Button from "$lib/components/ui/button/button.svelte";

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
    class="pt-20 sm:pt-24 md:pt-28 min-h-screen flex items-center bg-linear-to-br from-[#33A1E0]/10 to-[#FFF9AF]/20 safe-top"
>
    <div class="container mx-auto px-4 sm:px-6 py-12 sm:py-16 md:py-20 lg:py-24">
        <div
            class="grid grid-cols-1 lg:grid-cols-2 gap-8 md:gap-12 lg:gap-16 items-center"
        >
            <!-- Text Content -->
            <div class="space-y-6 sm:space-y-8 text-center lg:text-left">
                <div
                    class="inline-block bg-[#FFF9AF] px-4 sm:px-6 py-2 sm:py-3 rounded-full"
                >
                    <span
                        class="text-[#252525] font-medium text-sm sm:text-base lg:text-lg"
                        >✨ บริการซักรีดคุณภาพ</span
                    >
                </div>
                <h1
                    class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl xl:text-8xl font-bold text-[#252525] leading-tight tracking-tight"
                >
                    Smith Laundary
                </h1>
                <p
                    class="text-lg sm:text-xl md:text-2xl lg:text-3xl text-[#252525]/80 leading-relaxed max-w-3xl mx-auto lg:mx-0"
                >
                    ร้านซักรีดเสื้อผ้าที่ให้บริการด้วยความใส่ใจ ผ้าสะอาด หอม
                    นุ่ม พร้อมส่งมอบความสดใสให้กับทุกชิ้นผ้าของคุณ
                </p>
                <div
                    class="flex flex-col sm:flex-row gap-4 sm:gap-6 justify-center lg:justify-start"
                >
                    <Button
                        onclick={() => scrollToSection("pricing")}
                        class="px-8 sm:px-10 lg:px-12 py-4 sm:py-5 lg:py-6 text-lg sm:text-xl lg:text-2xl w-full sm:w-auto h-auto min-h-[52px] sm:min-h-[56px]"
                    >
                        ดูราคาบริการ
                    </Button>
                    <Button
                        onclick={() => scrollToSection("contact")}
                        variant="outline"
                        class="px-8 sm:px-10 lg:px-12 py-4 sm:py-5 lg:py-6 text-lg sm:text-xl lg:text-2xl w-full sm:w-auto h-auto min-h-[52px] sm:min-h-[56px]"
                    >
                        ติดต่อเรา
                    </Button>
                </div>
                <div
                    class="flex flex-col sm:flex-row flex-wrap gap-6 sm:gap-8 lg:gap-12 pt-6 sm:pt-8 justify-center lg:justify-start"
                >
                    <div
                        class="flex items-center gap-3 sm:gap-4 justify-center lg:justify-start"
                    >
                        <Clock
                            class="w-5 h-5 sm:w-6 sm:h-6 lg:w-7 lg:h-7 text-[#33A1E0] shrink-0"
                        />
                        <span class="text-[#252525]/70 text-base sm:text-lg lg:text-xl"
                            >เปิดทุกวัน 08:00-21:00</span
                        >
                    </div>
                    <div
                        class="flex items-center gap-3 sm:gap-4 justify-center lg:justify-start"
                    >
                        <Phone
                            class="w-5 h-5 sm:w-6 sm:h-6 lg:w-7 lg:h-7 text-[#33A1E0] shrink-0"
                        />
                        <span class="text-[#252525]/70 text-base sm:text-lg lg:text-xl"
                            >063-657-0399</span
                        >
                    </div>
                </div>
            </div>

            <!-- Image Placeholder -->
            <div class="relative order-first lg:order-last">
                <div
                    class="aspect-square lg:aspect-[4/3] bg-linear-to-br from-[#33A1E0] to-[#2a8bc7] rounded-2xl sm:rounded-3xl lg:rounded-4xl shadow-2xl flex items-center justify-center overflow-hidden"
                >
                    <div class="text-center text-white p-6 sm:p-8 lg:p-12">
                        <Shirt
                            class="w-20 h-20 sm:w-24 md:w-32 lg:w-40 sm:h-24 md:h-32 lg:h-40 mx-auto mb-4 sm:mb-6 lg:mb-8 opacity-50"
                        />
                        <p class="text-lg sm:text-xl lg:text-2xl font-medium mb-2">
                            รูปภาพร้านซักรีด
                        </p>
                        <p class="text-sm sm:text-base lg:text-lg opacity-80">
                            (แทนด้วยรูปจริง)
                        </p>
                    </div>
                </div>
                <!-- Floating Elements -->
                <div
                    class="absolute -top-4 -right-4 sm:-top-6 sm:-right-6 lg:-top-8 lg:-right-8 bg-[#FFF9AF] w-16 h-16 sm:w-24 sm:h-24 lg:w-32 lg:h-32 rounded-full animate-bounce-slow shadow-lg hidden sm:block"
                ></div>
                <div
                    class="absolute -bottom-4 -left-4 sm:-bottom-6 sm:-left-6 lg:-bottom-8 lg:-left-8 bg-[#33A1E0]/20 w-20 h-20 sm:w-32 sm:h-32 lg:w-40 lg:h-40 rounded-full animate-pulse hidden sm:block"
                ></div>
            </div>
        </div>
    </div>
</section>

<!-- Services Section -->
<section id="services" class="py-16 sm:py-20 md:py-24 lg:py-32 bg-white">
    <div class="container mx-auto px-4 sm:px-6">
        <div class="text-center mb-12 sm:mb-16 md:mb-20">
            <h2
                class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-bold text-[#252525] mb-4 sm:mb-6 lg:mb-8"
            >
                บริการของเรา
            </h2>
            <p class="text-lg sm:text-xl md:text-2xl lg:text-3xl text-[#252525]/70 max-w-3xl mx-auto">
                เลือกบริการที่ตรงกับความต้องการของคุณ
            </p>
        </div>

        <div
            class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 sm:gap-8 lg:gap-10"
        >
            {#each [{ icon: Sparkles, title: "ซัก + รีด", description: "บริการซักและรีดผ้าครบวงจร ผ้านุ่ม หอม สะอาด" }, { icon: Shirt, title: "รีดอย่างเดียว", description: "บริการรีดผ้าเรียบร้อย ดูดี พร้อมใส่" }, { icon: Clock, title: "ซักอย่างเดียว", description: "บริการซักผ้าเฉพาะ สะอาดหมดจด" }] as service}
                <div
                    class="bg-white rounded-2xl sm:rounded-3xl shadow-lg hover:shadow-2xl transition-all duration-300 overflow-hidden group hover:-translate-y-3 border border-gray-100"
                >
                    <div class="p-8 sm:p-10 lg:p-12">
                        <div
                            class="bg-[#33A1E0]/10 w-16 h-16 sm:w-20 sm:h-20 lg:w-24 lg:h-24 rounded-full flex items-center justify-center mb-6 sm:mb-8 group-hover:bg-[#33A1E0] transition-colors"
                        >
                            <svelte:component
                                this={service.icon}
                                class="w-8 h-8 sm:w-10 sm:h-10 lg:w-12 lg:h-12 text-[#33A1E0] group-hover:text-white transition-colors"
                            />
                        </div>
                        <h3
                            class="text-2xl sm:text-3xl lg:text-4xl font-bold text-[#252525] mb-3 sm:mb-4 lg:mb-6"
                        >
                            {service.title}
                        </h3>
                        <p
                            class="text-base sm:text-lg lg:text-xl text-[#252525]/70 leading-relaxed"
                        >
                            {service.description}
                        </p>
                    </div>
                    <div
                        class="h-2 sm:h-3 bg-linear-to-r from-[#33A1E0] to-[#2a8bc7]"
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
