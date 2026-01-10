<script lang="ts">
    import Container from "$lib/components/Container.svelte";
</script>

<nav class="fixed z-50 w-full bg-white/20 backdrop-blur-md border-b border-gray-100">
    <Container>
        <div class="flex items-center justify-between py-6">
            <div class="flex items-center">
                <a href="/" class="text-xl font-bold">Laundry Shop</a>
            </div>
            <ul class="flex items-center">
                <li><a href="/login" class="text-sm font-medium">Login</a></li>
                <li class="ml-4"><a href="/register" class="text-sm font-medium">Register</a></li>
            </ul>
        </div>
    </Container>
</nav>
