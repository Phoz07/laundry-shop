<script lang="ts">
    import { Sparkles, Menu, X } from "@lucide/svelte";
    import Button from "$lib/components/ui/button/button.svelte";

    let scrollY = $state(0);
    let mobileMenuOpen = $state(false);

    const scrollToSection = (id: string) => {
        const element = document.getElementById(id);
        if (element) {
            element.scrollIntoView({ behavior: "smooth" });
            mobileMenuOpen = false;
        }
    };

    const navItems = [
        { id: "hero", label: "หน้าแรก" },
        { id: "services", label: "บริการ" },
        { id: "pricing", label: "ราคา" },
        { id: "location", label: "ที่ตั้ง" },
    ];
</script>

<svelte:window bind:scrollY />

<nav
    class="fixed top-0 left-0 right-0 z-30 transition-all duration-300
        {scrollY > 50
        ? 'bg-white shadow-lg border-b border-gray-100'
        : 'bg-white/95 backdrop-blur-sm'}"
>
    <div class="container mx-auto px-4 lg:px-6 py-3 lg:py-4">
        <div class="flex items-center justify-between">
            <!-- Logo -->
            <Button
                onclick={() => scrollToSection("hero")}
                variant="ghost"
                class="flex items-center gap-2 hover:opacity-80 transition-opacity h-auto p-0"
            >
                <Sparkles class="w-6 h-6 lg:w-8 lg:h-8 text-[#33A1E0]" />
                <span class="text-lg lg:text-2xl font-bold text-[#252525]"
                    >Smith Laundary</span
                >
            </Button>

            <!-- Desktop Menu -->
            <div class="hidden md:flex items-center gap-4 xl:gap-6">
                {#each navItems as item}
                    <Button
                        onclick={() => scrollToSection(item.id)}
                        variant="ghost"
                        class="text-[#252525] hover:text-[#33A1E0] transition-colors font-medium"
                    >
                        {item.label}
                    </Button>
                {/each}
                <Button
                    onclick={() => scrollToSection("contact")}
                    class="font-medium"
                >
                    ติดต่อเรา
                </Button>
            </div>

            <!-- Mobile Hamburger -->
            <Button
                onclick={() => (mobileMenuOpen = !mobileMenuOpen)}
                variant="ghost"
                size="icon"
                class="md:hidden text-[#252525] hover:bg-gray-100 min-h-[44px] min-w-[44px]"
                aria-label="Toggle menu"
                aria-expanded={mobileMenuOpen}
            >
                {#if mobileMenuOpen}
                    <X class="w-6 h-6" />
                {:else}
                    <Menu class="w-6 h-6" />
                {/if}
            </Button>
        </div>
    </div>

    <!-- Mobile Dropdown — slide down ใต้ navbar -->
    <div
        class="md:hidden overflow-hidden transition-all duration-300 ease-in-out
            {mobileMenuOpen ? 'max-h-96 opacity-100' : 'max-h-0 opacity-0'}"
    >
        <div
            class="border-t border-gray-100 bg-white px-4 pb-4 pt-2 flex flex-col gap-1"
        >
            {#each navItems as item}
                <Button
                    onclick={() => scrollToSection(item.id)}
                    variant="ghost"
                    class="w-full justify-start text-left px-4 py-3 text-base font-medium text-[#252525] hover:text-[#33A1E0] hover:bg-gray-50 rounded-lg min-h-[52px]"
                >
                    {item.label}
                </Button>
            {/each}
            <Button
                onclick={() => scrollToSection("contact")}
                class="w-full mt-2 py-3 text-base font-medium min-h-[52px] bg-[#33A1E0] hover:bg-[#2a8bc7] text-white"
            >
                ติดต่อเรา
            </Button>
        </div>
    </div>
</nav>
