<script lang="ts">
    import { Sparkles, Menu, X } from "@lucide/svelte";
    import Button from "$lib/components/ui/button/button.svelte";

    let scrollY = $state(0);
    let mobileMenuOpen = $state(false);
    let isScrolling = $state(false);
    let scrollTimeout: number;

    const scrollToSection = (id: string) => {
        const element = document.getElementById(id);
        if (element) {
            element.scrollIntoView({ behavior: "smooth" });
            mobileMenuOpen = false;
            // Prevent body scroll when menu closes
            document.body.style.overflow = '';
        }
    };

    const toggleMobileMenu = () => {
        mobileMenuOpen = !mobileMenuOpen;
        // Prevent body scroll when menu is open
        if (mobileMenuOpen) {
            document.body.style.overflow = 'hidden';
        } else {
            document.body.style.overflow = '';
        }
    };

    const handleScroll = () => {
        isScrolling = true;
        clearTimeout(scrollTimeout);
        scrollTimeout = setTimeout(() => {
            isScrolling = false;
        }, 150);
    };

    // Close mobile menu on escape key
    const handleKeydown = (e: KeyboardEvent) => {
        if (e.key === 'Escape' && mobileMenuOpen) {
            toggleMobileMenu();
        }
    };

    // Close mobile menu on window resize
    const handleResize = () => {
        if (window.innerWidth >= 768 && mobileMenuOpen) {
            mobileMenuOpen = false;
            document.body.style.overflow = '';
        }
    };
</script>

<svelte:window bind:scrollY on:scroll={handleScroll} on:keydown={handleKeydown} on:resize={handleResize} />

<!-- Navbar -->
<nav
    class="fixed top-0 left-0 right-0 z-30 transition-all duration-300 safe-top {scrollY >
    50 || isScrolling
        ? 'bg-white/98 backdrop-blur-md shadow-lg border-b border-gray-100'
        : 'bg-white/95 backdrop-blur-sm'}"
>
    <div class="container mx-auto px-3 sm:px-4 lg:px-6 py-2 sm:py-3 lg:py-4">
        <div class="flex items-center justify-between">
            <!-- Logo -->
            <Button
                onclick={() => scrollToSection("hero")}
                variant="ghost"
                class="flex items-center gap-1.5 sm:gap-2 lg:gap-3 hover:opacity-80 transition-opacity h-auto p-0"
            >
                <Sparkles class="w-5 h-5 sm:w-6 sm:h-6 lg:w-8 lg:h-8 text-[#33A1E0]" />
                <span class="text-base sm:text-lg lg:text-2xl font-bold text-[#252525]"
                    >Smith Laundary</span
                >
            </Button>

            <!-- Desktop Menu -->
            <div class="hidden md:flex items-center gap-2 lg:gap-4 xl:gap-6">
                <Button
                    onclick={() => scrollToSection("hero")}
                    variant="ghost"
                    class="text-[#252525] hover:text-[#33A1E0] transition-colors font-medium text-xs sm:text-sm lg:text-base px-2 py-1"
                >
                    หน้าแรก
                </Button>
                <Button
                    onclick={() => scrollToSection("services")}
                    variant="ghost"
                    class="text-[#252525] hover:text-[#33A1E0] transition-colors font-medium text-xs sm:text-sm lg:text-base px-2 py-1"
                >
                    บริการ
                </Button>
                <Button
                    onclick={() => scrollToSection("pricing")}
                    variant="ghost"
                    class="text-[#252525] hover:text-[#33A1E0] transition-colors font-medium text-xs sm:text-sm lg:text-base px-2 py-1"
                >
                    ราคา
                </Button>
                <Button
                    onclick={() => scrollToSection("location")}
                    variant="ghost"
                    class="text-[#252525] hover:text-[#33A1E0] transition-colors font-medium text-xs sm:text-sm lg:text-base px-2 py-1"
                >
                    ที่ตั้ง
                </Button>
                <Button
                    onclick={() => scrollToSection("contact")}
                    class="px-2 sm:px-3 lg:px-4 xl:px-6 py-1.5 sm:py-2 lg:py-2.5 font-medium text-xs sm:text-sm lg:text-base min-h-[36px] sm:min-h-[40px]"
                >
                    ติดต่อเรา
                </Button>
            </div>

            <!-- Mobile Menu Button -->
            <Button
                onclick={toggleMobileMenu}
                variant="ghost"
                size="icon"
                class="md:hidden text-[#252525] hover:bg-gray-100 transition-colors min-h-[40px] min-w-[40px] sm:min-h-[44px] sm:min-w-[44px]"
                aria-label="Toggle menu"
                aria-expanded={mobileMenuOpen}
            >
                {#if mobileMenuOpen}
                    <X class="w-5 h-5 sm:w-6 sm:h-6" />
                {:else}
                    <Menu class="w-5 h-5 sm:w-6 sm:h-6" />
                {/if}
            </Button>
        </div>

        <!-- Mobile Menu -->
{#if mobileMenuOpen}
    <!-- Overlay -->
    <div 
        class="fixed inset-0 bg-black/50 z-40 md:hidden animate-in fade-in duration-200"
        onclick={toggleMobileMenu}
        aria-hidden="true"
    ></div>
    
    <!-- Mobile Menu Panel -->
    <div
        class="fixed top-0 right-0 bottom-0 w-72 sm:w-80 max-w-[90vw] sm:max-w-[85vw] bg-white z-50 md:hidden shadow-2xl animate-in slide-in-from-right duration-300 overflow-y-auto"
    >
        <!-- Mobile Menu Header -->
        <div class="flex items-center justify-between p-3 sm:p-4 border-b border-gray-200">
            <div class="flex items-center gap-1.5 sm:gap-2">
                <Sparkles class="w-5 h-5 sm:w-6 sm:h-6 text-[#33A1E0]" />
                <span class="text-base sm:text-lg font-bold text-[#252525]">Smith Laundary</span>
            </div>
            <Button
                onclick={toggleMobileMenu}
                variant="ghost"
                size="icon"
                class="text-[#252525] hover:bg-gray-100 transition-colors min-h-[40px] min-w-[40px]"
                aria-label="Close menu"
            >
                <X class="w-5 h-5 sm:w-6 sm:h-6" />
            </Button>
        </div>
        
        <!-- Mobile Menu Content -->
        <div class="p-3 sm:p-4 space-y-1.5 sm:space-y-2">
            {#each [
                { id: "hero", label: "หน้าแรก" },
                { id: "services", label: "บริการ" },
                { id: "pricing", label: "ราคา" },
                { id: "location", label: "ที่ตั้ง" }
            ] as item}
                <Button
                    onclick={() => scrollToSection(item.id)}
                    variant="ghost"
                    class="w-full justify-start text-left px-3 sm:px-4 py-3 sm:py-4 text-sm sm:text-base font-medium text-[#252525] hover:text-[#33A1E0] hover:bg-gray-50 rounded-lg transition-all duration-200 min-h-[44px] sm:min-h-[52px]"
                >
                    {item.label}
                </Button>
            {/each}
            
            <div class="pt-3 sm:pt-4 border-t border-gray-200">
                <Button
                    onclick={() => scrollToSection("contact")}
                    class="w-full px-3 sm:px-4 py-3 sm:py-4 text-sm sm:text-base font-medium min-h-[44px] sm:min-h-[52px] bg-[#33A1E0] hover:bg-[#2a8bc7] text-white"
                >
                    ติดต่อเรา
                </Button>
            </div>
        </div>
    </div>
{/if}
    </div>
</nav>
