<script lang="ts">
    import { MapPin, Phone, Mail, Clock } from "@lucide/svelte";
    import Button from "$lib/components/ui/button/button.svelte";
</script>

<!-- Location Section -->
<section id="location" class="py-16 sm:py-20 md:py-24 lg:py-32 bg-white">
    <div class="container mx-auto px-4 sm:px-6">
        <div class="text-center mb-12 sm:mb-16 md:mb-20">
            <h2
                class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-bold text-[#252525] mb-4 sm:mb-6 lg:mb-8"
            >
                ที่ตั้งร้าน
            </h2>
            <p class="text-lg sm:text-xl md:text-2xl lg:text-3xl text-[#252525]/70 max-w-3xl mx-auto">
                มาพบเราได้ที่นี่
            </p>
        </div>

        <div
            class="grid grid-cols-1 lg:grid-cols-2 gap-8 sm:gap-10 md:gap-12 lg:gap-16 max-w-7xl mx-auto"
        >
            <!-- Map Section -->
            <div
                class="rounded-2xl sm:rounded-3xl shadow-xl overflow-hidden aspect-video lg:aspect-[4/3] min-h-[350px] sm:min-h-[400px] lg:min-h-[500px] order-2 lg:order-1"
            >
                <iframe
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3872.0531688919978!2d100.74142137585208!3d13.955439892544662!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x311d79e403c2b4a9%3A0x85059d2bf745cb96!2z4Lij4LmJ4Liy4LiZ4LiL4Lix4LiB4Lij4Li14LiU4Liq4Lih4Li04LiX!5e0!3m2!1sen!2sth!4v1768113468711!5m2!1sen!2sth"
                    width="100%"
                    height="100%"
                    style="border:0; min-height: 350px;"
                    loading="lazy"
                    referrerpolicy="no-referrer-when-downgrade"
                    title="Smith Laundary Location Map"
                    class="w-full h-full"
                ></iframe>
            </div>

            <!-- Contact Info -->
            <div class="space-y-6 sm:space-y-8 order-1 lg:order-2">
                <div
                    class="bg-linear-to-br from-[#33A1E0] to-[#2a8bc7] text-white p-8 sm:p-10 lg:p-12 rounded-2xl sm:rounded-3xl shadow-xl h-full"
                >
                    <h3 class="text-2xl sm:text-3xl lg:text-4xl font-bold mb-6 sm:mb-8">
                        ข้อมูลติดต่อ
                    </h3>
                    <div class="space-y-6 sm:space-y-8">
                        <div class="flex items-start gap-4 sm:gap-6">
                            <MapPin
                                class="w-6 h-6 sm:w-8 sm:h-8 lg:w-10 lg:h-10 shrink-0 mt-1"
                            />
                            <div>
                                <p
                                    class="font-medium mb-2 text-base sm:text-lg lg:text-xl"
                                >
                                    50/233 หมู่ที่ 4 หมู่บ้านแพรมาพร
                                </p>
                                <p
                                    class="opacity-90 text-base sm:text-lg lg:text-xl leading-relaxed"
                                >
                                    ต.บึงคำพร้อย อ.ลำลูกกา<br
                                        class="hidden sm:inline lg:hidden"
                                    />
                                    จ.ปทุมธานี 12150
                                </p>
                            </div>
                        </div>
                        <div class="flex items-start gap-4 sm:gap-6">
                            <Phone
                                class="w-6 h-6 sm:w-8 sm:h-8 lg:w-10 lg:h-10 shrink-0 mt-1"
                            />
                            <div>
                                <p
                                    class="font-medium mb-2 text-base sm:text-lg lg:text-xl"
                                >
                                    โทรศัพท์
                                </p>
                                <div class="space-y-1">
                                    <p class="opacity-90 text-base sm:text-lg lg:text-xl">
                                        <a
                                            href="tel:063-657-0399"
                                            class="hover:underline transition-colors">063-657-0399</a
                                        >
                                    </p>
                                    <p class="opacity-90 text-base sm:text-lg lg:text-xl">
                                        <a
                                            href="tel:088-921-5124"
                                            class="hover:underline transition-colors">088-921-5124</a
                                        >
                                    </p>
                                </div>
                            </div>
                        </div>
                        <div class="flex items-start gap-4 sm:gap-6">
                            <Clock
                                class="w-6 h-6 sm:w-8 sm:h-8 lg:w-10 lg:h-10 shrink-0 mt-1"
                            />
                            <div>
                                <p
                                    class="font-medium mb-2 text-base sm:text-lg lg:text-xl"
                                >
                                    เวลาทำการ
                                </p>
                                <p class="opacity-90 text-base sm:text-lg lg:text-xl">
                                    จันทร์ - อาทิตย์: 08:00 - 21:00
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Contact/CTA Section -->
<section
    id="contact"
    class="py-16 sm:py-20 md:py-24 lg:py-32 bg-linear-to-br from-[#33A1E0] to-[#2a8bc7] safe-bottom"
>
    <div class="container mx-auto px-4 sm:px-6 text-center">
        <h2
            class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-bold text-white mb-6 sm:mb-8 lg:mb-10 leading-tight"
        >
            พร้อมให้บริการคุณแล้ว!
        </h2>
        <p
            class="text-lg sm:text-xl md:text-2xl lg:text-3xl text-white/90 mb-8 sm:mb-10 lg:mb-12 max-w-4xl mx-auto leading-relaxed px-4"
        >
            นำผ้าของคุณมาดูแลกับเรา รับประกันความสะอาดและคุณภาพ
        </p>
        <div
            class="flex flex-col sm:flex-row gap-4 sm:gap-6 justify-center max-w-md mx-auto sm:max-w-none"
        >
            <Button
                href="tel:063-657-0399"
                variant="secondary"
                class="px-8 sm:px-10 lg:px-12 py-4 sm:py-5 lg:py-6 text-lg sm:text-xl lg:text-2xl w-full sm:w-auto h-auto min-h-[52px] sm:min-h-[56px]"
            >
                <Phone class="w-5 h-5 sm:w-6 sm:h-6 lg:w-7 lg:h-7" />
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
                class="px-8 sm:px-10 lg:px-12 py-4 sm:py-5 lg:py-6 text-lg sm:text-xl lg:text-2xl w-full sm:w-auto h-auto min-h-[52px] sm:min-h-[56px] bg-white/10 border-white/20 text-white hover:bg-white/20 hover:border-white/30"
            >
                <MapPin class="w-5 h-5 sm:w-6 sm:h-6 lg:w-7 lg:h-7" />
                <span>ดูแผนที่</span>
            </Button>
        </div>
    </div>
</section>
