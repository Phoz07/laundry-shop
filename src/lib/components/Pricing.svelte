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

<section
    id="pricing"
    class="py-16 sm:py-20 md:py-24 lg:py-32 bg-linear-to-br from-[#FFF9AF]/30 to-[#33A1E0]/10"
>
    <div class="container mx-auto px-4 sm:px-6">
        <div class="text-center mb-12 sm:mb-16 md:mb-20">
            <h2
                class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-bold text-[#252525] mb-4 sm:mb-6 lg:mb-8"
            >
                ราคาบริการ
            </h2>
            <p class="text-lg sm:text-xl md:text-2xl lg:text-3xl text-[#252525]/70 max-w-3xl mx-auto">
                ราคาที่เป็นธรรม คุณภาพที่คุณวางใจได้
            </p>
        </div>

        <div
            class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 sm:gap-8 lg:gap-10 max-w-7xl mx-auto"
        >
            <!-- Wash + Iron -->
            <div
                class="bg-white rounded-2xl sm:rounded-3xl shadow-xl overflow-hidden border border-gray-100 hover:shadow-2xl transition-shadow duration-300"
            >
                <div class="bg-[#33A1E0] text-white p-6 sm:p-8 lg:p-10 text-center">
                    <Sparkles
                        class="w-12 h-12 sm:w-14 sm:h-14 lg:w-16 lg:h-16 mx-auto mb-3 sm:mb-4"
                    />
                    <h3 class="text-2xl sm:text-3xl lg:text-4xl font-bold">ซัก + รีด</h3>
                </div>
                <div class="p-6 sm:p-8 lg:p-10 space-y-4 sm:space-y-6">
                    {#each washAndIronPrices as item}
                        <div
                            class="flex justify-between items-start sm:items-center py-3 sm:py-4 border-b border-gray-100 gap-3 sm:gap-4 last:border-b-0"
                        >
                            <span
                                class="text-[#252525] font-medium text-base sm:text-lg lg:text-xl flex-1"
                            >
                                {item.item}
                            </span>
                            <span
                                class="text-[#33A1E0] font-bold text-base sm:text-lg lg:text-xl whitespace-nowrap"
                            >
                                {item.price}
                            </span>
                        </div>
                    {/each}
                </div>
            </div>

            <!-- Iron Only -->
            <div
                class="bg-white rounded-2xl sm:rounded-3xl shadow-xl overflow-hidden border border-gray-100 hover:shadow-2xl transition-shadow duration-300"
            >
                <div class="bg-[#33A1E0] text-white p-6 sm:p-8 lg:p-10 text-center">
                    <Wind
                        class="w-12 h-12 sm:w-14 sm:h-14 lg:w-16 lg:h-16 mx-auto mb-3 sm:mb-4"
                    />
                    <h3 class="text-2xl sm:text-3xl lg:text-4xl font-bold">รีดอย่างเดียว</h3>
                </div>
                <div class="p-6 sm:p-8 lg:p-10 space-y-4 sm:space-y-6">
                    {#each ironOnlyPrices as item}
                        <div
                            class="flex justify-between items-start sm:items-center py-3 sm:py-4 border-b border-gray-100 gap-3 sm:gap-4 last:border-b-0"
                        >
                            <span
                                class="text-[#252525] font-medium text-base sm:text-lg lg:text-xl flex-1"
                            >
                                {item.item}
                            </span>
                            <span
                                class="text-[#33A1E0] font-bold text-base sm:text-lg lg:text-xl whitespace-nowrap"
                            >
                                {item.price}
                            </span>
                        </div>
                    {/each}
                </div>
            </div>

            <!-- Wash Only -->
            <div
                class="bg-white rounded-2xl sm:rounded-3xl shadow-xl overflow-hidden md:col-span-2 lg:col-span-1 border border-gray-100 hover:shadow-2xl transition-shadow duration-300"
            >
                <div class="bg-[#33A1E0] text-white p-6 sm:p-8 lg:p-10 text-center">
                    <Droplet
                        class="w-12 h-12 sm:w-14 sm:h-14 lg:w-16 lg:h-16 mx-auto mb-3 sm:mb-4"
                    />
                    <h3 class="text-2xl sm:text-3xl lg:text-4xl font-bold">ซักอย่างเดียว</h3>
                </div>
                <div class="p-6 sm:p-8 lg:p-10 space-y-4 sm:space-y-6">
                    {#each washOnlyPrices as item}
                        <div
                            class="flex justify-between items-start sm:items-center py-3 sm:py-4 border-b border-gray-100 gap-3 sm:gap-4 last:border-b-0"
                        >
                            <span
                                class="text-[#252525] font-medium text-base sm:text-lg lg:text-xl flex-1"
                            >
                                {item.item}
                            </span>
                            <span
                                class="text-[#33A1E0] font-bold text-base sm:text-lg lg:text-xl whitespace-nowrap"
                            >
                                {item.price}
                            </span>
                        </div>
                    {/each}
                </div>
            </div>
        </div>

        <div class="mt-12 sm:mt-16 text-center">
            <p class="text-[#252525]/70 text-base sm:text-lg md:text-xl lg:text-2xl px-4 max-w-3xl mx-auto">
                💡 ราคาอาจมีการเปลี่ยนแปลงตามความเหมาะสม
            </p>
        </div>
    </div>
</section>
