<script lang="ts">
    import { Sparkles, Wind, Droplet } from "@lucide/svelte";

    const washAndIronPrices = [
        { item: "เสื้อ กางเกง ธรรมดา", price: "20 บาท/ตัว" },
        { item: "ชุดเดรส", price: "40 บาท/ตัว" },
        { item: "ชุดสูท", price: "100 บาท/ชุด" },
        { item: "ชุดผ้าปูที่นอน + ผ้านวม", price: "180-200 บาท/ชุด" },
    ];

    const ironOnlyPrices = [
        { item: "เสื้อ กางเกง ธรรมดา", price: "10 บาท/ตัว" },
        { item: "ชุดเดรส", price: "20 บาท/ตัว" },
        { item: "ชุดสูท", price: "50 บาท/ชุด" },
    ];

    const washOnlyPrices = [
        { item: "เสื้อ กางเกง ธรรมดา", price: "10 บาท/ตัว" },
        { item: "ชุดเดรส", price: "20 บาท/ตัว" },
        { item: "ผ้านวม", price: "100 บาท/ผืน" },
    ];
</script>

<!-- Pricing Section -->
<section
    id="pricing"
    class="py-12 sm:py-16 md:py-20 bg-gradient-to-br from-[#FFF9AF]/30 to-[#33A1E0]/10"
>
    <div class="container mx-auto px-4">
        <div class="text-center mb-10 sm:mb-12 md:mb-16">
            <h2
                class="text-3xl sm:text-4xl md:text-5xl font-bold text-[#252525] mb-3 sm:mb-4"
            >
                ราคาบริการ
            </h2>
            <p class="text-base sm:text-lg md:text-xl text-[#252525]/70">
                ราคาที่เป็นธรรม คุณภาพที่คุณวางใจได้
            </p>
        </div>

        <div
            class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 sm:gap-8 max-w-7xl mx-auto"
        >
            <!-- Wash + Iron -->
            <div
                class="bg-white rounded-xl sm:rounded-2xl shadow-xl overflow-hidden"
            >
                <div class="bg-[#33A1E0] text-white p-5 sm:p-6 text-center">
                    <Sparkles
                        class="w-10 h-10 sm:w-12 sm:h-12 mx-auto mb-2 sm:mb-3"
                    />
                    <h3 class="text-xl sm:text-2xl font-bold">ซัก + รีด</h3>
                </div>
                <div class="p-5 sm:p-6 space-y-3 sm:space-y-4">
                    {#each washAndIronPrices as item}
                        <div
                            class="flex justify-between items-start sm:items-center py-2 sm:py-3 border-b border-gray-100 gap-2"
                        >
                            <span
                                class="text-[#252525] font-medium text-sm sm:text-base flex-1"
                            >
                                {item.item}
                            </span>
                            <span
                                class="text-[#33A1E0] font-bold text-sm sm:text-base whitespace-nowrap"
                            >
                                {item.price}
                            </span>
                        </div>
                    {/each}
                </div>
            </div>

            <!-- Iron Only -->
            <div
                class="bg-white rounded-xl sm:rounded-2xl shadow-xl overflow-hidden"
            >
                <div class="bg-[#33A1E0] text-white p-5 sm:p-6 text-center">
                    <Wind
                        class="w-10 h-10 sm:w-12 sm:h-12 mx-auto mb-2 sm:mb-3"
                    />
                    <h3 class="text-xl sm:text-2xl font-bold">รีดอย่างเดียว</h3>
                </div>
                <div class="p-5 sm:p-6 space-y-3 sm:space-y-4">
                    {#each ironOnlyPrices as item}
                        <div
                            class="flex justify-between items-start sm:items-center py-2 sm:py-3 border-b border-gray-100 gap-2"
                        >
                            <span
                                class="text-[#252525] font-medium text-sm sm:text-base flex-1"
                            >
                                {item.item}
                            </span>
                            <span
                                class="text-[#33A1E0] font-bold text-sm sm:text-base whitespace-nowrap"
                            >
                                {item.price}
                            </span>
                        </div>
                    {/each}
                </div>
            </div>

            <!-- Wash Only -->
            <div
                class="bg-white rounded-xl sm:rounded-2xl shadow-xl overflow-hidden md:col-span-2 lg:col-span-1"
            >
                <div class="bg-[#33A1E0] text-white p-5 sm:p-6 text-center">
                    <Droplet
                        class="w-10 h-10 sm:w-12 sm:h-12 mx-auto mb-2 sm:mb-3"
                    />
                    <h3 class="text-xl sm:text-2xl font-bold">ซักอย่างเดียว</h3>
                </div>
                <div class="p-5 sm:p-6 space-y-3 sm:space-y-4">
                    {#each washOnlyPrices as item}
                        <div
                            class="flex justify-between items-start sm:items-center py-2 sm:py-3 border-b border-gray-100 gap-2"
                        >
                            <span
                                class="text-[#252525] font-medium text-sm sm:text-base flex-1"
                            >
                                {item.item}
                            </span>
                            <span
                                class="text-[#33A1E0] font-bold text-sm sm:text-base whitespace-nowrap"
                            >
                                {item.price}
                            </span>
                        </div>
                    {/each}
                </div>
            </div>
        </div>

        <div class="mt-8 sm:mt-12 text-center">
            <p class="text-[#252525]/70 text-sm sm:text-base md:text-lg px-4">
                💡 ราคาอาจมีการเปลี่ยนแปลงตามความเหมาะสม
            </p>
        </div>
    </div>
</section>
