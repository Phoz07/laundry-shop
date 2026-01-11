<script lang="ts">
    import { Sparkles, Menu, X } from "@lucide/svelte";

    let scrollY = $state(0);
    let mobileMenuOpen = $state(false);

    const scrollToSection = (id: string) => {
        const element = document.getElementById(id);
        if (element) {
            element.scrollIntoView({ behavior: "smooth" });
            mobileMenuOpen = false;
        }
    };

    const toggleMobileMenu = () => {
        mobileMenuOpen = !mobileMenuOpen;
    };
</script>

<svelte:window bind:scrollY />

<!-- Navbar -->
<nav
    class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 {scrollY >
    50
        ? 'bg-white shadow-md'
        : 'bg-white/95 backdrop-blur-sm'}"
>
    <div class="container mx-auto px-4 py-3 sm:py-4">
        <div class="flex items-center justify-between">
            <!-- Logo -->
            <button
                onclick={() => scrollToSection("hero")}
                class="flex items-center gap-2 hover:opacity-80 transition-opacity"
            >
                <Sparkles class="w-6 h-6 sm:w-8 sm:h-8 text-[#33A1E0]" />
                <span class="text-lg sm:text-2xl font-bold text-[#252525]"
                    >Smith Laundary</span
                >
            </button>

            <!-- Desktop Menu -->
            <div class="hidden md:flex items-center gap-4 lg:gap-6">
                <button
                    onclick={() => scrollToSection("hero")}
                    class="text-[#252525] hover:text-[#33A1E0] transition-colors font-medium text-sm lg:text-base"
                >
                    หน้าแรก
                </button>
                <button
                    onclick={() => scrollToSection("services")}
                    class="text-[#252525] hover:text-[#33A1E0] transition-colors font-medium text-sm lg:text-base"
                >
                    บริการ
                </button>
                <button
                    onclick={() => scrollToSection("pricing")}
                    class="text-[#252525] hover:text-[#33A1E0] transition-colors font-medium text-sm lg:text-base"
                >
                    ราคา
                </button>
                <button
                    onclick={() => scrollToSection("location")}
                    class="text-[#252525] hover:text-[#33A1E0] transition-colors font-medium text-sm lg:text-base"
                >
                    ที่ตั้ง
                </button>
                <button
                    onclick={() => scrollToSection("contact")}
                    class="bg-[#33A1E0] text-white px-4 lg:px-6 py-2 rounded-lg hover:bg-[#2a8bc7] transition-colors font-medium text-sm lg:text-base"
                >
                    ติดต่อเรา
                </button>
            </div>

            <!-- Mobile Menu Button -->
            <button
                onclick={toggleMobileMenu}
                class="md:hidden text-[#252525] p-2 hover:bg-gray-100 rounded-lg transition-colors"
                aria-label="Toggle menu"
            >
                {#if mobileMenuOpen}
                    <X class="w-6 h-6" />
                {:else}
                    <Menu class="w-6 h-6" />
                {/if}
            </button>
        </div>

        <!-- Mobile Menu -->
        {#if mobileMenuOpen}
            <div
                class="md:hidden mt-4 pb-4 border-t border-gray-200 pt-4 animate-in slide-in-from-top-2 duration-300"
            >
                <div class="flex flex-col gap-3">
                    <button
                        onclick={() => scrollToSection("hero")}
                        class="text-[#252525] hover:text-[#33A1E0] hover:bg-gray-50 transition-colors font-medium py-3 px-4 rounded-lg text-left"
                    >
                        หน้าแรก
                    </button>
                    <button
                        onclick={() => scrollToSection("services")}
                        class="text-[#252525] hover:text-[#33A1E0] hover:bg-gray-50 transition-colors font-medium py-3 px-4 rounded-lg text-left"
                    >
                        บริการ
                    </button>
                    <button
                        onclick={() => scrollToSection("pricing")}
                        class="text-[#252525] hover:text-[#33A1E0] hover:bg-gray-50 transition-colors font-medium py-3 px-4 rounded-lg text-left"
                    >
                        ราคา
                    </button>
                    <button
                        onclick={() => scrollToSection("location")}
                        class="text-[#252525] hover:text-[#33A1E0] hover:bg-gray-50 transition-colors font-medium py-3 px-4 rounded-lg text-left"
                    >
                        ที่ตั้ง
                    </button>
                    <button
                        onclick={() => scrollToSection("contact")}
                        class="bg-[#33A1E0] text-white px-4 py-3 rounded-lg hover:bg-[#2a8bc7] transition-colors font-medium text-center"
                    >
                        ติดต่อเรา
                    </button>
                </div>
            </div>
        {/if}
    </div>
</nav>
