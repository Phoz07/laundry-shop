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
    <div class="container mx-auto px-3 sm:px-4 lg:px-6">
        <div class="text-center mb-8 sm:mb-12 md:mb-16">
            <h2
                class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-bold text-[#252525] mb-3 sm:mb-4 lg:mb-6"
            >
                ราคาบริการ
            </h2>
            <p class="text-base sm:text-lg md:text-xl lg:text-2xl text-[#252525]/70 max-w-3xl mx-auto">
                ราคาที่เป็นธรรม คุณภาพที่คุณวางใจได้
            </p>
        </div>

        <div
            class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 sm:gap-6 lg:gap-8 max-w-7xl mx-auto"
        >
            <!-- Wash + Iron -->
            <div
                class="bg-white rounded-xl sm:rounded-2xl lg:rounded-3xl shadow-lg overflow-hidden border border-gray-100 hover:shadow-xl transition-shadow duration-300"
            >
                <div class="bg-[#33A1E0] text-white p-4 sm:p-6 lg:p-8 text-center h-[30%] flex flex-col justify-center items-center">
                    <Sparkles
                        class="w-8 h-8 sm:w-10 sm:h-10 lg:w-12 lg:h-12 mx-auto mb-2 sm:mb-3"
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
                <div class="bg-[#33A1E0] text-white p-6 sm:p-8 lg:p-10 text-center h-[30%] flex flex-col justify-center items-center">
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
                <div class="bg-[#33A1E0] text-white p-6 sm:p-8 lg:p-10 text-center h-[30%] flex flex-col justify-center items-center">
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
