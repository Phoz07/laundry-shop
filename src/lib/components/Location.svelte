<script lang="ts">
    import { MapPin, Phone, Mail, Clock } from "@lucide/svelte";
</script>

<!-- Location Section -->
<section id="location" class="py-12 sm:py-16 md:py-20 bg-white">
    <div class="container mx-auto px-4">
        <div class="text-center mb-10 sm:mb-12 md:mb-16">
            <h2
                class="text-3xl sm:text-4xl md:text-5xl font-bold text-[#252525] mb-3 sm:mb-4"
            >
                ที่ตั้งร้าน
            </h2>
            <p class="text-base sm:text-lg md:text-xl text-[#252525]/70">
                มาพบเราได้ที่นี่
            </p>
        </div>

        <div
            class="grid grid-cols-1 lg:grid-cols-2 gap-8 sm:gap-10 md:gap-12 max-w-7xl mx-auto"
        >
            <!-- Map Placeholder -->
            <div
                class="bg-gradient-to-br from-[#33A1E0]/20 to-[#FFF9AF]/30 rounded-xl sm:rounded-2xl shadow-xl aspect-video sm:aspect-auto sm:min-h-[350px] md:min-h-[400px] flex items-center justify-center order-2 lg:order-1"
            >
                <div class="text-center p-6 sm:p-8">
                    <MapPin
                        class="w-16 h-16 sm:w-20 md:w-24 sm:h-20 md:h-24 mx-auto mb-3 sm:mb-4 text-[#33A1E0]"
                    />
                    <p
                        class="text-lg sm:text-xl font-medium text-[#252525] mb-2"
                    >
                        แผนที่ตำแหน่งร้าน
                    </p>
                    <p class="text-xs sm:text-sm text-[#252525]/70">
                        (ใส่ Google Maps Embed จริง)
                    </p>
                </div>
            </div>

            <!-- Contact Info -->
            <div class="space-y-4 sm:space-y-6 order-1 lg:order-2">
                <div
                    class="bg-gradient-to-br from-[#33A1E0] to-[#2a8bc7] text-white p-6 sm:p-8 rounded-xl sm:rounded-2xl shadow-xl"
                >
                    <h3 class="text-xl sm:text-2xl font-bold mb-4 sm:mb-6">
                        ข้อมูลติดต่อ
                    </h3>
                    <div class="space-y-4 sm:space-y-5">
                        <div class="flex items-start gap-3 sm:gap-4">
                            <MapPin
                                class="w-5 h-5 sm:w-6 sm:h-6 flex-shrink-0 mt-0.5 sm:mt-1"
                            />
                            <div>
                                <p
                                    class="font-medium mb-1 text-sm sm:text-base"
                                >
                                    ที่อยู่
                                </p>
                                <p
                                    class="opacity-90 text-sm sm:text-base leading-relaxed"
                                >
                                    123 ถนนตัวอย่าง แขวง/ตำบล เขต/อำเภอ<br
                                        class="hidden sm:inline"
                                    />
                                    จังหวัด 10XXX
                                </p>
                            </div>
                        </div>
                        <div class="flex items-start gap-3 sm:gap-4">
                            <Phone
                                class="w-5 h-5 sm:w-6 sm:h-6 flex-shrink-0 mt-0.5 sm:mt-1"
                            />
                            <div>
                                <p
                                    class="font-medium mb-1 text-sm sm:text-base"
                                >
                                    โทรศัพท์
                                </p>
                                <p class="opacity-90 text-sm sm:text-base">
                                    <a
                                        href="tel:02-XXX-XXXX"
                                        class="hover:underline">02-XXX-XXXX</a
                                    >,
                                    <a
                                        href="tel:08X-XXX-XXXX"
                                        class="hover:underline">08X-XXX-XXXX</a
                                    >
                                </p>
                            </div>
                        </div>
                        <div class="flex items-start gap-3 sm:gap-4">
                            <Mail
                                class="w-5 h-5 sm:w-6 sm:h-6 flex-shrink-0 mt-0.5 sm:mt-1"
                            />
                            <div>
                                <p
                                    class="font-medium mb-1 text-sm sm:text-base"
                                >
                                    อีเมล
                                </p>
                                <p class="opacity-90 text-sm sm:text-base">
                                    <a
                                        href="mailto:smith.laundary@example.com"
                                        class="hover:underline break-all"
                                        >smith.laundary@example.com</a
                                    >
                                </p>
                            </div>
                        </div>
                        <div class="flex items-start gap-3 sm:gap-4">
                            <Clock
                                class="w-5 h-5 sm:w-6 sm:h-6 flex-shrink-0 mt-0.5 sm:mt-1"
                            />
                            <div>
                                <p
                                    class="font-medium mb-1 text-sm sm:text-base"
                                >
                                    เวลาทำการ
                                </p>
                                <p class="opacity-90 text-sm sm:text-base">
                                    จันทร์ - อาทิตย์: 08:00 - 20:00
                                </p>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="bg-[#FFF9AF] p-4 sm:p-6 rounded-xl sm:rounded-2xl">
                    <p
                        class="text-[#252525] font-medium text-center text-sm sm:text-base leading-relaxed"
                    >
                        🚗 มีที่จอดรถสะดวกสบาย<br />
                        🚇 ใกล้สถานี MRT/BTS (ตัวอย่าง)
                    </p>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Contact/CTA Section -->
<section
    id="contact"
    class="py-12 sm:py-16 md:py-20 bg-gradient-to-br from-[#33A1E0] to-[#2a8bc7]"
>
    <div class="container mx-auto px-4 text-center">
        <h2
            class="text-3xl sm:text-4xl md:text-5xl font-bold text-white mb-4 sm:mb-6 leading-tight"
        >
            พร้อมให้บริการคุณแล้ว!
        </h2>
        <p
            class="text-base sm:text-lg md:text-xl text-white/90 mb-6 sm:mb-8 max-w-2xl mx-auto leading-relaxed px-4"
        >
            นำผ้าของคุณมาดูแลกับเรา รับประกันความสะอาดและคุณภาพ
        </p>
        <div
            class="flex flex-col sm:flex-row gap-3 sm:gap-4 justify-center max-w-md mx-auto sm:max-w-none"
        >
            <a
                href="tel:02-XXX-XXXX"
                class="bg-white text-[#33A1E0] px-6 sm:px-8 py-3 sm:py-4 rounded-lg hover:bg-[#FFF9AF] transition-all hover:shadow-lg font-medium text-base sm:text-lg inline-flex items-center justify-center gap-2"
            >
                <Phone class="w-5 h-5" />
                <span>โทรติดต่อเลย</span>
            </a>
            <button
                onclick={() => {
                    const element = document.getElementById("location");
                    if (element) {
                        element.scrollIntoView({ behavior: "smooth" });
                    }
                }}
                class="bg-[#FFF9AF] text-[#252525] px-6 sm:px-8 py-3 sm:py-4 rounded-lg hover:bg-yellow-200 transition-all hover:shadow-lg font-medium text-base sm:text-lg inline-flex items-center justify-center gap-2"
            >
                <MapPin class="w-5 h-5" />
                <span>ดูแผนที่</span>
            </button>
        </div>
    </div>
</section>
