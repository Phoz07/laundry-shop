<script lang="ts">
    import { Sparkles, Facebook, Instagram, Phone, Mail } from "@lucide/svelte";

    const scrollToSection = (id: string) => {
        const element = document.getElementById(id);
        if (element) {
            element.scrollIntoView({ behavior: "smooth" });
        }
    };
</script>

<!-- Footer -->
<footer class="bg-[#252525] text-white py-10 sm:py-12">
    <div class="container mx-auto px-4">
        <div
            class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8 sm:gap-10 mb-8"
        >
            <!-- Brand -->
            <div class="col-span-1 text-center sm:text-left">
                <div
                    class="flex items-center gap-2 justify-center sm:justify-start mb-3 sm:mb-4"
                >
                    <Sparkles class="w-6 h-6 sm:w-8 sm:h-8 text-[#33A1E0]" />
                    <span class="text-lg sm:text-xl font-bold"
                        >Smith Laundary</span
                    >
                </div>
                <p class="text-white/70 text-sm sm:text-base">
                    ร้านซักรีดคุณภาพที่ใส่ใจในทุกรายละเอียด
                </p>
            </div>

            <!-- Quick Links -->
            <div class="text-center sm:text-left">
                <h3
                    class="font-bold mb-3 sm:mb-4 text-[#33A1E0] text-base sm:text-lg"
                >
                    ลิงก์ด่วน
                </h3>
                <ul class="space-y-2 text-sm sm:text-base">
                    <li>
                        <button
                            onclick={() => scrollToSection("hero")}
                            class="hover:text-[#33A1E0] transition-colors inline-block"
                        >
                            หน้าแรก
                        </button>
                    </li>
                    <li>
                        <button
                            onclick={() => scrollToSection("services")}
                            class="hover:text-[#33A1E0] transition-colors inline-block"
                        >
                            บริการ
                        </button>
                    </li>
                    <li>
                        <button
                            onclick={() => scrollToSection("pricing")}
                            class="hover:text-[#33A1E0] transition-colors inline-block"
                        >
                            ราคา
                        </button>
                    </li>
                    <li>
                        <button
                            onclick={() => scrollToSection("location")}
                            class="hover:text-[#33A1E0] transition-colors inline-block"
                        >
                            ที่ตั้ง
                        </button>
                    </li>
                </ul>
            </div>

            <!-- Services -->
            <div class="text-center sm:text-left">
                <h3
                    class="font-bold mb-3 sm:mb-4 text-[#33A1E0] text-base sm:text-lg"
                >
                    บริการของเรา
                </h3>
                <ul class="space-y-2 text-sm sm:text-base text-white/70">
                    <li>• ซัก + รีด</li>
                    <li>• รีดอย่างเดียว</li>
                    <li>• ซักอย่างเดียว</li>
                    <li>• บริการรับ-ส่ง</li>
                </ul>
            </div>

            <!-- Social Media & Contact -->
            <div class="text-center sm:text-left">
                <h3
                    class="font-bold mb-3 sm:mb-4 text-[#33A1E0] text-base sm:text-lg"
                >
                    ติดตามเรา
                </h3>
                <div
                    class="flex gap-3 sm:gap-4 justify-center sm:justify-start mb-4"
                >
                    <a
                        href="https://facebook.com"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="bg-white/10 hover:bg-[#33A1E0] p-2.5 sm:p-3 rounded-full transition-colors"
                        aria-label="Facebook"
                    >
                        <Facebook class="w-4 h-4 sm:w-5 sm:h-5" />
                    </a>
                    <a
                        href="https://instagram.com"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="bg-white/10 hover:bg-[#33A1E0] p-2.5 sm:p-3 rounded-full transition-colors"
                        aria-label="Instagram"
                    >
                        <Instagram class="w-4 h-4 sm:w-5 sm:h-5" />
                    </a>
                </div>
                <div
                    class="text-xs sm:text-sm text-white/70 space-y-1.5 sm:space-y-2"
                >
                    <p
                        class="flex items-center gap-2 justify-center sm:justify-start"
                    >
                        <Phone
                            class="w-3.5 h-3.5 sm:w-4 sm:h-4 flex-shrink-0"
                        />
                        <a
                            href="tel:02-XXX-XXXX"
                            class="hover:text-[#33A1E0] transition-colors"
                            >02-XXX-XXXX</a
                        >
                    </p>
                    <p
                        class="flex items-center gap-2 justify-center sm:justify-start"
                    >
                        <Mail class="w-3.5 h-3.5 sm:w-4 sm:h-4 flex-shrink-0" />
                        <a
                            href="mailto:smith.laundary@example.com"
                            class="hover:text-[#33A1E0] transition-colors break-all"
                        >
                            smith.laundary@example.com
                        </a>
                    </p>
                </div>
            </div>
        </div>

        <!-- Copyright -->
        <div
            class="border-t border-white/10 pt-6 sm:pt-8 text-center text-xs sm:text-sm text-white/60"
        >
            <p class="mb-1.5 sm:mb-2">
                © 2024 Smith Laundary. All rights reserved.
            </p>
            <p>Made with ❤️ for your clean clothes</p>
        </div>
    </div>
</footer>
