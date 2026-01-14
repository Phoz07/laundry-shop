<script lang="ts">
    import { MapPin, Phone, Mail, Clock } from "@lucide/svelte";
    import Button from "$lib/components/ui/button/button.svelte";
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
            <!-- Map Section -->
            <div
                class="rounded-xl sm:rounded-2xl shadow-xl overflow-hidden aspect-video sm:aspect-auto sm:min-h-87.5 md:min-h-100 order-2 lg:order-1"
            >
                <iframe
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3872.0531688919978!2d100.74142137585208!3d13.955439892544662!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x311d79e403c2b4a9%3A0x85059d2bf745cb96!2z4Lij4LmJ4Liy4LiZ4LiL4Lix4LiB4Lij4Li14LiU4Liq4Lih4Li04LiX!5e0!3m2!1sen!2sth!4v1768113468711!5m2!1sen!2sth"
                    width="100%"
                    height="100%"
                    style="border:0; min-height: 350px;"
                    loading="lazy"
                    referrerpolicy="no-referrer-when-downgrade"
                    title="Smith Laundary Location Map"
                ></iframe>
            </div>

            <!-- Contact Info -->
            <div class="space-y-4 sm:space-y-6 order-1 lg:order-2">
                <div
                    class="bg-linear-to-br from-[#33A1E0] to-[#2a8bc7] text-white p-6 sm:p-8 rounded-xl sm:rounded-2xl shadow-xl h-full"
                >
                    <h3 class="text-xl sm:text-2xl font-bold mb-4 sm:mb-6">
                        ข้อมูลติดต่อ
                    </h3>
                    <div class="space-y-4 sm:space-y-5">
                        <div class="flex items-start gap-3 sm:gap-4">
                            <MapPin
                                class="w-5 h-5 sm:w-6 sm:h-6 shrink-0 mt-0.5 sm:mt-1"
                            />
                            <div>
                                <p
                                    class="font-medium mb-1 text-sm sm:text-base"
                                >
                                    50/233 หมู่ที่ 4 หมู่บ้านแพรมาพร
                                </p>
                                <p
                                    class="opacity-90 text-sm sm:text-base leading-relaxed"
                                >
                                    ต.บึงคำพร้อย อ.ลำลูกกา<br
                                        class="hidden sm:inline"
                                    />
                                    จ.ปทุมธานี 12150
                                </p>
                            </div>
                        </div>
                        <div class="flex items-start gap-3 sm:gap-4">
                            <Phone
                                class="w-5 h-5 sm:w-6 sm:h-6 shrink-0 mt-0.5 sm:mt-1"
                            />
                            <div>
                                <p
                                    class="font-medium mb-1 text-sm sm:text-base"
                                >
                                    โทรศัพท์
                                </p>
                                <p class="opacity-90 text-sm sm:text-base">
                                    <a
                                        href="tel:063-657-0399"
                                        class="hover:underline">063-657-0399</a
                                    >,
                                    <a
                                        href="tel:088-921-5124"
                                        class="hover:underline">088-921-5124</a
                                    >
                                </p>
                            </div>
                        </div>
                        <div class="flex items-start gap-3 sm:gap-4">
                            <Clock
                                class="w-5 h-5 sm:w-6 sm:h-6 shrink-0 mt-0.5 sm:mt-1"
                            />
                            <div>
                                <p
                                    class="font-medium mb-1 text-sm sm:text-base"
                                >
                                    เวลาทำการ
                                </p>
                                <p class="opacity-90 text-sm sm:text-base">
                                    จันทร์ - อาทิตย์: 08:00 - 21:00
                                </p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- <div class="bg-[#FFF9AF] p-4 sm:p-6 rounded-xl sm:rounded-2xl">
                    <p
                        class="text-[#252525] font-medium text-center text-sm sm:text-base leading-relaxed"
                    >
                        🚗 มีที่จอดรถสะดวกสบาย<br />
                        🚇 ใกล้สถานี MRT/BTS (ตัวอย่าง)
                    </p>
                </div> -->
            </div>
        </div>
    </div>
</section>

<!-- Contact/CTA Section -->
<section
    id="contact"
    class="py-12 sm:py-16 md:py-20 bg-linear-to-br from-[#33A1E0] to-[#2a8bc7]"
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
            <Button
                href="tel:063-657-0399"
                variant="secondary"
                class="px-6 sm:px-8 py-3 sm:py-4 text-base sm:text-lg w-full sm:w-auto h-auto"
            >
                <Phone class="w-5 h-5" />
                <span>โทรติดต่อเลย</span>
            </Button>
            <Button
                onclick={() => {
                    const element = document.getElementById("location");
                    if (element) {
                        element.scrollIntoView({ behavior: "smooth" });
                    }
                }}
                variant="outline"
                class="px-6 sm:px-8 py-3 sm:py-4 text-base sm:text-lg w-full sm:w-auto h-auto"
            >
                <MapPin class="w-5 h-5" />
                <span>ดูแผนที่</span>
            </Button>
        </div>
    </div>
</section>
