<script lang="ts">
    import { Sparkles, Facebook, Instagram, Phone, Mail } from "@lucide/svelte";
    import Button from "$lib/components/ui/button/button.svelte";

    const scrollToSection = (id: string) => {
        const element = document.getElementById(id);
        if (element) {
            element.scrollIntoView({ behavior: "smooth" });
        }
    };
</script>

<!-- Footer -->
<footer class="bg-[#252525] text-white py-12 sm:py-16 lg:py-20">
    <div class="container mx-auto px-4 sm:px-6">
        <div
            class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8 sm:gap-10 lg:gap-12 mb-10 sm:mb-12"
        >
            <!-- Brand -->
            <div class="col-span-1 text-center sm:text-left">
                <div
                    class="flex items-center gap-3 justify-center sm:justify-start mb-4 sm:mb-6"
                >
                    <Sparkles
                        class="w-7 h-7 sm:w-8 sm:h-8 lg:w-10 lg:h-10 text-[#33A1E0]"
                    />
                    <span class="text-xl sm:text-2xl lg:text-3xl font-bold"
                        >Smith Laundary</span
                    >
                </div>
                <p
                    class="text-white/70 text-base sm:text-lg lg:text-xl leading-relaxed"
                >
                    ร้านซักรีดคุณภาพที่ใส่ใจในทุกรายละเอียด
                </p>
            </div>

            <!-- Quick Links -->
            <div class="text-center sm:text-left">
                <h3
                    class="font-bold mb-4 sm:mb-6 text-[#33A1E0] text-lg sm:text-xl lg:text-2xl"
                >
                    ลิงก์ด่วน
                </h3>
                <div
                    class="flex flex-col text-base sm:text-lg lg:text-xl text-white/70"
                >
                    <div
                        class="hover:text-white transition-colors cursor-pointer"
                    >
                        <Button
                            variant="ghost"
                            onclick={() => scrollToSection("hero")}
                        >
                            หน้าแรก
                        </Button>
                    </div>
                    <div
                        class="hover:text-white transition-colors cursor-pointer"
                    >
                        <Button
                            variant="ghost"
                            onclick={() => scrollToSection("services")}
                        >
                            บริการ
                        </Button>
                    </div>
                    <div
                        class="hover:text-white transition-colors cursor-pointer"
                    >
                        <Button
                            variant="ghost"
                            onclick={() => scrollToSection("pricing")}
                        >
                            ราคา
                        </Button>
                    </div>
                    <div
                        class="hover:text-white transition-colors cursor-pointer"
                    >
                        <Button
                            variant="ghost"
                            onclick={() => scrollToSection("location")}
                        >
                            ที่ตั้ง
                        </Button>
                    </div>
                </div>
                <!-- <Button
                    onclick={() => scrollToSection("hero")}
                    variant="ghost"
                    class="hover:text-[#33A1E0] transition-colors inline-block h-auto p-0 text-base sm:text-lg lg:text-xl text-left justify-center w-full sm:w-fit"
                >
                    หน้าแรก
                </Button>
                <Button
                    onclick={() => scrollToSection("services")}
                    variant="ghost"
                    class="hover:text-[#33A1E0] transition-colors inline-block h-auto p-0 text-base sm:text-lg lg:text-xl text-left justify-center w-full sm:w-fit"
                >
                    บริการ
                </Button>
                <Button
                    onclick={() => scrollToSection("pricing")}
                    variant="ghost"
                    class="hover:text-[#33A1E0] transition-colors inline-block h-auto p-0 text-base sm:text-lg lg:text-xl text-left justify-center w-full sm:w-fit"
                >
                    ราคา
                </Button>
                <Button
                    onclick={() => scrollToSection("location")}
                    variant="ghost"
                    class="hover:text-[#33A1E0] transition-colors inline-block h-auto p-0 text-base sm:text-lg lg:text-xl text-left justify-center w-full sm:w-fit"
                >
                    ที่ตั้ง
                </Button> -->
            </div>

            <!-- Services -->
            <div class="text-center sm:text-left">
                <h3
                    class="font-bold mb-4 sm:mb-6 text-[#33A1E0] text-lg sm:text-xl lg:text-2xl"
                >
                    บริการของเรา
                </h3>
                <div
                    class="flex flex-col space-y-3 text-base sm:text-lg lg:text-xl text-white/70"
                >
                    <div
                        class="hover:text-white transition-colors cursor-pointer"
                    >
                        ซัก + รีด
                    </div>
                    <div
                        class="hover:text-white transition-colors cursor-pointer"
                    >
                        รีดอย่างเดียว
                    </div>
                    <div
                        class="hover:text-white transition-colors cursor-pointer"
                    >
                        ซักอย่างเดียว
                    </div>
                    <div
                        class="hover:text-white transition-colors cursor-pointer"
                    >
                        บริการรับ-ส่ง
                    </div>
                </div>
            </div>

            <!-- Social Media & Contact -->
            <div class="text-center sm:text-left">
                <h3
                    class="font-bold mb-4 sm:mb-6 text-[#33A1E0] text-lg sm:text-xl lg:text-2xl"
                >
                    ติดตามเรา
                </h3>
                <div
                    class="flex gap-4 sm:gap-6 justify-center sm:justify-start mb-6"
                >
                    <a
                        href="https://facebook.com"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="bg-white/10 hover:bg-[#33A1E0] p-3 sm:p-4 rounded-full transition-colors min-h-[44px] min-w-[44px] flex items-center justify-center"
                        aria-label="Facebook"
                    >
                        <Facebook class="w-5 h-5 sm:w-6 sm:h-6 lg:w-7 lg:h-7" />
                    </a>
                    <a
                        href="https://instagram.com"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="bg-white/10 hover:bg-[#33A1E0] p-3 sm:p-4 rounded-full transition-colors min-h-[44px] min-w-[44px] flex items-center justify-center"
                        aria-label="Instagram"
                    >
                        <Instagram
                            class="w-5 h-5 sm:w-6 sm:h-6 lg:w-7 lg:h-7"
                        />
                    </a>
                </div>
                <div
                    class="text-sm sm:text-base lg:text-lg text-white/70 space-y-2 sm:space-y-3"
                >
                    <p
                        class="flex items-center gap-3 justify-center sm:justify-start hover:text-white transition-colors"
                    >
                        <Phone
                            class="w-4 h-4 sm:w-5 sm:h-5 lg:w-6 lg:h-6 shrink-0"
                        />
                        <a
                            href="tel:063-657-0399"
                            class="hover:text-[#33A1E0] transition-colors"
                            >063-657-0399, 088-921-5124</a
                        >
                    </p>
                    <p
                        class="flex items-center gap-3 justify-center sm:justify-start hover:text-white transition-colors"
                    >
                        <Mail
                            class="w-4 h-4 sm:w-5 sm:h-5 lg:w-6 lg:h-6 shrink-0"
                        />
                        <a
                            href="mailto:maverxk07@gmail.com"
                            class="hover:text-[#33A1E0] transition-colors break-all"
                        >
                            maverxk07@gmail.com
                        </a>
                    </p>
                </div>
            </div>
        </div>

        <!-- Copyright -->
        <div
            class="border-t border-white/10 pt-8 sm:pt-10 text-center text-sm sm:text-base lg:text-lg text-white/60"
        >
            <p class="mb-2 sm:mb-3">
                © 2026 Smith Laundary. All rights reserved.
            </p>
            <p>Made with ❤️ for your clean clothes</p>
        </div>
    </div>
</footer>
